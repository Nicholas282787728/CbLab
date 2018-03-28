## 3.4.2.5.1 - Restore to a Google Cloud Instance

This wizard page enables you to restore a disk image to a [Google Cloud instance](https://cloud.google.com/compute/docs/instances/).

![](/assets/restore-google-vm-instance.png)

First, you need to select an existing, or specify a new Google Cloud account. See the following article to learn how to add a new Google Cloud account to CloudBerry Backup: [Signing up for Google](https://help.cloudberrylab.com/cloudberry-backup/signing-up-for-the-cloud/google-cloud/signing-up-for-google).

> Please make sure that the "Request Google Cloud Platform scopes" option is enabled for the specified account. This option is required to be able restore to Google Compute Engine instances. You can find this setting in the **Google Cloud Account** dialog window that is invoked by clicking the **Edit Google VM Account** button on this wizard page.
>
> To enable this option, you first need to sign out from the current account and then sign in once this setting is turned on.  
> ![](/assets/google-cloud-account-dialog-window.png)

After selecting an account, specify the main settings of a target instance:

* **Name**
  Specifies the name of a [Google Compute Engine instance](https://cloud.google.com/compute/docs/instances/) to which to restore your disk image.

  > The specified name should comply with the RFC 1035 naming convention.

* Zone
* Machine type
* Disk type
* Subnet
* IP address





