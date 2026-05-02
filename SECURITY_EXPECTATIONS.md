# Security Expectations

Review this repository against OWASP Top 10 2021 and OWASP Top 10 2025 concepts where applicable.

The review must look for both obvious code vulnerabilities and deeper business-logic vulnerabilities.

## Security Areas to Inspect

### Authentication

Check for:

- Weak login logic
- Authentication bypass
- Hardcoded users or credentials
- Weak password policy
- Password reset abuse
- Account enumeration
- Missing brute-force protection
- Missing rate limiting on login
- Unsafe session handling
- Unsafe token expiration
- Unsafe refresh token logic
- Insecure remember-me functionality

### Authorization and Access Control

Check for:

- Missing authorization checks
- Broken access control
- IDOR
- User can access another user's records
- Admin-only routes accessible to normal users
- Client-side-only authorization
- Role/permission checks missing on backend
- Privilege escalation
- Mass assignment that allows role changes
- Insecure object references in URL/body/query parameters

### Injection

Check for:

- SQL Injection
- NoSQL Injection
- Command Injection
- LDAP Injection
- Template Injection
- Header Injection
- Log Injection
- ORM query injection
- Unsafe string concatenation in queries
- User-controlled input reaching query builders unsafely

### XSS

Check for:

- Stored XSS
- Reflected XSS
- DOM-based XSS
- Header-based XSS
- Unsafe HTML rendering
- Unsafe use of innerHTML
- Unsafe template rendering
- Weak sanitization
- Bypassable sanitization libraries
- User content rendered without output encoding

### SSRF

Check for:

- User-controlled URLs
- Server-side requests to external URLs
- Missing allowlist validation
- Localhost/internal IP access
- Cloud metadata endpoint access
- URL parser bypasses

### XXE

Check for:

- XML parsing
- External entity expansion
- Unsafe XML parser configuration
- XML upload features
- XML-based APIs

### File Upload and File Access

Check for:

- Missing file type validation
- File extension bypass
- MIME type bypass
- Large file upload abuse
- Path traversal
- Poison null byte
- File overwrite
- Public access to uploaded files
- Executable file uploads
- Insecure temporary file handling

### Sensitive Data Exposure

Check for:

- Hardcoded secrets
- API keys
- Tokens
- Passwords
- Private keys
- Database credentials
- Exposed backup files
- Public confidential documents
- Exposed logs
- Exposed debug data
- Stack traces
- Verbose error messages
- Personal data leakage
- Password hashes exposed

### JWT and Token Security

Check for:

- Weak signing algorithm
- None algorithm vulnerability
- Missing token signature validation
- Accepting unsigned tokens
- Confusing symmetric/asymmetric algorithms
- Long-lived tokens
- Tokens stored insecurely
- Hardcoded JWT secret
- Missing issuer/audience validation
- Missing expiration validation

### Cryptography

Check for:

- Weak hashing
- Weak encryption
- Hardcoded encryption keys
- Predictable tokens
- Insecure random number generation
- Custom cryptography
- Reversible password storage
- Weak coupon, reset, or invite token logic

### Redirects

Check for:

- Open redirects
- Allowlist bypass
- Redirects based on user input
- Unsafe returnUrl or redirectUrl parameters

### Security Misconfiguration

Check for:

- Directory listing
- Debug mode enabled
- Missing security headers
- Weak CORS policy
- Exposed admin interfaces
- Exposed metrics
- Exposed Swagger in production
- Exposed stack traces
- Default credentials
- Public sensitive routes
- Missing HTTPS enforcement

### Business Logic Abuse

Check for:

- Negative prices or quantities
- Coupon abuse
- Reusing expired coupons
- Race conditions
- Bypassing payment logic
- Manipulating order totals
- Changing another user's basket/cart
- Forging reviews or feedback
- Abuse of workflow sequence
- Missing server-side validation for business rules

### Anti-Automation

Check for:

- CAPTCHA bypass
- Rate limit bypass
- Missing throttling
- Brute-forceable endpoints
- No lockout or delay on sensitive actions
- Repeated action abuse

## Required Security Output

For every security issue, provide:

- Title
- OWASP category
- CWE
- Severity
- Confidence
- File path
- Line number
- Evidence
- Exploit scenario
- Recommended fix
