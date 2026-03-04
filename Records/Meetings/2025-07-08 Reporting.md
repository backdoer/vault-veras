---
created: 2025-05-29 20:39
modified: 2025-07-08 17:18
date: 2025-07-08
meeting-type: internal-meeting
company-name: Veras
role: participant
tags:
  - keep-import
---

# Reporting

Timesheets:
✅ Scheduled shifts on day report aren't always lining up with timesheet shifts
✅ Timesheets mis-associating with shift actuals for some reason
✅ Set stale if not updated
✅ Contributing towards ppd & on the floor (apply to timesheets)
✅ Is_Deleted flag from workday
✅ Consistency across timesheets, shift actuals, timesheet shifts, and rolled up ppd and overtime
✅ Doubles aren't associating correctly to timesheets (e.g. extra time)
✅ Change daily report on dashboard to calculate instead of using the timeseries data? Only use timeseries for timeseries charts.
✅ Dedupe overtime timesheets
✅ Insert 0-overtime days
✅ Add area and position filters to facility reports
✅ Add summary rows to the rest of the chart report drill downs
✅ Add tardies 
✅ Move leaderboard in with the rest of analytics
✅ Pagination
✅ Move credentials to be an extra report and off the nav
✅ Pull hourly from workday
✅ Extra time math not adding up
✅ Different colors and chart summary descriptions
✅ Week constrained overtime and rolled up weekly hours on table. And click 
through to see shifts. Make it a utilization report?
✅ Overtime should calculate at the facility/inividual level. Not the department level.
✅ respect facility filter when marking timesheets stale 
✅ Should we cluster timesheets? (new timesheet shift)
✅ Fix edge duplicates with timesheet shift association and unassociation logic 
✅ make timesheet shift a hypertable
✅ error handling around sync and mark sync as failed 
✅ Switch meal remedies to be based on new timesheet shift
✅ Update daily report cards to use new metrics
✅ Backfill meal break remedies (filter out stale)
✅ Make meal breaks logic consistent across app 
✅ remove state filter from meal remedy task
✅ Actuals & PPD on BIPA
- Stalled more than allowable limit bull errors
- Tests for timesheet clustering
- Cluster agency shifts and get them into the PPD report
- Add dates to dashboard conflicts even if multiple shifts
- Updated OT logic and pull OT off shift  (midnight to midnight) and update in background more
- More reports:
    ✅ Facility leaderboard
    ✅ Shift incentive
    ✅ Un-filled open shifts
    ✅ Unscheduled 
    ✅ Absences
    ✅ Time off
    ✅ Messages
    ❓ Shift swaps
    ❓ Utilization
    ❌ Shift invite accept rate 
    ❌ Budget
    ❌ Outlier Timesheets?
    ❌ Employee turnover
- Add expected hours to "OvertimeActual" and "OvertimeProjected" reports and we can do utilization with it?
- Make overtime fields not nullable and actualMatched shift column
- Drill-down on specific point dates on graph
- Configurable extra time, tardy, and missed break thresholds
✅ Trend lines
✅ Tooltip on the thresholds we're using for extra time and tardies
✅ Add meal breaks flow back into report
✅ Speed up reporting and integrations and clustering pipelines
   ✅ monitoring 
   ✅ Drop old reports
   ✅ Bulk inserts
✅ Increase resources of integrations DB so we get less errors
✅ Redo leaderboard metrics
✅ Simplify enterprise reporting and rip out unnecessary reports and events
✅ Timesheet counts towards ppd:
   ❌ set from shift?
   ✅ display that it doesn’t count on table
   ❌ Allow them to change it from the table?
✅ Disclaimers on slow-to-update pages  
❌ Sanity checks
❌ New PACS data
❌ Pull summarized PPD/OT
❌ Allure auto deducts breaks (are we getting that from smartlinx?)
❌ Shorten backfill ranges
❌ Charts to be configurable
❌ Maybe rename things so they don't compare apples to oranges
❌ Refreshes in place for Overtime and Shift/Timesheet associations
❌ Timesheet statuses?
❌ Calculate future overtime based on actuals 
❌ Track whether a shift pick up came from an invite or request
