---
created: 2024-11-05 14:50
modified: 2024-11-05 15:19
date: 2024-11-05
plan-type: project
tags:
  -


# CPU Heavy Tasks

Reporting
- PPD calculations
- Overtime calculations

Timesheet Analysis
-  Timesheet grouping
- Timesheet stats (inferring schedules)

Integrations
- XML/JSON/CSV parsing
- Serialization/Deserialization 

Genetic Algorithm

Scheduling
- Generating schedules based on rotations

--- Possible solutions ----
- Worker threads (more cpus per machine)
    - workerpool
    - Custom implementation using worker_threads
    - Bullmq worker threads/processes
- Spin up more bullmq worker instances
