## Virtual address space for literals

By default, 1gb of virtual address space is reserved for literals in BEAM code and for persistent terms.
The amount of virtual address space for literals can be changed by using:
```
erl +MIscs 2048
```
