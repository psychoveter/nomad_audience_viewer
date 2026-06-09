# Nomad Audience Viewer

Static GitHub Pages viewer for `audience_02.md`.

## Files

- `index.html` — GitHub Pages entrypoint.
- `audience_visualizer.html` — standalone SPA.
- `audience_02.md` — source markdown with cohorts and axes.
- `.github/workflows/pages.yml` — GitHub Actions workflow for Pages deploy.

The SPA reads `audience_02.md` from the same directory at runtime, so edits to the markdown schema and cohort cards do not require rebuilding the viewer.

## Local Preview

```bash
npm run dev
```

Then open:

```text
http://127.0.0.1:8787/
```

## GitHub Pages Deploy

This folder is already a static Pages bundle. No build step is required. Deployment is handled by GitHub Actions.

Recommended repository settings:

- Source: `GitHub Actions`

On every push to `main`, `.github/workflows/pages.yml` uploads the repository root as a Pages artifact and deploys it.

Before pushing, you can run:

```bash
npm run pages:check
```
