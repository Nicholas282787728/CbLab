## 3.1.3 - Specify the Restore Destination

On this wizard page, you need to select where to restore the selected files.

![](/assets/specify-restore-destination.png)

You can choose one of the following options:

* **Restore to the original location**

  This will restore the selected files to the same directory where the source files were located.

* **Restore to a specific location**

  This will restore the selected files to a custom directory.

You can make the Restore Wizard to use this location as a default destination for newly created restore plans by enabling a corresponding option.

In addition, you can specify the following options on this wizard page:

* **Restore deleted files**

  Enables you to select whether or not to restore locally deleted files if the corresponding backup was configured to keep track of them.

  > When configuring a new backup, the Create Backup Plan Wizard enables you to choose whether or not the backup should store any data that has been deleted from a local storage. When this feature is enabled for a backup, the Restore Wizard lets you choose whether to include locally deleted files in the restored data.​

* **Overwrite existing files**

  This option is only available in the Advanced backup mode \(that is, when multiple versions are supported for a backup\). It specifies whether to replace the existing files in the destination folder with their newer versions, or keep the older files and do not restore their newer versions.

  > Different file versions are attributed to the same file only if their names are identical to that of the original file. This is why a file that has been renamed in a local storage will not be considered to be a new version of the previously named file.

  When this option is enabled, you can also specify whether to restore only newer file versions, or all files regardless of their modification time.

* **Restore NTFS permissions**

  When a backup is configured to store NTFS permissions assigned to files and folders, you can enable this option to restore these permissions along with the selected files. See the following article online to learn more about this feature:[ ](http://www.ntfs.com/ntfs-permissions.htm.)[NTFS Permissions](http://www.ntfs.com/ntfs-permissions.htm).

When using an Amazon cloud storage, you can choose whether to restore any files located in [Amazon Glacier](https://aws.amazon.com/glacier/) using the corresponding option on this wizard page.

> In most cases, these files do not need to be restored and we recommend that you leave this option disabled. Otherwise, please be informed that restoring these files can be either too slow \(up to several hours\), or too expensive.
>
> However, if you still need to restore Amazon Glacier data, you can select the preferred data retrieval mode on the next wizard page by choosing the corresponding option.
>
> ![](/assets/restore-glacier-data.png)
>
> See [Restoring Amazon Glacier Data](/concepts/restoring-amazon-glacier-data.md) for more information.



