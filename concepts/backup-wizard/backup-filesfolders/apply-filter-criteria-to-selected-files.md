## Apply Filter Criteria to Selected Files

On this wizard page, you can define various criteria based on which a backup service should select files to upload to your backup destination.

![](/assets/backup-wizard-files-advanced-filter.png)

You can specify the following criteria on this page:

* Select the file types to include in your backup.  
  You can choose whether to back up all files in the selected folders, as well as specify a "white" or "black" list for the file types to include in the backup.

  In addition, you can specify whether the backup should include system, hidden and locked files contained in the selected folders.

* Select the folders to exclude from your backup.  
  You can specify whether to back up empty folders and list folders that you do not need to include in the backup.

* Specify the time period within which the files should have been modified to be included in your backup.
  You can make the backup only include files that were modified earlier that a certain number of days.
  For example, setting this value to **14** days will only back up files that were modified earlier than two weeks ago.

  In addition, you can make the backup only include files that were modified after a certain date and time.  
  For example, setting this value to **12/31/2009 23:59** will only back up files that were modified since the beginning of year **2010**.

* Specify the maximum size for the files included in your backup.
  You can avoid backing up files exceeding a certain size.



