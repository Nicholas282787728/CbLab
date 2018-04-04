### Chaining Your Backups and Using Pre- And Post Actions

This article describes how to make CloudBerry Backup execute custom scripts before and/or after running a backup task and chain multiple backup tasks for their sequential execution.

### Executing Custom Scripts

You can execute custom scripts before or after running the current backup task by enabling the following options in the Backup Wizard:

* **Pre-backup action**  
  Specifies the script to be executed before running the current task.

  > When you enable this option, you can choose whether to skip or continue the current task when this script's execution fails.

* **Post-backup action**  
  Specifies the script to be executed after running the current task.

  > When you enable this option, you can choose whether to execute this script only after successfully completing the current task, or regardless of the current task's execution result.

Your script can be stored in an EXE, COM, BAT, CMD, or PIF file.

Unless you specified an absolute path to the script file, it is searched for in the "C:\Windows\System32" directory.

When you need to launch an EXE file, please make sure that it can be properly executed in the CloudBerry Backup application's context. In particular, CloudBerry Backup will only be able to execute EXE files that do not provide graphical user interface and are closed after their execution.

For example, CloudBerry Backup will not be able to execute following script...

```
cmd.exe /F:ON
```

... and you need to execute this command with the "/C" parameter, as follows:

```
cmd.exe /F:ON /C
```



You can specify powershell scripts



We recommend that you perform a test run for the created backup plan to ensure that CloudBerry Backup can properly execute the specified scripts.





### Chaining Your Backups

In addition, you can make the Backup Wizard automatically trigger the execution of another backup or restore plan after finishing the current backup task.

After enabling the "**Backup chain**" option, you can select a plan to execute and choose among the following two options:

* Execute the specified plan only after successfully completing the current task
* Execute the specified plan regardless of the current task's execution result

---



For instance, you can run a script that turns off the computer when the backup plan completes executing.

Alternatively, you can run a script that disables all incoming connections during the plan execution.

