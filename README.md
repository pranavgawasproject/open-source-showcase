# open-source-showcase

[![Live demo](https://img.shields.io/badge/Live%20demo-GitHub%20Pages-161b22?style=for-the-badge&logo=github)](https://pranavgawasproject.github.io/open-source-showcase/)
[![License: MIT](https://img.shields.io/badge/license-MIT-e8a33d.svg?style=for-the-badge)](LICENSE)

> A terminal-inspired, client-side dashboard for exploring `pranavgawasproject`'s public GitHub repositories.

**[Open the live dashboard →](https://pranavgawasproject.github.io/open-source-showcase/)**

## Overview

open-source-showcase turns a public GitHub profile into a searchable repository wall. It reads repository metadata directly from the GitHub REST API, then renders the result in a dark terminal-inspired interface—no build pipeline, backend, or stale local cache required.

## Screenshots / Demo

![open-source-showcase rate-limit state](docs/screenshot-home.jpg)

The screenshot captures the dashboard's anonymous GitHub API rate-limit state. That is an expected demo condition: the public API allows a limited number of unauthenticated requests per hour, so the page may show an empty/error state until the limit resets. When the API is available, the same UI fills with repository cards.

Try it at **[pranavgawasproject.github.io/open-source-showcase](https://pranavgawasproject.github.io/open-source-showcase/)**.

## Features

- **Live repository data** fetched from the public GitHub REST API.
- **Search** by repository name, description, or topic.
- **Sorting** by stars, recent updates, forks, or name.
- **Language filters** generated from the loaded repositories.
- **Fork visibility toggle** for focused or complete browsing.
- **Repository cards and README modal** with metadata and links back to GitHub.
- **Responsive, accessible terminal UI** with keyboard-friendly controls and reduced-motion support.

## Tech stack

- **Frontend:** Static HTML, CSS, and vanilla JavaScript
- **Data source:** GitHub REST API (`api.github.com`)
- **Hosting:** GitHub Pages
- **Tooling:** None required; the page is served directly from the repository root

## Setup

There is no package install or build step. Clone the repository and serve it locally with a simple static server so browser requests work as expected. For example, run a local Python HTTP server from the repository root on port 8000, then open http://localhost:8000.

## Environment variables

None are required. The dashboard intentionally uses anonymous public GitHub API requests. Because it does not ship a token, anonymous rate limits can temporarily produce the empty/error state shown in the screenshot.

## Deploy

GitHub Pages can serve the repository root directly: enable Pages for the `main` branch and select the `/ (root)` directory. No build command or environment configuration is needed.

## Contributing

Keep the dashboard dependency-free and client-side. For UI or accessibility changes, test with a local static server and verify both successful API responses and rate-limit/error states before opening a pull request.

## License

MIT. See [LICENSE](LICENSE).
