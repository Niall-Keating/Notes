---
project: EDGE Insights
date: 20-09-2022
type: project notes
tags: [aws, ec2, rds, security-groups, edge-insights, dms, infrastructure]
---

# AWS Misc


```dataview
TABLE date, project, type FROM "Work"
WHERE project = "HealthBeacon 3.0" and type = "internal meeting"
SORT date ASC
```


```dataview
TABLE file.name AS File FROM "Work"
```





## EC2 Landing
| Instance URL                                      | Instance ID                                                                                                                              | Instance Size |
| ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| [[industrial.taoglas.com]] | [i-0d9001bc6eb32f1d2](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-0d9001bc6eb32f1d2) | c6g.large     |
| [connect.taoglas.com](#connect.taoglas.com)       | [i-06c019317d3f45829](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-06c019317d3f45829) | c6g.large     |
| [locate.taoglas.com](#locate.taoglas.com)         | [i-09afeaae7d260d0ac](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-09afeaae7d260d0ac) | t2.medium     |
| [lvlogics.firmwave.com](#locate.taoglas.com)      | [i-0b088722ecc90b842](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-0b088722ecc90b842) | t2.medium     |
| [connect02.taoglas.com](#connect02.taoglas.com)   | [i-06a4d1280f6f4e245](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-06a4d1280f6f4e245) | c6g.medium    |
| [dev2.firmwave.com](#dev2.firmwave.com)           | [i-0dbb425f963055020](https://eu-west-1.console.aws.amazon.com/ec2/home?region=eu-west-1#InstanceDetails:instanceId=i-0dbb425f963055020) | t2.micro      |


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














## Links
[Example](https://www.example.org)



### fw-industrial-taoglas
yes

ass


