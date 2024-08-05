## For-loop OOOOOOR?

alternative:
```rust

let array: [u64; 4] = [4, 8, 16, 32];
let mut iterator = array.iter();

.
.
.

iterator.next().unwrap();
iterator.next().unwrap();
iterator.next().is_none();

```
