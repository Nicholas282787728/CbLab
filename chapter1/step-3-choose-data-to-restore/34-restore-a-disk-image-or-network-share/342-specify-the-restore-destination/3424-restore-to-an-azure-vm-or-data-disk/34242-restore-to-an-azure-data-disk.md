## 3.4.2.4.2 - Restore to an Azure Data Disk

page blob

disk size - 4 TB max



This option enables you to restore a disk image to a [Microsoft Azure data disk](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/about-disks-and-vhds).

![](/assets/restore-azure-data-disk-account.png)

With this option selected, switching to the next wizard page enables you to specify the settings of a target data disk.

First, you need to select an existing Azure account or create and configure a new one.

After you selected an account, specify the following options:

* **Data disk name**  
  Specifies the name assigned to the target data disk.

* **Resource group**  
  Specifies the container that holds related _resources_ \(such as virtual machines, storage accounts, web apps, databases, and virtual networks\) for an Azure solution. See [Resource groups](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-overview#resource-groups) for more information.

* **Storage**  
  Specifies the storage on the target data disk.  
  See the following document to learn about the available storage options: [About disks storage for Azure Windows VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/about-disks-and-vhds).

* **Container**  
  Specifies the bucket to which the data disk will be placed.



