---
project: Lvlogics
date: 30-08-2022
type: external meeting
tags: [aws, dms, Thingsboard, Lvlogics, Silo]
---

## Tasks
- [ ] Niall to send on documentation on how the nested structure of the org units structure works ⏳ 2022-09-02 🔽 
- [ ] Niall to create tasks to review notification rules and add any tasks identified in this call.⏳ 2022-09-02 🔼 

## Attendees
- Padraig Skelly (Lvlogics)
- Niall Keating (Taoglas)
- Shane Bradley (Taoglas)
- Paul McGarrigle (Taoglas)


## Notes
- Lvlogics are using groups on the DMS to partition devices into units
	- When they create a group on the DMS, this name is not reflected on the dashboard, they have to find the *NULL* row in the lsit and then use the edit button to name it.
		- This would be streamlined for them if the asset could be named frmo thre DMS
		- (NK) - This is Possible
	- I proposed using org units on the new site as this will save a significant amount of effort for us. 
	- The have the concept of Area Sales Managers(ASM's), these are sales people in DairyGold that are responsible for a certain number of farmers. 
		- DairyGold is broken down into TC units, these are units of silos and different ASM's can have views of different silo's with in a TC
		- Therefore the units may not work as you cannot limit what devices a user can see in an org unit. 
- They often have multiple browser tabs open with multipls pages, i.e. device list/edit pages, groups, dashboard, rules etc
	- Would be very convientent if you could go to a devices strapping table and edit page from the dashbaord
		- (NK) - This is posssible
- Update notification rule contacts so that you can save them without having to enter a phone number.
- On the Dashboard, add external battery to the 1 month, 3 month and 6 month views.


