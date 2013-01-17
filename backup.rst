Backups
> All dumps are done on s3 bucket form hub-backups which is located in Oregon AWS region data centre
> Plan to setup replication instances for mysql and mongodb, backups will be performed on the replica sets only


Mysql
> mysqldump done nightly
> duplicity does full daily backups
> should duplicity daily backups become incremental backups with full backup every 7/n days?

MongoDB
> mongodump done nightly
> duplicity does full daily backups
> should duplicity daily backups become incremental backups with full backup every 7/n days?

Snapshots
