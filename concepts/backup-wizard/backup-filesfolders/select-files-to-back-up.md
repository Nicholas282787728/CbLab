## Select Files to Back Up

On this wizard page, you need to specify which files and/or folders to include in your backup.

![](/assets/backup-wizard-files-select-source.png)

Clicking the burger icon on this wizard page invokes a menu where you can choose additional options.

![](/assets/backup-wizard-files-select-source-advanced-options.png)

The following options are available on this menu:

* **Add user profile      
  **Use this option to include user folders in your backup.  
  ![](/assets/backup-wizard-select-files-add-user.png)  
  Please be informed that a backup will not be completed on encountering a user folder to which it has no access \(when the privileges under which the backup service is running do not allow accessing this folder\).  
  ![](/assets/backup-wizard-user-folder-access-denied.png)  
  Consider running the backup service under different account to avoid such errors.  
  You can change the account by right-clicking the backup service status in the application's status bar...

  ![](blob:https://legacy.gitbook.com/47134d8a-4701-493e-9ba1-92b728bc9444)

  ...or by switching to the **Tools **tab in the application toolbar and clicking **Change Service Account**.  
  ![](/assets/ribbon-tools-change-service-account.png)

* **Add network share**  
  Opens a dialog window where you can specify the path to network share containing files that you wish to include in the backup.  
  ![](/assets/backup-add-network-share.png)  
  In this dialog, you can specify user credentials used to access the network share. Alternatively, you can specify these credentials on the [next wizard page](/concepts/backup-wizard/backup-filesfolders/1-check-network-shares.md).

* **Open in dialog**  
  Invokes a new dialog window displaying the file tree.

* **Show legend**  
  Invokes a dialog window explaining how to interpret the different states of check boxes in the file tree, as follows.

  | Icon | Description |
  | :--- | :--- |
  | ![](/assets/icon-checkbox-01.png) | Neither the folder, nor any of its contents are selected. |
  | ![](/assets/icon-checkbox-02.png) | The folder is selected along with all of its contents \(the backup will include all newly created subitems in this folder as well\). |
  | ![](/assets/icon-checkbox-03.png) | The folder is selected along with some of its contents \(the backup will include all newly created subitems in this folder as well\). |
  | ![](/assets/icon-checkbox-04.png) | Some of the folder's contents are selected, but not the folder itself \(the backup will only include explicitly selected subitems, and not newly created ones\). |



