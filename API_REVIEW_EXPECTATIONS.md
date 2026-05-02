# API Review Expectations

Review all API endpoints for security, correctness, consistency, performance, and production readiness.

## API Security

Check for:

- Missing authentication
- Missing authorization
- Broken access control
- IDOR
- Mass assignment
- Missing input validation
- SQL/NoSQL injection
- Unsafe file upload
- SSRF
- XXE
- XSS through API responses
- Sensitive data exposure
- Token/JWT weaknesses
- Overly permissive CORS
- Missing rate limits

## API Design

Check for:

- Inconsistent HTTP status codes
- Inconsistent error response format
- Inconsistent success response format
- Missing pagination
- Missing sorting/filtering limits
- Missing request body size limits
- Returning unnecessary fields
- Returning sensitive internal fields
- Poor endpoint naming
- Lack of versioning where applicable
- Swagger/OpenAPI mismatch with implementation

## API Performance

Check for:

- Large unbounded responses
- Expensive queries
- N+1 query patterns
- Missing caching
- Repeated work per request
- Missing timeout for external calls
- Missing payload limits
- Excessive synchronous work

## API Reliability

Check for:

- Unhandled exceptions
- Unhandled promise rejections
- Missing validation failure handling
- Missing not-found handling
- Missing conflict handling
- Poor retry behavior
- No graceful behavior when dependencies fail

## Required API Output

For every API issue, provide:

- Endpoint or route
- HTTP method if known
- File path
- Line number
- Issue title
- Category
- Severity
- Evidence
- Production impact
- Recommended fix
