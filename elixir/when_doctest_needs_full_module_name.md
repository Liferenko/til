### When doctest wants module's fullname

for using doctest without import issue, I need to use `doctest SomeLongModuleName.SubModule, import: true`

##### without import
```elixir
defmodule KVServer.Command do
  @doc ~S"""
  Parses the given `line` into a command.

  ## Examples

      iex> KVServer.Command.parse("CREATE shopping\r\n")
      {:ok, {:create, "shopping"}}

  """
  def parse(_line) do
    ...
  end
end
```

##### with import
```elixir
# file test/.../command_test.exs

defmodule KVServer.Command do
  doctest KVServer.Command, import: true
  ...
end

# file lib/.../command.ex
defmodule KVServer.Command do

  @doc ~S"""
  ## Examples

      iex> parse("CREATE shopping\r\n")
      {:ok, {:create, "shopping"}}

  """
  def parse(_line) do
    ...
  end
end
```
