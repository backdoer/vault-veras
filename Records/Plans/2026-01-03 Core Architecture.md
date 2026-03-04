---
created: 2025-09-24 21:41
modified: 2026-01-03 04:17
date: 2026-01-03
plan-type: project
tags:
  - keep-import
---

# Core Architecture

Architecture:
Single tenant (sharding)
Domain driven design with lean interfaces 
Integrations
Reporting platform
Messaging architecture
Master schedule architecture (rotations, applying master schedule, etc.)
Shift request/Shift Invite hashing
Workers
Crons
Tasks
Date lib (timezones)
Requests lifecycle (action handlers, fetchers, type safety, file handling, params)
Get grouped scheduling resources
Budgeting
Optimize open shifts
Optimize shift positions/areas
Notifications
Time partitioning
Time resources (partial denormalization)
Archival/lifecycle management (S3 Parquet)
Websockets
TImesheet/Shift Clustering
Infer schedules
Vite migration / builds
Instrumentation/monitoring/alerts (exporters, grafana, pghero, betterstack)
BI platform (metabase)
Testing configuration (big help from Garrett)
Prisma enhancements (timeseries, kysely custom query, upsert many)
Shift positions (many job positions can take a shift position)
sequentialMap & concurrentMap
Multi-select
Care Levels
Overtime logic

Themes:
- Proactive typescript
- Zod (redis, workers, websockets, integrations, requests, tasks, crons)
- Adapter pattern 


Values:
- Regression coverage 
- Extensibility 
- Scalability
- Simplicity 
- Quality 
- Readability
- Discoverability 











Architecture I didn't build:
- Mobile app
- Authentication
- Component library
