## Specify the Target Databases

On this wizard page, you can choose whether to overwrite the existing databases with their restored versions and specify the names for the restored databases.

![](/assets/restore-sql-db-names-3.png)

You can select one of the default names when restoring system databases or specify a custom name on this wizard page.

The wizard will not be able to overwrite an existing database unless you explicitly enable the corresponding option. It will display the following error on such an attempt, prompting you to enable this option or specify another database name.

![](blob:https://www.gitbook.com/72ab3cd7-a4fd-44ec-9c17-7361da22ae01)

> Please be informed that this option affects all selected databases.
>
> The wizard will not be able to overwrite a "**master**" database.



