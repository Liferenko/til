## Multiple WITH

```sql
WITH common_table_expression_one AS (select ...),
    common_table_expression_two AS (select ...)
SELECT ...
FROM common_table_expression_two
INTERSECT common_table_expression_one ...
```

Source: https://learnsql.com/blog/multiple-with-statements/
