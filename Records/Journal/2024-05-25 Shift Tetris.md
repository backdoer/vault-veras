---
created: 2024-05-25 13:52
modified: 2024-05-25 18:36
date: 2024-05-25
journal-type: reflection
tags:
  -


# Shift Tetris

Desired Monday CNA AM: 160 hours 
Desired Avg each hour: 20 hours 

Current Monday CNA AM: 130 hours 
Current Avg each hour: 16 hours 

9: 20 hours 
10: 15 hours 
11: 16 hours 
12: 19 hours 
13: 17 hours 
14: 16 hours 
15: 18 hours 
16: 16 hours 
17: 18 hours 
18: 15 hours 
…etc

Possible Algorithms:
- Genetic Algorithm 
- Simulated Annealing

Prep: 
- Convert each budget type to hours 
- Create list of shift templates the algorithm can use (existing templates and then exhaustive list of every iteration between the shortest length and longest length and across all hours of the day
- Fetch the relevant shifts 
- Create scoring mechanism for each current state

Score:
- Hours are distributed as evenly as possible across the hours of the day. Standard deviation of hours is low. 
- Shifts use the facility’s specified shift templates as much as possible (not our derivations). 

Rules:
- Every time of day’s constraints are met 
- You can only create shifts from the given templates
- Shifts must stay exactly within the dates given (at a certain point, we can’t keep taking the next period into account…)

Moves you can make:
- Create shift from template
- Remove existing un-filled shift
- Shorten existing un-filled shift
- Lengthen existing un-filled shift in 30 minute increments
- Merge shifts (don't go over length bounds)
- Split shifts (don't go under length bounds)

Thinking ahead:
- Supply the algorithm with the list of existing shifts so that we can eventually include filled shifts and be able to suggest lengthening/shortening shifts
