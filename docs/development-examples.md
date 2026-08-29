# Development Examples

These are a few examples from the actual EarnVerity development history. I included them because they show the kind of work that went into the site beyond the final page design.

## Screenshot examples

I also kept a few screenshots from the development and testing process. They include an early homepage layout problem, the cleaned-up homepage, mobile testing on a long platform page, and Cloudflare deployment checks.

[View screenshot examples](screenshots.md)

## Fixing broken guide pages

Two guide pages were returning internal errors. I replaced the broken records with valid comparison-page records and checked that all ten pages in the batch returned HTTP 200 after the fix.

The same update also refreshed several existing pages using Search Console data instead of creating more pages just for traffic.

[View PR #246](https://github.com/InsomniaTeaS/EarnVerity/pull/246)

## Cleaning up repeated and robotic copy

As the site grew, some pages started repeating the same explanations and using wording that sounded more like internal notes than normal website copy.

I went through the shared content and removed repeated sections, simplified user-facing wording, fixed duplicate sportsbook summaries, and cleaned up stale review-date text without changing the main URLs or referral destinations.

[View PR #268](https://github.com/InsomniaTeaS/EarnVerity/pull/268)

## Making review dates more accurate

A shared update was causing some pages to look newly reviewed even when only shared code had changed. I changed the logic so pages only show a review date when that page actually has its own review date.

This was a small detail, but it mattered because EarnVerity is supposed to make it clear when information was checked.

[View PR #269](https://github.com/InsomniaTeaS/EarnVerity/pull/269)

## Adding full site-integrity checks

I added a validation step that checks every sitemap page and the internal links found across those pages. The check makes sure canonical pages return correctly, links do not lead to broken destinations, and redirects stay on the correct EarnVerity domain.

This runs as part of the normal build so broken internal routes can be caught before a production update.

[View PR #272](https://github.com/InsomniaTeaS/EarnVerity/pull/272)

## Deployment checks

For production changes, I used GitHub pull requests and Cloudflare preview deployments to check the exact version before merging it into the live site.

This made it easier to catch problems on a preview build before they reached production.
