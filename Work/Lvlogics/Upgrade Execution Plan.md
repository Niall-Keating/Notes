---
project: Lvlogics
date: 29-08-2022
type: project notes
tags: [aws, dms, Thingsboard, Lvlogics, Silo]
---

# Cloud Upgrade Rollout Plan

1. Before the upgrade should begin, the following features need to be added to master code base:
	- Silo strapping feature needs to be added to master(in a Silo Application)
	- Organisation Units need to be modified to allow a device to be in multiple org units.
	- HTML templates visible/editable on the front end needs to be added to master
	- Display of Thingsboard dashboard needs to be added to the user edit page on the dms front end
	- Need to make sure we can mimic existing functionanality in the rules engine
	- Need to have a plan for migrating each model as some models will be moved to differnet apps
		- Templates Model
		- Strapping Model
		- 
1. On agreed kickoff date, take a snapshot of both the MySQL and Postgres databases associated with lvlogics.firmwave.com
2. Spin up a new AWS EC2 instance once the snapshots are complete 
3. Use these database snapshots to perform the required database migrations for the upgrades to master version of the DMS 
4. Upgrade thingsboard using the snapshotted data
	- The following widgets need to be upgraded for newer thingsboard?
5. Once the existing codebase and models have been upgraded, start the dervice on an internal lvlogics domain, silo-temp.firmwave.com?
6. Begin validation testing to ensure everything is running as expected
7. Once validation testing is complete, we need a plan to start moving customers, there is 2 approaches:
	1. Perform an out of hours maintenance window during this time all of the customer data between the initial snapshot and the downtime is migrated to the new instance, this is brought back online as the new instance 
		- Disadvantage here is that the TB urls will all have to be sent out again in one go
			- Taoglas could offer a solution to automatically send logins via whatsapp to the farmers?
	2. Migrate over the customers/devices on a per customer basis. This is much more labor intensive but Padraig can notify customers on a one to one basis
8. Once the overall upgrade is completed documentation should be written up for the support team and for Barry 
9. 