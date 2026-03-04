---
created: 2025-12-11 23:21
modified: 2026-02-07 06:22
date: 2026-02-07
meeting-type: architecture
company-name: Veras
role: participant
participants:
  - Tyler Doermann
tags:
  - keep-import
---

# Single Tenant Migration

High level:
✅ Every single experience should be scoped to an employer id, even user edits
✅ Create central member database/service to house all members. Put a account id on the user and start running auth through the members service.
✅  Make sure every prisma call in the app has access to an employer id 
✅ Migrate to the new data model: A member can have many users. A user has a member id and employer id on it and can be an employee, an agency worker, etc.

New data structure:
✅ An employer worker should be unique based on user, not employee... right?
✅ Remove unique constraint between user and employer on employee

Clean up:
✅ Re-organize contexts (move user employer, merge candidate with user, etc.)
✅ Rename remaining functions/models/tables that reference "employee"
✅ Fix partition archivals
✅ Checkbox to push account changes to all users
✅ Don't archive shifts unless flag is on

DB changes:
✅ Create centralized prismaCore DB
- Move reporting to its own DB (or just leave in one of the shards as is for now?)
- Merge time schema in with regular schema?
   - Add some foreign keys and prefix the reverse relations with unsafe
   - Update trigger with time refs
   - Rename time_partitions to partitions
   - Ship late at night since there will be temporary downtime

Late Night thoughts:
- add name to shard?
- encrypted creds or aws secret ref for db url? 
- Cache enriched account in redis on read
- Overtime needs to be rolled up to business entity

Sharding Complexities:
- Health checks (point at dedicated "health check" tenant?)
- Partitions
- Migrations
- Pgbouncer instances
- Admin portal (should this query redshift? or just make single tenant?)
- Data warehouse (redshift?)

