---
project: Lvlogics
date: 26-08-2022
type: project notes
tags: [aws, dms, Thingsboard, Lvlogics, Silo]
---

# Cloud Differences Matrix
This page is to develop a matrix/table that highlights the differences between [EDGE Insights] master and the DMS running lvlogics.firmwave.com. This table is based on the information gathered in [[Cloud Upgrade Planning]].

## Differences between Lvlogics and Master Codebase(Matrix)

| App                            | Available on lvlogics? | Available on Master |             Models Notes             |
|:------------------------------ |:----------------------:|:-------------------:|:------------------------------------:|
| Alarms                         |           X            |          X          |            No Differences            |
| Analytics                      |           X            |          X          |            No Differences            |
| Auth Tokens                    |           X            |          X          |            No Differences            |
| Files                          |           X            |          X          |            No Differences            |
| History                        |           X            |          X          |            No Differences            |
| Sites                          |           X            |          X          |            No Differences            |
| Horseware                      |           O            |          X          | Not Present on lvlogics.firmwave.com |
| Authentication & Authorization |           X            |          X          |         Missing: Permissions         |
| Devices                        |           X            |          X          |       Differences listed below       |
| Rules                          |           X            |          X          |             Differences              |
| Sim Card                       |           O            |          X          | Not Present on lvlogics.firmwave.com |
| Users                          |           X            |          X          |            No Differences            |
| Sim Manager D                  |           O            |          X          | Not Present on lvlogics.firmwave.com |
| Subscriptions                  |           O            |          X          | Not Present on lvlogics.firmwave.com |


Devices:
- Missing Models:
	- BLE Sensors
	- Device Alarms
	- Device Configuration 
	- Device Mode State,
	- Display Modes
	- Faults
	- Invents
	- J1939
	- Modbus
	- Modbus Configs
	- Settings Display Modes
	- Telemetry Keys
	- URLs
	- Webhooks
- Additional Models:
	- Network Operator
	- Sim Card
	- Silo Strappings

Rules: 
- Missing Models:Notification Rule History
	- Notification Rule Types

## Other Differences
- Sim card is under device on Lvlogics but seperate on master
- Sim Manager D
- Vodafone APIs
- Missing all Subscriptions
- Notifications
- Plans
- Subscriptions
- Transactions
- Users
- Missing:
	- Background Images
	- Brandings
	- Organisational Units
	- Roles
	- Twillio Accounts
	- Weather

## Notes
- No permissions system
- uses groups instead of OU 
- needs silo strappings (Lazer mappings to percentage full)

