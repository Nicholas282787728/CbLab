## Restoring MS Exchange Data

CloudBerry Backup enables you to back up and restore [Microsoft Exchange](http://office.microsoft.com/en-us/exchange/) data.

> Microsoft Exchange 2010, 2013 and 2016 are supported.

To restore Microsoft Exchange data from a backup, switch to the **Home** tab of the CloudBerry Backup main menu and click **Restore**.

![](/assets/restore-button.png)

Because Microsoft Exchange databases are composed of files \(such as EDB files and transaction logs\), you need to select "**Restore files and folders**" on the corresponding Restore Wizard page.

![](/assets/restore-select-data-type-03-files-folders.png)

Item-level restore is available for Microsoft Exchange 2010, and instead of restoring an entire Exchange database you can restore individual files, such as specific emails and contact data.

> Item-level restore is only available for Microsoft Exchange databases that are stored in [full backups](https://www.cloudberrylab.com/blog/block-level-backup-and-full-backup-explained/).

To restore individual files from an Exchange Server database, switch to the **Backup Storage** tab in your CloudBerry Backup application and locate the Microsoft Exchange database storage. Right-click the required backup and select **Item Level Restore**.![](/assets/restore-exchange-item-level-storage-2.png)

You can select the files to restore on the [next wizard page](/concepts/restoring-ms-exchange-data/select-a-restore-point.md).

**Specify the restore source \(select files to restore\)**

![](/assets/ms-exchange-restore-source.png)

Specify the restore source

You can't restore to original location within the wizard, you will need to dismount your current database \(if any\) and replace Exchange files with restored files.

Encryption

Notification

**Check Network Shares**

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

