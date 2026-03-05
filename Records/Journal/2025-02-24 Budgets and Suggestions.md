---
created: 2025-01-31 17:04
modified: 2025-02-24 17:43
date: 2025-02-24
journal-type: reflection
tags:
  -


# Budgets and Suggestions

Census/CMI:
- Master schedule budgets should be based on AVERAGE census. Regress to the mean. Add average CMI to Facility and Area tables.
- Show current schedule based on actual day's census.
- Add CMI to facility census table. 
- Eventually, start tracking area census/CMI. Averages and per day.

Factor in preferences into master schedule recommendations (for employment schedules). 

Could be interesting to convert the master schedule into a budget report (head counts of shift templates per day).

Love the idea of being able to assign an "OpenShiftPlan" to a worker

Master schedule un-filled shifts:
- make employee optional on employer worker. Can use all current utilities employer worker offers (archivals, default areas, etc.)
- filter out nulls and adjust types on all current queries to maintain backwards compatibility
- AI suggestions for worker schedules to create with genetic algorithm. AWESOME use case!
- Duplicate button to quickly add new schedules 
- Create un-filled shift when shift skipped for time off 

Need to show budgets for un-budgeted resources when grouping. Currently showing nothing, for example, if there are no budgets for a certain shift template. Even though they have shifts there and it's technically a surplus.

Figure out how to display area budget rows when not budgeting by area. Probably don’t. Just do roll up.

New design for displaying the puzzle of the budget vs the actual
- Puzzle can solved for both master schedule AND the current schedule

3 dimensions of schedule: 
- Master 
- Planned (schedule)
- Actual (timesheets)

PUZZLE:
BUDGETED (can only be under):
- create open shifts (top up)
- fill open shifts
   - invite people (dynamic share)
   - pass to agency
- ask for volunteers to stay late
- pull from "un-budgeted" shifts
   - change area
   - change position
   - change time? (more friction)

UN-BUDGETED (can only be over):
- cancel un-filled shifts
- cancel filled shifts? (controversial)
- ask for volunteers to go home early or take day off
   - depending on size of gap
- re-allocate to a gap in "budgeted"
- change budget

MASTER SCHEDULE PUZZLE:
  - Simulated hires and how it would affect master schedule 
  - Suggesting changing someone's schedule based on collected preferences
