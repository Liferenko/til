# Bad and good SQL for removing expired items

```sql
-- bad case
SELECT ... WHERE DateDiff(mm, OrderDate,GetDate()) >= 30;


-- good case
SELECT ... WHERE OrderDate < DateAdd(mm, -30, GetDate());
```

