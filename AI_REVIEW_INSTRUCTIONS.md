# AI Review Instructions

This repository must be reviewed as if it is intended for a secure, scalable, production-grade environment.

The review should not be limited to syntax, style, dependencies, or simple SAST findings. The AI reviewer must inspect the project from the following perspectives:

1. Security
2. Performance
3. Production readiness
4. API quality
5. Architecture and maintainability
6. Infrastructure and deployment readiness
7. Business logic risks
8. Logging and observability
9. Error handling
10. Dependency and supply-chain risk

## Review Depth Required

The AI reviewer must inspect:

- Route handlers
- Controllers
- Services
- Middleware
- Authentication logic
- Authorization logic
- JWT/token handling
- Password reset/recovery flows
- File upload handling
- Database queries
- ORM usage
- XML parsing
- Template rendering
- Redirect logic
- CORS configuration
- Security headers
- Error handling
- Logging
- Docker files
- Swagger/OpenAPI files
- Environment/configuration files
- Frontend DOM sinks
- Package dependencies
- CI/CD files
- Seed/demo/test data if they affect runtime behavior

## Important Instruction

Do not only report dependency vulnerabilities. Also report application-level issues, business-logic issues, production risks, performance risks, and insecure implementation patterns.

## Output Required for Every Finding

For each finding, provide:

- Finding title
- Category
- Severity
- Confidence level
- File path
- Line number
- Evidence from code
- Why this matters in production
- OWASP category if security-related
- CWE if security-related
- Recommended fix
- Whether the issue is SAST, SCA, IaC, secret, performance, architecture, or business-logic related
