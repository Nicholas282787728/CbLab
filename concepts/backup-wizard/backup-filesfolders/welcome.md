## Select the Backup Route and Enable Ransomware Protection

On the first wizard page, you can select a route for your backup and choose whether you need to protect your backup from ransomware activity.

![](/assets/backup-wizard-welcome-page-hybrid-local-cloud-ransomware.png)

### Selecting a Backup Route

Your backup data can take one of the following routes:

* Back up your data directly to a local or cloud storage \(**one-way backup**\).

![](/assets/icon-local-to-cloud.png)  
This is the default way to back up your data, without introducing any intermediate storage between the backup source and destination.

* Back up your data first to a local storage, and then copy it from there to a cloud \(**two-way** or **hybrid backup**\).

![](/assets/icon-hybrid-backup.png)

Use this option to send your backup to two destinations at once and avoid repeated processing of data.

With this option selected, the backup service first processes your data and moves it to a Network-attached storage \(NAS\) or similar local storage, from where the already processed backup makes its way to a cloud storage.

This allows you to avoid repeated processing of your data when you need to compress and/or encrypt it, because the backup service performs these operations only once, before the saving the backup to the local storage.

For this reason, when you only need to compress and/or encrypt your backup in a cloud, and not in a local storage, you should create two separate one-way backup tasks instead of selecting the hybrid backup option.

> Limitations:
>
> * no Archive Mode support
> * **no "delete files if they were deleted locally" support \(hybrid backups will not delete files that have been deleted locally - from the cloud/backup destination. Or will be purged according to your retention policy.\)**
>
> * existing backup plan cannot be converted to hybrid, you need to create a hybrid backup plan from scratch.
>
> * ??/ Is it mentioned in the text that there is encryption on the local target, does this include encrypting the name of the files?
>
> * ?? Is there any way to have different retention policies for local and cloud? \(I typically keep 6+ months of retention on-site and only a month of retention off-site to reduce costs.\)

### Enabling Ransomware Protection

Use this feature to enable additional protection against ransomware attacks by making CloudBerry Backup detect suspicious encryption activity over files in your backup.

With this feature enabled, CloudBerry Backup performs a [full initial backup](https://www.cloudberrylab.com/blog/block-level-backup-and-full-backup-explained/) and uses heuristics to find out whether the byte structure of each file has changed in subsequent backups because of encryption.

If your files were already encrypted during the first processing of your backup, CloudBerry Backup will still be able to detect any changes in the encryption applied by subsequent backups.

> Ransomware protection only applies to locally stored backups and CloudBerry Backup will not analyze files that are already stored in the cloud.

**\[is the above correct?\]**

On detecting suspicious encryption applied to your files, CloudBerry Backup prevents deletion of existing backups regardless of the current retention policy settings to ensure that at least one undamaged version of your backup is still available, and prompts you about which action to take next.

Please be informed that enabling ransomware protection will increase your backup size because of the need to keep additional file versions until the backup administrator confirms their deletion.





Notes:

Ransomware protection is currently supported only for file backups. 



This feature is most effective for preventing you from ransomware attacks when used as part of a broader protection strategy that includes appropriate lifecycle and retention policies. Please refer to the following blog post online to learn how to protect your backups: [4 Ways to Protect Against Ransomware with Backups](https://www.cloudberrylab.com/blog/how-ransomware-works/).



With the ransomware detection enabled, you can only choose the [Advanced backup mode](/concepts/backup-wizard/backup-filesfolders/shared-select-the-backup-mode.md) further in this wizard.

**\[why?\]**



After saving your backup plan, it displays a "lock" icon on its title, indicating that ransomware protection is enabled for this backup plan.





If the lock symbol is red then click on in and choose "Show result"





The backup plan completes normally



and notify 









notifications:

Admins can quickly see a list all of all affected files and approve any false-positive detections.



> test

You manually inspect those files in_Windows / File Explorer\_using the\_Show in Folder\_option. If you want to remove the most recent backup of an affected file from backup storage, select the file and click\_Delete_.

If you click_Cancel_, purge settings for any affected files will continue to be disabled and those files will remain on the list.

You can also be notified with an email that lists of all flagged files.

[https://www.cloudberrylab.com/blog/ransomware-protection-in-cloudberry-backup-5-8/](https://www.cloudberrylab.com/blog/ransomware-protection-in-cloudberry-backup-5-8/)

Delete - deletes the potentially ransomware affected files

Approve - means that files are not ransomware affected and they would not be deleted.

Limitation: no black/whitelist directories for the Ransomeare Protection





---

See also: [Increasing Backup Processing Speed](/concepts/increasing-backup-processing-speed.md)

