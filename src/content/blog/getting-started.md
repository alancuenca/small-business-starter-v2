---
title: Getting Started with This Template
description: A quick guide to setting up your new small business website using this Astro template.
author: Team
date: 2026-01-15
tags: [guide, setup]
draft: false
---

Welcome to your new small business website! This template is designed to get you online fast with a professional, mobile-first site that loads in under a second.

## Quick Setup

1. Clone the repository
2. Run `pnpm install` to install dependencies
3. Run `pnpm dev` to start the development server
4. Open `http://localhost:4321` in your browser

## Customise Your Business Info

Everything you need to change lives in one file: `src/data/siteData.ts`. Open it and update your business name, phone number, email, address, services, reviews, and team members.

## Change the Look

The colour palette and fonts are controlled by two files:

- **`src/config/brand.ts`** — colour hex values, font names, and border radius
- **`src/styles/theme.css`** — CSS custom properties that Tailwind reads from

Change the colours in both files and your entire site updates instantly.

## Add Your Images

Drop your photos into the folders under `src/assets/images/`:

- `hero/` — your main homepage image
- `about/` — a photo of your team or workspace
- `gallery/` — project photos (as many as you like)

Then update `src/config/images.ts` to point to your new files. Until you add your own, the template uses placeholder images.

## Deploy

This template is pre-configured for Netlify. Push your repo to GitHub and connect it in Netlify — the `netlify.toml` file handles the rest.

Happy building!
