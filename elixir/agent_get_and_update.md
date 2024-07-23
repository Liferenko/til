## Read Agent's current state. Update it on the next step

in this example get_and_update/2 did 2 valuable actions:
1) set a value for a var `old_list`
2) at the same time updated Agent's state. So next call of `Agent.get_and_update/2` returns updated state 

```elixir
  koan "Use get_and_update when you need to read and change a value in one go" do
    Agent.start_link(fn -> ["Milk"] end, name: :groceries)

    old_list =
      Agent.get_and_update(:groceries, fn old ->
        {old, ["Bread" | old]}
      end)

    assert old_list == ["Milk"]
    assert Agent.get(:groceries, & &1) == ["Bread", "Milk"]
  end
```


It is kind of obvious but still damn interesting, if you ask me :)

## named Agent

Looks easier than Registry-based. Just a name looks cool
```elixir
{:ok, pid} = Agent.start_link(fn -> "Fin." end, name: :stoppable)

Agent.stop(:stoppable)
```

