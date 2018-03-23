## 3.4.2.4.1 - Restore to an Azure Virtual Machine

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
  - [Sizes for Windows virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes)  
  - [Sizes for Linux virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/sizes)

* **Network**  
  When you create an Azure virtual machine, you must create a _virtual network \(VNet\)_ or use an existing VNet.  
  See the following document for more information: [Virtual networks and virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/network-overview).

* **Subnet**  
  Specifies the subnet in the virtual network.  
  A subnet is a range of IP addresses in the VNet. You can divide a VNet into multiple _subnets _for organization and security. Each NIC in a VM is connected to one subnet in one VNet. NICs connected to subnets \(same or different\) within a VNet can communicate with each other without any extra configuration.  
  See the following document for more information: [Virtual networks and virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/network-overview).

* **Storage**
  Specifies the storage on the target virtual machine.  
  See the following document to learn about the available storage options: [About disks storage for Azure Windows VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/about-disks-and-vhds).

* **Container**
  Specifies the bucket to which the virtual machine's disks will be placed.

* **Boot diagnostic storage**
  Specifies the storage for [boot diagnostic files](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/boot-diagnostics).

* **Operating system**
  Specifies the operating system of the target virtual machine \(Windows or Linux\).

Next, ...

