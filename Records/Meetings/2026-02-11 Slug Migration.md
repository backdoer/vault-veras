---
created: 2026-02-09 21:41
modified: 2026-02-11 00:47
date: 2026-02-11
meeting-type: architecture
company-name: Veras
role: participant
tags:
  -


# Slug Migration

Migrate: 
1. Departments
2. Job positions
3. Care levels

Structure:
- Employer tables (Department, CareLevel, JobPosition)
- Facility tables (FacilityDepartment, FacilityCareLevel)

Migration plan:
1. Replace all types/references with strings
2. Implement new table structure (leave slugs in)
   - Rename CareLevel to FacilityCareLevel
   - Repurpose JobPosition to be owned by Employer
   - Create new Department and CareLevel tables
3. Reorganize contexts/functions
4. Replace all jobPositionId references 😳
5. Start fetching the dynamic values and passing them around
  -  Remove all upperCaseToTitleCase imlementations
6. Remove all of the jobPositionIds and careLevelIds from tables. Instead, have the slug and employer id.

Thoughts:
- Put slugs on all the time resources 
- Take department name off of all of the time resources?
- What about the denormalized department name on the reporting resources? 

Don't do:
- Replace slugs with ids across the board? 
   - This would have big integrations implications as well...

Should we migrate leave type as well? 
