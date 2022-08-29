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
	- HTML templates on th
2. On agreed kickoff date, take a snapshot of both the MySQL and Postgres databases associated with lvlogics.firmwave.com
3. Spin up a new AWS EC2 instance once the snapshots are complete 
4. Use these database snapshots to perform the required database migrations for the upgrades to master version of the DMS 
5. Once the existing codebase has been upgraded 