## 3.6 - Restore System State Data



**This feature is only available for Windows Server.**



![](/assets/restore-system-state-choice.png)

A system state backup includes essential data related to an operating system. A typical Windows system state backup contains the following data:

* Windows System Registry

* Performance Counter Configuration information

* Component Services Class registration database

* Boot and system files, including those protected by Windows File Protection \(WFP\)

* Configuration of system-dependent Microsoft applications, such as Certificate Services, Active Directory, and Internet Information Services \(IIS\)

A system state backup can protect you from configuration-dependent system faults \(such as BSOD errors\) and file or system registry corruption. Such backups are small in size and are quick to process.

> When restoring a system state, you cannot restore only some part of it because system state is always stored as a single object.



