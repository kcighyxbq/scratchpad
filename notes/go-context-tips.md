# Go Context Tips

- Always pass `context.Context` as the first argument.
- Use `context.WithTimeout` for HTTP calls and DB queries.
- Don't store contexts in structs; pass them explicitly.
- Cancel contexts when done to free resources.

Example: `ctx, cancel := context.WithTimeout(parent, 2*time.Second)`
