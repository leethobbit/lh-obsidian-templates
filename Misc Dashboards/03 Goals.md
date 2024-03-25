---
cssclasses:
  - cards
banner: "[[image.jpg]]"
banner_x: 0.5
banner_y: 0.144
---

# OKRs
```tasks
not done
path includes 02 Action
group by filename
tags include #okr
```

# Reference
- [7 Key Tenets for OKRs by Todoist](https://todoist.com/productivity-methods/okrs-objectives-key-results#7-key-tenets-for-making-okrs-work)
- [More OKR examples](https://www.whatmatters.com/get-examples)

# Completed or On Hold
```dataview
TABLE
	why AS "Why",
	value AS "Value",
	deadline as "Deadline",
	complete as "Complete"
FROM "00 Meta/02 Action/03 Goals"
WHERE file.name != "03 Goals" AND complete != "❌"
```

## Work Goals
```dataview
TABLE
	why AS "Why",
	value AS "Value",
	deadline as "Deadline",
	complete as "Complete"
FROM "00 Meta/02 Action/03 Goals"
WHERE file.name != "03 Goals" AND complete = "❌" AND goal_type = "work"
```