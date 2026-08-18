# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a personal static website for Christophe MacIntosh, served via GitHub Pages at `christophemacintosh.com` (see `CNAME`). There is no build process, package manager, framework, or test suite — it is plain HTML/CSS deployed directly by GitHub Pages from this repo.

## Development

There are no build, lint, or test commands — the site is static files served as-is.

To preview locally, open `index.html` directly in a browser, or serve the directory with any static file server (e.g. `python3 -m http.server`) and visit it.

Deployment is automatic: GitHub Pages serves whatever is pushed to the repo's default branch, so pushing changes to `index.html`/`style.css`/`images/` is equivalent to deploying.

## Structure

- `index.html` — the single page of the site (landing page with name header and social links).
- `style.css` — all styling, including the full-viewport background image and mobile landscape fix.
- `images/` — image assets referenced by `index.html`/`style.css` (background photo, social icons).
- `CNAME` — custom domain configuration for GitHub Pages (`christophemacintosh.com`); do not remove unless intentionally changing/dropping the custom domain.
- `_config.yml` — Jekyll config file (currently empty), present because GitHub Pages runs content through Jekyll by default.

## Conventions

- Keep it a single static page unless asked to expand it — the README's "Potential improvements" section lists ideas (photo gallery, blog, reading list, resume page) that have not been started.
- Google Analytics (gtag.js) is embedded directly in `index.html`'s `<head>`; preserve the tracking ID (`G-X74ZMNJEG7`) when editing that block unless told to change it.
- Image filenames in `images/` include spaces (e.g. `2021 Twitter logo - white.png`) — match existing references exactly when adding/editing `<img>` tags.
