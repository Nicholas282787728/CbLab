## Microsoft Exchange - Item-Level Restore

Item-level restore is only available for Microsoft Exchange databases that are stored in [full backups](https://www.cloudberrylab.com/blog/block-level-backup-and-full-backup-explained/).



After restoring the files, ...

The next step is going to be outside CloudBerry Backup. Launch the **Exchange Management Console**.

Using Exchange Management Console **dismount the database **\(-s\) you would like to restore.

![](/assets/restore-exchange-console-dismount.png)

**Locate the log files **\(see Log Folder Path\) and the .edb database file \(see Database File Path\).![](/assets/restore-exchange-console-locate-logs.png)**Move them **to another location \(or delete if you no longer need them\).![](/assets/restore-exchange-console-move-logs.png)

Open the **folder with the files **you have restored and copy these files to the original folders \("Database File Path" for .edb file and "Log Folder Path" for the logs\).![](/assets/restore-exchange-open-folder.png)

**Mount **the Exchange database.![](/assets/restore-exchange-mount.png)

And that's it.

