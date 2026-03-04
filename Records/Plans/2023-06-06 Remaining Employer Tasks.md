---
created: 2023-06-02 23:22
modified: 2023-06-06 17:44
date: 2023-06-06
plan-type: project
tags:
  - keep-import
---

# Remaining Employer Tasks

Done:
Cron to expire jobs
Automatically adding expiration dates based on config
Auto add credits (should be idempotent and mutexed)

If we need to add custom expiration dates later, we can add a one-off days-to-live to the job that will override the default daysUntilExpiration in the plan config.
