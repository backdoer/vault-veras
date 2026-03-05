---
created: 2024-12-06 16:21
modified: 2024-12-06 19:39
date: 2024-12-06
journal-type: reflection
tags:
  -


# Multi Tenant

Multi Tenant Principles:
- User identity verification (implicit right now - we trust integrations)
- User account ownership (sticky fields - fields updated by user stick)
- Tenant invites & approvals (implicit right now - we trust integrations)

Solution:
- Don't allow user phone/email updates by scheduler in app
   - Can only be updated by Veras support & directly by users
- Only allow user updates in integration if employee is active & user isn't admin
   - Maybe only allow the update if user is in one active tenant?

Need to go clean up un-used usernames
