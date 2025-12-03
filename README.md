# Practices

✅ What is Middleware in ASP.NET Core?

In ASP.NET Core, middleware is software that sits in the HTTP request pipeline and processes requests and responses.

Each middleware component can:

✔ Read request
✔ Modify request
✔ Pass the request to the next middleware
✔ Short-circuit the pipeline
✔ Modify the outgoing response


🟦 Common Built-in Middleware Examples

| Middleware              | Purpose                |
| ----------------------- | ---------------------- |
| `UseRouting()`          | Matches incoming route |
| `UseAuthentication()`   | Validates JWT/cookies  |
| `UseAuthorization()`    | Checks roles/policies  |
| `UseCors()`             | Enables CORS           |
| `UseStaticFiles()`      | Serve static files     |
| `UseExceptionHandler()` | Global error handling  |
| `UseHttpsRedirection()` | Redirect to HTTPS      |
