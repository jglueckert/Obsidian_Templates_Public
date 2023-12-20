---
projectid: 
type: MoC
---

# List of Experiments

## USP Experiments
```dataview
TABLE status

FROM -"Templates" 

WHERE projectid = this.projectid AND type = "Experiment" AND stage = "USP"

SORT status
```

___

## DSP Experiments
```dataview
TABLE status

FROM -"Templates" 

WHERE projectid = this.projectid AND type = "Experiment" AND stage = "DSP"

SORT status
```

___

# Reports
```dataview
TABLE status

FROM -"Templates" 

WHERE projectid = this.projectid AND type = "Report" 

SORT status
```

___

# Meetings
```dataview
TABLE file.ctime

FROM -"Templates" 

WHERE icontains(file.etags, this.projectid) OR projectid = this.projectid

WHERE type = "meeting"

SORT date
```

___

# Total list of tags
```dataview
TABLE file.ctime

FROM -"Templates" 

WHERE icontains(file.etags, this.projectid)

SORT date
```

___

# List of Backlinks / Mentions
```dataview
TABLE file.ctime 
from [[]] and !outgoing([[]])
```
