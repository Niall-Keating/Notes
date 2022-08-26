---
project: Lvlogics
date: 26-08-2022
type: project notes
tags: [aws, dms, Thingsboard, Lvlogics, Silo, ec2, rds]
---

# EC2 Differences
- Lvlogics codebase/environment
	- Nginx version: nginx/1.10.3 Industrial: 1.14.0
	- TB: 2.3.0 Industrial: 3.2.1
	- Package requirements
		- Pycrypto 2.6.1
		- six 1.10.0

These changes are required when merging with master codebase, might not be needed if we add additional Lvlogics features to master codebase

Change to related name between simcard and device

Since Merge:

strtobool removed devices/models

Device Getbulk refactor *

History (Add history/logs for SigfoxConfView in api/views)

Need to update:

Merge removes tb_adapter, history, frontend (Lvlogic specific, should probably stay), gulpfile.js, devices/receivers.py, .jshintrc, .editorconfig

Any files in the Firmwave folder should be kept as it contains front end and management commands but a merge will remove them