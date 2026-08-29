# Development Examples

These are a few examples from the actual EarnVerity development history. I included them because they show the kind of work that went into the site beyond the final page design.

The production repository is private, so this public case study summarizes the work without exposing private source files or internal links.

## Screenshot examples

I kept clear screenshots from the development and testing process when an original capture was available. The current set includes a previous homepage and the later homepage so the design changes can be compared directly.

[View screenshot examples](screenshots.md)

## Fixing broken guide pages

Two guide pages were returning internal errors. I replaced the broken records with valid comparison-page records and checked that all ten pages in the batch returned HTTP 200 after the fix.

The same update also refreshed several existing pages using Search Console data instead of creating more pages only to target traffic.

What I checked:

- repaired the two failing guide routes
- verified all ten target pages returned HTTP 200
- kept the existing URLs instead of creating duplicate replacement pages
- used existing Search Console opportunities to decide which pages were worth improving

## Cleaning up repeated site copy

As the site grew, some pages started repeating the same explanations and using wording that sounded more like internal notes than normal website copy.

I went through shared content and page-specific text to remove repeated sections, simplify user-facing wording, fix duplicate sportsbook summaries, and clean up stale review-date text without changing the main URLs or referral destinations.

This was mainly a content QA pass, but it also required checking shared templates because one repeated block could affect many pages at once.

## Making review dates more accurate

A shared update was causing some pages to look newly reviewed even when only shared code had changed. I changed the logic so a page shows its own review date instead of inheriting a newer date just because shared site code was updated.

This mattered because verification dates are supposed to tell the visitor when that specific information was checked.

## Adding full site-integrity checks

I added a validation step for the sitemap and internal links across the site. The check runs during the normal build and looks for problems before a production update.

It checks for things such as:

- sitemap URLs using the correct canonical origin
- duplicate, query-string, and hash URLs in the sitemap
- pages returning HTTP 200
- canonical tags matching the page being checked
- internal links reaching valid destinations
- redirects staying on the expected EarnVerity domain
- broken one-hop redirects

This turned several manual checks into a repeatable build step.

## Deployment checks

For production changes, I used GitHub pull requests and Cloudflare preview deployments to check the exact version before merging it into the live site.

My normal flow was to make the change, wait for the preview build, confirm the build result, test the deployed page itself, fix anything that failed, and only treat the work as complete after the deployed version behaved correctly.
