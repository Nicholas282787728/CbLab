## Specify the Restore Options

On this wizard page, you can specify the options for restoring the database backup files.

![](/assets/restore-sql-db-backup-options.png)

First, you need to specify a destination folder for the restored files.

When restoring backup files from multiple databases, you can make the wizard automatically create a separate directory in the destination folder for each of these databases by enabling the corresponding option on this wizard page.

Finally, you need to specify a template for the restored backup file names. This template can include the following variables enclosed in the percent \(%\) symbol:

* **%DATABASENAME%**
* **%TYPE%**
* **%yyyy%**
* **%MM%**
* **%dd%**
* **%HH%**
* **%mm%**
* **%ss%**



