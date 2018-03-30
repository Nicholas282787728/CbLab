## Preparing a Bootable USB/ISO Image for Bare Metal Recovery

With CloudBerry Backup, you can create a bootable flash drive or create ISO image file for an emergency "bare metal" recovery in case of a system or hardware crash.

To create a recovery disk, switch to the **Home** tab of the CloudBerry Backup main menu and click the **Make Bootable USB** button.![](/assets/bare-metal-make-bootable-usb-menu.png)This invokes the **Create Recovery Disk** dialog window where you need to select a USB device or specify the ISO image file name for storing the recovery data.

![](/assets/bare-metal-make-bootable-usb-dialog.png)

> When selecting a USB device, please be informed that all information on it will be permanently lost after starting the disk creation process. Please backup all necessary information from the target USB device beforehand.

In addition, you can specify the following options:

* **Add CloudBerry Remote Assistant to the recovery disk**  
  This installs [CloudBerry Remote Assistant](https://www.cloudberrylab.com/remote-assistant.aspx)** **that will simplify the recovery process and provide you with additional features, such as ...

* **Protect the recovery disk with a master password**  
  We strongly recommend that you specify a password to protect the recovery drive against unauthorized access to any sensitive information that may be stored on it, such as ...

Next, you can install additional drivers to the recovery disk by specifying a folder where they are located.

> Use this option to be able to use this disk on a hardware configuration that is different from the current machine.

The specified folder must contain the required drivers in the INF file format \(EXE and other file types will be ignored\).

Most importantly, you need to add network drivers compatible with the target machine. Without such drivers, the boot disk will be unable to discover the network environment. A live network connection is required for recovery of a disk image from a network share, as well as for WinPE installation.

> Normally, the operation system automatically installs [Windows Preinstallation Environment \(WinPE\)](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/winpe-intro) in a dedicated [recovery partition](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference). If the recovery disk is unable to locate a WinPE image in this partition, it prompts you to download and install an appropriate version of [Windows Assessment and Deployment Kit \(Windows ADK\)](https://www.microsoft.com/en-us/download/details.aspx?id=39982) or [Windows Automated Installation Kit \(AIK\)](https://www.microsoft.com/en-us/download/details.aspx?id=5753) which in turn, will install WinPE as well.



### CloudBerry Boot Menu

Booting from a recovery USB device or ISO disk image file opens the CloudBerry Boot Menu.

![](/assets/cloudberry-boot-menu.png)

The following options are available in this menu:

* **Bare Metal Recovery** 
  Runs CloudBerry Backup where you can start the recovery process.

* **CloudBerry Remote Assistant**
  This option is available when [CloudBerry Remote Assistant](https://www.cloudberrylab.com/remote-assistant.aspx) is installed on the recovery disk.  
  It enables you to allow remote control over the current PC or take control over another computer remotely.

* **Tools**
  Provides various tools for configuring the restored machine. These tools include:

  * Microsoft Windows Command Prompt

  * Registry Editor

  * Save CloudBerry Backup application logs

### Troubleshooting







