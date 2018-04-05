## Syncing Your Repository

**\[What is the difference between syncing Amazon Glacier and other vendors' repositories?\]**

**\[Add info and links on consistency check as well.\]**

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

### Syncing Repository when using a Custom Mode for File Backups

When you backing up files using a [custom mode](/concepts/backup-wizard/backup-filesfolders/shared-select-the-backup-mode.md), the backup service copies these files to a specified folder in the target storage as is, without storing any meta data, such as information about file versions and their modification dates.

To restore such files after you have deleted the CloudBerry Backup repository, you need to synchronize your repository via the command line interface, as follows.

* Run the Command Prompt with appropriate privileges.
* Navigate to the Cloudberry Backup installation folder.
* Execute the following command:

```
cbb.exe account -s "your_account_name" -custom "folder_name"
```

In this example, "**your\_account\_name**" stands for your cloud storage account name and "**folder\_name**" stands for the name of the folder that is missing in the file tree under your bucket/container.

**\[Installation folder?\]**



