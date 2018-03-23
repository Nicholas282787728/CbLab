## 3.1.2.3.2 - Restore to Amazon Machine Image \(AMI\)

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





