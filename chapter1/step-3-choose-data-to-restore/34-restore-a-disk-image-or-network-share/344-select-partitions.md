## 3.4.4 - Select Partitions to Restore

\[\*\*If you don't restore to EBS, never exclude recovery partitions from the list.\]

* OS disk must be here\*\*

**-UEFI is not supported - **not our problem \(we support, e.g. virtual box\) - this is the cloud service limitation

\(Azure plans to support UEFI boot\)

Collect requirements \(Google, Azure, Amazon\) - and give links

images - !!!  \(GPT\) -&gt; try MBR screenshot

On this wizard page, you need to select which partitions to restore.

![](/assets/image-based-virtual-select-partitions-2.png)

When restoring an NTFS partition, you can customize additional options. See [Resizing NTFS Partitions](/concepts/restoring-ntfs-partitions.md) for more information.

> Please be informed that UEFI/EFI BIOS and boot partitions are not supported by VM Import/Export with **\[Amazon EC2\]**. See the following document for more information: [VM Import/Export Requirements](https://docs.aws.amazon.com/vm-import/latest/userguide/vmie_prereqs.html).

You can also reorganize the restored partitions by selecting the corresponding option. This invokes the **Resize Partitions** dialog window where you can create new virtual disks and map the restored partitions to them using the drag-and-drop operation.

![](/assets/resize-partitions-dialog-2.png)

