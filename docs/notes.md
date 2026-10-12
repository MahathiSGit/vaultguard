# VaultGuard service notes

My own summary of each AWS service used in the project.

- **S3:** Stores a website's static files (HTML, CSS, JavaScript, images).
- **CloudFront:** A content delivery network (CDN) that caches and delivers the website's content globally with low latency.
- **Route 53:** AWS's Domain Name System (DNS) service, which routes user requests to my infrastructure.
- **API Gateway:** The front door for backend requests. It creates and manages REST/HTTP APIs that route requests to services like Lambda, and can also handle authentication checks, throttling, and input validation.
- **Lambda:** Runs backend code as serverless functions in response to events (such as a call from API Gateway) without me managing servers.
- **IAM (Identity and Access Management):** Controls who and what can access AWS resources. Roles let a service like Lambda get only the permissions it needs (least privilege).
- **Cognito:** Handles user authentication: sign-up, sign-in, and issuing tokens (JWTs). It proves who the user is, but my own code must still check what each user is allowed to access (authorization).
- **DynamoDB:** (draft, rewrite in my own words) A NoSQL database that stores items by key. VaultGuard uses it for accounts and transactions.
