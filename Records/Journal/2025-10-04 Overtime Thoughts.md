---
created: 2025-10-04 23:07
modified: 2025-10-04 23:07
date: 2025-10-04
journal-type: reflection
tags:
  - keep-import
---

# Overtime Thoughts

Revisit overtime
✅ Day overtime not being calculated correctly - not accounting for all shifts/ts
✅ Change the cutoffs to midnight-midnight
✅ Take off the shift and put in reporting
✅ Staleness instead of zeroing out every record
- New hybrid report reflecting timesheets -> shifts (once T&A is ready)
❌ Granularity should be at employee, not worker...? But facility needs to be there..
❌ Account for utilization in same report? Utilization needs to be at week level

Tables:
- Employee Daily (Scheduled/Actual/Hybrid) Work
    - Factors in ot, dt, regular hours and shift count
    - Hybrid could have short ttl (will mirror actual)
- Employee Weekly (Scheduled/Actual) Work
    - Factors in ot, dt, regular hours and shift count
    - Factors in utilization (hrs and shift count)
- Facility Daily (Actual/Scheduled) PPD
- Facility Daily (Actual/Sched.)(TOD/ST) Budget
    - Don’t factor in areas here
    - Maybe include areas as a jsonb or diff table?

