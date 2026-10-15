## Purpose

Provides a minimal JSON endpoint that confirms the API layer is reachable and responding correctly.

## ADDED Requirements

### Requirement: Hello endpoint returns fixed greeting
The system SHALL respond to `GET /api/hello` with a JSON body of `{"message": "hello"}` and HTTP 200.

#### Scenario: Successful hello request
- **WHEN** a client sends `GET /api/hello`
- **THEN** the system responds with HTTP 200, `Content-Type: application/json`, and body `{"message": "hello"}`
