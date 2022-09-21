# EDGE Insights Landing Page

Sharepoint: 
GIthub:


## Internal Meetings
```dataview
TABLE date, project, type FROM "Work"
WHERE project = "EDGE Insights" and type = "internal meeting"
SORT date ASC
```

## External Meetings
```dataview
TABLE date, project, type FROM "Work"
WHERE project = "EDGE Insights" and type = "external meeting"
SORT date ASC
```

## Project Notes
```dataview
TABLE date, project, type FROM "Work"
WHERE project = "EDGE Insights" and type = "project notes"
SORT date ASC
```

## Architecture Diagrams
```dataview
TABLE date, project, type FROM "Work"
WHERE project = "EDGE Insights" and type = "architecture diagram"
SORT date ASC
```
