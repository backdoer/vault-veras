---
created: 2025-01-24 14:53
modified: 2025-01-24 14:55
date: 2025-01-24
plan-type: project
tags:
  -


# Deadlock Plan

Create a new createShifts function that handles the bulk creation (could do some in parallel) and then grabs the unique worker weeks and refreshes overtime with a new function (refreshShiftOvertimes). Put the logic from cancelShiftsWhere and unassignShiftsWhere into refreshShiftOvertimes and then use that function from there as well. Have an arg that we can pass into createShift that tells it not to run refreshOvertime (will only be used from places that are creating in bulk).
