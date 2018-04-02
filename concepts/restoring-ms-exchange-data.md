## Restoring MS Exchange Data

On this wizard page, you can restore your [Microsoft Exchange](/office.microsoft.com/en-us/exchange/) data from a backup.

* Select backup storage

* Specify the plan name

* Restore files and folders

* Select file versions to restore

\(item-level restore\)

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

https://kb.cloudberrylab.com/kb1050/





