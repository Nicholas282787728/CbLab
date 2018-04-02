## Preparing a Bootable USB/ISO Image for Bare Metal Recovery

With CloudBerry Backup, you can create a bootable USB drive or create ISO image file for an emergency "bare metal" recovery in case of a system or hardware crash.

> CloudBerry Backup runs under the Local System account by default. When running it under a user account, this user must be granted local administrator permissions to be able to make a recovery disk.

To create a recovery disk, switch to the **Home** tab of the CloudBerry Backup main menu and click the **Make Bootable USB** button.![](/assets/bare-metal-make-bootable-usb-menu.png)This invokes the **Create Recovery Disk** dialog window where you need to select a USB device or specify the ISO image file name for storing the recovery data.

![](/assets/bare-metal-make-bootable-usb-dialog.png)

> When selecting a USB device, please be informed that all information on it will be permanently lost after starting the disk creation process. Please backup all necessary information from the target USB device beforehand.

In addition, you can specify the following options:

* **Add CloudBerry Remote Assistant to the recovery disk**  
  This installs [CloudBerry Remote Assistant](https://www.cloudberrylab.com/remote-assistant.aspx) to enable remote access to the restored machine.

* **Protect the recovery disk with a master password**  
  We strongly recommend that you specify a password to protect the recovery drive against unauthorized access to any sensitive information that may be stored on it, such as password hashes stored for accessing your cloud accounts from the recovery disk.

## Installing Additional Drivers

Next, you can install additional drivers to the recovery disk by specifying a folder where they are located.

> Use this option to be able to use this disk on a hardware configuration that is different from the current machine.

The specified folder must contain the required drivers in the INF file format \(EXE and other file types will be ignored\).

Most importantly, you need to add network drivers compatible with the target machine. Without such drivers, the boot disk will be unable to discover the network environment. A live network connection is required for recovering a disk image from a cloud or network share.

> Normally, the operation system automatically installs [Windows Preinstallation Environment \(WinPE\)](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/winpe-intro) in a dedicated [recovery partition](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference). If CloudBerry Backup is unable to locate a WinPE image in this partition by the moment of creating a recovery disk, it prompts you to download and install an appropriate version of [Windows Assessment and Deployment Kit \(Windows ADK\)](https://www.microsoft.com/en-us/download/details.aspx?id=39982) or [Windows Automated Installation Kit \(AIK\)](https://www.microsoft.com/en-us/download/details.aspx?id=5753) which in turn, will install WinPE as well.

### Configuring a Network Share and Local Accounts

The recovery disk will include information about all accounts that are currently available in CloudBerry Backup and you will be able to restore a disk image from any of these accounts after booting from the recovery disk. The available accounts are listed in the application's main menu.

![](/assets/backup-app-main-menu-accounts.png)

To make it easier to restore a disk image from a network share, we recommend that you configure a corresponding network account before starting the recovery disk creation process.

To specify valid credentials so that the recovery disc is able to access the network share, switch to the Tools tab on the application's menu and click **Network Credentials**.

![](/assets/app-ribbon-tools-network-credentials.png)

When using a Local File system account, please keep in mind that the recovery disk might change the drive letter in the path string. To configure the local account after booting from the recovery disk, run CloudBerry Backup from the boot disk and click **File \| Edit Accounts**. In the **Registered Accounts** dialog, select your disk storage account and click **Edit**.

![](/assets/boot-disk-backup-edit-accounts.png)

test



### Configuring BIOS Settings

When booting from a recovery disk, you might need to customize some of the BIOS settings to make sure that the recovery disk configuration matches that of both the current PC and source PC on which the recovery disk was created, so that the recovery disk is able to load its operating system.

For example, you might not be able to restore a disk image unless the SATA configuration of the current PC matches that of a computer on which the recovery disk was created.

### CloudBerry Boot Menu

Booting from a recovery USB device or ISO disk image file opens the **CloudBerry Boot Menu**.

![](/assets/cloudberry-boot-menu.png)

This menu provides the following options:

* **Bare Metal Recovery**  
  Runs CloudBerry Backup where you can start the recovery process.

* **CloudBerry Remote Assistant**  
  This option is available when [CloudBerry Remote Assistant](https://www.cloudberrylab.com/remote-assistant.aspx) is installed on the recovery disk.  
  It enables you to allow remote control over the current PC or take control over another computer remotely.

* **Tools**  
  Provides various tools for configuring the restored machine. These tools include:

  * [Microsoft Windows Command Prompt](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)

    > See the [Command Line Interface](https://help.cloudberrylab.com/cloudberry-backup/miscellaneous/command-line-interface) for an overview of the native CloudBerry commands.

  * [Registry Editor](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-6.0/aa243964%28v=vs.60%29)

  * Save CloudBerry Backup application logs

### Changing the Virtual Disk Size

Upon loading, the recovery disk creates a virtual drive in the PC memory \(this drive is assigned the letter **X**\).

The virtual disk size varies depending on the operating system family and generally, it does not exceed **512 **MB.

This virtual disk is used to contain a repository storing the image-related data. Every time you boot from the restore disk, this repository is created from scratch.

When you are required to store an increased amount of image-related information, the repository might exceed the virtual disk size, which results in an error and the failure of the recovery process. To avoid this, you can check the required repository size before starting the recovery disk creation process by switching to the **Tools** tab of the application menu and clicking the **Options** button.

![](/assets/app-ribbon-tools-options.png)

This invokes the **Options **dialog window where you can switch to the **Repository **tab indicating the current database size.

![](/assets/backup-options-repository.png)

If it exceeds **512 **MB, you can shrink and/or relocate the repository.

**\[Or this can be done post factum, after the boot using CLI?  
As in "Moving repository file \(CBBackup.db\) to alternative location" at **[https://help.cloudberrylab.com/cloudberry-backup/miscellaneous/command-line-interface\](https://help.cloudberrylab.com/cloudberry-backup/miscellaneous/command-line-interface\)**\]**

### Troubleshooting

**Problem:**  
The boot disk cannot discover the network.

**Possible solution \(our favorite one\):**  
Ensure that the network cable connecting the computer to the network is working.

Upon booting from a recovery disk, you can check the network access by running the "**ipconfig**" command in the **Command Prompt** that is available in the **Tools** category of the **CloudBerry Boot Menu** \(see the **CloudBerry Boot Menu** section of this document for more information\).

![](/assets/boot-menu-command-prompt.png)

---

**Problem:**  
When restoring a disk image from Amazon S3, the following error occurs: _"The clock is not synchronized."_

**Solution:**  
On the **CloudBerry Boot Menu**, switch to **Tools** and press **T** to synchronize the local and network clocks.

---

**Problem:**  
The disk image is not found.

**Possible solution:**  
Try changing the [backup prefix](/concepts/changing-the-backup-prefix.md) to make it match the name of a computer on which the disk image was created.

---

**Problem:**  
When trying to log in to the CloudBerry agent, the following error occurs: _"The remote name could not be resolved: '_[_mspbackups.com_](http://mspbackups.com/)_'"._

**Possible solution:**  
This error may occur if the IP address configuration is missing, for example when the machine is located in a network without a DHCP server. See the following Knowledge Base article for more information: [KB 1082](https://kb.cloudberrylab.com/kb1082/).

---

**Problem: **  
On an attempt to restore a disk image using a recovery USB device, the following error occurs: _"A connection to the deployment share could not be made. The following networking device did not have a driver installed."_

**Possible solution:**  
The reason for this error may be a missing network device driver or some failure during the import of drivers. See the following Knowledge Base article for more information: [KB: 1081](https://kb.cloudberrylab.com/kb1081/).

