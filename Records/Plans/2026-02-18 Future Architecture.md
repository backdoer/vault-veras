---
created: 2025-10-17 03:25
modified: 2026-02-18 22:59
date: 2026-02-18
plan-type: checklist
tags:
  - keep-import
---

# Future Architecture

Time off:
- keep the current start and end as dates 
    - probably rename to startDate and endDate
- add new fields for time (start and end)
- Then we won’t have to refactor the current way of using the whole day. It’d be additive. 
- Potentially only allow the new way for people on our time and attendance/time off product. 

Multiple services:
- remix can continue to act as the bff forever 
- we could pull out certain backend functionality if we want to isolate it or write it in a different language. We could also share the same single tenant databases and pool with pgbouncer. 

Node (CPU):
- add an abstraction around worker threads to be able to utilize multiple CPUs and offload intensive tasks to a different thread (worker threads)

Databases:
- Core
    - Put the majority of reads in Redis
- Reporting
    - Move to its own postgres DB and scale reads with replicas
    - Time partitioning
- Integrations
   - Could move to Dynamo
   - Could clear more often
   - etc.
- Tenant
   - Spread out load across multiple databases
   - Single-tenant for some customers
   - Time partitioning

Could always add custom web url to shard if we want to do single tenant web 
