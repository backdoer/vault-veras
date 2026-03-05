---
created: 2024-03-06 01:13
modified: 2024-03-27 16:01
date: 2024-03-27
journal-type: goals
tags:
  -


# Scheduling V1

Questions:
How do we want to prevent scheduling conflicts?
Connect AgencyScheduledWorker to Agency resource (which would have cost data associated)?
Should a user be able to update their account if they were created by workday? We could add a copy of contact info to the employee?
How should we collect ratios? They are general per facility

Auto:
- Auto prefill settings from time sheets
- Auto create
- Auto assign shifts
- Auto assign areas
   - Should we re-assign every time any shift scheduled worker changes?
- Auto invite empty shifts
- Auto correct to hit PPD goal

Resources being sourced by Azure:
- User
- Employee

Resources being sourced by Workday:
- Facility
- EmployerWorker
- ShiftReport...? Timesheet?
    - Should this be something else? Probably. Going to be hard to associate with a shift. We also don't care as much about Jobwise EOR overtime (from ShiftReport) - it's a separate consideration.
