## Syncing Your Repository

**\[What is the difference between syncing Amazon Glacier and other vendors' repositories?\]**

**expedited \(fast\)/standard/bulk**

**image OR files**

**\[Add info and links on consistency check as well.\]**

If some of the files are missing in the file tree displaying the contents of your backup, this may be because your repository has not yet been synchronized to make the file tree reflect the latest modification made to your storage.

> CloudBerry Backup's repository is SQLite database containing information about the backed up data, including the operations that have been performed with the data and additional service information. CloudBerry Backup uses this repository to keep track of the backed up data and ensure that the backup services will not repeatedly upload files that already reside in the cloud. This reduces the number of requests sent to the cloud and lowers your storage bills.

You can do one of the following to ensure that your local repository is up to date:

* Perform a [consistency check](/concepts/performing-a-consistency-check.md) to detect any discrepancies between the repository and the backup storage and take appropriate action on finding any mismatch.
* Synchronize your repository to delete the current repository and update it according to the current backup storage contents from scratch.

> Please be informed that such synchronization may take up to several hours. This is why we do not recommend you to perform synchronization unless this is absolutely necessary.
>
> You cannot schedule a synchronization routine to make it run automatically, and you need to launch the synchronization manually.
>
> Syncing the repository only updates the local CloudBerry Backup database. It neither affects the data in the cloud, nor your backup/restore plans.

You can launch the synchronization process by clicking the corresponding link in the wizard.

![](/assets/synchronize-repository-dialog-window.png)

To sync a repository without using the wizard, click **Options **in your CloudBerry Backup application's menu.

![](/assets/cb-backup-ribbon-tools-options.png)

In the **Options** dialog that is invoked, switch to the **Repository **tab and click **Synchronize Repository**.

![](/assets/cb-backup-options-repository-sync.png)

Synchronization is logged in the **console.log** file located in the application folder within the **ProgramData** directory.

### Syncing Repository when using a Custom Mode for File Backups

When you backing up files using a [custom mode](/concepts/backup-wizard/backup-filesfolders/shared-select-the-backup-mode.md), the backup service copies these files to a specified folder in the target storage as is, without storing any meta data, such as information about file versions and their modification dates.

To restore such files after you have deleted the CloudBerry Backup repository, you need to synchronize your repository via the command line interface, as follows.

* Run the Command Prompt with appropriate privileges.
* Navigate to the Cloudberry Backup installation folder.
* Execute the following command:

```
cbb.exe account -s "your_account_name" -custom "folder_name"
```

In this example, "**your\_account\_name**" stands for your cloud storage account name  
 and "**folder\_name**" stands for the name of the folder that is missing in the file tree under your bucket/container.

