# NagaraSetu — Smart Civic Issue Reporting and Management

NagaraSetu is a web-based civic service desk for residents, municipal officers,
and city administrators. Residents can report location-specific issues with
photos, receive smart category and priority suggestions, track service-team
progress, and confirm resolutions. Officers work a routed service queue while
city administrators manage teams, access, and citywide issues.

## Run locally

This project must be opened through its Express server. VS Code Live Server
(usually port 5500) serves static files only and cannot handle the `/api`
routes.

1. Install dependencies with `npm install`.
2. Start the app with `npm start`.
3. Open <http://localhost:3000>.

The app stores data locally in `db/campusdesk.sqlite` (the legacy filename is
kept to preserve existing data). MongoDB and a `.env`
file are not required. An optional `.env` can still configure SMTP,
`SESSION_SECRET`, `SUPERADMIN_KEY`, or a custom `DATABASE_PATH`.

Use Citizen IDs in the form `CIT12345` and officer IDs in the form `OFF12345`.

If `public/structure.html` is accidentally opened through Live Server on port
5500 or 5501, it automatically redirects to the Express server on port 3000.
