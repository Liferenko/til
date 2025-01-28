## Create an index with a where argument

I was using it for email validation, but it can be used for other things as well.

```
create unique_index(:categories, [:name], where: "parent_id IS NULL")
```
