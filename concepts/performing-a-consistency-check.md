## Performing a Consistency Check



The backup files may be corrupted as a result of direct access to your cloud storage.

* The backup files may be corrupted due to the internal issue with the cloud storage provider.
* In the local backup scenario, the user may replace the disk or NAS device where the actual backup files absent

To ensure seamless recovery, implement regular proactive consistency checks.



Run OR Schedule

UI: Welcome tab of the 

![](/assets/backup-welcome-storage-accounts-run-consistency-check.png)

other \(schedule\)

![](/assets/consistency-check.png)

---

[https://cloudberry.gitbook.io/test/cloudberry-backup/miscellaneous/repository-sync](https://cloudberry.gitbook.io/test/cloudberry-backup/miscellaneous/repository-sync)

\[add cross-links to the Sync topic, and maybe "File tree troubleshooting"\]

sync is one-way

cons.check is two-way, history will list not found \(warning\) and added files \(green files\)

this list -&gt; history filter by files

..

sync kills and creates \(re init\)

..

if \(file name encr\){

specify password before cons.check

}

else {

files wuill be skipped}

..

can be scheduled \(unlike the sync\)

e.g. when push from different machines in a same prefix

..

c.c. cannot be executed during backup to this account occurs \(warning will be seen\)

..

c.c. performed one by one \(not simultaneously\)

..

