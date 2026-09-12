# Small Business Starter

A minimal, fast, and fully customisable website template for small businesses — built with **Astro 7** and **Tailwind CSS v4**.

Edit one file to set up your entire site: business name, phone, email, address, services, reviews, team, hours, and navigation.

## Quick Start

```bash
# Clone the template
git clone https://github.com/your-username/small-business-starter.git
cd small-business-starter

# Install dependencies (pnpm required)
pnpm install

# Start the dev server
pnpm dev
```

Open `http://localhost:4321` to see your site.

## Customise Your Site

### 1. Business information (one file)

Open **`src/data/siteData.ts`** and update:

| Field | What it controls |
|---|---|
| `name` | Business name in header, footer, SEO |
| `tagline` | Hero heading and footer tagline |
| `description` | SEO meta description |
| `email` | Contact page and footer |
| `phoneForTel` / `phoneFormatted` | Click-to-call links everywhere |
| `license` | License badge in header (empty string hides it) |
| `address` | Contact page, footer, JSON-LD schema |
| `hours` | Contact page sidebar |
| `socials` | Footer social links (empty string hides a link) |
| `nav` | Header and mobile navigation links |
| `services` | Services page and homepage cards |
| `reviews` | Reviews page and homepage testimonials |
| `about.story` | About page story paragraphs |
| `about.team` | About page team grid |
| `trustItems` | Homepage trust bar strip |
| `footerNav` | Footer navigation columns |

### 2. Colours and fonts

Edit **`src/config/brand.ts`** and **`src/styles/theme.css`** to change the colour palette, fonts, and border radius. Both files must stay in sync.

To swap fonts, also update the `fonts` array in **`astro.config.mjs`**.

### 3. Images

Drop your photos into folders under `src/assets/images/`:

- `hero/` — homepage hero image
- `about/` — team or workspace photo
- `gallery/` — project photos (any number)

Then update `src/config/images.ts` to import your files. Placeholder images from Unsplash are used until you add your own.

### 4. Site URL

Update the `site` field in `astro.config.mjs` and the `url` field in `siteData.ts` to match your production domain. This ensures sitemaps, canonical URLs, and structured data are correct.

## Blog

Add Markdown files to `src/content/blog/`. Each post needs frontmatter:

```markdown
---
title: Your Post Title
description: A short description for SEO.
author: Team
date: 2026-03-01
tags: [guides]
draft: false
---

Your post content here.
```

The filename becomes the URL slug.

## Pages

| Route | File |
|---|---|
| `/` | `src/pages/index.astro` |
| `/about` | `src/pages/about.astro` |
| `/services` | `src/pages/services.astro` |
| `/reviews` | `src/pages/reviews.astro` |
| `/contact` | `src/pages/contact/index.astro` |
| `/blog` | `src/pages/blog/index.astro` |
| `/blog/[slug]` | `src/pages/blog/[...slug].astro` |

## Deploy to Netlify

1. Push your repo to GitHub
2. Connect it in [Netlify](https://app.netlify.com)
3. Build settings are auto-detected from `netlify.toml`
4. The contact form uses Netlify Forms (no config needed)

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | Astro 7 |
| Styling | Tailwind CSS v4 |
| Typography | @tailwindcss/typography |
| SEO | @astrojs/sitemap, astro-robots-txt |
| Testing | Playwright |
| Hosting | Netlify (static) |

## Commands

| Command | Action |
|---|---|
| `pnpm dev` | Start dev server at `localhost:4321` |
| `pnpm build` | Build production site to `dist/` |
| `pnpm preview` | Preview production build locally |
| `pnpm test` | Run Playwright tests |

## License

[MIT](LICENSE) — free to use, modify, and distribute.
