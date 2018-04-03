## Update the Exchange Server Database

CloudBerry Backup cannot restore Microsoft Exchange files directly to the Exchange Server database. After restoring the database files, you need to dismount a corresponding Exchange database, manually replace the required files with their restored versions and mount the database back on the server.

> A user must be granted appropriate permissions to be able to access and modify a Microsoft Exchange database.

Launch the [Exchange Management Console](https://msdn.microsoft.com/en-us/library/cc505909.aspx) to replace older files with their restored versions in a Microsoft Exchange database.

First, you need to dismount the required database.![](/assets/restore-exchange-dismount.png)Right-click the database once again and select **Move Database Path** in the context menu that is invoked.

Specify new locations for the EDB database files and logs and click **Move**.

that you need to update \(under the "**Database File Path**" and "**Log Folder Path**" columns, respectively\)![](/assets/restore-exchange-console-locate-logs.png)

Move these files to another location or delete them if they are no longer required.![](/assets/restore-exchange-console-move-logs.png)

Open the folder containing the restored files and manually copy them to the destination folders \(corresponding to the "**Database File Path**" and "**Log Folder Path**" settings of the Microsoft Exchange Server\).![](/assets/restore-exchange-open-folder.png)

Finally, mount the database back on the Microsoft Exchange server to apply the changes.![](/assets/restore-exchange-mount.png)

