## IO.inspect/2

the closest solution from pure Erlang is `erlang:display/1`

```erlang
fetching_what_is_not_available_is_troublesome() ->
    Res = bad_fetch(),
    erlang:display("============="),
    erlang:display(Res),
    erlang:display("============="),
    badarg =:= bad_fetch().
```

There is an alternative where you may import Elixir's IEx.Helper, but it sounds as an overkill.
Anyway, here is it - https://elixirforum.com/t/equivalent-of-elixirs-inspect-feature-in-erlang-shell/15171/2
