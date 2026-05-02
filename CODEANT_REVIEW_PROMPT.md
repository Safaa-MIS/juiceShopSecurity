# CodeAnt AI Review Prompt

Perform a deep production-grade review of the full repository.

Do not review only changed files. Do not focus only on dependency vulnerabilities. Review the complete codebase, configuration, dependencies, API behavior, infrastructure, and production-readiness risks.

## Main Review Objectives

Find as many valid issues as possible across:

1. Security
2. Performance
3. Architecture
4. API quality
5. Production readiness
6. Infrastructure
7. Secrets
8. Dependency vulnerabilities
9. Business logic risks
10. Observability and logging

## Security Review Scope

Review against OWASP Top 10 2021 and 2025 concepts.

Look specifically for:

- SQL Injection
- NoSQL Injection
- Command Injection
- Template Injection
- XSS: stored, reflected, DOM-based, header-based
- Broken Access Control
- IDOR
- Authentication bypass
- Weak password reset
- JWT verification bypass
- Weak token handling
- Hardcoded secrets
- Sensitive data exposure
- Directory listing
- Exposed backups
- Exposed logs
- Exposed metrics
- Exposed Swagger/OpenAPI
- SSRF
- XXE
- Open redirect
- Path traversal
- Unsafe file upload
- Mass assignment
- Prototype pollution
- Insecure deserialization
- Unsafe eval
- Weak cryptography
- Rate-limit bypass
- CAPTCHA bypass
- Business logic abuse
- Security misconfiguration
- Vulnerable dependencies
- Supply-chain risks

## Performance Review Scope

Look specifically for:

- Blocking synchronous operations
- CPU-heavy work in request handlers
- Inefficient loops
- Expensive queries
- N+1 query patterns
- Missing pagination
- Unbounded responses
- Unbounded request body size
- Unbounded file uploads
- Missing caching
- Excessive logging
- Memory leak risks
- Missing timeout handling
- Inefficient middleware order
- Inefficient frontend asset loading
- Large bundle risks
- Missing compression
- Missing healthchecks

## Architecture Review Scope

Look specifically for:

- God files
- God functions
- Business logic inside controllers/routes
- Poor separation of concerns
- Duplicated logic
- Deep nesting
- Tight coupling
- Global mutable state
- Hardcoded configuration
- Scattered business rules
- Poor testability
- Poor module boundaries
- Circular dependencies

## API Review Scope

Look specifically for:

- Missing authentication
- Missing authorization
- Inconsistent response structure
- Inconsistent error handling
- Missing validation
- Missing pagination
- Returning sensitive fields
- Excessive payloads
- Missing rate limits
- Unsafe CORS
- Wrong HTTP status codes
- Swagger mismatch
- Missing request size limits

## Infrastructure Review Scope

Look specifically for:

- Docker security issues
- Missing Docker HEALTHCHECK
- Root container user
- Unpinned image versions
- Exposed ports
- Hardcoded credentials
- Unsafe CI/CD permissions
- Secrets in config
- Swagger/OpenAPI missing limits
- Missing production environment controls

## Required Output Format

For every finding, return:

- Title
- Category
- Severity: Critical, High, Medium, Low, Info
- Confidence: High, Medium, Low
- File path
- Line number
- Evidence from code
- Why it matters
- Production impact
- OWASP category if relevant
- CWE if relevant
- Recommended fix
- Type: SAST, SCA, Secret, IaC, Performance, Architecture, API, Business Logic, or Production Readiness

## Important Rules

- Prefer real evidence from code.
- Avoid vague generic suggestions.
- Do not report false positives without explaining uncertainty.
- If the issue requires runtime validation, mark it as "Needs runtime validation".
- If a vulnerability is intentionally present because this is a vulnerable training app, still report it clearly.
- Include business-logic issues even if they are not detected by normal SAST rules.
