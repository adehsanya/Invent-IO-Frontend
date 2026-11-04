# INVENT IO production frontend

This branch runs the API-connected merchant application. There is no demo login, local simulated sales store, Figma fixture data or design-review route. The browser calls /api/v1, proxied by the Node server to the configured API_ORIGIN. The backend defaults to https://invent-io-backend-production.up.railway.app. No backend credentials belong in this repository.

Run npm run check, npm run build, and npm start. Node 22 or later is required. Build command: npm run build; start command: npm start; root directory: /. Railway assigns PORT automatically.

Connected flows: login/register, password change/reset/verification, catalog create/edit/import, pending payments, cash-payment recording, sale allocation, sale detail and web-push configuration. Server permissions and persisted backend responses control the UI.

The deployed backend login was observed returning HTTP 500. Successful authentication and database persistence remain unverified. Admin dashboard, billing and team APIs are not fabricated; their implementation still requires the actual backend contracts. The backend tenancy bootstrap patch is maintained separately in the shared repository work.
