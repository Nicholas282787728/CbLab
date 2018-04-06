## Select the Backup Mode

> This page is not available when choosing **Hybrid Backup** or enabling Ransomware Protection on the [first wizard page](/concepts/backup-wizard/backup-filesfolders/welcome.md). In these cases, you need to specify the advanced options on the [next wizard page](/concepts/backup-wizard/backup-filesfolders/shared-specify-the-advanced-options.md).

On this page, you can select how your backup routine should be executed by choosing any of the following backup modes:

* **Advanced Mode**  
  This is the default mode that provides maximum flexibility in terms of the available settings.

  > Please be informed that when choosing this mode, you will only be able to access the contents of files in your backup using CloudBerry software. We cannot guarantee the ability to access this contents when using third-party software.

* **Simple Mode**  
  This mode does not support encryption, block-level backup and custom retention policy.

  > When choosing this mode, you will be able to access the contents of files in your backup using any appropriate third-party file manager/explorer tool.

* **Custom Mode**  
  With this mode, the backup service copies your files to a specified folder in the target storage as is, without storing any meta data, such as information about file versions and their modification dates. This is similar to copying files using a file explorer.

  > Please be informed that after deleting the CloudBerry Backup repository, restoring such files can be a non-trivial task, requiring you to manually sync your repository via the command line interface. See [Syncing Your Repository](/concepts/syncing-your-repository.md) for more information.

* **Archive Mode**  
  With this mode selected, the backup service combines all these files into a single archive. This enables you to reduce the number of requests sent to the cloud storage when your backup contains a lot of small files.

> When choosing a Simple or Custom mode, please be informed that the backup service will overwrite a file in the backup storage if this file has been locally changed.

After you selected the required mode, proceed to the [next wizard page](/concepts/backup-wizard/backup-filesfolders/shared-specify-the-advanced-options.md) to specify additional settings for your backup plan.



