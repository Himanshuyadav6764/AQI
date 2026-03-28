# aqi-monitoring.finall
# aqi-monitoring.finall
# aqi-monitoring.final2

## Deploy On Vercel

This repository is now configured to deploy both frontend and backend from the repo root.

### 1) Import the GitHub repository in Vercel

- In Vercel, click **Add New Project** and import this repository.
- Keep the project root as the repository root (`AQI-project`).

### 2) Set Environment Variables (Vercel Project Settings)

- `WAQI_TOKEN`
- `OPENWEATHER_API_KEY`
- `CORS_ORIGINS` (comma-separated origins, for example your Vercel domain and localhost)

Example:

`https://your-project.vercel.app,http://localhost:5173`

### 3) Deploy

- Trigger a deployment from Vercel dashboard (or push to `main`).

### Notes

- Frontend calls backend through same-domain API routes (`/api/predict`, `/api/forecast`, `/api/get-ai-advice`).
- Vercel serverless Python entrypoint is in `api/[...path].py`.
