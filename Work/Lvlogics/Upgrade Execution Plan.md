---
project: Lvlogics
date: 29-08-2022
type: project notes
tags: [aws, dms, Thingsboard, Lvlogics, Silo]
---

# Cloud Upgrade Rollout Plan

1. On agreed kickoff date, take a snapshot of both the MySQL and Postgres databases associated with lvlogics.firmwave.com
2. Spin up a new AWS EC2 instance once the snapshots are complete 
3. Use these database snapshots to perform the required database migrations for the upgrades to master version of the DMS 