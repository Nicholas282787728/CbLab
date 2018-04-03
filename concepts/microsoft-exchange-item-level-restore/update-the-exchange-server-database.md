## Update the Exchange Server Database

CloudBerry Backup cannot restore Microsoft Exchange files directly to the Exchange Server database. After restoring the database files, you need to dismount a corresponding Exchange database, manually replace the required files with their restored versions and mount the database back on the server.

> A user must be granted appropriate permissions to be able to access and modify a Microsoft Exchange database.

Launch the [Exchange Management Console](https://msdn.microsoft.com/en-us/library/cc505909.aspx) to replace older files with their restored versions in a Microsoft Exchange database.

First, you need to dismount the required database.![](/assets/restore-exchange-dismount.png)Right-click the database once again and select **Move Database Path** in the context menu that is invoked.

Copy the locations for the database file and its logs.

![](/assets/restore-exchange-database-path.png)

Locate this files on the computer and relocate them, or delete if they are no longer required.

Open the folder containing the restored files and manually copy them to the destination folders \(corresponding to the "**Database File Path**" and "**Log Folder Path**" settings of the Microsoft Exchange Server\).

Mount the database back on the Microsoft Exchange server to apply the changes.

![](/assets/restore-exchange-mount-2.png)

