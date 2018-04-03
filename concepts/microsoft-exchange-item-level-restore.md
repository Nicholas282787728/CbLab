## Microsoft Exchange - Item Level Restore

When restoring Microsoft Exchange 2010 data, you can restore individual files instead of restoring the complete server database.

To restore individual items from a Microsoft Exchange Server database, switch to the **Backup Storage** tab in your CloudBerry Backup application, select the required database and right-click a corresponding full backup. Select **Item Level Restore** in the context menu that is invoked.

![](/assets/restore-exchange-item-level-storage-2.png)

This invokes a dialog prompting you whether to apply logs to the opened Exchange database.

![](/assets/restore-exchange-item-level-logs-dialog.png)

After CloudBerry Backup has processed the backup data, the **Echange Item Level Restore** window is invoked where you can explore the Microsoft Exchange database and locate the required items.![](/assets/restore-exchange-item-level-window.png)Clicking a item invokes a context menu in which you can click **Restore** to restore the corresponding item to a required destination.

![](/assets/restore-exchange-item-level-email-restore.png)

> Use the "**Send to support**" option to send the meta information to our Support Team if for any reason, the item's content is displayed incorrectly.

Next, you need to specify the Exchange server, user email and credentials, as well as choose a folder to which to restore the selected item.

![](/assets/restore-exchange-item-level-email-restore-dialog.png)



**\[User permissions \(management roles\)...\]**

CloudBerry Backup cannot restore Microsoft Exchange data directly to the database. After restoring the files, you will need to dismount a corresponding Exchange database, manually replace the required files with their restored versions and mount the database back on the server.

Launch the **Exchange Management Console** to put the restored items to the Microsoft Exchange database.

First, you need to dismount the corresponding database.

![](/assets/restore-exchange-console-dismount.png)

Next, locate the EDB database files and logs that you need to update \(in the "**Database File Path**" and "**Log Folder Path**" columns, respectively\)![](/assets/restore-exchange-console-locate-logs.png)

Move these files to another location or delete them if they are no longer required.![](/assets/restore-exchange-console-move-logs.png)

Open the folder containing the restored files and manually copy them to the destination folders \(corresponding to the "**Database File Path**" and "**Log Folder Path**" settings of the Microsoft Exchange Server\).![](/assets/restore-exchange-open-folder.png)

Finally, mount the database back on the Microsoft Exchange server to apply the changes.![](/assets/restore-exchange-mount.png)

