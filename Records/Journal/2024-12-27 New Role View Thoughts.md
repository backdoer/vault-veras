---
created: 2024-12-27 16:18
modified: 2024-12-27 16:34
date: 2024-12-27
journal-type: reflection
tags:
  - keep-import
---

# New Role View Thoughts

I think the new role view could be built in an hour. There are 2 ways we could approach this. Hear me out.

Here are the steps (option 1):
1. Copy and paste the staff calendar and the getScheduleByStaff context
2. Keeping allowing 3 group bys up top
3. Use the first group as a header row
4. Use the next 2 groups to replace the current worker row name/position. Have a row contain "headerOneTitle", "headerOneColor", "headerTwoTitle", "headerTwoColor". 
5. Do we let them remove any group bys? What shows up in the group header if so?
6. When formatting on the backend, just have things fall into rows based on index. Go until there are no more indexes left.

Option 2:
The area view is basically already this view. We could use 3 header rows (like we do on the staff calendar) with no y axis. So it would essentially be merging the area view and the staff view.
