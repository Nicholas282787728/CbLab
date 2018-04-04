## Operation System Licensing for Virtual Machines

When restoring a virtual machine image to Microsoft Azure, Amazon EC2 or Google Compute Engine, CloudBerry Backup passes the information about an operating system over to these services.

> Please be informed that the hourly rates for using imported machines include the fees that these cloud service providers impose for using Windows and Linux machines.

When restoring an image to AWS, you can add the ["bring your own licenses" \(BYOL\)](https://aws.amazon.com/windows/resources/licensing/) option to the restore plan's configuration as follows.

```
<?xml version="1.0"?>
<configuration>
<!-- ... -->​

<RestoreToEC2>
    <LicenseType>BYOL</LicenseType>
</RestoreToEC2>​

</configuration>
```

Hyper-V machines

