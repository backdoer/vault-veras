---
created: 2025-07-16 00:00
modified: 2025-07-16 13:40
date: 2025-07-16
plan-type: project
tags:
  - keep-import
---

# Postgres Partitioning

QA Plan:
- Fork our production database and re-index our tables to be postgres partitioned instead, and then test query performance

Not using timescale's:
- Continuous aggregates
- Compression
- Native archival

New benefits:
- RDS instead of Timescale Cloud
- More control over partition creation
- Automatically updates partition when you update the partitioned value

Refactor:
- time_bucket_gapfill function

Implementation:
- Put the partitions in their own partitions schemas to get rid of noise
❌ Use pg_partman to automate the partition creation process
