# Architecture Expectations

Review this repository for maintainability, scalability, and clean structure.

The review should identify architectural risks that may create future production problems.

## Architecture Areas to Inspect

### Separation of Concerns

Check for:

- Business logic inside controllers/routes
- Large files with too many responsibilities
- Mixed authentication, validation, database, and response logic
- Tight coupling between modules
- Repeated logic across files
- Poor boundary between frontend and backend
- Poor boundary between infrastructure and business logic

### Maintainability

Check for:

- God files
- God functions
- Large route handlers
- Deep nesting
- Complex conditionals
- Unclear naming
- Duplicated code
- Magic strings
- Magic numbers
- Hardcoded business rules
- Scattered configuration
- Inconsistent error handling
- Inconsistent response structures

### Testability

Check for:

- Logic that is hard to unit test
- Direct dependency on global state
- Direct dependency on environment variables throughout code
- Database access mixed into business logic
- No clear service boundaries
- No abstraction for external integrations
- No clear validation layer

### Scalability

Check for:

- Single points of bottleneck
- Global mutable state
- In-memory state that breaks horizontal scaling
- File-system dependency that may break in containers
- Lack of pagination
- Lack of queueing for heavy background work
- Lack of caching strategy where obvious

### Modularity

Check for:

- Poor folder organization
- Feature code scattered across unrelated folders
- Missing module boundaries
- Circular dependencies
- Unclear ownership of responsibilities
- Inconsistent imports

## Required Architecture Output

For every architecture issue, provide:

- Title
- Area
- Severity
- Confidence
- File path
- Line number
- Evidence
- Why it matters
- Recommended improvement
