---
created: 2024-11-27 18:31
modified: 2024-12-04 18:14
date: 2024-12-04
journal-type: reflection
tags:
  - keep-import
---

# DB Migration

✅ Fix timeseries query
❌ Rename gravity-db-integrations to gravity-integrations-db?
✅ Move time and reporting data into gravity-db
✅ Point time and reporting urls at new DB
✅ Set proper connection counts on url strings (20 time/gravity, 10 reporting)
✅ Consolidate gravity staging dbs (timescale and regular) into one db
✅ Deploy migration changes
✅ Scale new gravity-db to 4 performance cpus (on main machine) and 8 GB of memory. Replicas can be way less resources.
✅ Set up pg hero
- Remove old time, reporting and gravity dbs

Possibilities:
- Users with access to one schema
- Read replicas in other regions (especially for reporting DB)
- Read replica in other region for purpose of metabase & grafana
