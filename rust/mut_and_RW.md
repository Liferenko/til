# Concept idea of `&x` and `&mut x`

in Rust we may use `let y = &x` as a read-only reference and `let y = &mut x` as RW reference.
This RW-* is kinda new for me. 

When we need to use `&mut x` - we must declare `x` as mutable - `let mut x = ...`

---
in Rust docs it says:
```
    let mut x = vec![1, 2, 3];
    let y = &mut x; // y is a mutable reference to x
```

In this example, y is a mutable reference to the vector x. The reference y can be used to modify the vector's elements without transferring ownership.

