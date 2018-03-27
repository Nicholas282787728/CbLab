## 3.4.2.4 - Restore to Azure Virtual Machine or Data Disk

On this wizard page, you can select whether you need to restore an image to an Azure Virtual Machine or Azure Data Disk.

![](/assets/restore-azure.png)

The following tutorials provide step-by-step instructions on how to set up you Microsoft Azure account for restoring an image disk:

* [3.4.2.4.1 - Restore to an Azure Virtual Machine](/chapter1/step-3-choose-data-to-restore/34-restore-a-disk-image-or-network-share/342-specify-the-restore-destination/3424-restore-to-an-azure-vm-or-data-disk/34241-restore-to-an-azure-virtual-machine.md)
* [3.4.2.4.2 - Restore to an Azure Data Disk](/chapter1/step-3-choose-data-to-restore/34-restore-a-disk-image-or-network-share/342-specify-the-restore-destination/3424-restore-to-an-azure-vm-or-data-disk/34242-restore-to-an-azure-data-disk.md)

**\[An overview note comes here:\]**

Unlike Amazon Web Services that provides a [single IAM account](https://aws.amazon.com/iam/) for managing any user activity, Microsoft Azure uses different sets of credentials for backing up, storing and restoring data. See the following articles to learn more about the Role-Based Access Control \(RBAC\) used in the Azure portal:

* [Get started with Role-Based Access Control in the Azure portal](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#)

* [Use Role-Based Access Control to manage access to your Azure subscription resources](https://docs.microsoft.com/en-us/azure/active-directory/role-based-access-control-configure)

Each Azure subscription is associated with one Azure Active Directory \(AD\) directory. Users, groups, and applications from that directory can manage resources in the Azure subscription. Microsoft provides two different types of accounts that are both linked to an Azure AD:

* **Personal account **\(can be referred to as _"Microsoft account"_, formerly known as _"Windows Live ID"_\)
  This account is linked to an individual and is not supposed to change after changing one's job. Such accounts cannot access services outside of their respective Azure AD.
* **Work or school account** \(sometimes, it is also called an "_organizational account"_\)
  This account is tied to your company and is used to manage access to your Office 365, Azure cloud, SharePoint, and other services. Furthermore, this account can belong to one of the following domains:  
  - Local domain  
  - Azure AD   
  Invited users  
  test  
  test

 



CloudBerry provides 













