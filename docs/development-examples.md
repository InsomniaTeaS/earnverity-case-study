# Development Examples

These are a few examples of work I did on EarnVerity while building and maintaining the site.

The main project repo is private, so this page gives simple summaries without sharing private code.

## Screenshots

I kept clear screenshots when I had the original files. The current screenshots show an older homepage and the current homepage so the changes are easy to compare.

[View screenshots](screenshots.md)

## Fixing broken guide pages

Two guide pages were returning errors. I fixed the broken records and then checked the affected pages again.

I also checked the full group of ten pages from that update and made sure they all returned HTTP 200.

What I checked:

- fixed the two broken guide pages
- checked all ten pages in the update
- kept the existing page URLs
- used Search Console data to decide which pages needed work

## Cleaning up repeated copy

Some pages started repeating the same information as the site grew.

I went through shared and page-specific text, removed repeated sections, simplified wording, fixed duplicate sportsbook summaries, and cleaned up old review-date text.

Because some text was shared across many pages, I checked those changes carefully so one update would not create problems elsewhere.

## Fixing review dates

Some pages looked newly reviewed even when only shared site code had changed.

I changed the logic so each page could use its own review date instead of automatically showing a newer shared date.

## Checking links and sitemap pages

I added a build check for the sitemap and internal links.

It checks things like:

- sitemap pages loading correctly
- duplicate sitemap URLs
- page canonical links
- broken internal links
- redirects going to the right place

This made some checks automatic instead of having to do all of them by hand.

## Deployment checks

For bigger changes, I used GitHub pull requests and Cloudflare preview builds before updating the live site.

My normal process was simple: make the change, wait for the preview, check the page, fix anything that was wrong, and then finish the update after the deployed version worked correctly.
