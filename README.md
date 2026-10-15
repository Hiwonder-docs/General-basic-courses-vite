# General_basic_courses Documentation

This repository contains the General_basic_courses VitePress documentation site. The
documentation source files are Markdown files under `docs/docs/`.

## Local development

Install dependencies and start the local documentation server:

```bash
npm ci
npm run docs:dev
```

The local site is available at
`http://localhost:5173/projects/General_basic_courses/en/latest/`.
To use a fixed local address and fail if the port is already occupied:

```bash
npm run docs:dev -- --host 127.0.0.1 --port 5173 --strictPort
```

Build the production site and stage the artifacts:

```bash
npm run docs:build
npm run docs:stage-main
```

The staged production files are generated in `projects/General_basic_courses/en/latest/`.

## GitHub Pages deployment

The build artifacts under `projects/` are committed to the repository. Open
**Settings > Pages**, select **Deploy from a branch**, and choose **main** and
**/(root)**. Do not bind a custom domain.

The GitHub Pages direct URL is:

```text
https://hiwonder-docs.github.io/General_basic_courses-vite/projects/General_basic_courses/en/latest/
```

The public-facing URL (via the baota Nginx reverse proxy) is:

```text
https://wiki-test.hiwonder.com/projects/General_basic_courses/en/latest/
```
