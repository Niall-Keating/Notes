---
project: EDGE - Insigths
date: 20-09-2022
type: project notes
tags: [aws, ec2, rds, security-groups, edge-insights, dms, infrastructure]
---

# AWS Misc

## EC2 Landing
| Instance URL                                      | Instance ID                                                                                                                              | Instance Size |
| ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| [industrial.taoglas.com](#industrial.taoglas.com) | [i-0d9001bc6eb32f1d2](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-0d9001bc6eb32f1d2) |               |
| [connect.taoglas.com](#connect.taoglas.com)       | [i-06c019317d3f45829](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-06c019317d3f45829) |               |
| [locate.taoglas.com](#locate.taoglas.com)         | [i-09afeaae7d260d0ac](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-09afeaae7d260d0ac) |               |
| [lvlogics.firmwave.com](#locate.taoglas.com)      | [i-0b088722ecc90b842](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-0b088722ecc90b842) |               |
| [connect02.taoglas.com](#connect02.taoglas.com)   | [i-06a4d1280f6f4e245](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-06a4d1280f6f4e245) |               |
| [dev2.firmwave.com](#dev2.firmwave.com)           | [i-0dbb425f963055020](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-0dbb425f963055020) |               |
|                                                   |                                                                                                                                          |               |

## RDS Landing
| Database Identifier                                                                                                                                                | Database Engine | Database Size |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------- | ------------- |
| [connect-thingsboard](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=connect-thingsboard;is-cluster=false)                         |    PostgreSQL             |               |
| [connectlocate-database-postgres](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=connectlocate-database-postgres;is-cluster=false) |                 |               |
PostgreSQL| [database-1](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=database-1;is-cluster=false)                                           |                 |               |
| [dev-postgres](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=dev-postgres;is-cluster=false)                                       |                 |               |
| [dev2-dms](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=dev2-dms;is-cluster=false)                                               |                 |               |
| [fw-connect-20200112](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-connect-20200112;is-cluster=false)                         |                 |               |
| [fw-dev](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-dev;is-cluster=false)                                                   |                 |               |
| [fw-hb-staging](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-hb-staging;is-cluster=false)                                     |                 |               |
| [fw-industrial-taoglas](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-industrial-taoglas;is-cluster=false)                     |                 |               |
| [fw-locate](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-locate;is-cluster=false)                                             |                 |               |
| [fw-silo-2019-08-22-01-18](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-silo-2019-08-22-01-18;is-cluster=false)               |                 |               |
| [fw-staging](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-staging;is-cluster=false)                                           |                 |               |
| [fw-staging-19012020](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=fw-staging-19012020;is-cluster=false)                         |                 |               |
| [industrial-dms](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=industrial-dms;is-cluster=false)                                   |                 |               |
| [industrial-taoglas](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=industrial-taoglas;is-cluster=false)                           |                 |               |
| [thingsboard-m6g-1](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=thingsboard-m6g-1;is-cluster=false)                             |                 |               |
| [thingsboard-vodafone](https://eu-west-1.console.aws.amazon.com/rds/home?region=eu-west-1#database:id=thingsboard-vodafone;is-cluster=false)                       |                 |               |
|                                                                                                                                                                    |                 |               |


### industrial.taoglas.com
- Ubuntu Version: XXX
- DMS Comnmit Hash: XXX
- Thingsboard Version: XXX
- MySQL(RDS): XXX
- Postgres (RDS): XXX

#### notes


### connect.taoglas.com
- Ubuntu Version: XXX
- DMS Comnmit Hash: XXX
- Thingsboard Version: XXX
- MySQL(RDS): XXX
- Postgres (RDS): XXX

#### notes


### locate.taoglas.com
- Ubuntu Version: XXX
- DMS Comnmit Hash: XXX
- Thingsboard Version: XXX
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
- Ubuntu Version: XXX
- DMS Comnmit Hash: XXX
- Thingsboard Version: XXX
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




## RDS Notes
| Instance URL | AWS ID | DMS Commit hash | Thingsboard Version | RDS(MySql) | RDS(PostGres) |
| ------------ | ------ | --------------- | ------------------- | ---------- | ------------- |
|              |        |                 |                     |            |               |

## Links
[Example](https://www.example.org)
