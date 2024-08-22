## Erlang tracers in Elixir

I suppose there are the same methods which :observer uses when I've been (unsuccessfully) tried to use for tracing. 


`:erlang.trace/3`
`:erlang.trace_pattern/3`


more in tracing - :redbug and Rexbug
Example:
```elixir
iex(3)> Rexbug.start("Map.get/_ :: return") # asking for the return value too
{105, 2}
iex(4)> Map.get(%{}, :foo)
nil

# 10:49:02 #PID<0.1057.0> IEx.Evaluator.init/4
# Map.get(%{}, :foo)

# 10:49:02 #PID<0.1057.0> IEx.Evaluator.init/4
# Map.get(%{}, :foo, nil)

# 10:49:02 #PID<0.1057.0> IEx.Evaluator.init/4
# Map.get/3 -> nil

# 10:49:02 #PID<0.1057.0> IEx.Evaluator.init/4
# Map.get/2 -> nil
redbug done, timeout - 2
```
Read more here - https://github.com/nietaki/rexbug
