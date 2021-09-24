# RDS - Relational Database Service
The following database engines are supported and managed by AWS:
- MySQL
- MariaDB
- Postgres
- Oracle
- Microsoft SQL Server
- Aurora DB

As a managed service, you get:
- Automated Provisioning
- OS Patches
- Point in Time Restore: Continuous backup and restore to a specific timestamp
- Monitoring Dashboards
- Read Replicas
- Disaster Recovery using Multi AZ
- Maintenance windows for upgrades
- Capability for horizontal and vertical scaling
- Storage backed by EBS (using GP2 or IO1)

## RDS Backups

### Automated Backups
- Daily full backups (over the maintenance window)
- Transaction logs backed-up every 5 minutes
- 7 days retention (expandable to 35 days)
- Ability to restore any backup from 5 minutes ago until oldest backup

### Snapshot Backups
- Manually triggered by user
- Can be retained forever

### RDS Storage Auto Scalling
Enables you to have an auto scaling storage based on usage, you just need to set the Maximum Storage Threshold.
Automatically expands storage if:
- Free storage is less than 10%
- Low-storage lasts at least 5 minutes
- 6 hours have passed since last modification

## Read Replica vs Multi AZ
- Read replicas helps you to speed up reading queries
  - Up to 5 read replicas
  - Within AZ, Cross AZ or Cross Region
  - Replication is always ASYNC, making read eventually consistent
  - Replicas can be promoted to their own DB
  - **No network costs for AWS Read Replicas inside same region** (no costs for different AZ on same region)
- Multi AZ is meant for Disaster Recovery situations
  - SYNC Replication
  - One DNS name to automatically connect to the database
  - Provides failover in case of AZ loss, network, instance or storage failure

## Encryption
- At rest encryption
  - Supports encryption with AWS KMS - AES-256 Encryption
  - It needs to be defined at lunch time
  - **If master is not encrypted, replicas cannot be encrypted**
  - Transparent Data Encryption (TDE) available for Oracle and SQL Server

- In-flight Encryption
  - SSL certificates to encrypt data in transit
  - SSL options with trust certificate when connecting to the database

- If database is not encrypted, snapshots are not encrypted
- You can copy an uncrypted snapshot into an encrypted one
