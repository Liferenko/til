## Consecutive using window func + LEAD() + LAG()

There was a task on Leetcode: 
> Write a solution to display the records with three or more rows with consecutive id's, and the number of people is greater than or equal to 100 for ea

And it has been resolved using window f + LEAD() + LAG()
Quick note:
- LEAD(column_name, %following_row_index) - next Nth row after current row
- LAG(column_name, %previous_row_index) - previous Nth row after current row
- OVER (...) - the scope over which window function LEAD/2 or LAG/2 will be working. Usually looks like `OVER (ORDER BY date) %var_name%``OVER (PARTITION BY date) %var_name%`




#### Example: 

```sql
SELECT id
    , people
    , visit_date
FROM (
    SELECT id
    , visit_date
    , people
    , LAG(people, 2) OVER (ORDER BY id) pre_pre
    , LAG(people, 1) OVER (ORDER BY id) pre
    , LEAD(people, 1) OVER (ORDER BY id) next
    , LEAD(people, 2) OVER (ORDER BY id) next_next
    FROM Stadium
) wdw_func
WHERE (people >= 50 AND wdw_func.pre_pre >= 50 AND wdw_func.pre >= 50)
OR (people >= 50 AND wdw_func.pre >= 50 AND wdw_func.next >= 50)
OR (people >= 50 AND wdw_func.next >= 50 AND wdw_func.next_next >= 50)
```

faster version using WITH:
```sql
WITH wdw AS (
    select id
    , visit_date
    , people
    , LAG(people, 2) OVER (ORDER BY id ASC) pre2
    , LAG(people, 1) OVER (ORDER BY id ASC) pre
    , LEAD(people, 1) OVER (ORDER BY id ASC) nxt
    , LEAD(people, 2) OVER (ORDER BY id ASC) nxt2
    from Stadium
)
select id
    , visit_date
    , people
from wdw
where (people >= 100 AND wdw.pre2 >= 100 AND wdw.pre >= 100)
OR (people >= 100 AND wdw.pre >= 100 AND wdw.nxt >= 100)
OR (people >= 100 AND wdw.nxt >= 100 AND wdw.nxt2 >= 100);
```

Source: 
- LEAD in PostgreSQL - https://www.postgresqltutorial.com/postgresql-window-function/postgresql-lead-function/
- https://leetcode.com/problems/human-traffic-of-stadium/solutions/911779/mysql-use-window-function-for-big-data
