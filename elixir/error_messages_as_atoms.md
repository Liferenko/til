## Error messages as atoms instead of strings


Best Practices for the Error Tuple
Source - https://medium.com/@moxicon/elixir-best-practices-for-error-values-50dc015a06f5


Summary:
- Two-Element Tuple
- Try to avoid strings
- Encoding Errors in Regular Structs


GPT summarized:
Elixir Error Handling Motto: Use {:ok, result} or {:error, reason} tuples to return errors without throwing exceptions, keeping consistency and allowing pattern matching. For structured errors, use custom structs or defexception, not strings. Let error handling remain flexible for easy customization by function consumers.
