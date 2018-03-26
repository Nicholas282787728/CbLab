## **3.4.5 - Specify the Destination Disk Capacity**

After switching to the next wizard page, you can specify the capacity of the destination disk.

![](/assets/ami-destination-capacity.png)

The wizard indicates the minimum and maximum capacity value, where the minimum size is the total target size for all selected partitions on the previous step.

* Volume / disk capacity:
* previous step we calculate the volume size

volumes are on disks and their sum is limited by the disk size



MBR: disk cannot be more than 2 TB

\[cloud services limit this: 2 TB for instance and 4 TB for data disk\]



upper limit on the disk size \(dynamically changes in "Resizing NTFS" doc\)

ask Slava Bukhtiyarov



Be aware \(when restoring virtual disks and we don't impose upper limits\):

Windows MBR section cannot be more than 2 TB

If you resize your MBR partition on a data disc,  Learn about MBR volume limitations \(and clusters\) in MS docs

















