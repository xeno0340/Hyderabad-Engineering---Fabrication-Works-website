# Hyderabad Engineering & Fabrication Works - Business Website

A multilingual, SEO-optimized marketing website built for a stainless steel fabrication business based in Mahabubnagar, Telangana, India, designed to establish local search visibility across a linguistically diverse customer base.

**Live site:** https://hyderabadengineeringworks.com

## Problem

The client, an established steel fabrication and railing installation business operating since 2014, had no direct digital presence beyond third-party directory listings (Justdial, IndiaMART), which limited control over branding, content accuracy, and discoverability. The business serves a customer base spanning multiple language communities across Telangana, requiring a site usable by non-English speakers without relying on browser-level translation.

The project required building a site from a real client brief with an existing brand identity (logo, color scheme, established business name) rather than a blank-slate design exercise, and integrating it with the business's existing Google Business Profile and local search presence.

## Approach

The site was scoped as a single-page, static brochure site rather than a multi-page application, given the absence of any backend requirements (no user accounts, forms, or dynamic data). Content is presented in four languages - English, Hindi, Urdu, and Telugu - selected through a mandatory language prompt on first visit, with the choice persisted in browser storage and changeable at any time through a header switcher. Urdu is rendered with full right-to-left layout support.

Particular attention was paid to search engine visibility for a newly registered domain competing against established, high-authority directory sites for local search terms. This included implementing JSON-LD structured data (Schema.org LocalBusiness and Organization types), ensuring core content is present in static HTML rather than injected exclusively by JavaScript, submitting an XML sitemap through Google Search Console, and configuring keyword-relevant metadata aligned with actual local search query patterns rather than generic industry terms.

| Component            | Responsibility                                                                            |
| -------------------- | ----------------------------------------------------------------------------------------- |
| Language system      | Detects first visit, presents language gate, persists choice, applies RTL layout for Urdu |
| Structured data      | JSON-LD LocalBusiness schema describing address, hours, services, and service area        |
| Static content layer | Services and gallery content rendered directly in HTML for crawler visibility             |
| SEO metadata         | Canonical tags, Open Graph tags, sitemap, robots.txt                                      |

## Tech stack

- HTML5, CSS3, vanilla JavaScript
- Tailwind CSS (utility-first styling)
- Google Fonts (Oswald, Inter)
- Hosting: Cloudflare Pages, continuous deployment from GitHub
- DNS and SSL: Cloudflare

## Running locally

Clone the repository:

    git clone https://github.com/xeno0340/Hyderabad-Engineering---Fabrication-Works-website.git
    cd Hyderabad-Engineering---Fabrication-Works-website

No build step or dependencies are required. Open `index.html` directly in a browser, or serve the directory with any static file server, for example:

    npx serve .

## Project structure

    index.html      Page markup, structured data, and metadata
    style.css        Custom styling, animations, and theming
    script.js         Translation data and language-switching logic
    sitemap.xml    XML sitemap for search engine submission
    robots.txt       Crawler access configuration
    images/              Logo, storefront, and project photography

## Limitations

The site is intentionally framework-free and has no backend, so it cannot currently support features such as a contact form with server-side handling, an admin-editable content system, or a customer review submission flow directly on the site. Translations were produced with machine assistance and reviewed for structural correctness, though full native-speaker verification across all four languages is an ongoing process.

## Future work

- Native-speaker verification pass across Hindi, Urdu, and Telugu content
- Integration of a lightweight backend for a direct quote-request form
- Expansion of the project gallery with categorized filtering
- Analytics integration to track which language variants and services drive the most engagement

## Author

Developed and deployed independently for a family-owned business, covering the full project lifecycle: client requirements gathering, information architecture, multilingual content strategy, visual design within an existing brand system, frontend development, DNS and hosting configuration, and technical SEO implementation including structured data and search console integration.
