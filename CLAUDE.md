# CLAUDE.md — Carnelian Landing Page

## Project Overview

A single-page marketing website for Carnelian, a distraction-free desktop writing application built with Tauri and Svelte. The site is hosted on GitHub Pages and its sole purpose is to make writers want to download the app. It links to itch.io for downloads and optional pay-what-you-want donations.

This is a static site — no frameworks, no build tools, no dependencies. One HTML file, one CSS file, one folder of images.

## Target Audience

Writers — novelists, essayists, screenwriters, bloggers working on long-form content. These are not developers. They do not care about the tech stack. They care about how the app feels to write in, whether it helps them focus, and whether it handles the mechanics of organising a manuscript.

## Tech Stack

- **HTML** — single index.html file
- **CSS** — single style.css file, no preprocessors, no utility frameworks
- **JavaScript** — minimal, only if needed for interactions (theme preview, smooth scroll). No frameworks.
- **Fonts** — Nunito Sans (Google Fonts) for body text, tagline, headings, and buttons. Courier New for the page title ("Carnelian") and navbar brand. No serif fonts in use.
- **Hosting** — GitHub Pages at **carnelianwriter.app** (custom domain via Cloudflare DNS). No server-side code, no build step.

## Design Principles

- **Writer-facing, not developer-facing.** No mention of Tauri, Svelte, CodeMirror, or any technical detail anywhere on the page. The word "markdown" should only appear where necessary to explain the file format, and even then, frame it simply.
- **Calm and warm.** The page should feel like the app — minimal, unhurried, pleasant. Earthy tones that echo the Parchment and Sepia themes.
- **Show, don't list.** Lead with screenshots and visual examples of the app in use, not bullet-point feature lists. The goal is to let writers imagine themselves using it.
- **One clear action.** Everything funnels toward the download button. No competing calls to action, no mailing list signup, no social media links cluttering the page (a small footer link to the GitHub repo is fine for those who want it).

## Page Structure

### Navbar
- Fixed to the top of the page. Left side: Carnelian icon (Carnelian Transparent.png) and "Carnelian" in Courier New, left-aligned with a "Download" link in Nunito Sans (carnelian red). No right-aligned items.

### Hero Section
- Two-column layout on desktop: left column has the "Carnelian" heading (Courier New), tagline, description paragraph, and download button — all left-aligned. Right column has the Carnelian Logo v2.png image. On mobile, the logo stacks above the text.
- Below the two-column area, a full-width screenshot placeholder.
- A prominent download button linking to the itch.io page. Label it "Download for free" or similar.

### Features Section
Three or four key features, each with a screenshot or visual and a short description (two to three sentences max). No bullet points. The features to highlight are:

1. **Typewriter mode** — the standout feature. Explain that it locks the cursor to the end of the document so you can only write forward. Frame it as freedom from the temptation to endlessly revise. Show a screenshot of typewriter mode active.
2. **Themes** — show two or three of the themes side by side (Parchment, Dracula, Forest are the most visually distinctive). Frame it as "your writing space, your atmosphere."
3. **Compile and export** — explain that you can combine chapter files into a single manuscript and export as markdown or Word. Frame it as "from scattered chapters to finished manuscript in one click." This is the feature that competes with Scrivener.
4. **Local and private** — briefly note that everything stays on the user's machine, no account needed, no cloud dependency. Frame it as "your words stay yours."

### How It Works Section (optional, keep very brief)
A three-step visual: (1) open a folder as a project, (2) write your chapters, (3) compile into a manuscript. This is for writers who need to understand the workflow before committing to a download. Keep it tight — three short sentences with simple icons or illustrations, not screenshots.

### Download Section
A repeated download button at the bottom of the page, same link to itch.io. Mention that it works on Mac, Windows, and Linux. Add a small note: "Carnelian is free to use. If you find it useful, you can support its development with a donation."

### Footer
Minimal. A link to the GitHub repository (for technical users who find their way here), a link to a simple privacy statement ("Carnelian collects no data"), and a credit line.

## Visual Direction

- **Colour palette:** Warm and earthy. Draw from the app's Parchment theme — soft creams, warm browns, muted gold or amber accents. Avoid bright whites and harsh contrasts. The page should feel like paper, not a screen.
- **Typography:** Courier New for the "Carnelian" title and navbar brand name. Nunito Sans (via Google Fonts) for all other text — body, headings, tagline, and buttons. Light weight (300) italic for the tagline, regular (400) for body, semi-bold (600) for buttons and nav links, bold (700) for section headings. Never use Inter, Roboto, or system-only fonts.
- **Layout:** Generous whitespace. Content centred with a comfortable reading width (max ~720px for text). No sidebar, no grid of cards, no multi-column layouts. The page reads like a document, top to bottom.
- **Screenshots:** These are the most important visual element. They should be large, high quality, with subtle drop shadows or rounded corners to set them apart from the page background. Show the app with real writing visible — not lorem ipsum.
- **Animations:** Subtle only. A gentle fade-in on scroll for sections is fine. No parallax, no bouncing elements, no dramatic transitions. The page should feel as calm as the app.

## Screenshots

Screenshots need to be provided as image files in an /images folder. The page should reference:
- hero.png — main app screenshot for the hero section (Parchment or Sepia theme, with real text visible)
- typewriter.png — typewriter mode active, showing the mode indicator
- themes.png — two or three themes shown side by side (or separate images: theme-parchment.png, theme-dracula.png, theme-forest.png)
- compile.png — the compile window with some files selected

Placeholder images should be used during development if real screenshots are not yet available.

## Hosting and Domain

- **Repository:** https://github.com/herny22/carnelian-site.git
- **Custom domain:** carnelianwriter.app (configured via CNAME file in repo root)
- **DNS:** Cloudflare (free plan), all records set to "DNS only" (grey cloud) — do not enable Cloudflare proxy as it conflicts with GitHub Pages SSL.
- **SSL:** GitHub Pages auto-issues via Let's Encrypt. "Enforce HTTPS" should be enabled in repo Settings > Pages once the certificate is issued.
- **SEO:** `robots.txt` currently blocks all crawlers (`Disallow: /`). Change to `Allow: /` when the site is ready to go public.

## External Links

- **itch.io download page:** [URL to be provided] — this is where all download buttons point
- **GitHub repository:** https://github.com/herny22/carnelian-site — footer link only, not prominent
- **Privacy statement:** can be a separate privacy.html page or a section within the main page

## Performance and Accessibility

- The page must load fast. No JavaScript frameworks, no heavy assets. Optimise images.
- All images must have descriptive alt text.
- The page must be fully readable without JavaScript enabled.
- Ensure sufficient colour contrast for all text, especially with the warm colour palette.
- The page must work well on mobile — writers may discover it on their phone even though the app is desktop-only.

## Things to Avoid

- No developer jargon. No mention of Tauri, Svelte, CodeMirror, npm, or any technical terms.
- No "built with" badges or tech stack listings.
- No testimonial section (we don't have testimonials yet).
- No comparison tables with competitor apps.
- No feature roadmap or "coming soon" promises.
- No mailing list signup or newsletter integration.
- No cookies, analytics, or tracking scripts.
- No AI-generated stock imagery. Only real screenshots of the app.
- Do not use generic AI design patterns: no purple gradients, no glassmorphism cards, no Inter font, no hero sections with abstract geometric backgrounds.
