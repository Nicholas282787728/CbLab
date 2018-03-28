## 3.4.4 - Select Partitions to Restore

On this wizard page, you can select which partitions to restore.

\[\*\*If you don't restore to EBS, never exclude recovery partitions from the list.\]

* OS disk must be here\*\*

images - !!!  \(GPT\) -&gt; try MBR screenshot

On this wizard page, you need to select which partitions to restore.

![](/assets/image-based-virtual-select-partitions-2.png)

When restoring an NTFS partition, you can customize additional options. See [Resizing NTFS Partitions](/concepts/restoring-ntfs-partitions.md) for more information.

> Please be informed that import of UEFI/EFI BIOS and boot partitions is not supported by most cloud services \(such as AWS, Miscrosoft Azure and Google Cloud\). Please consult the official documentation of a particular cloud service vendor to find out the information about their specific requirements for virtual machine import.

You can also reorganize the restored partitions by selecting the corresponding option. This invokes the **Resize Partitions** dialog window where you can create new virtual disks and map the restored partitions to them using the drag-and-drop operation.

![](/assets/resize-partitions-dialog-2.png)

