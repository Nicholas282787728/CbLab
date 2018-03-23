## 3.4.2.1 - Restore to a Physical Disk

Select this option if you need to restore your data to a physical disk.

![](/assets/image-based-select-partitions.png)

> When restoring an NTFS partition, you can customize additional options. See [Restoring NTFS Partitions](/concepts/restoring-ntfs-partitions.md) for more information.

On the next wizard page, select a physical disk to be used as a destination for the restored backup.

![](/assets/image-based-restore-physical-destination.png)

You can choose from the following two options:

* **Restore to an entire physical disk      
  **Select this option to make an entire physical disk a destination for your backup.

  > Please be informed that you will not be able to restore to a boot volume.
  >
  > **IMPORTANT**: All information on the selected disk will be permanently destroyed. Please consider backing up the existing disk image before submitting the restore process.

* **Restore to a specific partition**

  Select this option to manually map each of the restored partitions to a specific destination.

> When restoring [Amazon Glacier](https://aws.amazon.com/glacier/) data or Amazon S3 files with the [Glacier storage class](https://aws.amazon.com/s3/storage-classes/), you can choose whether or not you need to restore data from Amazon Glacier on the next wizard page. See [Restoring Amazon Glacier Data](/concepts/restoring-amazon-glacier-data.md) to learn more about this feature.



