---
project: Lvlogics
date: 26-08-2022
type: project notes
tags: [aws, dms, Thingsboard, Lvlogics, Silo]
---

# Cloud Upgrade Plan

## Differences between Lvlogics and Master Codebase(Apps)

Alarms:
- No difference

Analytics:
- No difference

Auth Token:
- No difference

Files:
- No difference

History:
- No difference

Sites:
- No difference

Authentication & Authorization:
- Missing:
	- Permissions

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
- Missing Notification Rule History, Notification Rule Types

## Other Differences
Sim card is under device on Lvlogics but seperate on master

Sim Manager D

Vodafone APIs

Missing all Subscriptions

Notifications

Plans

Subscriptions

Transactions

Users

Missing Background Images, Brandings, Organisational Units, Roles, Twillio Accounts, Weather

No permissions system, uses groups instead of OU, needs silo strappings (Lazer mappings to percentage full)

