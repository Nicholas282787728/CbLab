### Chaining Your Backups and Using Pre- And Post Actions

You can execute custom scripts before or after running the current backup task by enabling the following options in the Backup Wizard:

* **Pre-backup action**  
  Specifies the script to be executed before running the current task.

  > When you enable this option, you can choose whether to skip or continue the current task when this script's execution fails.

* **Post-backup action**  
  Specifies the script to be executed after running the current task.

  > When you enable this option, you can choose whether to execute this script only after successfully completing the current task, or regardless of the current task's execution result.



In addition, you can make the Backup Wizard automatically trigger the execution of another backup or restore plan after finishing the current backup task.

After enabling the "**Backup chain**" option, you can select a plan to execute and choose among the following two options:

* Execute the specified plan only after successfully completing the current task
* Execute the specified plan regardless of the current task's execution result

---

EXE, COM, BAT, CMD, PIF

For instance, you can run a script that turns off the computer when the backup plan completes executing.

Alternatively, you can run a script that disables all incoming connections during the plan execution.

