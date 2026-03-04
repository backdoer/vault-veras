---
created: 2026-02-13 16:57
modified: 2026-02-13 16:58
date: 2026-02-13
meeting-type: architecture
company-name: Veras
role: participant
participants:
  - Tyler Doermann
tags:
  - keep-import
---

# Old Architecture Thoughts

Contexts: 1 per product

Custom departments:
- Could honestly allow custom job positions (at employer level) and still use slugs (prefix theirs with department and CUSTOM)
    - Could do the same thing with departments....? Custom department slugs with custom job positions under it?
    - Basically you make it so employers can create their own deparment/job position slugs/config and we prefill those always but then let them create their own. Always prefix with CUSTOM
    - Migration would involve changing all of the departmentslug args to accept a string (or centralize a new department slug type that is just a string or BaseDepartmentSlug (our current ones). Would need to get rid of all uppercasetotitle
    - allows renaming departments & job positions
    - We’re basically just converting our current job position config file into employer/facility tables. And converting our current slug enums into strings
- Have a FacilityJobPosition and EmployerJobPosition table. The slugs are how you link them. So facilities could have their own custom positions and departments (wouldn’t be able to integrate them). The EmployerDepartment would source the current checkboxes in settings  and EmployerJobPosition would source the current integration mappings. 
- Could do the same thing with care levels. 
- If an employer archives a top level department, facilities who are on it can stay on it. We’d just call out that it’s deprecated. 

Databases:
- Make main database single tenant (shard)
- Pull reporting out into its own db - could load balance writes and scale reads with replicas
- Centralized core database that could be scaled with replicas or redis hydration
- Integrations db (could be put in dynamo if needed)

Payroll:
- Home facility? And everything transfer back to that facility for payroll purposes but we credit/debit where necessary to keep the books in check
- A facility can only have 1 EIN (EIN can have many facilities)
- This would make it so an employee would only ever have one W2
- Payroll could technically live at the facility level with this model

Payroll edge cases:
- one worker working at 2 different facilities with different eins and being paid out by one of them and handling the labor allocation with GL
- one worker working at 2 different facilities with different eins and being paid out by both individually
- one worker working at 2 different facilities with the same ein 

Effective at/until dates on settings? Or how to make sure things get snapshotted correctly

