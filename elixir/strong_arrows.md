# Strong arrows in Elixir

same way usually I used it like this:
```
def active?(state) when is_integer(state) do
  ...
end
```

according to source, we may use it this way:

```
$ int() -> boolean()
def active?(state) do
    if state > something do
        true
    else:
        false
    end
end
```

Source - https://elixir-lang.org/blog/2023/09/20/strong-arrows-gradual-typing/


