---
project: EDGE Insights
date: 20-09-2022
type: project notes
tags: [aws, ec2, rds, security-groups, edge-insights, dms, infrastructure]
---

# AWS Misc

## EC2 Landing
| Instance URL                                      | Instance ID                                                                                                                              | Instance Size |
| ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| [industrial.taoglas.com](#industrial.taoglas.com) | [i-0d9001bc6eb32f1d2](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-0d9001bc6eb32f1d2) | c6g.large     |
| [connect.taoglas.com](#connect.taoglas.com)       | [i-06c019317d3f45829](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-06c019317d3f45829) |               |
| [locate.taoglas.com](#locate.taoglas.com)         | [i-09afeaae7d260d0ac](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-09afeaae7d260d0ac) |               |
| [lvlogics.firmwave.com](#locate.taoglas.com)      | [i-0b088722ecc90b842](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-0b088722ecc90b842) |               |
| [connect02.taoglas.com](#connect02.taoglas.com)   | [i-06a4d1280f6f4e245](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-06a4d1280f6f4e245) |               |
| [dev2.firmwave.com](#dev2.firmwave.com)           | [i-0dbb425f963055020](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-0dbb425f963055020) |               |
|                                                   |                                                                                                                                          |               |

## RDS Landing
| Database Identifier                                                                                                                                                | Database Engine | Database Size |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------- | ------------- |
| [connect-thingsboard](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=connect-thingsboard;is-cluster=false)                         | PostgreSQL      | db.t3.micro   |
| [connectlocate-database-postgres](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=connectlocate-database-postgres;is-cluster=false) | PostgreSQL      | db.t2.small   |
| [database-1](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=database-1;is-cluster=false)                                           | PostgreSQL      | db.t2.medium  |
| [dev-postgres](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=dev-postgres;is-cluster=false)                                       | PostgreSQL      | db.t2.small   |
| [dev2-dms](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=dev2-dms;is-cluster=false)                                               | MySQL Community | db.t3.small   |
| [fw-connect-20200112](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-connect-20200112;is-cluster=false)                         | MySQL Community | db.t2.micro   |
| [fw-dev](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-dev;is-cluster=false)                                                   | MySQL Community | db.t3.micro   |
| [fw-hb-staging](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-hb-staging;is-cluster=false)                                     | MySQL Community | db.t2.micro   |
| [fw-industrial-taoglas](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-industrial-taoglas;is-cluster=false)                     | MySQL Community | db.t2.medium  |
| [fw-locate](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-locate;is-cluster=false)                                             | MySQL Community | db.t2.micro   |
| [fw-silo-2019-08-22-01-18](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-silo-2019-08-22-01-18;is-cluster=false)               | MySQL Community | db.t2.micro   |
| [fw-staging](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-staging;is-cluster=false)                                           | MySQL Community | db.t2.micro   |
| [fw-staging-19012020](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-staging-19012020;is-cluster=false)                         | MySQL Community | db.t2.micro   |
| [industrial-dms](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=industrial-dms;is-cluster=false)                                   | MySQL Community | db.t3.medium  |
| [industrial-taoglas](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=industrial-taoglas;is-cluster=false)                           | PostgreSQL      | db.t2.small   |
| [thingsboard-m6g-1](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=thingsboard-m6g-1;is-cluster=false)                             | PostgreSQL      | db.m6g.large  |
| [thingsboard-vodafone](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=thingsboard-vodafone;is-cluster=false)                       | PostgreSQL      | db.t3.micro   |


## EC2 Instance Details
### industrial.taoglas.com
- Ubuntu Version: Ubuntu 18.04.5 LTS
- DMS Commit:
	- Hash: eec2160805a1af8f4378e86446c7b879c73775cc
	- Date: 04/11/2021
- Thingsboard Version: 3.3.0
- MySQL(RDS): XXX
- Postgres (RDS): XXX

#### notes


### connect.taoglas.com
- Ubuntu Version: Ubuntu 18.04.5 LTS
- DMS Commit:
	- Hash: f76cd42797924bf0527b63c2e1fb307fdf689578
	- Date: 01/07/2021
- Thingsboard Version: 3.3.0
- MySQL(RDS): XXX
- Postgres (RDS): XXX

#### notes


### locate.taoglas.com
- Ubuntu Version: Ubuntu 16.04.6 LTS
- DMS Commit:
	- Hash: 744621fc6c09e0f2a981802efc3e0e8cbeb03d28
	- Date: 03/03/2020
- Thingsboard Version: 2.4.2
- MySQL(RDS): XXX
- Postgres (RDS): XXX

#### notes


### lvlogics.firmwave.com
- Ubuntu Version: XXX
- DMS Comnmit Hash: XXX
- Thingsboard Version: XXX
- MySQL(RDS): XXX
- Postgres (RDS): XXX

#### notes


### connect02.taoglas.com 
- Ubuntu Version: Ubuntu 18.04.6 LTS
- DMS Commit:
	- Hash: b44a8be5872957810c85c488c54f670f93afe447
	- Date: 23/09/2021
- Thingsboard Version: 3.3.1
- MySQL(RDS): XXX
- Postgres (RDS): XXX

#### notes


### dev2.firmwave.com 
- Ubuntu Version: XXX
- DMS Comnmit Hash: XXX
- Thingsboard Version: XXX
- MySQL(RDS): XXX
- Postgres (RDS): XXX

#### notes


### dev.firmwave.com 
- Ubuntu Version: Ubuntu 14.04.6 LTS
- DMS Comnmit Hash: XXX
- Thingsboard Version: 2.0.3
- MySQL(RDS): XXX
- Postgres (RDS): XXX

#### notes


## Links
[Example](https://www.example.org)
