## 3.4.4 - Select Partitions to Restore

On this wizard page, you need to select which partitions to restore.

![](/assets/image-based-select-partitions.png)

When restoring an NTFS partition, you can customize additional options. See [Restoring NTFS Partitions](/concepts/restoring-ntfs-partitions.md) for more information.

> Please be informed that UEFI/EFI BIOS and boot partitions are not supported by VM Import/Export with Amazon EC2. See the following document for more information: [VM Import/Export Requirements](https://docs.aws.amazon.com/vm-import/latest/userguide/vmie_prereqs.html).

You can also reorganize the restored partitions by selecting the corresponding option. This invokes the **Resize Partitions** dialog window where you can create new virtual disks and map the restored partitions to them using the drag-and-drop operation.

![](/assets/resize-partitions-dialog.png)

