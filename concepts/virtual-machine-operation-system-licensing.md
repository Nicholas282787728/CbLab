## Operation System Licensing for Virtual Machines

When restoring a virtual machine image to Microsoft Azure, Amazon EC2 or Google Compute Engine, CloudBerry Backup passes the information about an operating system over to these service providers.

> Please be informed that the hourly rates for using imported machines include the fees that these cloud service providers impose for using Windows and Linux machines.

See the following documents for more information:

* [Google Compute Engine Pricing](https://cloud.google.com/compute/pricing#premiumimages)
* [Google Cloud - Importing Virtual Disks](https://cloud.google.com/compute/docs/images/importing-virtual-disks#support_for_bring_your_own_license_byol)
* [Microsoft Azure - Virtual Machines licensing FAQ](https://azure.microsoft.com/en-us/pricing/licensing-faq/)

### Enabling BYOL for AWS Import

When restoring an image to AWS, you can enable the ["bring your own licenses" \(BYOL\)](https://aws.amazon.com/windows/resources/licensing/) option for the restore plan.

To quickly access a restore plan's configuration, locate the plan under the **Restore Plans** tab in your CloudBerry Backup application, press and hold **Ctrl+Alt** and click **View History**.![](/assets/restore-plans-view-history.png)In the opened restore plan configuration, add a **LicenseType** flag to the **RestoreToEC2** section, as follows.

```
<?xml version="1.0"?>
<BasePlan xsi:type="RestoreDiskImagePlan">
<!-- ... -->​

<RestoreToEC2>
    <LicenseType>BYOL</LicenseType>
</RestoreToEC2>​

<!-- ... -->​
</BasePlan>
```



