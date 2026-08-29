# Screenshots

These are real EarnVerity development screenshots. I am only adding images here when I have a clear original capture instead of a compressed thumbnail.

## Early homepage layout issue

The search controls and category links were running together in an early version of the homepage. I used this as one of the layout issues to clean up.

## Current homepage

The later homepage uses a cleaner hero section, clearer navigation, and a simpler category-browsing layout. I changed the page so users can understand what EarnVerity does faster and start browsing without digging through too much repeated content.

![Current EarnVerity homepage](../assets/current-homepage-hd.jpg)

## Mobile platform page testing

I checked long platform pages on a phone-sized layout to make sure detailed information stayed readable and usable on smaller screens.

### What I checked on mobile

**Top of the page**

I checked that the warning, breadcrumb, platform name, main heading, description, and offer card stayed readable without horizontal overflow.

**Long sections and cards**

I checked sections such as required action, eligibility, timing, costs, payout steps, and promotion details to make sure the cards stacked correctly and the page was still easy to scan.

**Long-page usability**

Because platform pages can contain a lot of information, I checked spacing, text wrapping, button width, section order, and whether the page remained usable while scrolling on a narrow screen.

## Deployment QA

I used Cloudflare preview deployments to check changes before treating them as finished. When a build failed, I checked the failed deployment, fixed the problem, and ran the deployment again instead of assuming the change worked locally.

My normal check was:

- make the change in GitHub
- wait for the Cloudflare preview build
- check whether the build passed or failed
- open the deployed version and test the affected page
- fix any issue and deploy again if needed
- only treat the update as complete after the deployed version worked

This helped catch problems that were not always obvious while editing the site.

I am leaving the early-layout, mobile, and deployment screenshots out for now because the copies I recovered are low-resolution thumbnails. I will only add those once I have usable original captures.
