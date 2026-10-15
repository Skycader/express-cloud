## Purpose

Exposes the running application's version number so clients and operators can verify which build is deployed.

## ADDED Requirements

### Requirement: Version endpoint returns current app version
The system SHALL respond to `GET /api/version` with a JSON body containing the app's current version string, sourced from `package.json`, and HTTP 200.

#### Scenario: Successful version request
- **WHEN** a client sends `GET /api/version`
- **THEN** the system responds with HTTP 200, `Content-Type: application/json`, and body `{"version": "0.1.0"}` matching the `version` field in `package.json`
