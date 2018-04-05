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

The new feature is designed to protect a customer's existing, good backups, from being overwritten by encrypted ones because of a ransomware attack.

CloudBerry Backup now detects encryption changes in files and prevents existing backups from being overwritten until an administrator confirms if there is an issue.

1.CloudBerry performs the initial backup and efficiently analyzes the bit structure of each file to determine if the file is encrypted.

1. During subsequent backups, we compare the original byte structure to the current byte structure. This allows us to identify any newly encrypted files. The backup plan completes normally, however, we prevent existing backups from being deleted regardless of retention policies. This way, existing good backups are protected and are available for restore. 

> Ransomware protection is currently supported only for File-Level Backup.

Once the plan is saved, you'll see a "lock" icon for any plan with ransomware protection enabled.

If the lock symbol is red then click on in and choose "Show result"

notifications:

If encryption changes are detected, any deletes from backup storage will be disabled for flagged files. Admins can quickly see a list all of all affected files and approve any false-positive detections.

The feature is about protecting your files, not the backup data. If your files get encrypted they will still be stored on backup store, but CB will keep the last unencrypted version, regardless of purge settings, until you confirm that it was not a reasonware attack, so you will always have at least one version unencrypted on your backup.

> The software is looking at the first state of the files. In other words - if the files are non-encrypted and after some 10th backup become encrypted \(not by the software\), we suspect those files. If files are encrypted on the first run - it's ok. If their encryption is changed - then it's not ok.

You manually inspect those files in_Windows / File Explorer\_using the\_Show in Folder\_option. If you want to remove the most recent backup of an affected file from backup storage, select the file and click\_Delete_.

If you click_Cancel_, purge settings for any affected files will continue to be disabled and those files will remain on the list.

You can also be notified with an email that lists of all flagged files.

[https://www.cloudberrylab.com/blog/ransomware-protection-in-cloudberry-backup-5-8/](https://www.cloudberrylab.com/blog/ransomware-protection-in-cloudberry-backup-5-8/)

Delete - deletes the potentially ransomware affected files

Approve - means that files are not ransomware affected and they would not be deleted.

Limitation: no black/whitelist directories for the Ransomeare Protection

Only Advanced backup mode is supported with this feature on

* So, this will increase the size of the cloud backup? I wouldnt know how many versions of each file I have?  
  * Yes, that's correct. Until you click delete or approve buttons, the files will remain on the cloud storage

Hi! It will analyze current files on your backup source and on the next start the software will begin to check the encryption.

We, however, cannot analyze files, that are already on the cloud storage \(in some cases it's not possible and in some - it would be quite expensive\)



Note:

Should use other measures: https://www.cloudberrylab.com/blog/protect-against-ransomware-with-backups/



---

See also: [Increasing Backup Processing Speed](/concepts/increasing-backup-processing-speed.md)

