---
created: <% tp.date.now("YYYY-MM-DD HH:mm") %>
modified: <% tp.date.now("YYYY-MM-DD HH:mm") %>
date: <% tp.date.now("YYYY-MM-DD") %>
meeting-type: <% tp.system.suggester(["1-on-1", "customer-call", "internal-meeting", "board-meeting", "discovery-call", "vendor-call", "interview", "all-hands", "architecture", "conference"], ["1-on-1", "customer-call", "internal-meeting", "board-meeting", "discovery-call", "vendor-call", "interview", "all-hands", "architecture", "conference"]) %>
company-name:
role: <% tp.system.suggester(["manager", "participant"], ["manager", "participant"]) %>
participants:
  -
tags:
  -
---

# <% tp.file.title %>

<% tp.file.cursor() %>
