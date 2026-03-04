---
created: 2022-11-24 19:05
modified: 2022-12-01 00:42
date: 2022-12-01
tags:
  - keep-import
---

# Embedded Job Board Migration

- [ ] Announce deprecation date of old job boards. Tell people to go through and curate their job board (location, categories, styles, etc.)
- [ ] Add google analytics to site
- [x] Add job boards to postgres
- [x] Migrate data
- [x] FIx job descriptions
- [x] Fix picture hosting
- [x] Fix resume hosting
- [x] Put fallback icon into prod bucket and point at that
- [x] Account for all jobwise calls
- [x] Flip domain
- [x] Redirect app.jobwise.com to jobwise.com
- [x] Fix google places api whitelist
- [x] Handle post-a-job-route
- [x] Handle benefits?
- [x] Davis high schools need to swap out their snippet ASAP
- [x] Double check app.jobwise.com...
- [x] Add categories to embedded job boards 
- [x] google places search...
- [x] Address gets overridden if you change a category...
- [x] Pull action function out
- [x] Put in location and categories into static text? 
- [x] Versioning - flip old column?
- [x] Iframe 
- [x] Make job board responsive. Make settings page responseive.
- [x] Jobs aren't updating across different job boards.... only the first javascript loads 😔
- [x] Solidify static content
- [x] Ability to delete job board
- [x] Surface "too many job boards" error
- [x] Create job board creation portal 
- [x] Tell them when they need to replace the snippet (style changes)
- [x] Store version in db instead of needs update and last accessed date. Consolidate migrations
- [x] Referrer urls and utm? 
- [x] Add banner for schools that don't have phone number
- [x] Debounce all queries to update job board. Ensure reasonable amount of queries made.
- [x] Include both city and state in formatted address (fix google place id?)
- [x] Add descriptions to inputs (location, radius, etc.)
- [x] Allow custom values for font
- [x] Handle js injection 
- [x] Memory leak?
- [x] Handle employer logos that aren't there
