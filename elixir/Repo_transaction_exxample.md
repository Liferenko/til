## Repo Transaction example

```elixir
  def all_active_accounts(callback) when is_function(callback, 1) do
    Repo.transaction(fn ->
      UserAccount
      |> where([s], is_nil(s.archived_at))
      |> Repo.stream(max_rows: 100)
      |> Stream.chunk_every(100)
      |> Stream.each(callback)
      |> Stream.run()
    end)
  end
```
