## Syncing Your Repository

**\[What is the difference between syncing Amazon Glacier and other vendors' repositories?\]**

If some of the files are missing in the file tree displaying the contents of your backup, this may be because your repository has not yet been synchronized to make the file tree reflect the latest modification made to your storage.

> CloudBerry Backup's repository is SQLite database containing information about the backed up data, including the operations that have been performed with the data and additional service information. CloudBerry Backup uses this repository to keep track of the backed up data and ensure that the backup services will not repeatedly upload files that already reside in the cloud. This reduces the number of requests sent to the cloud and lowers your storage bills.

You can manually launch the synchronization process by clicking the corresponding link on this wizard page.

![](/assets/synchronize-repository-dialog-window.png)

> Please be informed that such synchronization may take up to several hours. This is why we do not recommend you to force synchronization unless this is absolutely necessary.
>
> Syncing the repository will neither affect the data in the cloud, nor the backup/restore plans.

To sync a repository without using the wizard, click **Options **in your CloudBerry Backup application's menu.

![](/assets/cb-backup-ribbon-tools-options.png)

In the **Options** dialog that is invoked, switch to the **Repository **tab and click **Synchronize Repository**.

![](/assets/cb-backup-options-repository-sync.png)



