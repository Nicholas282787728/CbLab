On the first wizard page, you can select a route for your backup and choose whether you need to protect your backup from ransomware activity.

![](/assets/backup-wizard-welcome-page-hybrid-local-cloud-ransomware.png)

### Selecting a Backup Route

Your backup data can take one of the following routes:

1. Back up your data directly to a local or cloud storage \(**one-way backup**\).

![](/assets/icon-local-to-cloud.png)

This is the default way to back up your data, without introducing any intermediate storage between the backup source and destination.

1. Back up your data first to a local storage, and then copy it from this storage to a cloud \(**two-way** or **hybrid backup**\).

![](/assets/icon-hybrid-backup.png)

Use this option to send your backup to two destinations at once and avoid repeated processing of data.

With this option selected, the backup service first processes your data and moves it to a Network-attached storage \(NAS\) or similar local storage, from where the already processed backup makes its way to a cloud storage.

This allows you to avoid repeated processing of your data when you need to compress and/or encrypt it, because the backup service performs these operations only once, before the saving the backup to the local storage.

For this reason, when you only need to compress and/or encrypt your backup in a cloud, and not in a local storage, you should create two separate one-way backup tasks instead of selecting the hybrid backup option.

### Enabling Ransomware Protection





