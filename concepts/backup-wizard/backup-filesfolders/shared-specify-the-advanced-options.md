## Specify the Advanced Options

This wizard page provides different customization options depending on which [backup mode](/concepts/backup-wizard/backup-filesfolders/shared-select-the-backup-mode.md) and [backup route](/concepts/backup-wizard/backup-filesfolders/welcome.md) you selected, as well as on whether or not you enabled [ransomware protection](/concepts/backup-wizard/backup-filesfolders/welcome.md) for this backup plan.

### Advanced Mode Settings

> This is the default mode and the only one that is available when enabling Ransomware Protection and/or choosing the hybrid backup type on the [first wizard page](/concepts/backup-wizard/backup-filesfolders/welcome.md).

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

  The [Restore Wizard](/chapter1/step-3-choose-data-to-restore/31-restore-filesfolders-or-ms-exchange-data/313-specify-the-restore-destination.md) will then enable you to choose whether or not to restore these permissions along with the recovered files.

* **Save deleted data                    
  **This option specifies whether or not the storage should keep locally deleted files.

  When this feature is enabled for a backup, the [Restore Wizard](/chapter1/step-3-choose-data-to-restore/31-restore-filesfolders-or-ms-exchange-data/313-specify-the-restore-destination.md) enables you to choose whether to restore copies of locally deleted files along with the rest of the data.​

* **Use Backup Operator            
  **CloudBerry Backup is running under the Local System account by default, which does not allow the backup service to access NTFS and other important permissions.  
  Use this option to enable users with Backup Operator permissions to back up files regardless of any security permissions assigned to these files.

  > If you are a member of the Administrators or Backup Operators group on the local computer, you can back up any file and folder on the local computer to which the local group applies. Likewise, if you are a member of the Administrators or Backup Operators group on a domain controller, you can back up any file and folder locally on any computer in the domain with which you have a two-way trust relationship. See the following document for more information: [Back up files and directories - security policy setting](https://docs.microsoft.com/en-us/windows/security/threat-protection/security-policy-settings/back-up-files-and-directories).

  The service account under which CloudBerry Backup is running must be a member of the Backup Operators group. You can change the account by right-clicking the backup service status in the application's status bar.

![](/assets/application-console-status-bar-change-service-account.png)

See the following blog post online to learn how to add a user to the Backup Operators group: [Support for Backup Operators API in CloudBerry Backup 5.7](https://www.cloudberrylab.com/blog/support-for-backup-operators-api-in-cloudberry-backup-5-7/).

* **Use fast NTFS scan                                        
  **Use this option to speed up backup processing by using a custom file scanning algorithm when you need to back up a considerably large number of files that are stored on an NTFS-formatted device.

  The resulting performance gain may vary depending on which storage device you are using and the number of files contained in your backup. While this gain may not be evident when running your backup plan for the first time, you should notice the difference when running subsequent differential backup.

  Enabling this option will enforce the Volume Shadow Copy Service protocol \(see below\).

  See the following blog post online to learn more about using this feature: [Fast NTFS scan in CloudBerry Backup 5.7](https://www.cloudberrylab.com/blog/fast-ntfs-scan-in-cloudberry-backup-5-7/).

* **Force using Volume Shadow Copy Service \(VSS\)          
  **This option enables [Volume Shadow Copy Service \(VSS\)](https://msdn.microsoft.com/en-us/library/windows/desktop/aa384649%28v=vs.85%29.aspx) that captures and copies stable images for backup on running systems without degrading the performance and stability of the services they provide. Use this option to force backing up of files that may be locked at the time of backup.

  > When using this feature, you can specify a custom VSS provider of your choice \(see below\).

  Please consider the following limitations that apply to using this service:

  * VSS cannot be used to back up network files, such as network shares and mapped network drives.

  * VSS cannot make snapshots of data stored in FAT32-partitioned volumes.

* **\(Use system VSS provider\)          
  **When using VSS for making snapshots of all files on a volume \(see above\), you can use this option to specify a custom third-party VSS provider. In some cases, this enables you to avoid errors resulting from using the standard Windows VSS provider.

### Configuring Other Modes

When choosing the Simple, Custom or Archive mode on the [previous wizard page](/concepts/backup-wizard/backup-filesfolders/shared-select-the-backup-mode.md), the set of settings available on this page is limited by the following three options:

* **Use fast NTFS scan**

* **Force using Volume Shadow Copy Service \(VSS\)**

* **Use system VSS provider**

See the previous section of this document to learn about these settings.

### 



