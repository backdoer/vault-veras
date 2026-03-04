---
created: <% tp.date.now("YYYY-MM-DD HH:mm") %>
modified: <% tp.date.now("YYYY-MM-DD HH:mm") %>
date: <% tp.date.now("YYYY-MM-DD") %>
plan-type: <% tp.system.suggester(["project", "checklist", "roadmap", "agenda"], ["project", "checklist", "roadmap", "agenda"]) %>
tags:
  -
---

# <% tp.file.title %>

<% tp.file.cursor() %>
