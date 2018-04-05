On the first wizard page, you can select a route for your backup and choose whether you need to protect your backup from ransomware activity.

![](/assets/backup-wizard-welcome-page-hybrid-local-cloud-ransomware.png)

### Selecting a Backup Route

Your backup data can take one of the following routes:

* Back up your data directly to a local or cloud storage \(**one-way backup**\).

![](/assets/icon-local-to-cloud.png)  
This is the default way to back up your data, without introducing any intermediate storage between the backup source and destination.

* Back up your data first to a local storage, and then copy it from there to a cloud \(**two-way** or **hybrid backup**\).

![](/assets/icon-hybrid-backup.png)

Use this option to send your backup to two destinations at once and avoid repeated processing of data.

With this option selected, the backup service first processes your data and moves it to a Network-attached storage \(NAS\) or similar local storage, from where the already processed backup makes its way to a cloud storage.

This allows you to avoid repeated processing of your data when you need to compress and/or encrypt it, because the backup service performs these operations only once, before the saving the backup to the local storage.

For this reason, when you only need to compress and/or encrypt your backup in a cloud, and not in a local storage, you should create two separate one-way backup tasks instead of selecting the hybrid backup option.

Limitations:

* no Archive Mode support 
* **no "delete files if they were deleted locally" support \(hybrid backups will not delete files that have been deleted locally - from the cloud/backup destination. Or will be purged according to your retention policy.\)**

* test

### Enabling Ransomware Protection

---

test

Our software uploads file in chunks. Chunk is a part of a file. You can set the size of the chunk going to Tools \| Options \| Advanced

Multipart upload allows to split files into multiple chunks and upload them in multiple threads. It is enabled by default.

also:

Cloudberry prepares chunks in memory \(for instance with default settings of 6 thread count and 100 MB chunk size the following happens: 6 threadcount x 100 MB x 2 workflows = 1200 MB is required\).

By default the amount of allocated memory is 300 MB and is not available in the UI, however it is possible to change in settings.list.

`<MemoryManagerMaxMemoryUsage>314572800</MemoryManagerMaxMemoryUsage>`

[https://kb.cloudberrylab.com/kb1046/](https://kb.cloudberrylab.com/kb1046/)

