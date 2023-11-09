# AzureManagedDisk

| Type | Description | Persistence | Max Capacity | Storage Lifecycle on VMs | Target Device |
| :--- | :--- | :--- | :--- | :--- | :--- |
| OS Disk | Every virtual machine has one attached operating system disk. That OS disk has a pre-installed OS, which was selected when the VM was created. This disk contains the boot volume. | Yes | 4TB | **By default the OS disk is set to Delete with VM.** If you don't want to delete the OS disk, clear the checkbox.<br> ![delete-disk.png](https://github.com/developer-onizuka/AzureManagedDisk/blob/main/delete-disk.png)| RAID Array |
| Data Disk | A data disk is a managed disk that's attached to **a virtual machine to store application data, or other data you need to keep**. Data disks are registered as SCSI drives and are labeled with a letter that you choose.<br> The size of the virtual machine determines how many data disks you can attach to it and the type of storage you can use to host the disks. | Yes | 64TB<br>(Premium SSD v2) | If you choose Create and attach a new disk, the Create a new disk page opens and you can select whether to delete the disk when you delete the VM.<br> ![delete-data-disk.png](https://github.com/developer-onizuka/AzureManagedDisk/blob/main/delete-data-disk.png)| RAID Array |
| Temporary Disk | Most VMs contain a temporary disk, which is not a managed disk. The temporary disk provides short-term storage for applications and processes, and is intended to only store data such as page files, swap files, or SQL Server tempdb. **Data on the temporary disk may be lost during a maintenance event, when you redeploy a VM, or when you stop the VM.** | No | The size of the temporary disk varies, based on the size of the virtual machine (and it’s available physical memory). | On Azure Linux VMs, the temporary disk is typically **/dev/sdb** and on Windows VMs the temporary disk is **D:** by default. | Internal Disk |

> https://learn.microsoft.com/en-us/azure/virtual-machines/delete?tabs=portal2%2Ccli3%2Cportal4%2Cportal5 <br>
> https://learn.microsoft.com/en-us/azure/virtual-machines/azure-vms-no-temp-disk <br>
> https://learn.microsoft.com/en-us/azure/virtual-machines/managed-disks-overview <br>
> https://az-start.com/vm-cost-management/ <br>
> https://azure.microsoft.com/ja-jp/pricing/details/managed-disks/ <br>
