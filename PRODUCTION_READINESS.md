# Production Readiness Expectations

Review this repository as if it will be deployed to a real production environment.

The project should be evaluated for readiness across security, reliability, maintainability, observability, performance, and deployment safety.

## Production Requirements

### Configuration

Check that:

- Environment-specific configuration is separated
- Secrets are not hardcoded
- Production values are not committed
- Development/debug options are disabled in production
- Configuration is validated at startup
- Missing environment variables fail safely
- Sensitive config is not logged

### Error Handling

Check that:

- Errors are handled consistently
- Stack traces are not exposed to users
- API error responses follow a standard format
- Internal errors are logged safely
- Expected business errors are separated from system errors
- Errors do not leak sensitive data
- Unhandled promise rejections are avoided
- Uncaught exceptions are handled properly

### Logging

Check that:

- Important security events are logged
- Important system events are logged
- Logs are structured where possible
- Logs avoid passwords, tokens, secrets, and personal data
- Logs have enough context for debugging
- Excessive noisy logs are avoided
- Audit-worthy actions are traceable

### Observability

Check for:

- Healthcheck endpoint
- Readiness/liveness checks
- Metrics exposure with proper protection
- Request tracing
- Error tracking readiness
- Performance telemetry readiness
- Dependency failure visibility

### Availability and Resilience

Check for:

- Timeouts on external calls
- Retry with backoff where appropriate
- No infinite loops
- No unbounded resource usage
- Graceful shutdown
- Request size limits
- File upload limits
- Rate limiting
- Protection against DoS patterns

### Data Safety

Check for:

- Sensitive data protection
- Avoiding unnecessary data exposure
- Proper validation before persistence
- Safe deletion behavior
- Audit trail for sensitive actions
- Avoiding insecure direct object references
- Avoiding accidental data overwrite

### Deployment

Check for:

- Production build process
- Docker healthcheck
- Non-root container user where applicable
- Minimal base image where appropriate
- Pinned dependency versions
- Safe exposed ports
- No debug endpoints exposed publicly
- Swagger/OpenAPI exposure controlled by environment
- CI/CD secret handling

## Required Production Readiness Output

For every issue, provide:

- Title
- Area
- Severity
- Confidence
- File path
- Line number
- Evidence
- Production risk
- Recommended fix
