# String.to_atom/1 is a danger

>`String.to_atom/*` creates a new atom if one of its name wasn't use before, which is dangerous for dynamic/unknown data.

>`String.to_existing_atom/*` does only allow you to convert strings to atoms when the atom already exists at that point via some other means of usage of it.

**according to these:**
- https://www.erlang.org/doc/efficiency_guide/introduction
- https://hexdocs.pm/credo/Credo.Check.Warning.UnsafeToAtom.html


