---
created: 2024-01-31 19:59
modified: 2024-02-01 01:26
date: 2024-02-01
journal-type: reflection
tags:
  - keep-import
---

# Decouple JPN

Build out a page for joining an employer's temp pool of a specific position. This is what the advertising will link to.

We gotta figure out how to shoehorn Genesis' use case into the new model w/out the JPN.

Display shift if (shift match user view should respect this):
- Person is in employer temp pool
- Person is in JPN and employer has posted shift to JPN

Does Jobwise enforce any kind of lockout period for JPN temps? Nursa and Shiftkey don't.

Give job seekers a page where they can see their employer relationships

EmployerPoolWorkerLocation?

Should we tie the following resources to EmployerPoolWorker?:
- Shift request
- Shift invite


Rename EmployerContact to EmployerTemp?

User Owner and/or Employer Contact Owner?
- USER
- AGENCY
- JPN
- EMPLOYER

We could potentially do something here to help broker the relationship with the agency based on when the temp was first added and when the employer is allowed to try to poach them

handle "Would work there again" and "blocked at" differently.

EmployerContactStatus:
- ACTIVE
- PENDING_ONBOARDING
- PENDING_VERIFICATION
- LOCKED_BY_AGENCY
- INACTIVE
   - blocked by user
   - blocked by employer

Is onboarding different per employer?

EmployerContactPositionStatus:
- ACTIVE
- INACTIVE

onboardingCompletedAt
blockedByUserAt
blockedByEmployerAt

Employer Contact Applicant?






Applicant Status:
- New
- In Review
- Accepted
- Rejected
- Withdrawn

Agency Status:
- Locked by agency
- Not locked by agency

Contact Status:
- Active
- Pending onboarding
- Blocked by user
- Blocked by employer

Approved Positions

Pricing is also coupled currently

Does it make sense for an employer to approve a temp for a specific position?


