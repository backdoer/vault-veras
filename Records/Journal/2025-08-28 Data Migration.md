---
created: 2025-08-28 20:20
modified: 2025-08-28 21:02
date: 2025-08-28
journal-type: reflection
tags:
  -


# Data Migration

Create all time tables (un-partitioned) in public
Spin down the app
Backfill the tables
Change the env var of time to point at public
Spin up the app
Change all of the prismaTime references to use prisma
Add foreign keys
Use kysely to replace all denormalized field references
Drop old denormalized fields from tables
