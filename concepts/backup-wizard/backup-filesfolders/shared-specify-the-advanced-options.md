## Specify the Advanced Options

The set of options available on this wizard page differs depending on the selected backup mode.

### Advanced Mode

\(the only supported mode when using Ransomware Protection\)

test

* **Use block-level backup**
* **Backup NTFS permissions**
* **Save deleted data**
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



