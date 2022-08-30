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
- Pagination will be available
- Easier device provisioning on newer(via device type confs)
- How will be use organisations?

## My Additional Notes
What we need to do(task-wise)

- Create a new SIlo App, this should contain all of the Silo specific business logic
	- Silo Strapping
	- Sigfox Adapter? Is this a webhook?
- Modify Org Unit's to allow multiple device associations?
	- Need to check with Paul how possible it is going to be to use template dashboards
- See [rules engine diff](https://github.com/taoglas-iot/device_manager/compare/master...lvlogics#diff-4dae34cba453d2a822c887a0d74723dc5fd61cec1f39484bf3c8e5c459017146R17-R22)
- And [HERE](https://github.com/taoglas-iot/device_manager/compare/master...lvlogics#diff-4dae34cba453d2a822c887a0d74723dc5fd61cec1f39484bf3c8e5c459017146R57-R61)
- What is ADS.py?
	- Aggregrate Data Stream, this is where silo strapping is performed
- Analytics_dashbaord_url?
- Some diff in the [User/forms.py](https://github.com/taoglas-iot/device_manager/compare/master...lvlogics#diff-36b4d731c2240967afb4b917ec37c15cca339c080522aaee8c97432632c61720R565)
- 
- 