# AzureManagedDisk

| Type | Description | Managed | Max Capacity | Lifecycle |
| :--- | :--- | :--- | :--- | :--- |
| OS Disk | A data disk is a managed disk that's attached to a virtual machine to store application data, or other data you need to keep. Data disks are registered as SCSI drives and are labeled with a letter that you choose. The size of the virtual machine determines how many data disks you can attach to it and the type of storage you can use to host the disks. | True | 4TB | By default the OS disk is set to Delete with VM. If you don't want to delete the OS disk, clear the checkbox.<br> ![delete-disk.png](https://github.com/developer-onizuka/AzureManagedDisk/blob/main/delete-disk.png)|
