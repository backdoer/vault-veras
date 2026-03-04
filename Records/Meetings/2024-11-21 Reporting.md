---
created: 2024-08-15 05:17
modified: 2024-11-21 17:25
date: 2024-11-21
meeting-type: internal-meeting
company-name: Veras
role: participant
participants:
  - Tyler Doermann
tags:
  - keep-import
---

# Reporting

✅ Look into formatting of report minutes on downloads (we're sometimes converting to hours at display time)
✅ Need to pass in downloadRows to table instead of canDownload (so we get all of the data)

CSV download of the schedule

Reports:
- Shifts on employment schedule vs off 
- Report for a day on PPD, census, all shifts, etc.
- Agency Spend
- OT & DT %
- Email/Text Digest 
- Facility Leaderboard
- Clinician satisfaction from surveys
- Spend reports
   - Agency
   - Wages
   - Missed Meals
   - Extra Time
- Consecutive days worked OT reporting (Chad request)
- Budget reporting
   - Shifts that weren't picked up/Expired Shifts
- Assignment reporting
- Compliance/Regulation reporting (1 RN on the floor)
- Time off Reporting 
- Messages reporting
- Area Reporting
  - PPD
  - etc.
- Un-planned overtime (wasn't planned per the shifts)
- Unnecessary overtime
- Who approved shift requests report
- Who assigned people to overtime shifts
- Who assigned people to agency shifts
- Raises over time?
(Tegan requests):
-how many shifts were picked up through the app and approved by scheduler
-how many shifts were shared
-consolidated report of shifts
-how many call off invites were sent and how many were picked up by staff
-origin of picked up shifts

What does "Last Minute Pickup" mean on the leaderboard?

Sanity check:
SELECT *
FROM "Timesheet"
WHERE "startTime" > NOW() - INTERVAL '14 days'
AND NOW() - "updatedAt" > INTERVAL '48 hours';

Agency:
- Put hours worked on Agency Shifts report
- Would be cool to coalesce worked hours with planned hours on PPD actual? (similar to cost)
- Maybe separate out projected and actual spend functions so we can always just use shifts with projected instead of coalescing timesheets...

Enhancements:
- Hide the legend
- Commas on the numbers
- Spend for agency, extra time, missed meals, etc.
- Who's approving shift requests?
- Rolled up table metrics at the bottom
- Be able to sort by the closest expiration date on a credential
- Facility groups 
- when seeing mult communities on a report, not giving the sum, but where each one is at
✅ Hire date on termination report
✅ Put filters in drawer
✅ CSV Downloads (add to the Table component (using columns) and Chart component)
✅ Sorting
✅ Sort the data in the tooltips to make it easier to read
- Position filter?
- AI summaries
❌ Server side pagination so we can show all records?
- Link between reports
- Information icons
- Saved Filter Views
