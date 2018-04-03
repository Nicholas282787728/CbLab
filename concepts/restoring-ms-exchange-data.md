## Restoring Microsoft Exchange Data

CloudBerry Backup enables you to back up and restore [Microsoft Exchange](http://office.microsoft.com/en-us/exchange/) data.

> Microsoft Exchange versions 2010, 2013 and 2016 are supported.

To restore Microsoft Exchange data from a backup, switch to the **Home** tab of the CloudBerry Backup main menu and click **Restore**.

![](/assets/restore-button.png)

Because Microsoft Exchange databases are composed of files \(such as EDB files and transaction logs\), you need to select the "**Restore files and folders**" option on the corresponding Restore Wizard page.

![](/assets/restore-select-data-type-03-files-folders.png)

Item-level restore is available for Microsoft Exchange 2010, and instead of restoring an entire Exchange database you can restore individual files, such as specific emails and contact data.

> Item-level restore is only available for Microsoft Exchange databases that are stored in [full backups](https://www.cloudberrylab.com/blog/block-level-backup-and-full-backup-explained/).

Encryption

Notification

\(Check Network Shares\)

---

After restoring the files, ...

The next step is going to be outside CloudBerry Backup. Launch the **Exchange Management Console**.

Using Exchange Management Console **dismount the database **\(-s\) you would like to restore.

![](/assets/restore-exchange-console-dismount.png)

**Locate the log files **\(see Log Folder Path\) and the .edb database file \(see Database File Path\).![](/assets/restore-exchange-console-locate-logs.png)**Move them **to another location \(or delete if you no longer need them\).![](/assets/restore-exchange-console-move-logs.png)

Open the **folder with the files **you have restored and copy these files to the original folders \("Database File Path" for .edb file and "Log Folder Path" for the logs\).![](/assets/restore-exchange-open-folder.png)

**Mount **the Exchange database.![](/assets/restore-exchange-mount.png)

And that's it.

### Troubleshooting

MS Exchange Server 2007: Connection to the remote server failed

[https://kb.cloudberrylab.com/kb1050/](https://kb.cloudberrylab.com/kb1050/)

