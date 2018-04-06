## Performing a Consistency Check

CloudBerry Backup uses a local database \(repository\) to keep track of backed up data. You can do one of the following to ensure that the repository is up to date:

* [Synchronize your repository](/concepts/syncing-your-repository.md) to delete the current repository and update it according to the current backup storage contents from scratch. This is a time-consuming task and we do not recommend that you perform it unless absolutely necessary. This is why you cannot schedule a synchronization routine to make it run automatically.
* Perform a consistency check to detect any discrepancies between the repository and the backup storage and take appropriate action on finding any mismatch.

The consistency check enables you to avoid losing data \(for example, when some of the files in your backup storage get corrupted, or when you replace your local NAS device storing the backup files\). On finding any discrepancies, you will receive a notification informing you that some of the files are missing in the local repository or there is a mismatch between the file modification dates. Another common scenario is to check the repository consistency after uploading multiple backups from different computers to the same bucket/container using the same [backup prefix](/concepts/changing-the-backup-prefix.md).

> We strongly recommend that you run a consistency check on a regular basis to ensure the integrity of data in your backups.

You can run a consistency check manually or on schedule by switching to the **Welcome** tab of your CloudBerry Backup application and navigating to the **Storage Accounts** section. Click the burger icon for the required storage and select the required option.

![](/assets/backup-welcome-storage-accounts-run-consistency-check.png)

Clicking **Run Consistency Check** makes the backup service check whether any backup is currently being uploaded to this storage. If this is the case, it displays a warning notifying that you first need to wait until the current backup routine is finished.

> Only a single consistency check can run at a time. When multiple consistency checks are scheduled to be executed by the same time, they run one after another.
>
> If file names in your backup are encrypted, you need to specify the encryption password before running a consistency check. Otherwise, the backup service will be unable to identify encrypted files and will skip them during the consistency check execution.

Clicking **Schedule Consistency Check **invokes the **Storage Account** dialog window, where you can specify the schedule for automatic check for this storage consistency on a regular basis.

![](/assets/backup-account-s3-consistency-check.png)

After finishing a consistency check, the storage account displays an icon indicating the consistency check result.

![](/assets/consistency-check-results.png)

A green icon indicates that the check has been performed successfully.

A yellow icon indicates that warnings were found during the consistency check. Clicking the link indicating the date of the last consistency check navigates you to the **History** tab where you can find detailed information about discovered inconsistencies.

![](/assets/consistency-check-history-2.png)



