## Run `mix format` within nvim


My case: I want to use `mix format` only for current file Im working with.

`:execute ':!mix format ' . shellescape(expand('%'))`
