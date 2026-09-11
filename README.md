# Project-Management-UI

Angular frontend for a project management tool. Pairs with [Project-Management-API](https://github.com/hassan7865/Project-Management-API).

## Overview

Standalone Angular app with login, route guards, and a shell layout (sidebar + top bar). Auth and user calls go to the companion ASP.NET Core API. The home area is still early; the focus so far is auth, layout, and API wiring.

## Stack

- Angular 18 (standalone components)
- Angular Material / CDK, PrimeNG
- TypeScript, RxJS
- `ngx-cookie-service` for session cookies

## Structure

```
src/app/
  Pages/        # Login, home
  Layout/       # Authenticated shell
  Components/   # Sidebar, top bar
  Services/     # Auth, user, shared helpers
  Guards/       # Auth / login guards
src/Environment/
```

## Getting started

```bash
npm install
npm start
# serves at http://localhost:4200
```

Build:

```bash
npm run build
```

Point `src/Environment/environment.ts` (`BASEURL`) at your local or deployed API (default expects something like `https://localhost:44319/api`).

## Notes

- Requires the API to be running for login and protected routes to work.
- Do not commit real credentials or production API keys.
