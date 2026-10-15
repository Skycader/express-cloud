## Purpose

Serves the app's static landing page and related static assets over HTTP so a browser hitting the site root gets a basic HTML page back.

## ADDED Requirements

### Requirement: Static landing page served at root
The system SHALL serve `public/index.html` as the response when a client requests `GET /`.

#### Scenario: Root request returns landing page
- **WHEN** a client sends `GET /`
- **THEN** the system responds with HTTP 200 and the content of `public/index.html`, with a `Content-Type` of `text/html`

### Requirement: Public directory served as static assets
The system SHALL serve any file placed under the `public/` directory at the corresponding URL path.

#### Scenario: Static asset request
- **WHEN** a client requests `GET /<filename>` for a file that exists in `public/`
- **THEN** the system responds with HTTP 200 and the file's contents

#### Scenario: Missing static asset
- **WHEN** a client requests `GET /<filename>` for a file that does not exist in `public/` and does not match any other route
- **THEN** the system responds with HTTP 404
