## Managing Azure Active Directory Accounts

Unlike Amazon Web Services that provides a [single IAM account](https://aws.amazon.com/iam/) for managing any user activity, Microsoft Azure uses different sets of credentials for backing up, storing and restoring data. See the following articles to learn more about the Role-Based Access Control \(RBAC\) used in the Azure portal:

* [Get started with Role-Based Access Control in the Azure portal](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#)

* [Use Role-Based Access Control to manage access to your Azure subscription resources](https://docs.microsoft.com/en-us/azure/active-directory/role-based-access-control-configure)

Each Azure subscription is associated with one [Azure Active Directory \(AD\)](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-whatis). Users, groups, and applications from that directory can manage resources in the Azure subscription. Microsoft provides two different types of accounts, both of which can be linked to an Azure AD:

* **Personal account **\(can be referred to as _"Microsoft account"_, formerly known as _"Windows Live ID"_\)
  This account is linked to an individual and is not supposed to change after changing one's job. Such accounts cannot access services outside of their respective Azure AD.
* **Work or school account** \(sometimes, it is also called an "_organizational account"_\)  
  This account is tied to your company and is used to manage access to your Office 365, Azure cloud, SharePoint, and other services. Furthermore, this account can belong to one of the following domains:

  * **A local domain**

  * **An Azure AD**

  > It is important to keep in mind that external Azure AD users can be [invited to an Azure AD from outside](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b). Please be informed that invited users may not have access to your Azure Virtual Machine account via CloudBerry products. You need to manually add a new to the Azure AD instead. Otherwise, an [error will occur on an attempt to authorize using such user's credentials](https://kb.cloudberry.online/microsoft-azure/sorry-but-were-having-trouble-signing-you-in.-we-received-a-bad-request.).



