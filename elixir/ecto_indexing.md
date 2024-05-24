# Ecto.Migration.index/3

first time saw it in Branchaud's TIL - https://github.com/jbranchaud/til/blob/master/elixir/creating-indexes-with-ecto.md

here is an example from doc:

```
defmodule MyRepo.Migrations.CreateIndexes do
  use Ecto.Migration
  @disable_ddl_transaction true # No idea what it means (yet)

  def change do
    create index("posts", [:slug], concurrently: true)
  end
end
```

