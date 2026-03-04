---
created: 2025-11-25 20:05
modified: 2025-11-25 20:33
date: 2025-11-25
meeting-type: internal-meeting
company-name: Veras
role: participant
tags:
  - keep-import
---

# Senior Lifestyle PPD Budgeting Reporting

PPD report will not show budgets, it will show goals (hours, ppd, etc.). This will always be based on job positions and employments. PPD report does not show budgets. We just need to clean up the logic for assigning a job position to a shift. If, in the future, they want more control over which job position/employment gets selected, we could add a select to the shift. If we want to put the employment on the shift, we should probably make the job position on the employment immutable. This assumption will help pre-fill the employment select at the point of clock-in (which the worker can then override).

Budget report will be a different report that will report based on TimesheetShifts. Budgeting is a scheduling concept. It is based off of shift positions.

We also need to get a care level on a timesheet. When they're clocking in, if the employment they pick has multiple care levels, then we ask them which care level they're working. 

We'll eventually let them create custom job positions and departments, and when they add them, we'll ask them for the pertinent CMS job code for that job position.
