# Lambda
- If you increase the memory available for your lambda, you also improve CPU and network.
- Lambda to ALB conversions happen using JSON to HTTP (request and response follows a JSON format with key/values for headers, body and query parameters)
- ALB Multi-Header Values are supported
  - HTTP: `https://domain.com/path?name=Marcelo&name=Rodrigo`
  - JSON: `"queryStringParamenters: {"name": ["Marcelo","Rodrigo"]}`

## Supported Languages
- Node.js (Javascript)
- Python
- Java
- C# (.NET Core / Powershell)
- Go
- Ruby
- Custom Runtime API (Community supported, eg. Rust)
- Lambda Container Image
  - Image must implement Lambda Runtime API
  - ECS / Fargate is prefered for running Docker images
## Syncronous Invocations
- CLI, SDK, Api Gateway, Application Load Balancer
- Error handling must happen at client side (retries, exponential backoff, etc)
## Asynchronous Invocations

