## 3.4.1 - Select File Versions to Restore

On this wizard page, you can select whether you need to restore specific file versions, or restore to a specific point in time.

![](/assets/image-based-select-file-versions-to-restore.png)

The following options are available in the wizard:

* **Latest version        
  **Enables you to restore the latest versions of your images available in a backup.

  > CloudBerry backups include only images that was modified since the previous backup date. As a result, selecting this option will restore only those image versions that were modified before the most recent backup.

* **Point in time        
  **Enables you to restore image versions available in your backup storage at the specified date and time.

  > CloudBerry backups include only images that were modified since the previous backup date. As a result, selecting this option will restore only those image versions that were modified before the most recent backup and are not yet available in the destination folder.
  >
  > If earlier versions of the corresponding images already exist in the destination folder, they will not be restored unless you explicitly enable their overwriting further in this wizard.

* **Manually        
  **Enables you to select which versions of each image to restore. You can specify which versions to restore on the next wizard page:  
  ![](/assets/image-based-select-image.png)

If some of the disks are missing in the list on this page, this may be because your repository has not yet been synchronized to make this list reflect the latest modification made to your storage. In this case, you might need to manually launch the synchronization process.

![](/assets/synchronize-repository-dialog-window.png)

> Please be informed that such synchronization may take up to several hours. This is why we do not recommend you to force synchronization unless this is absolutely necessary.
>
> See the following topic to learn how to synchronize data from Amazon Glacier and other cloud storage providers: [Synchronizing Your Repository](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#).


