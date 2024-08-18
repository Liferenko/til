## Soft delete


Ecto

##### add new postgres rule
in migration:
```elixir
add :deleted_at, :utc_datetime

execute """
  CREATE OR REPLACE RULE soft_deletion AS ON DELETE TO orders
  DO INSTEAD UPDATE orders SET deleted_at = NOW() WHERE id = OLD.id AND deleted_at IS NULL RETURNING OLD.*;
  """,
  """
  DROP RULE IF EXISTS soft_deletion ON orders;
  """
```
[read more about Postgres rules](https://www.postgresql.org/docs/current/rules.html)






##### change view to see only rows where deleted_at = null

add rules' view into migration:
```elixir
execute "CREATE OR REPLACE VIEW visible_orders AS SELECT * FROM orders WHERE deleted_at IS NULL",
  "DROP VIEW IF EXISTS visible_orders"
```

[read more about rules' views](https://www.postgresql.org/docs/current/rules-views.html)


Source: https://dashbit.co/blog/soft-deletes-with-ecto
