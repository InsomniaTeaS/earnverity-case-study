# EarnVerity Case Study

EarnVerity is a website I built to make it easier to compare apps and websites that offer ways to earn or save money. It organizes information such as eligibility, payout timing, fees, categories, restrictions, and disclosures so users can compare options without opening a long list of separate sources.

This public repository is a case study of the project. The production source code is private, so this repo focuses on the decisions, testing, QA work, and changes I made while building and maintaining the site.

**Live site:** [earnverity.com](https://earnverity.com)

**Project evidence:** [Screenshot comparison](docs/screenshots.md) | [Development examples](docs/development-examples.md)

## Homepage redesign

The homepage changed as I learned more about how the site was being used. An older version put search, listing counts, verification checks, and directory information directly into the opening section. The current version explains the purpose of the site first and gives users a cleaner way to choose where to start.

### Previous homepage

![Previous EarnVerity homepage](assets/previous-homepage.png)

### Current homepage

![Current EarnVerity homepage](assets/current-homepage.png)

The redesign was not only visual. I reduced crowded information near the top, made the purpose of the site clearer, simplified navigation, and moved category browsing into a more organized structure.

[See the full screenshot notes](docs/screenshots.md)

## What I worked on

- Built and maintained a mobile-friendly directory for earning, saving, finance, and related platforms.
- Organized platform information into structured fields so listings are easier to compare.
- Added search, filters, saved listings, dark mode, availability information, and platform detail pages.
- Improved navigation and page layout across desktop and mobile.
- Added SEO and indexing tools for individual platform and guide pages.
- Added validation checks for broken routes, canonical URLs, sitemap entries, redirects, and internal links.

## Data and quality checks

A large part of the project has been keeping the information organized and consistent. I regularly checked the site for:

- outdated or inconsistent information
- duplicate records
- broken or incorrect links
- missing platform details
- inconsistent labels and categories
- mobile layout problems
- unclear buttons or page states
- pages that looked recently reviewed when only shared code had changed

When I found issues, I corrected the data, content, or page logic instead of only changing the visual design.

## Site improvements

As the site grew, some pages became too long and repeated the same information. I reviewed the existing content and simplified parts of the site so users could get to useful information faster.

Some changes included:

- shortening repeated homepage content
- reorganizing navigation into clearer sections
- making platform information easier to scan
- improving contrast and readability
- fixing responsive layout problems
- cleaning up duplicated or outdated content
- making review dates more page-specific
- adding broader build-time integrity checks

## Research and verification

I checked information before adding or updating a platform. This included reviewing official pages, payout details, eligibility rules, fees, availability, and other restrictions when available.

For newer platforms, I sometimes contacted the company directly to clarify details instead of presenting uncertain information as verified.

## Testing and deployment

I tested pages across different screen sizes and checked common user actions such as searching, filtering, opening detail pages, saving listings, following external links, switching themes, and using long pages on mobile layouts.

For production changes, I used GitHub pull requests and Cloudflare preview deployments, tested the deployed version, fixed failures when needed, and treated the work as finished only after the deployed page behaved as expected.

## Development examples

The public development notes include examples of:

- fixing broken guide pages and checking the affected URLs returned HTTP 200
- cleaning up repeated and internal-sounding copy
- correcting review-date logic
- adding sitemap and internal-link integrity checks to the build
- checking Cloudflare preview deployments before production

[View development examples](docs/development-examples.md)

## Tools used

- HTML
- CSS
- JavaScript
- Git and GitHub
- Cloudflare Pages
- Google Analytics 4
- Google Search Console
- Bing Webmaster Tools
- IndexNow

## What I learned

This project gave me more experience with web development, structured data, QA, debugging, responsive design, deployment checks, and maintaining a live website over time. It also showed me that keeping information accurate, testable, and easy to understand can take as much work as building the interface itself.
