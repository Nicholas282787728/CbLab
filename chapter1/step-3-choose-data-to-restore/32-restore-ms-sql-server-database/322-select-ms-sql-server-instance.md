## 3.2.2 - Select MS SQL Server Instance

On this wizard page, you can select a SQL Server instance to which to restore the database.

![](/assets/restore-sql-server-instance-2.png)

You need to specify the following main settings on this wizard page:

* **SQL Server Instance**  
  Specifies the SQL Server instance to which to restore your database.

* **Authentication**  
  Specifies the authentication mode to use for connecting to SQL Server. The following modes are available:

  * **Windows Authentication**
    Uses Windows credentials of the current user to connect to SQL Server.
  * **SQL Server Authentication**  
    Connects to SQL Server using the specified credentials.  
    **You can save this password in the CloudBerry Backup configuration file by enabling the corresponding option.**

    > The selected authentication mode [should be enabled in SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/security/choose-an-authentication-mode).

In addition, you can enable the following options on this wizard page:

* Check if the specified account has necessary permissions to perform the restore operation  
  Enable this option to make the wizard automatically check whether the specified user account has all necessary permissions to restore the database.

  > The user must be assigned the [sysadmin](https://docs.microsoft.com/en-us/sql/reporting-services/security/role-definitions-create-delete-or-modify) role in SQL Server.

* Use secure connection \(SSL/TLS\)  
  Use this option to select whether you need to secure an encrypted SSL/TLS connection between the database server and CloudBerry Backup.

  The SQL Server instance must have a corresponding certificate installed, which becomes automatically trusted by the CloudBerry client application. See the following article for more information: [How to enable SSL encryption for an instance of SQL Server by using Microsoft Management Console](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-mi).



