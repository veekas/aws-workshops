# AWS and Database Services Overview

- use GP2 to start off with (almost always)
- IO1 is only better if you're utilizing more
- you can scale computer/memory and EBS storage up or down
- ensuring database availability
  - Multi-AZ: "enterprise grade fault tolerance" for production databases
  - different locations, power grids, etc.
- read replicas
  - async copy of data
  - supported for PostgreSQL and others

| -----------------------------------------------------------|
| Multi-AZ                | Read Replicas                    |
| ----------------------- | -------------------------------- |
| sync                    | async                            |
| only primary is active  | all instances active             |
| backups from secondary  | no default backups               |
| 2 avail zones in region | within, cross-AZ, or cross-zones |
| db upgrades on primary  | db updated independently         |
| -----------------------------------------------------------|

- backups: snapshots are kept at different intervals, customizable
- restoring backups: full performance can take a while even though the volume is usable immediately
- securing a database:
  - network isolation
  - identify and access management (IAM)
  - encryption at rest
- best practicing for encrypting database
  - always encrypt: no performance penalty
  - centralized access and audit of key activity
  - if course is replaced, read replicas must be envrupted
  - to encrupt a db that already exists, take a snapshot and encrypt that (more work, just encrypt from the beginning)
- monitoring
  - RDS
  - new: Amazon RDS Performance Insights
      - measures db load
      - identifies bottlenecks
      - only PostgreSQL and Aurora right now but will expand later
  - use CloudWatch and alerts
- pricing variables
  - db instance (instance hours)
    - region + instance type + database engine + license
  - db storage (GB per month)
    - provisioned (Amazon EBS) or consumed (Amazon Aurora)
    - provisioned IOPS iff IO1 storage type
    - db IP requests for Aurora/EBS magnetic-storage types
  - understanding the bill
    - charges grouped by region
    - instances grouped by engine
    - charges are cross-engine
    - use AWS Cost Explorer for grpahical comparison
    - use AWS Cost and Usage Report for billing details (after enabling)
  - saving money
    - reserved instances are discounted over on-demand
