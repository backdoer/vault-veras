---
created: 2024-06-29 00:42
modified: 2024-07-03 12:15
date: 2024-07-03
journal-type: reflection
tags:
  -


# Assignment Architecture

Create custom assignments. Define scopes for assignment:
- Only people with assignment attached 
- Only people with certain job titles…? (Optional)
- Anyone 

Are these defined at the top level or under each position? Probably nested. 

You can then attach assignments to workers (like areas) and specify whether that worker works that assignment on certain days, every day, or as needed. 

During the filled automation, check whether the person is eligible to pick up an assignment, check if there are available allocations (assuming it’s as needed), and if both check out, add it to the assigned shift. 

During the unfilled automation, just create shifts with them attached if there are openings. Only let people pick up shifts if their assignments check out. 

Also….

Job Listing Rules: 
- make sure there is at least one RN on the floor at all times. Etc. not on a shift, hour based. 
- The other possible solution to this is to just add a job title filter to the calendar page so they can eyeball it.
