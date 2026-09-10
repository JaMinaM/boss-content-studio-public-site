# BOSS Content Studio — Public Site

The standalone public product and legal website for BOSS Content Studio. It is intentionally separate from the private BOSS application and contains no application code, provider integrations, accounts, databases, or secrets.

## Local preview

This is a dependency-free static site. From the repository root, run:

```powershell
python -m http.server 4173 --directory dist
```

Then open `http://localhost:4173`.

## Build

There is no build step. The deployable static files are committed in `dist/`.

## Deployment

The included `vercel.json` identifies `dist/` as the static output directory. The directory-based routes work as direct public URLs:

- `/`
- `/privacy`
- `/terms`

No environment variables or backend services are required for basic deployment. Do not connect this repository to the private BOSS application, and never commit keys, tokens, credentials, or other secrets.
