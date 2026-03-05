---
created: 2025-10-29 22:09
modified: 2026-02-17 06:47
date: 2026-02-17
plan-type: project
tags:
  -


# My Priorities

Actual and projected PPD should probably both be using job position. Projected is currently still using shift position.

Put wage info on separate resource and link it to the timesheet directly. Timesheet will have employment id, employment wage, and job position. Employment wage should have effective at. 

Timesheet tagging:
- Leaning towards re-coding timesheets based on settings within a pay period
- Allow manual overrides on the timesheet - which would not be re-calculated
- Changes to the start and end time of a timesheet follows the immutable flow of marking the old timesheet as deleted and creating a new and re-running the coding
- PPD and overtime can have a custom start of day time
- Shift positions and employments will be assigned based on shifts when possible, otherwise primary employment when possible, otherwise etc.
- Keep tags separated on timesheet? So they can more easily override them? Or store flattened?

Old timesheet tagging:
- Write the segments and tag immediately at creation
- Eventually, allow overrides of the segments which updates the timesheet segments inline, with an audit trail

Senior Lifestyle:
- Timesheet coding/reporting
- Add admissions department
- Custom timeframe for PPD
- Census and projected PPD in PPD line chart
- Agency hours/cost
   - https://verasco.slack.com/archives/C0960CUAGTW/p1761863651804739
- Hours don't line up
   - https://app.hubspot.com/contacts/20279079/record/0-5/33560611505/
   - https://verasco.slack.com/archives/C0960CUAGTW/p1761662534370649
   - https://verasco.slack.com/archives/D07BSPRB2EQ/p1761761951953399
- Add budgets to PPD report
   - https://verasco.slack.com/archives/C0960CUAGTW/p1761058940145779
- New positions
   - https://verasco.slack.com/archives/C0960CUAGTW/p1761320005024899
- Summary
   - https://verasco.slack.com/archives/C0960CUAGTW/p1761601720580689

AWS Cleanup
- Touchmark integration -> gravity
- Grafana
- Tigris -> S3
- Back to you SFTP server
- Turn off fly

Bugs:
- Shifts double creating 
   - https://verasco.slack.com/archives/D07BSPRB2EQ/p1761237471548409

Other:
- Arbor integration
- Tide integration timesheets and time off
- Sapphire timesheets
- Vetter data relay
- Nursa integration
- Clean up (tests, hygiene, etc.)
- Master schedule recommendations based on logged optimziations

