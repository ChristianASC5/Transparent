# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Transparent is a static HTML/CSS brand site for a radical price-transparency apparel brand. No build system, no framework — pure HTML files served directly via GitHub Pages.

**Live site:** https://christianasc5.github.io/Transparent/

## Pages

| File | Route | Purpose |
|------|-------|---------|
| `index.html` | `/` | Main product page — The Everyday Tee with full cost breakdown |
| `about.html` | `/about.html` | Brand origin story and values |
| `coming-soon.html` | `/coming-soon.html` | Waitlist page for upcoming products |


## Design System

All pages share an identical CSS design system defined inline in each file's `<style>` block. CSS variables:

```css
--sand: #F5F1EB    /* warm off-white, used for alternate section backgrounds */
--bark: #2C2419    /* near-black brown, primary text and CTA buttons */
--moss: #4A5E3A    /* dark green, eyebrow labels and accents */
--clay: #B5714A    /* terracotta, numbered list accents */
--cream: #FBF8F3   /* page background */
--stone: #8C8880   /* secondary/muted text */
--divider: rgba(44,36,25,0.12)  /* subtle borders */
```

Typography uses Google Fonts: `DM Serif Display` (headings) and `DM Sans` (body). The `@import` is at the top of each `<style>` block.

## Cost Breakdown Bar

The proportional cost bar on the landing page and teaser on the coming-soon page uses `flex` values that correspond directly to dollar amounts — e.g. `style="flex: 8.7"` represents $8.70. The segment colors map to the cost categories (moss → materials, dark moss → labour, clay → ops, bark → margin, stone → tax).

## Incomplete Sections

`about.html` and `coming-soon.html` have placeholder `<!-- COMMENT -->` content throughout the "How it works", "Values", "Details", and CTA sections. These are intentionally left for copy to be filled in.

## Deployment

Pushing to `main` deploys automatically via GitHub Pages. No CI/CD pipeline.
