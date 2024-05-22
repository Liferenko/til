# List of splitters

Today I learned in Elixir it is possible to `String.split/2` nur only with one splitter but with a list of them:

```elixir
String.split(asf, ["/", " ", "+"])
```
