---
type: daily
date: <% tp.date.now("YYYY-MM-DD-dddd") %>
tags:
---
# Date: <% tp.date.now("YYYY-MM-DD-dddd") %>


```button
name New Meeting
type note(TKTK, split) template
action New Meeting
templater true
```
^button-newmeeting
# Tasks To Do
## Overdue Tasks
```dataview 
TASK
WHERE due < this.file.day AND !completed
```
## Tasks Due Today
```dataview 
TASK
WHERE due = this.file.day 
```
## Tasks This Week
```tasks
Due this week
not done
```

# Notes


# Activities



# Daily Meetings
```dataview
TABLE summary as "Summary"

FROM  [[]] and !outgoing([[]]) AND"Timestamps/Meetings" and -#MOC
```


# Tasks Completed Today
```dataview
task
WHERE completion = date(this.file.day)
```