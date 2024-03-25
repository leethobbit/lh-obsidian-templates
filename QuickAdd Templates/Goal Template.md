---
tags:
  - goal
goal_type: "{{VALUE:personal,work}}"
year: "{{DATE:YYYY}}"
duration: "{{VALUE:Duration?,quarter,year}}"
complete: ❌
---

# <% tp.file.title %>

## Related Tasks
### Key Results
- [ ] #okr {{VALUE:Key result 1?}}
- [ ] #okr {{VALUE:Key result 2?}}

## Related Projects
```dataview
TABLE
	target AS "Target",
	goal AS "Goal",
	deadline as "Deadline",
	complete as "Complete"
FROM "00 Meta/02 Action/02 Projects"
WHERE goal = [[<% tp.file.title %>]]
SORT complete DESCENDING
```