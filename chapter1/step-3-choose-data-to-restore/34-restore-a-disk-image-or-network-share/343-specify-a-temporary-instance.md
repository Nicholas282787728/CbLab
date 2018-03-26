## 3.4.3 - Specify a Temporary Instance

**\[more details - any recommendations on which to choose? any errors/precautions\]**

**do not choose micro nano instances \(t2-micro, t1 nano, ets.\)**

t-instances up to large \(medium-large\)

several stages:

* Raising a temp machine. This time does not depend on anything ~ 4 min
* The time to install the client
* The time to process an image-based backup - !
* The time to process the created image by AWS - we cannot do anything - the longest \(depends on size, region, other factors\)

AWS has a script to check a machine whose image is made checks for import requirements. When "a machine wasn't able to launch or establish connection:

* Any mismatch does not guarantee that it fails. 
* The script is outdated. A user can take this script and check the backed up machine using this script \(troubleshooting\) but without any warrant

if restore failed - you can try to customize the source machine 

we cannot control the processing time

On this wizard page, you can select whether you need to use a temporary instance during the restore process.

![](/assets/image-based-restore-to-ami-temp-instance.png)

These two options are described below.

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

* **Subnet**

  A virtual private cloud \(VPC\) is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud. You can launch your AWS resources, such as Amazon EC2 instances, into your VPC.

  > A VPC spans all the Availability Zones in the region.
  >
  > After creating a VPC, you can add one or more subnets in each Availability Zone.
  >
  > See [VPCs and Subnets](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) for more information[.](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#)

* **Security group**

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

  * **General Purpose SSD \(gp2\)            
    **A general purpose SSD volume that balances price and performance for a wide variety of workloads.

  * **Provisioned IOPS SSD \(io1\)            
    **The highest-performance SSD volume for mission-critical low-latency or high-throughput workloads.

  * **Magnetic \(standard, a previous-generation type\)            
    **A previous generation HDD. If you need higher performance or performance consistency than previous-generation volumes can provide, we recommend that you consider using _General Purpose SSD \(gp2\)_ or other current volume types.

  > See [Amazon EBS Volume Types](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) to learn more.



