# Hyderabad Engineering & Fabrication Works - Business Website

A multilingual, responsive marketing website built for a stainless steel fabrication business based in Mahabubnagar, Telangana, India. The site is designed to serve a linguistically diverse local customer base and to support the business's local search visibility.

**Live site:** https://hyderabadengineeringworks.com

## Overview

The client is a steel fabrication and railing installation business serving customers across Telangana. The site was built to establish a professional digital presence, replace reliance on third-party directory listings, and support local search discoverability through structured data and on-page SEO.

## Features

- **Multilingual support** - English, Hindi, Urdu, and Telugu, with a mandatory language-selection prompt on first visit and a persistent language switcher. Includes full right-to-left layout support for Urdu.
- **Responsive design** - built mobile-first with a consistent experience across phone, tablet, and desktop viewports.
- **Local SEO implementation** - JSON-LD structured data (Schema.org LocalBusiness and Organization types), a submitted XML sitemap, a configured robots.txt, canonical tags, and Open Graph metadata.
- **Static, crawlable content** - core content (services, gallery, business information) is rendered directly in HTML rather than injected exclusively via JavaScript, to ensure full visibility to search engine crawlers regardless of JavaScript execution.
- **Custom visual identity** - a design system built around the client's existing brand colors and logo, including a custom typographic pairing, scroll-triggered reveal animations, and an SVG-based service icon set.
- **Integrated business tools** - embedded Google Maps location, direct-dial and WhatsApp contact links, and a live connection to the business's Google Business Profile.

## Tech Stack

- HTML5, CSS3, vanilla JavaScript (no framework dependency)
- Tailwind CSS for utility-first styling
- Google Fonts (Oswald, Inter)
- Hosted on Cloudflare Pages with automatic deployment from this repository
- DNS and SSL managed through Cloudflare

## Architecture Notes

The site is intentionally framework-free. Given the scope - a single-page brochure site with no backend, authentication, or dynamic data requirements - a static HTML/CSS/JS approach was chosen over a JavaScript framework to minimize build complexity, eliminate a build step entirely, and keep deployment straightforward through direct Git integration with Cloudflare Pages.

Translations are stored as a structured JavaScript object and applied via a single rendering function, allowing the four supported languages to share one page structure without duplicating markup.

## Project Structure

    ├── index.html          Main page markup and structured data
    ├── style.css            Custom styles, animations, and theming
    ├── script.js             Language switching, translation data, scroll interactions
    ├── sitemap.xml         XML sitemap for search engine submission
    ├── robots.txt            Crawler access rules
    └── images/                  Logo, storefront, and project photography

## Deployment

The site is deployed via Cloudflare Pages, connected directly to this repository's `main` branch. Any commit pushed to `main` triggers an automatic rebuild and redeployment, with no manual upload step required.

## Author

Developed and deployed independently, covering the full project lifecycle: requirements gathering, information architecture, visual design, multilingual content strategy, frontend development, deployment configuration, and technical SEO implementation.
