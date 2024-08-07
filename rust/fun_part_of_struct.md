## Slightly ypdated struct

In case when you need to make yet another Account but with slight changes - you can use `..blah` to paste blah's data

```rust
    struct Account {
        holder: &'static str,
        account_number: &'static str,
        balance: f64,
    }

    let broke = Account {
        holder: "Morgan Stanley",
        account_number: "00021948523756312",
        balance: 0.00,
    };

    let rich = Account {
        balance: 1000000.00,
        ..broke
    };

    assert_eq!(rich.holder, "Morgan Stanley");
    assert_eq!(rich.balance, 1000000.00);
```
