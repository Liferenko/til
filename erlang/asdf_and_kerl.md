# Erlang via asdf and via kerl

I had a case when a project required Erlang v23. But asdf didn't install it properly due to openssl@3 and openssl@1.1 issue (even if you using --with-ssl=(brew --prefix openssl@1.1)).

In this case I needed to resolve it with Kerl as a side installer without removing Erlang from asdf.
And seems like it works good. I didn't know kerl works quite similar to python venv - you need to activate certain version of Erlang using `. /path/to/installed/erlang/23.3.3/activate` and deactivate it when you need. 

Works like a charm. But it still a shame on asdf (or I'm dull)
