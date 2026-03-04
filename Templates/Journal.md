---
created: <% tp.date.now("YYYY-MM-DD HH:mm") %>
modified: <% tp.date.now("YYYY-MM-DD HH:mm") %>
date: <% tp.date.now("YYYY-MM-DD") %>
journal-type: <% tp.system.suggester(["reflection", "learning", "goals", "experience"], ["reflection", "learning", "goals", "experience"]) %>
tags:
  -
---

# <% tp.file.title %>

<% tp.file.cursor() %>
