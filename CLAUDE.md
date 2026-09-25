# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Personal portfolio and blog site for Tim Sent, served via GitHub Pages at www.timsent.com. Pure static HTML/CSS — no build system, no framework, no JavaScript dependencies.

## Structure

- `index.html` — portfolio homepage
- `*.html` — individual blog post/article pages
- `css/style.css` — legacy stylesheet (used by older content); new pages use inline `<style>` blocks instead

## Conventions

**Styling:** All modern pages embed their CSS in a `<style>` block in `<head>`. The design system uses CSS custom properties defined in `:root`:

- Fonts: `Inter` (body) and `JetBrains Mono` (code/labels), loaded from Google Fonts
- Colors: `--bg`, `--surface`, `--border`, `--text-primary`, `--text-secondary`, `--text-muted`, `--accent` (#1c5fdd), `--pink` (#e8433d)
- Layout: centered 720px max-width container with 28px side padding via `.container`
- Nav: sticky, blurred backdrop, 58px height

**New pages** should follow the `language-of-machine-learning.html` or `nvidia-cobalt-robotics.html` pattern (self-contained HTML with inline styles matching the design system above), not `css/style.css`.

## Deployment

Push to `main` branch → GitHub Pages auto-deploys to www.timsent.com (CNAME set). No CI/CD or preview environments.
