# Performance Expectations

Review this repository for production performance risks.

The review should identify both code-level and architecture-level performance problems.

## Backend Performance

Check for:

- Blocking synchronous operations inside request handlers
- CPU-heavy work on the main request thread
- Inefficient loops
- Nested loops over large collections
- Repeated processing of the same data
- Missing pagination
- Returning large unbounded responses
- Inefficient filtering/sorting in application code
- Expensive database queries
- N+1 query patterns
- Missing database indexes where obvious
- Loading unnecessary columns or relations
- Repeated database calls inside loops
- Missing caching for frequently accessed data
- Inefficient middleware order
- Repeated initialization per request
- Excessive logging inside hot paths
- Unbounded JSON parsing
- Unbounded request body size
- Unbounded file upload size
- Memory leak risks
- Event listener leaks
- Missing timeout handling
- Missing request cancellation handling
- Missing compression where appropriate

## API Performance

Check for:

- Slow endpoints caused by poor code structure
- Endpoints returning too much data
- Missing pagination on list endpoints
- Missing filtering limits
- Missing max page size
- Missing rate limits
- Missing response caching
- Inefficient serialization
- Unnecessary nested response objects
- No timeout for external API calls
- No retry/backoff strategy for external calls
- No circuit breaker for unstable integrations

## Frontend Performance

Check for:

- Large bundle risks
- Expensive rendering
- Unnecessary re-renders
- Heavy client-side processing
- Loading unnecessary assets
- Unoptimized images
- Excessive network requests
- Missing lazy loading
- Blocking scripts
- Unused dependencies
- Large third-party libraries
- Inefficient DOM operations

## Infrastructure Performance

Check for:

- Missing Docker healthcheck
- Inefficient base image
- Missing resource limits
- Missing runtime environment optimization
- No production build command
- No caching strategy
- Inefficient static file serving
- Missing gzip/brotli compression
- Missing CDN assumptions for static assets

## Required Performance Output

For every performance issue, provide:

- Title
- Category: Backend, API, Frontend, Database, Infrastructure, or Runtime
- Severity
- Confidence
- File path
- Line number
- Evidence from code
- Why it may affect performance
- Possible production impact
- Recommended optimization
