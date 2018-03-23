## 3.1.2.3.3 - Restore to Elastic Block Store \(EBS\) Volume

[Amazon EBS](https://aws.amazon.com/ebs/) provides raw storage – just like a hard disk – which you can attach to your EC2 instances. Once attached, you create a file system and get immediate access to your storage.

With this option selected, switching to the next wizard page enables you to specify the settings of a target EC2 instance.

![](/assets/ebs-instance-details.png)

First, you need to select an existing, or specify a new _"S3"_ or _"S3 China"_ instance account.

After selecting an account, specify the main settings of a target EC2 instance:

* **Region**  
  Amazon EC2 is hosted in multiple locations world-wide that are composed of regions and Availability Zones. Each region is a separate geographic area encompassing multiple, isolated locations known as Availability Zones. Amazon EC2 provides you the ability to place resources, such as instances, and data in multiple locations. Resources are not replicated across regions unless you do so specifically.

  > Note that there is a charge for data transfer between regions.
  >
  > See [Regions and Availability Zones](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) for more information.

* **Availability Zones**

  Click **Refresh** to obtain the list of Availability Zones available for this region.

  > The wizard indicates whether [VM import](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) user roles are configured property. See [Configuring a VMimport Role](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) for more information.

* **EBS volume type**

  Amazon EBS \(Elastic Block Store\) provides the following volume types, which differ in their performance characteristics and price, so that you can tailor your storage performance and costs to the requirements of your applications. CloudBerry Backup supports the following volume types:

  * **General Purpose SSD \(gp2\)                                                        
    **A general purpose SSD volume that balances price and performance for a wide variety of workloads.

  * **Provisioned IOPS SSD \(io1\)                                                        
    **The highest-performance SSD volume for mission-critical low-latency or high-throughput workloads.

  * **Magnetic \(standard, a previous-generation type\)                                                        
    **A previous generation HDD. If you need higher performance or performance consistency than previous-generation volumes can provide, we recommend that you consider using _General Purpose SSD \(gp2\)_ or other current volume types.

  * **Throughput Optimized HDD \(st1\)**  
    A low cost HDD volume designed for frequently accessed, throughput-intensive workloads.

  * **Cold HDD \(sc1\)**_  
    _The lowest cost HDD volume designed for less frequently accessed workloads.

> See [Amazon EBS Volume Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) to learn more.



