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

🎯 How Middleware Executes (Order Matters)

Example pipeline:

app.UseHttpsRedirection();
app.UseAuthentication();
app.UseAuthorization();
app.MapControllers();


📌 If you place UseAuthorization() before UseAuthentication() → Authorization will fail because no user is authenticated.


🔥 Real-Time Use Cases of Middleware
Use Case	Example
Logging	Log request/response
Authentication	Validate JWT token
Rate Limiting	Block too many requests
CORS	Allow cross-domain API calls
Localization	Change language based on header
Response Wrapping	Convert all responses to a consistent format
Exception Handling	Handle API errors globally
🚀 Small Interview-Ready Summary

Middleware in ASP.NET Core is a series of components that process HTTP requests and responses in a pipeline. Each middleware can run code before and after the next middleware. Order is important. Custom middleware is created by implementing a class with InvokeAsync and registering it using UseMiddleware() or via an extension method.
