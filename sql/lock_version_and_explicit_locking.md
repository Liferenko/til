## Why use lock_version?

Levels of locking:
- table-level
- row-level
- page-level
- deadlock


ELI5 explanation from AI:
- Lock versions are like taking turns drawing, so you don't accidentally draw over each other’s pictures. When your friend is drawing, you wait, and when they are done, it's your turn.
- Explicit locking is like agreeing to use specific colored pencils only one at a time. If you're using the red pencil, your friend waits until you finish before they start using it.

Source - https://www.postgresql.org/docs/current/explicit-locking.html
