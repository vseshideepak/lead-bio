# Lead Research Explorer — Vercel-ready frontend

This package contains the existing React + TypeScript + Vite frontend, with its
source files placed at the repository root so Vercel can find `src/` and
`tsconfig.app.json` together.

## Publish on GitHub and Vercel

1. Extract this ZIP.
2. Upload **the contents inside the extracted folder** to the top level of
   your GitHub repository (not the containing folder itself).
3. In Vercel, import or redeploy that repository.
4. Set **Root Directory** to `.` / leave it at the repository root.
5. Use:
   - Framework: Vite
   - Build command: `npm run build`
   - Output directory: `dist`
   - Install command: `npm install`
6. Deploy.

The `vercel.json` file also configures SPA route fallback to `index.html`.

## Important backend note

This is the frontend deployment package. The project also uses a Python
FastAPI backend for API-powered features. Vercel's static frontend deployment
does not run that FastAPI server or provide persistent SQLite storage.
Those API features require the backend to be deployed separately (for example,
using the included backend in a suitable Python hosting service), then setting
`VITE_API_BASE_URL` to that backend URL in Vercel and redeploying.

## Local build test

Run from this folder:

```bash
npm install
npm run build
```
