---
project: Teva
date: 23-08-2022
type: internal meeting
tags: [Thingsboard, DMS, AWS, Teva, JSON, session-endpoint, updates-endpoint]
---


Cloud Planning

### Attendees:
- Niall Keating
- Paul McGarrigle
- Darragh Morrissey


### Notes:
- See background notes in [[Cloud App Initial Thoughts]]
- Plan to extend the existing DMS functionality on the `session` endpoint
	- Save the samples to tb similar to `updates` endpoint
		- bat_mv
		- pres_min
		- duration_ms
	- All of the above values should use the single `epoch` uploaded for the collection of samples
		- See sample payload in [[Cloud App Initial Thoughts#]]
- Once in TB we can write a script to poll TB/DMS API from test laptop
	- 