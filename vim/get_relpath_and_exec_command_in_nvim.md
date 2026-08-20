## Run `mix format` within nvim

UPDATE: seems like I can use `:!mix format %`. Same logic works for test current file: `:!mix test %`


My case: I want to use `mix format` only for current file Im working with.

`:execute ':!mix format ' . shellescape(expand('%'))`
