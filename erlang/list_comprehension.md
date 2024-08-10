## List comprehension

I find it quite similar to Python and Elixir at the same time. 

```erlang
representing_a_list() ->
    [1, 2, 3] =:= [Item || Item <- [1, 2, 3]].

mapping_a_function() ->
    [2, 4, 6] =:= [Item * 2 || Item <- [1, 2, 3]].

applying_a_filter() ->
    [2] =:= [Item || Item <- [1, 2, 3], Item rem 2 =:= 0].

all_together_now() ->
    [4] =:= [Item * 2 || Item <- [1, 2, 3], Item rem 2 =:= 0].

```


for me this example...
```erlang
mapping_a_function() ->
    [2, 4, 6] =:= [Item * 2 || Item <- [1, 2, 3]].
```

seems like Elixir's reverted `Enum.map([1,2,3], fn item -> item * 2 end).
Looke like in Python they have pretty similar list comprehension
```python
result = [x * 2 for x in [1, 2, 3]]
result == [2, 3, 6]
```
