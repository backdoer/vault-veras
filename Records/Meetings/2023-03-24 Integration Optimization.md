---
created: 2023-03-17 04:44
modified: 2023-03-24 17:41
date: 2023-03-24
meeting-type: internal-meeting
company-name: Veras
role: participant
tags:
  -


# Integration Optimization

v2:
- Add indices to heavily searched fields 
- Decouple dump from load
- Should external and connectors be merged?
- Dynamo.....?
- Fix Ellucian timing issues (maintenance window)
- Pull nexus wage and FE resources (for Heavy Equipment)
- Integration coverage documentation (what's pulled/pushed for each)
- Use a loadedAt instead of updatedAt on external tables to check against for syncs

v3:
- Better upsert many (in load) sql (instead of one-off upserts)
- Pointers for load/sync table workers that can pick back up where they left off
- Add error reporting back in
