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

Most importantly, you need to add network drivers compatible with the target machine. Without such drivers, the boot disk will be unable to discover the network.



The boot disk will install [Windows Preinstallation Environment \(WinPE\)](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/winpe-intro) in a dedicated [recovery partition](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference) that is normally provisioned by the operating system installation.



The Windows Assessment and Deployment Kit \(ADK\) 



When recovering a volume that does not have



+

Windows installs the environment in recovery partitions

