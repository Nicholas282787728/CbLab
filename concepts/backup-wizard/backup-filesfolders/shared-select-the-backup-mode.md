## Select the Backup Mode

> This page is not available when choosing **Hybrid Backup** or enabling Ransomware Protection on the [first wizard page](/concepts/backup-wizard/backup-filesfolders/welcome.md). In these cases, you need to specify the advanced options on the [next wizard page](/concepts/backup-wizard/backup-filesfolders/shared-specify-the-advanced-options.md).

On this page, you can select how your backup routine should be executed by choosing any of the following backup modes:

* **Advanced Mode**  
  This is the default mode that provides maximum flexibility in terms of the available settings.  
  **On the downside, you will not be able to access individual files in your backup when using any of the following features:**

  * **encryption;  **
  * **compression;  **
  * **file-name encryption;**
  * **block-level backup.**

* **Simple Mode**  
  This mode does not support encryption, block-level backup and custom retention policy.  
  **On the other hand, you will be able to access individual files in such a backup.**

* **Custom Mode**  
  With this mode, the backup service copies your files to a specified folder in the target storage as is, without storing any meta data, such as information about file versions and their modification dates. This is similar to copying files using a file explorer.

  > Please be informed that after deleting the CloudBerry Backup repository, restoring such files can be a non-trivial task, requiring you to manually sync your repository via the command line interface. See [Syncing Your Repository](/concepts/syncing-your-repository.md) for more information.

* **Archive Mode**  
  With this mode selected, the backup service combines all these files into a single archive. This enables you to reduce the number of requests sent to the cloud storage when your backup contains a lot of small files.

After you selected the required mode, proceed to the [next wizard page](/concepts/backup-wizard/backup-filesfolders/shared-specify-the-advanced-options.md) to specify additional settings for your backup plan.



**\[custom mode/simple mode:  
if a file has changed - do we overwrite this file?\]**



