## 3.4.2.3 - Restore to an Amazon EC2 Instance, Elastic Block Store Volume, or Machine Image

You can restore your disk image to any of the following destinations:

* Restore as Amazon EC2 Instance
* Create AMI \(Amazon Machine Image\)
* Restore as EBS \(Elastic Block Store\) Volume

This options are detailed further in this article.

### Restore to Amazon EC2 Instance

This option enables you to restore your disk image to an [Amazon EC2 instance](https://aws.amazon.com/ec2/instance-types/) of your choice.

This feature is supported for the following operation systems:

* Windows Server 2008
* Windows Server 2012
* Windows Server 2016

With this option selected, switching to the next wizard page enables you to specify the settings of a target EC2 instance.

![](/assets/image-based-to-ec2-instance-details.png)

First, you need to select an existing, or specify a new _"S3"_ or _"S3 China"_ instance account.

_**\[See the following article to learn how to add a new S3 account to CloudBerry Backup.\]**_

_**\[Please make sure that the specified account has all required permissions.\]**_

_**\[Are the following settings required?\]**_

After selecting an account, specify the main settings of a target instance:

* #### **Region**

  You can place Amazon EC2 instances in multiple locations across the globe. These locations are composed of _regions_ and _Availability Zones_. Each region is a separate geographic area encompassing multiple, isolated locations known as Availability Zones.

  > When you view your resources, you can only see the resources tied to the region you have specified. This is because regions are isolated from each other, and Amazon AWS does not replicate resources across regions automatically.  
  >   
  > Some AWS resources might not be available in all regions and Availability Zones. Ensure that you can create the resources you need in the desired regions or Availability Zone before launching an instance in a specific Availability Zone.  
  >   
  > Please note that there is a charge for data transfer between regions.  
  >   
  > See [Regions and Availability Zones](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html) for more information.

_**\[What happens with a plan after migrating an instance to another Availability Zone?\]**_

* #### **Instance type**

  Amazon EC2 provides a wide selection of instance types optimized to fit different use cases, such as computing, memory use, accelerated computing and optimized storage.

  > See [Amazon EC2 Instance Types](https://aws.amazon.com/ec2/instance-types/) learn about the available instance types.

* #### **Subnet**

  A virtual private cloud \(VPC\) is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud. You can launch your AWS resources, such as Amazon EC2 instances, into your VPC.

  > A VPC spans all the Availability Zones in the region.
  >
  > After creating a VPC, you can add one or more subnets in each Availability Zone.
  >
  > See [VPCs and Subnets](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Subnets.html) for more information[.](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Subnets.html.)

* #### **Security group**

  AWS enables you to increase security in your VPC by using the following features:

  * **Security groups **act as a firewall for associated Amazon EC2 instances, controlling both inbound and outbound traffic at the instance level.

  * **Network access control lists \(ACLs\) **act as a firewall for associated subnets, controlling both inbound and outbound traffic at the subnet level.

  While you are more likely to use security groups, you can also use network ACLs if you want an additional layer of security for your VPC.

  > When you launch an instance in a VPC, you can associate one or more security groups that you've created. Each instance in your VPC could belong to a different set of security groups. If you don't specify a security group when you launch an instance, the instance automatically belongs to the default security group for the VPC.
  >
  > See [Security](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Security.html) to learn more about this feature[.](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Security.html.)

  _**\[What this note on VMware is about?\]**_

  \_\*\*\[Do we need to elaborate on Network ACL here? Is it up and running automatically?\]

  ---

* #### **EBS volume type**

  Amazon EBS \(Elastic Block Store\) provides the following volume types, which differ in their performance characteristics and price, so that you can tailor your storage performance and costs to the requirements of your applications. CloudBerry Backup supports the following volume types:

  * **General Purpose SSD \(gp2\)          
    **A general purpose SSD volume that balances price and performance for a wide variety of workloads.

  * **Provisioned IOPS SSD \(io1\)          
    **The highest-performance SSD volume for mission-critical low-latency or high-throughput workloads.

  * **Magnetic \(standard, a previous-generation type\)          
    **A previous generation HDD. If you need higher performance or performance consistency than previous-generation volumes can provide, we recommend that you consider using _General Purpose SSD \(gp2\)_ or other current volume types.

  * _Throughput Optimized HDD \(st1\)_

  * _Cold HDD \(sc1\)_

  > See [Amazon EBS Volume Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) to learn more.

---

### Restore to **Amazon Machine Image \(AMI\)**

This option enables you to restore your disk image to an [Amazon Machine Image \(AMI\)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html) of your choice.

This feature is supported for the following operation systems:

* Windows 7
* Windows 8
* Windows 10
* Windows Server 2008
* Windows Server 2012
* Windows Server 2016











---

### Restore to Elastic Block Store \(EBS\) Volume



Amazon EBS provides raw storage – just like a hard disk – which you can attach to your EC2 instances. Once attached, you create a file system and get immediate access to your storage. You can create EBS General Purpose \(SSD\) and Provisioned IOPS \(SSD\) volumes up to **16** TB in size, and slower, legacy magnetic volumes.



