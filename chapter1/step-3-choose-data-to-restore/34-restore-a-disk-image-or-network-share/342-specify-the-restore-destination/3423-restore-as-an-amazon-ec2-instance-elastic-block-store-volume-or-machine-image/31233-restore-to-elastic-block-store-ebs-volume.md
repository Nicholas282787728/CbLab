## 3.1.2.3.3 - Restore to Elastic Block Store \(EBS\) Volume

[Amazon EBS](https://aws.amazon.com/ebs/) provides raw storage – just like a hard disk – which you can attach to your EC2 instances. Once attached, you create a file system and get immediate access to your storage.

With this option selected, switching to the next wizard page enables you to specify the settings of a target EC2 instance.

![](/assets/ebs-instance-details.png)

First, you need to select an existing, or specify a new _"S3"_ or _"S3 China"_ instance account.

_**\[See the following article to learn how to add a new S3 account to CloudBerry Backup.\]**_

_**\[Please make sure that the specified account has all required permissions.\]**_



After selecting an account, specify the main settings of a target EC2 instance:

* **Region  
  **Amazon EC2 is hosted in multiple locations world-wide that are composed of _regions_ and _Availability Zones_. Each region is a separate geographic area encompassing multiple, isolated locations known as Availability Zones. Amazon EC2 provides you the ability to place resources, such as instances, and data in multiple locations. Resources are not replicated across regions unless you do so specifically.

> Note that there is a charge for data transfer between regions.
>
> See [Regions and Availability Zones](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html) for more information.

* **Instance type**

  Amazon EC2 provides a wide selection of instance types optimized to fit different use cases, such as computing, memory use, accelerated computing and optimized storage.

  > See[Amazon EC2 Instance Types](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#)learn about the available instance types.

* **Subnet**

  A virtual private cloud \(VPC\) is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud. You can launch your AWS resources, such as Amazon EC2 instances, into your VPC.

  > A VPC spans all the Availability Zones in the region.
  >
  > After creating a VPC, you can add one or more subnets in each Availability Zone.
  >
  > See[VPCs and Subnets](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#)for more information[.](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#)

* **Security group**

  AWS enables you to increase security in your VPC by using the following features:

  * **Security groups**act as a firewall for associated Amazon EC2 instances, controlling both inbound and outbound traffic at the instance level.

  * **Network access control lists \(ACLs\)**act as a firewall for associated subnets, controlling both inbound and outbound traffic at the subnet level.

  While you are more likely to use security groups, you can also use network ACLs if you want an additional layer of security for your VPC.

  > When you launch an instance in a VPC, you can associate one or more security groups that you've created. Each instance in your VPC could belong to a different set of security groups. If you don't specify a security group when you launch an instance, the instance automatically belongs to the default security group for the VPC.
  >
  > See[Security](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#)to learn more about this feature[.](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#)

  _**\[What this note on VMware is about?\]**_

  \_\*\*\[Do we need to elaborate on Network ACL here? Is it up and running automatically?\]

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



