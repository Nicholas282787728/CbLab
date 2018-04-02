## Restoring MS Exchange Data

\[supported MS Exchange verions? 2010, 13, 16\]

On this wizard page, you can restore your [Microsoft Exchange](/office.microsoft.com/en-us/exchange/) data from a backup.

* Select backup storage

* Specify the plan name

* Restore files and folders

* Select file versions to restore

\(item-level restore\): you can recover separate emails, contact data, and other stuff \(2010 only\)

You don't need to restore the full database to access your mailboxes, emails,![](/assets/restore-exchange-item-level-storage.png)

![](/assets/restore-exchange-item-level-storage.png)

To enable the feature, you must make the **new full backup **of the Exchange database.





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

