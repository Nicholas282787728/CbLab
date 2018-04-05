

cautions against using multiple backup plans to back up a single database, as that may lead to unintentional data corruption.

[https://www.cloudberrylab.com/blog/backup-and-restore-of-sql-server-databases/](https://www.cloudberrylab.com/blog/backup-and-restore-of-sql-server-databases/)

If you have two products running backups on the same set database, you may end up with differential and transaction log backups that cannot be restored. Do feel free, however, to utilize our Hybrid Backup feature to back up your SQL server to two different locations.

