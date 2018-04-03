## Select Files to Restore

On this wizard page, you can select which files you need to restore.

![](/assets/ms-exchange-restore-source.png)

> When restoring a backup that was made on another computer, you may need to [synchronize the repository](/concepts/syncing-your-repository.md) to refresh the file tree.

When restoring Microsoft Exchange 2010 data, you can restore individual files instead of restoring the complete server database. 

The wizard does not allow restoring Microsoft Exchange data directly to the database. You will need to dismount your current Microsoft Exchange database, manually replace the required files with their restored versions and mount the database back on the server.

See [Item Level Restore](/concepts/microsoft-exchange-item-level-restore.md) for more information.



> When restoring Microsoft Exchange Server 2007 data, you might encounter the following error on this wizard page: "Connecting to remote server failed." See the following Knowledge Base article for more information: [KB 1050](https://kb.cloudberrylab.com/kb1050/).



