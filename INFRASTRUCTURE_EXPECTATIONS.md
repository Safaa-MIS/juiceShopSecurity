# Infrastructure and Deployment Expectations

Review infrastructure, deployment, container, and API documentation files.

## Docker

Check Dockerfiles for:

- Missing HEALTHCHECK
- Running as root
- Unpinned base image
- Use of latest tag
- Large image size
- Unnecessary packages
- Secrets copied into image
- Development dependencies in production image
- Missing production build step
- Missing environment configuration
- Exposed unnecessary ports
- Insecure file permissions

## Docker Compose

Check for:

- Hardcoded credentials
- Public database ports
- Missing healthchecks
- Missing restart policy
- Missing resource limits
- Unsafe volume mounts
- Secrets in plain text
- Overly broad networks

## CI/CD

Check for:

- Secrets printed in logs
- Unsafe use of pull_request_target
- Unpinned third-party actions
- Missing dependency scan
- Missing security scan
- Missing build/test gates
- Deployment without approval
- Overly broad permissions
- Missing branch protection assumptions

## Swagger/OpenAPI

Check for:

- Missing input limits
- Missing max array size
- Missing max string length
- Missing authentication definitions
- Sensitive endpoints exposed
- Internal schemas exposed
- Inaccurate security requirements
- Missing error responses
- Missing rate-limit assumptions

## Required Infrastructure Output

For every issue, provide:

- Title
- File path
- Line number
- Severity
- Confidence
- Evidence
- Production risk
- Recommended fix
