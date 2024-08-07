## Moved vs copied

In an example below, a value will be moved from `String::from("Chris")` but will be copied from "Chris" (here is a `&'static str`)

```rust
// Another example of a variables ownership ending is the concept of "moving" the value.
// When a variable's value is moved to a new variable, the original binding is cleaned up.
#[test]
fn moving_a_value() {
    let name = String::from("Chris");
    let first_name = name;
    assert_eq!(first_name, "Chris".to_string());
}

// Some confusion can arise with moving values, because certain data types aren't moved.
// Primitive types like &'static str are copied rather than being moved,
// which means ownership doesn't end.
#[test]
fn copying_a_value() {
    let name = "Chris";
    let first_name = name;
    assert_eq!(name, "Chris");
}
```
