# Backend & Cloud Engineering

**Technical focus:** Tested REST service with authorization and relational integrity.

## Business challenge
Provide a secure REST interface for a small relational application.

## Architecture and approach
Flask, SQLAlchemy, PostgreSQL, JWT, Docker Compose and GitHub Actions.

[Conceptual architecture](../architecture/backend-cloud.md)

## Engineering decision and trade-off
Enforce authorization in the API and integrity in the relational model. Container configuration supports repeatable local setup; CI runs tests, not deployment.

## Engineering evidence
Source includes password hashing, role checks, relational constraints and positive and negative pytest cases. CI reported success.

[Evidence record](../evidence/backend-cloud.md)

## Contribution and provenance
Commits attributed to the portfolio owner; manual authorship not established.

## Limitations and next validation
Tests use SQLite; PostgreSQL integration, deployment scale and Kubernetes are not independently verified.

## Business value hypothesis
Reduce integration regressions and unauthorized operations; measure contract-test pass rate and database integration failures. These are proposed success measures, not achieved outcomes.

## Next evidence milestone
Add PostgreSQL-backed integration tests and a clean container startup check.
