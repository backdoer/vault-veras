---
created: 2024-07-08 16:28
modified: 2024-08-09 01:05
date: 2024-08-09
plan-type: checklist
tags:
  -


# Project Cleanups

PPD Optimization:
- Move ppd suggestion modules into their own behavior files
- Additive suggestions
- Don't let them click the dashboard optimize button in the past
- Add a unique to the relevant user ids (for people scheduled twice in same day)
- Go through and handle decimal places throughout
- Add note input if they change hours
- Figure out default goal deviations and what to do when not present. Also when census isn't present.
- Smarter shift template suggestions
- Need to account for shifts being across multiple days
- Make sure the zod schema parse doesn't break pages. Maybe simplify what we're storing?
- Use shift position instead of job position in ppd displays
- Use the reported hours from the scheduler to project PPD instead of the hours in Jobwise....?
- When restarting the optimization, start with the hours they originally entered
- Don't let them optimize the future past today? Should maybe be a daily thing. Future could just be getting in line with budgets.
- Need to get salaried hours into the system.
- Add everything to mobile app 
- Other goal types

Later:
- Allow them to change current optimizations (cancel outstanding volunteer requests, etc.)
- Frontend for job seeker to volunteer 
- Create VolunteerRequest table for handling opt ins for shortens and lengthens 
- Eventually create ShiftAlteration table for storing when the shifts get updated (would also tie into the audit log on shifts)
- Create facility census record from the value they put into census? Get rid of "Add daily census"?
- Give reports on how often and successfully they're optimizing
- Tapered outreach for volunteers 

Nice to have inbox:
- In noti, add link to change notis. Also include prompt to install app.
- Callouts when people leave or join conversation
- Denormalize user connections
- Tags
  - Searching
  - Filtering
  - In current conversation, position, facility, agency, etc.
  - Etc.
- Remove code
   - twilio registration status
   - twilio registration process
- Notification callouts in convo
