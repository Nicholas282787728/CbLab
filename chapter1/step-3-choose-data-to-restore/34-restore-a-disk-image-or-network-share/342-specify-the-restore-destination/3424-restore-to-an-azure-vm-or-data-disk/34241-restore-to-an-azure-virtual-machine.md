## 3.4.2.4.1 - Restore to an Azure Virtual Machine

as oppsed to amazon \(we take disk and amazon processes it\), azure doesn't care what's on disk

amazon uses a single account \(IAM\), azure uses one creds for backup \(storage creds and other creds for restore \(IAM creds\)

-&gt; IAM user must have the rights \(see the KB\), there are limitations \(different for standalone and MBS\)

two parameters:

* location
* resource group

**network / storage - must belong to one region and resource group**

or you'll see empty fields :\)

beforehand, use the az\ure console tpo create a user, subscription, region, resource groups, storage account **\(!! general purpose, not blob because \),** container, 

blobs:

* block blob
* page blob \(only here Vm disk is stored, and page blob is only available in general purpose account\) and page blobs are not available on zone redundancy \(not use redundancy\)
* append blob

Never disable boot diagnostics \(because you won't be able what;s going - access to VM only via RDP \(unlike vmware\) -&gt; you need OS, betwork, RDP service, external IP address etc. 

Boot Diag - is a machine's screenshot.

When using an Azure this is OK

But when import on Azure, enable boot diag.

Azure launches as is silently without any warning \(regardless of whether OS is launched\) and you are charged

This helps during emergency recovery \(as skips diagnostics gives extra speed\)

* find links to this specifics \(installing Azure agent, add-ons etc. on your VM \)



THERE is :  
- premium storage accs \(only to store page blobs, but expensive as uses SSD, only used for storing VM disks\) - it cannot store boot diagmostics \(can be disable\). Use a regular acc instead.



This wizard page enables you to restore a disk image to a [Microsoft Azure virtual machine](https://docs.microsoft.com/en-us/azure/virtual-machines/).

![](/assets/restore-azure-vm-instance.png)

With this option selected, switching to the next wizard page enables you to specify the settings of a target virtual machine instance.

First, you need to select an existing Azure account or create and configure a new one.

After you selected an account, specify the following options:

* **Computer name**  
  Specifies the computer name assigned to the target virtual machine.

* **Location**  
  Specifies the virtual machine's location.  
  Azure operates in multiple data centers around the world that are grouped into geographic regions, giving you flexibility in choosing where to build your applications. See [Regions and availability for virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/regions-and-availability) to learn how and where your virtual machines operate in Azure, along with your options to maximize performance, availability, and redundancy.

* **Resource group**  
  Specifies the container that holds related _resources_ \(such as virtual machines, storage accounts, web apps, databases, and virtual networks\) for an Azure solution. See [Resource groups](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-overview#resource-groups) for more information.

* **Virtual machine size**  
  Specifies the size of the target virtual machine. See the following documents for more information:

  * [Sizes for Windows virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes)  
  * [Sizes for Linux virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/sizes)

* **Network**  
  When you create an Azure virtual machine, you must create a _virtual network \(VNet\)_ or use an existing VNet.  
  See the following document for more information: [Virtual networks and virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/network-overview).

* **Subnet**  
  Specifies the subnet in the virtual network.  
  A subnet is a range of IP addresses in the VNet. You can divide a VNet into multiple \_subnets \_for organization and security. Each NIC in a VM is connected to one subnet in one VNet. NICs connected to subnets \(same or different\) within a VNet can communicate with each other without any extra configuration.  
  See the following document for more information: [Virtual networks and virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/network-overview).

* **Storage**  
  Specifies the storage on the target virtual machine.  
  See the following document to learn about the available storage options: [About disks storage for Azure Windows VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/about-disks-and-vhds).

* **Container**  
  Specifies the bucket to which the virtual machine's disks will be placed.

* **Boot diagnostic storage**  
  Specifies the storage for [boot diagnostic files](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/boot-diagnostics).

* **Operating system**  
  Specifies the operating system of the target virtual machine \(Windows or Linux\):

\[**this is useful when restoring from VM \(for image based use Windows - strongly recommend\) - we cannot detect yet\]**



Next, ...

