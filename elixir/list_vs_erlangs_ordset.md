## :ordset.new/0 vs List.new/0

AFAIK, the main difference between `:ordset.new/0` and `List.new/0` is that `:ordset` is a data structure that GUARANTEES that the elements are ordered, while `List` does not guarantee that.




```elixir
iex(17)> liiist = :ordsets.to_list(my_ordset)
["pliferenko@ahoo.de", "pliferenko@gmail.com"]
iex(18)> my_ordset = :ordsets.add_element("aaa", my_ordset)
["aaa", "pliferenko@ahoo.de", "pliferenko@gmail.com"]
iex(19)> my_ordset = :ordsets.add_element("aab", my_ordset)
["aaa", "aab", "pliferenko@ahoo.de", "pliferenko@gmail.com"]
iex(20)> my_ordset = :ordsets.add_element("bbbb", my_ordset)
["aaa", "aab", "bbbb", "pliferenko@ahoo.de", "pliferenko@gmail.com"]
iex(21)> my_ordset = :ordsets.add_element("aaab", my_ordset)
["aaa", "aaab", "aab", "bbbb", "pliferenko@ahoo.de",
 "pliferenko@gmail.com"]
iex(22)> my_ordset = :ordsets.add_element("aaa1", my_ordset)
["aaa", "aaa1", "aaab", "aab", "bbbb", "pliferenko@ahoo.de",
 "pliferenko@gmail.com"]
iex(23)> my_ordset = :ordsets.add_element("aaa2", my_ordset)
["aaa", "aaa1", "aaa2", "aaab", "aab", "bbbb", "pliferenko@ahoo.de",
 "pliferenko@gmail.com"]
iex(24)> my_ordset = :ordsets.add_element("aaa3", my_ordset)
["aaa", "aaa1", "aaa2", "aaa3", "aaab", "aab", "bbbb",
 "pliferenko@ahoo.de", "pliferenko@gmail.com"]
iex(25)> 
```
