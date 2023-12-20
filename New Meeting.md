---
type: "meeting"
projectid: ""
date: [[<% tp.date.now("YYYY-MM-DD-dddd") %>]] <% await tp.file.move("/Timestamps/Meetings/" + tp.date.now("YYYY-MM-DD") + " " + tp.file.title) %> # [[<% tp.date.now("YYYY-MM-DD") + " " + tp.file.title %>]]
tags: 
summary: " "
---
Date: [[<% tp.date.now("YYYY-MM-DD") %>]]
<% await tp.file.move("/Timestamps/Meetings/" + tp.date.now("YYYY-MM-DD") + " " + tp.file.title) %>
___
# Notes



