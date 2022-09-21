---
project: EDGE Insights
date: 20-09-2022
type: project notes
tags: [aws, ec2, rds, security-groups, edge-insights, dms, infrastructure]
---

# AWS Landing

## EC2 Landing
```dataview
TABLE AWS-ID AS "AWS Identifier", Size FROM "Work/EDGE Insights/AWS/EC2"
```

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


## Links
[Example](https://www.example.org)
