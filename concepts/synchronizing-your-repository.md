## Synchronizing Your Repository



When a machine on which you are restoring your backup is different from the one that was used to back up these files, the Restore Wizard may not get access to some of the files in your backup. This document illustrates how to work around this issue and grant the Restore Wizard access to all files in your backup from another computer.



Do one of the following to make the Restore Wizard display all files from a backup created on another computer.

## Specify a Correct Prefix

First, make sure that the prefix on the computer on which you are restoring your files matches that of the computer used to save the backup. You can change the prefix in you cloud storage settings. To access these settings, open the_CloudBerry Backup_application menu and select your storage account.





Click the**Advanced Settings**link on the first tab of the invoked dialog window and specify the necessary prefix.

**\[Contact your system administrator if you are not sure about which prefix to specify.\]**







## Sync Your Repository



[https://www.cloudberrylab.com/blog/why-you-sometimes-cannot-see-your-files-when-restoring/](https://www.cloudberrylab.com/blog/why-you-sometimes-cannot-see-your-files-when-restoring/)

+

[https://www.cloudberrylab.com/blog/how-to-continue-backup-on-another-computer/](https://www.cloudberrylab.com/blog/how-to-continue-backup-on-another-computer/)

+

[https://www.reddit.com/r/cloudberrylab/comments/7p7q8x/synchronize\_repository/](https://www.reddit.com/r/cloudberrylab/comments/7p7q8x/synchronize_repository/)





Please be informed that you cannot instantly retrieve data from long-term storages used to backup infrequently accessed data, such as_Amazon Glacier_. This is why you may need to sync your repository if**Restore Wizard**does not display some of the files in your backup.

Please be informed that the synchronization process is time-consuming, and it may take up to several hours to obtain a list of your files from such a long-term storage.

Do one of the following to sync a repository depending on the storage provider you use.

### Amazon Glacier





**If you connect Restore Only mode then it syncs instantly. You don't need to wait for all files to download and sync try that.**



**Select the same bucket, vault or container**



**When restoring data from an Amazon Glacier account, you need to run the repository sync process manually. To do this, switch to the by going to Tools \| Options \| Repository: click “Synchronize Repository”. It will take about 4-5 hours.**



### Other Storage Providers

To sync with repositories of cloud storages other than Amazon Glacier, select**Options**in your_CloudBerry Backup_application's menu and click**Synchronize Repository**.

{image}

Next, select a storage account that you want to sync and click**Synchronize Now**.

