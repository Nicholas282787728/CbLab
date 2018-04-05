## Specify the Advanced Options

This wizard page provides different customization options depending on which [backup mode](/concepts/backup-wizard/backup-filesfolders/shared-select-the-backup-mode.md) and [backup route](/concepts/backup-wizard/backup-filesfolders/welcome.md) you selected, as well as on whether or not you enabled [ransomware protection](/concepts/backup-wizard/backup-filesfolders/welcome.md) for this backup plan.

### Advanced Mode

> This is the default mode and the only mode available when enabling Ransomware Protection and/or choosing the hybrid backup type on the [first wizard page](/concepts/backup-wizard/backup-filesfolders/welcome.md).

This mode provides a complete set of customization options for configuring your backup plan. However, you will not be able to access individual files in your backup using conventional file management tools, because a backup will be stored as a single solid object.

The available options are explained below.

* **Use block-level backup            
  **As opposed to a full backup which uploads a complete copy of each file to a storage, a block-level backup uploads the full copy of your data only during the first execution of the backup plan. On each subsequent running, the backup service uploads only blocks that were modified since the last backup date, which can dramatically decrease the processing time required for completing your backup routine, as well as reduce the required storage space.

  > See the following articles online to learn more about the difference between each backup type:
  >
  > * [Best Practices: Block-Level Backup](https://www.cloudberrylab.com/blog/best-practices-block-level-backup/)
  > * [Block Level Backup and Full Backup Explained](https://www.cloudberrylab.com/blog/block-level-backup-and-full-backup-explained/)

* **Backup NTFS permissions            
  **Enable this option to retain all [NTFS permissions](http://www.ntfs.com/ntfs-permissions.htm) assigned to your files, folders and network shares.

  The [Restore Wizard](/chapter1/step-3-choose-data-to-restore/31-restore-filesfolders-or-ms-exchange-data/313-specify-the-restore-destination.md) will then enable you to choose whether or not to restore these permissions along with the files.

* **Save deleted data      
  **This option specifies whether or not the storage should keep locally deleted files.

  When this feature is enabled for a backup, the [Restore Wizard](/chapter1/step-3-choose-data-to-restore/31-restore-filesfolders-or-ms-exchange-data/313-specify-the-restore-destination.md) enables you to choose whether to restore copies of locally deleted files along with the rest of the data.​

* **Use Backup Operator**  
  [https://www.cloudberrylab.com/blog/support-for-backup-operators-api-in-cloudberry-backup-5-7/](https://www.cloudberrylab.com/blog/support-for-backup-operators-api-in-cloudberry-backup-5-7/)

* **Use fast NTFS scan                          
  **In CloudBerry Backup 5.7 we've added an option to use our own proprietary file scanning & search mechanism. In essence, our method — as opposed to Windows's NTFS file scanning method — generates a file tree. Navigating through the said file tree is considerably faster, resulting in overall faster backups. Needless to say, performance varies depending on the type of storage device you're using and the number of files targeted for backup.

We've run a series of tests to examine the performance of the new feature and collected the data in a separate post that also explains how you can enable our file scanning mechanism in the Restore Wizard.

[https://www.cloudberrylab.com/blog/fast-ntfs-scan-in-cloudberry-backup-5-7/](https://www.cloudberrylab.com/blog/fast-ntfs-scan-in-cloudberry-backup-5-7/)  
  Ensure that the files you're backing up are stored on an NTFS-formatted storage device; elsewise, there is no point in using the feature.

Perhaps you won't notice much difference during the initial backup, but further differential backups will undoubtedly save you time.

Also note that utilizing Fast NTFS Search entails facing two appreciable disadvantages:

* It is not recommended when few files are selected;
* VSS snapshot is invariably required.

* **Force using Volume Shadow Copy Service \(VSS\)**

* **\(Use system VSS provider\)**

### Simple, Custom and Archive Modes

* **Use fast NTFS scan**
* **Force using Volume Shadow Copy Service \(VSS\)**
* **\(Use system VSS provider\)**

### Hybrid

**Backup NTFS permissions**

**Use Backup Operator**

**Use fast NTFS scan      **

**Force using Volume Shadow Copy Service \(VSS\)**

* **\(Use system VSS provider\)**



