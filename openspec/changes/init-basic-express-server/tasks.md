## 1. Project Setup

- [ ] 1.1 Add a `start` script to `package.json` (`"start": "node index.js"`) and update the `version` field from `1.0.0` to `0.1.0`; verify by running `npm start` and confirming the server boots without errors
- [ ] 1.2 Create the `public/` directory with a basic `public/index.html` landing page; verify the file exists and is valid HTML

## 2. Server Bootstrap

- [ ] 2.1 Create `index.js` that requires `express`, creates the app, and listens on a port (e.g. `process.env.PORT || 3000`), logging the listening address on startup; verify by running `node index.js` and seeing the log line
- [ ] 2.2 Wire up `express.static` to serve the `public/` directory (satisfies the `static-site` spec's static asset and root `index.html` scenarios); verify with `curl http://localhost:3000/` returns the contents of `public/index.html` with HTTP 200, and `curl http://localhost:3000/does-not-exist.html` returns HTTP 404

## 3. API Routes

- [ ] 3.1 Add `GET /api/hello` returning `{"message": "hello"}` as JSON (satisfies the `api/hello` spec); verify with `curl http://localhost:3000/api/hello` returns HTTP 200 and that exact JSON body
- [ ] 3.2 Add `GET /api/version` that reads `version` from `package.json` and returns it as `{"version": "<value>"}` (satisfies the `api/version` spec); verify with `curl http://localhost:3000/api/version` returns HTTP 200 and `{"version": "0.1.0"}`

## 4. Verification

- [ ] 4.1 Start the server and manually exercise all three routes (`/`, `/api/hello`, `/api/version`) plus a 404 case, confirming responses match the specs in `openspec/changes/init-basic-express-server/specs/`
