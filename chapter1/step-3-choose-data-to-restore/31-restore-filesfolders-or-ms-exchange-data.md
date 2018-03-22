## 3.1 - Restore Files/Folders or MS Exchange Data

When restoring your files and/or folders with CloudBerry Backup, you have complete control over which file versions to restore. This tutorial describes how to use the Restore Wizard to set up a restore configuration for files/folders, as well as Microsoft Exchange Server data.

To restore files and/or folders, select the corresponding option in the wizard.

![](/assets/restore-files-and-folders.png)

Then, proceed with the following wizard steps to configure your restore task.

### 3.1.1 - Select File Versions to Restore

First, you need to select whether to restore specific file versions, restore to a specific point in time, or only restore versions that were modified/backed up during a specific time interval.

![](/assets/select-file-versions-to-restore.png)

This wizard page provides the following options:

#### **Restore the latest versions**

Enables you to restore the latest versions of your files available in a backup.

CloudBerry backups include only files/folders that were modified since the previous backup date. As a result, selecting this option will restore only those file versions that were modified before the most recent backup.

#### ​**Restore to a point in time**

Enables you to restore file versions available in your backup storage at the specified date and time.

CloudBerry backups include only files/folders that were modified since the previous backup date. As a result, selecting this option will restore only those file versions that were modified before the most recent backup and are not yet available in the destination folder.

If earlier versions of the corresponding files already exist in the destination folder, they will not be restored unless you explicitly enable their overwriting further in this wizard.

#### **Restore modifications from a time interval**

Restores the latest versions of files that were modified during a specific period of time.

CloudBerry backups include only files/folders that were modified since the previous backup date. As a result, selecting this option will restore only those file versions that were modified before the most recent backup and are not yet available in the destination folder.

If earlier versions of the corresponding files already exist in the destination folder, they will not be restored unless you explicitly enable their overwriting further in this wizard.

If multiple versions of the same file are available within the specified period of time, only its latest version will be restored.

#### **Restore backups from a time interval**

Enables you to restore the latest file versions from all backups that were made during a specific period of time.

If multiple versions of the same file are available across different backups made within this period of time, only the latest versions of such files will be restored.

If multiple versions of the same file are available within the specified period of time, only its latest version will be restored.

#### **Restore specific versions**

Enables you to select which versions of each file to restore. You specify which versions to restore on the next wizard page.

![](/assets/restore-specific-versions.png)

If some of the files are missing in the file explorer, this may be because your repository has not yet been synchronized to make the file tree reflect the latest modification made to your storage. In this case, you might need to manually launch the synchronization process by clicking the corresponding link on this wizard page.









