## 3.1.2.3.2 - Restore to an Amazon Machine Image \(AMI\)

This option enables you to restore your disk image to an [Amazon Machine Image \(AMI\)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html) of your choice.

> This feature is supported for the following operation systems:
>
> * Windows 7
> * Windows 8
> * Windows 10
> * Windows Server 2008
> * Windows Server 2012
> * Windows Server 2016

After switching to the next wizard page, you need to specify the instance details.

![](/assets/image-based-restore-to-ami-instance-details.png)

First, you need to select an existing, or specify a new _"S3"_ or _"S3 China"_ instance account.

After selecting an account, specify the main settings of a target instance:

* **Region**  
  Amazon EC2 is hosted in multiple locations world-wide that are composed of regions and Availability Zones. Each region is a separate geographic area encompassing multiple, isolated locations known as Availability Zones. Amazon EC2 provides you the ability to place resources, such as instances, and data in multiple locations. Resources are not replicated across regions unless you do so specifically.

  > Note that there is a charge for data transfer between regions.
  >
  > See [Regions and Availability Zones](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) for more information.

* **EBS Volume Type**

  Amazon EBS \(Elastic Block Store\) provides the following volume types, which differ in their performance characteristics and price, so that you can tailor your storage performance and costs to the requirements of your applications. CloudBerry Backup supports the following volume types:

* **General Purpose SSD \(gp2\)                                                          
  **A general purpose SSD volume that balances price and performance for a wide variety of workloads.

* **Provisioned IOPS SSD \(io1\)                                                          
  **The highest-performance SSD volume for mission-critical low-latency or high-throughput workloads.

* **Magnetic \(standard, a previous-generation type\)                                                          
  **A previous generation HDD. If you need higher performance or performance consistency than previous-generation volumes can provide, we recommend that you consider using _General Purpose SSD \(gp2\)_ or other current volume types.

> See [Amazon EBS Volume Types](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) to learn more.

On the next wizard page, select whether you need to use a temporary instance during the restore process.

![](/assets/image-based-restore-to-ami-temp-instance.png)

The options are described below.

* **Do not use temporary instance **  
  This option enables copying your files via a local computer, which is usually slower and depends on the local Internet connection speed.

* **Use temporary instance **  
  This option enables faster copying of your files at a higher cost, which depends on the instance type and running time of the restore process.

To use a temporary instance, you need to specify the settings of your temporary EC2 instance on the next wizard page.

First, you need to select an existing, or specify a new "S3" or "S3 China" instance account.

After selecting an account, specify the main settings of a target instance:

* **Region**

  Amazon EC2 is hosted in multiple locations world-wide that are composed of regions and Availability Zones. Each region is a separate geographic area encompassing multiple, isolated locations known as Availability Zones. Amazon EC2 provides you the ability to place resources, such as instances, and data in multiple locations. Resources are not replicated across regions unless you do so specifically.

  > Note that there is a charge for data transfer between regions.
  >
  > See [Regions and Availability Zones](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) for more information.

* **Instance type**

  Amazon EC2 provides a wide selection of instance types optimized to fit different use cases, such as computing, memory use, accelerated computing and optimized storage.

  > See [Amazon EC2 Instance Types](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) learn about the available instance types.

* #### **Subnet**

  A virtual private cloud \(VPC\) is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud. You can launch your AWS resources, such as Amazon EC2 instances, into your VPC.

  > A VPC spans all the Availability Zones in the region.
  >
  > After creating a VPC, you can add one or more subnets in each Availability Zone.
  >
  > See [VPCs and Subnets](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) for more information[.](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#)

* #### **Security group**

  AWS enables you to increase security in your VPC by using the following features:

  * **Security groups **act as a firewall for associated Amazon EC2 instances, controlling both inbound and outbound traffic at the instance level.

  * **Network access control lists \(ACLs\) **act as a firewall for associated subnets, controlling both inbound and outbound traffic at the subnet level.

  While you are more likely to use security groups, you can also use network ACLs if you want an additional layer of security for your VPC.

  > When you launch an instance in a VPC, you can associate one or more security groups that you've created. Each instance in your VPC could belong to a different set of security groups. If you don't specify a security group when you launch an instance, the instance automatically belongs to the default security group for the VPC.
  >
  > See [Security](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) to learn more about this feature[.](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#)

* **AMI    
  **Enables you to select a target Amazon Machine Image.

* **EBS volume type**

  Amazon EBS \(Elastic Block Store\) provides the following volume types, which differ in their performance characteristics and price, so that you can tailor your storage performance and costs to the requirements of your applications. CloudBerry Backup supports the following volume types:

  * **General Purpose SSD \(gp2\)**A general purpose SSD volume that balances price and performance for a wide variety of workloads.

  * **Provisioned IOPS SSD \(io1\)**The highest-performance SSD volume for mission-critical low-latency or high-throughput workloads.

  * **Magnetic \(standard, a previous-generation type\)**A previous generation HDD. If you need higher performance or performance consistency than previous-generation volumes can provide, we recommend that you consider using _General Purpose SSD \(gp2\)_ or other current volume types.

  > See [Amazon EBS Volume Types](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) to learn more.



---

---

On the next wizard page, you need to select which partitions to restore.

![](/assets/image-based-virtual-select-partitions.png)

> When restoring an NTFS partition, you can customize additional options. See [Restoring NTFS Partitions](/concepts/restoring-ntfs-partitions.md) for more information.
>
> Please be informed that UEFI/EFI BIOS and boot partitions are not supported by VM Import/Export with Amazon EC2. See the following document for more information: [VM Import/Export Requirements](https://docs.aws.amazon.com/vm-import/latest/userguide/vmie_prereqs.html).

You can also reorganize the restored partitions by selecting the corresponding option. This invokes the **Resize Partitions** dialog window where you can create new virtual disks and map the restored partitions to them using the drag-and-drop operation.

![](/assets/resize-partitions-dialog.png)

After switching to the next wizard page, you can specify the capacity of the destination disk.

![](/assets/ami-destination-capacity.png)

The wizard indicates the minimum and maximum capacity value, where the minimum size is the total target size for all selected partitions on the previous step.

> When restoring [Amazon Glacier](https://aws.amazon.com/glacier/) data or Amazon S3 files with the [Glacier storage class](https://aws.amazon.com/s3/storage-classes/), you can choose whether or not you need to restore data from Amazon Glacier on the next wizard page. See [Restoring Amazon Glacier Data](/concepts/restoring-amazon-glacier-data.md) to learn more about this feature.


