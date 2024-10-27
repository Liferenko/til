# Transaction levels

Four levels of transaction isolation

1. Read Committed Isolation level
- is a default isolation level

```sql
BEGIN;
UPDATE accounts SET balance = balance + 100.00 WHERE acctnum = 12345;
UPDATE accounts SET balance = balance - 100.00 WHERE acctnum = 7534;
COMMIT;
```
If two such transactions concurrently try to change the balance of account 12345, we clearly want the second transaction to start with the updated version of the account's row. Because each command is affecting only a predetermined row, letting it see the updated version of the row does not create any troublesome inconsistency.

2. Repeatable Read Isolation level
- only sees data before TX began

3. Serializable Isolation Level
- is the strictiest tx isolation 

"SELECT" query will see only data commited before query began.

4. Read uncommitted


Read more here - https://www.postgresql.org/docs/current/transaction-iso.html
Youtube video (in ru) - https://www.youtube.com/watch?v=yVlCjzJAOOo
