---
project: Lvlogics
date: 29-08-2022
type: internal meeting
tags: [aws, dms, Thingsboard, Lvlogics, Silo]
---

# Chat with Paul 29/08/2022
## Attendees
Niall Keating
Paul McGarrigle 

## Notes
- Some silo strapping stuff in Master, but it's tied to the devices model, need to consider moving this to a seperate(Silo?) app.
- Org unit in master instead of org units, aim to get lvlogics to move to org units 
	- NK Q, Can you map a device to multiple org units?
	- NK, Barry can go this with groups currently
- Notifications, need to keep access for Barry to templates
- Ignore need to update, as this is just if we were upgrading lvlogics rather than adding silo features to master
- How do we handle org unit states when deice visibility currently depends on the users?

## My Additional Notes
What we need to do(task-wise)

- Create a new SIlo App, this should contain all of the Silo specific business logic
	- Silo Strapping
	- Sigfox Adapter? Is this a webhook?
- Modify Org Unit's to allow multiple device associations?
	- Need to check with Paul how possible it is going to be to use template dashboards