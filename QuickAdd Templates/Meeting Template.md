---
date: <% tp.date.now("YYYY-MM-DD") %>
week: <% tp.date.now("YYYY - [W]ww", 0, tp.file.title, "YYYY-MM-DD") %>
month: <% tp.date.now("YYYY - MM - MMMM", 0, tp.file.title, "YYYY-MM-DD") %>
year: <% tp.date.now("YYYY", 0, tp.file.title, "YYYY-MM-DD") %>
type: meeting
project: {{VALUE:Project}}
duration: {{VALUE:Duration?,0.5,1,1.5,2,3,4}} hours
tags: meetings
summary: 
---
# Project: [[{{VALUE:Project}}]]
# [[<% tp.file.title %>]]
## Attendees
### Internal
- [[Johnny Bananas]]

### External

## Notes

