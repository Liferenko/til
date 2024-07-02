## Alternative to :ets

Better for frequent readings and close-to-never updates

How it looks:
```erlang
:persistent_term.put(:my_data, data)

%% Read
:persistent_term.get(:my_data)[key]

%% Update
def put(key, value) do
  data = :persistent_term.get(:my_data)
  updated = Map.put(data, key, value)
  :persistent_term.put(:my_data, updated)
end
```

Suitable uses for persistent_term:
- Storing of config data that must be accessible by any process
- Storing of references for NIF resources
- Storing of references for efficient counters
- Storing an atom to indicate a logging level or whether debugging is turned on

More better use-cases for :persistent_term - https://www.erlang.org/blog/persistent_term/

! NB:
- It is recommended to use keys like `?MODULE` or `{?MODULE,SubKey}` to avoid name collisions.
- Prefer creating a few large persistent terms to creating many small persistent terms.

Docs - https://www.erlang.org/doc/apps/erts/persistent_term.html
Source - https://dockyard.com/blog/2024/06/18/choosing-the-right-in-memory-storage-solution-part-1
