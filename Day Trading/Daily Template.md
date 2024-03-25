---
tags:
  - daily-note
full-date: <% tp.file.title %>
week: <% tp.date.now("YYYY - [W]ww", 0, tp.file.title, "YYYY-MM-DD") %>
month: <% tp.date.now("YYYY - MM - MMMM", 0, tp.file.title, "YYYY-MM-DD") %>
year: <% tp.date.now("YYYY", 0, tp.file.title, "YYYY-MM-DD") %>
banner: "[[image.jpg]]"
banner_y: 0.16334
daily_profits: 0
trade_notes: 
habit-weight: 
habit-steps: 
---

###### [[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>|↶ YESTERDAY]] ⁝ [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>|TOMORROW ↷]]
# ◌ <% tp.date.now("dddd -  MMMM Do YYYY", 0, tp.file.title, "(📅) YYYY-MM-DD") %>
### ⁕  NOTES


> [!todo] Current Tasks
> ```tasks
due before <% tp.date.now("YYYY-MM-DD", 7, tp.file.title, "YYYY-MM-DD") %>
not done
short mode
hide task count

> [!abstract] Meetings Today
>```dataview
TABLE
project AS "Project",
duration AS "Duration",
summary AS "Summary"
FROM "00 Meta/02 Action/05 Meetings"
WHERE date = date(<% tp.file.title %>)
SORT file.name DESC

> [!success] Completed Today
>```tasks
done date is <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
hide task count

> [!question] On This Day
>```dataview
table file.mtime as LastEdit
from ""
where contains(file.name, "{{date:-MM-DD}}") and !contains(file.name, "{{date:YYYY}}")


