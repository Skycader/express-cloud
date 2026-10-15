## Why

The `express-cloud` project currently has only a package.json and an `express` dependency — there is no server code yet. We need a minimal working Express app to serve as the project's foundation: a static landing page plus a couple of simple API endpoints to validate the setup end-to-end.

## What Changes

- Add an Express app entry point (`index.js`, per `package.json`'s `main` field) that starts an HTTP server.
- Serve a `public/` directory as static files, with `public/index.html` as the basic landing page served at `/`.
- Add `GET /api/hello` returning `{"message": "hello"}`.
- Add `GET /api/version` returning the app's current version, read from `package.json` (e.g. `{"version": "0.1.0"}`).
- Update `package.json`'s `version` field from `1.0.0` to `0.1.0` to reflect the project's actual current version (matches the "0.1" version requested), and add a `start` script to run the server.

## Capabilities

### New Capabilities
- `static-site`: Serves `public/index.html` (and other static assets in `public/`) over HTTP as the app's landing page.
- `api/hello`: `GET /api/hello` endpoint that returns a fixed greeting JSON payload.
- `api/version`: `GET /api/version` endpoint that returns the running app's version number.

### Modified Capabilities
None — this is a greenfield change; no existing specs are affected.

## Impact

- New files: `index.js` (or `src/index.js`), `public/index.html`.
- Modified files: `package.json` (`version` field, `start` script).
- No new dependencies — `express` is already present in `package.json`.
- No breaking changes (no prior server behavior existed).
