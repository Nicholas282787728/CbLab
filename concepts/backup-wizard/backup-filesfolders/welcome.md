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

This allows you to avoid repeated processing of your data when you need it to be compressed and/or encrypted in both target storages, because the backup service performs these operations only once, before the saving the backup to the local storage.

For this reason, when you only need to compress and/or encrypt your backup in a cloud, and not in a local storage, you should create two separate one-way backup tasks instead of selecting the hybrid backup option.

> At present, it is not possible to switch your existing backup plans to a Hybrid mode and you need to manually create a hybrid backup plan from scratch.
>
> You can only apply a single set of retention policies to both the local and cloud storage at the time.
>
> The [Archive mode](/concepts/backup-wizard/backup-filesfolders/shared-select-the-backup-mode.md) is not supported for Hybrid backups \(only the Advanced mode's settings are available further in this wizard\).

### Enabling Ransomware Protection

Use this feature to enable additional protection against ransomware attacks by making CloudBerry Backup detect suspicious encryption activity over locally stored files in your backup.

> Ransomware protection only applies to locally stored backups and CloudBerry Backup will not analyze files that are already stored in the cloud.

With this feature enabled, CloudBerry Backup performs a [full initial backup](https://www.cloudberrylab.com/blog/block-level-backup-and-full-backup-explained/) and uses heuristics to find out whether the byte structure of files in the backup has changed in subsequent backups because of encryption.

> Ransomware protection is currently supported only for file backups.

If your files were already encrypted during the first processing of your backup, CloudBerry Backup will still be able to detect any changes in the encryption applied by subsequent backups.

On detecting suspicious encryption applied to your files, CloudBerry Backup prevents deletion of existing backups regardless of the current retention policy settings to ensure that at least one undamaged version of your backup is still available, and prompts you about which action to take next.

> With the ransomware detection enabled, you can only choose the [Advanced backup mode](/concepts/backup-wizard/backup-filesfolders/shared-select-the-backup-mode.md) further in this wizard.
>
> This is because the backup service analyzes source files on the fly, while a backup is being processed. It is able to detect a possibly corrupted file only after it has already been uploaded to the destination storage. For this reason, using the Simple backup mode would result in a corrupted file overwriting its previous, uncorrupted version before the backup service is able to detect and prevent this. This is not the case with the Advanced mode, in which a corrupted file becomes uploaded as a new version, with keeping the previous file version intact.

Please be informed that enabling ransomware protection may increase the size of your backup because of the need to keep additional versions of suspicious files until the backup administrator confirms their deletion.

After saving your backup plan, it displays a "lock" icon on its title, indicating that ransomware protection is enabled for this backup plan.![](/assets/backup-plans-ransomware-protection-lock-icon.png)When the backup service suspects that your files may be affected by ransomware, it completes the current backup task and sends you an email containing the list of supposedly affected files and prompting you to take action.

The "lock" icon displayed on the backup plan's title becomes red. Clicking this icon invokes a dialog window listing all suspicious files. You can open the folder containing these files by clicking the corresponding context link in this dialog. Next, you can either approve that such a file is not affected by ransomware or delete it by clicking the corresponding button.

You can click **Cancel** to postpone the investigation and keep the affected files intact.

False positives may occur when the backup service mistakenly attributes legitimate changes to ransomware. Please pay attention to the flagged files reported by the backup service and ensure whether or not such files are actually corrupted before deleting them.

> This feature is most effective for preventing you from ransomware attacks when used as part of a broader protection strategy that includes appropriate lifecycle and retention policies. Please refer to the following blog post online to learn how to protect your backups: [4 Ways to Protect Against Ransomware with Backups](https://www.cloudberrylab.com/blog/how-ransomware-works/).



