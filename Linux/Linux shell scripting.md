

`ls -ltr 
`
This commond is use to show the file and directory and who is the owner of file and when file created. It show the the file with time stamp.We can list the file and folder with its properties.


`touch
`
For create file we can use touch commond -

touch file name

`Vi
`
For creating file and editing
`

`vim
`

It is advance version of vi 


`rm 
`
For removing the file 

`rm -r
`
For removing directory 

`free -g
`
For what is the memory of your laptop

`nproc
`
To see the number of CPU in your laptop / desktop

`df -h
`
To see the disk size in system 

`top
`
To see the all details- like cpu, memory, and memory useges etc.

`cat
`
To read the content of file

How we can run the script ?
 sh scriptname or ./scriptname

 `chmod
 `
 is the commond that grants permission.

 `chmod 777 filename
 `
 chmode grantes the permission in three category
 1- what is the permission of root user
 2- what is the permission of group
 3- what is the permssion of you

 it use 4 2 1 formul
  4 is for write 
  2 is for read
  1 is for executive

  `mkdir
  `
  To make the directory

Below is the sample script 

  #!/bin/bash
# create a folder
mkdir ajaycloud
# create two file
cd ajaycloud
touch firstfile secondfile

Why we use shell scripting ?

suppose- i am a devops engineer and i have to manage 100 server so what i can do i'll write a simple shell script who help me to monitor the vm. Like- memory utilization, CPU utilization, HdD utilization.

If someone ask there are many monitoring tool why you use scrip to do this- we can say we don't use such type of monitoring tool.

`set -x
`
commond is use to debuginging mode
like- below-

``
ajay@DESKTOP-M8NEQM2:~/linux$ vi nodehealth.sh
ajay@DESKTOP-M8NEQM2:~/linux$ ./nodehealth.sh
+ df -h
Filesystem      Size  Used Avail Use% Mounted on
none            1.9G     0  1.9G   0% /usr/lib/modules/5.15.167.4-microsoft-standard-WSL2
none            1.9G  4.0K  1.9G   1% /mnt/wsl
drivers         136G   67G   70G  49% /usr/lib/wsl/drivers
/dev/sdc       1007G  4.0G  952G   1% /
none            1.9G   80K  1.9G   1% /mnt/wslg
none            1.9G     0  1.9G   0% /usr/lib/wsl/lib
rootfs          1.9G  2.2M  1.9G   1% /init
none            1.9G  796K  1.9G   1% /run
none            1.9G     0  1.9G   0% /run/lock
none            1.9G     0  1.9G   0% /run/shm
tmpfs           4.0M     0  4.0M   0% /sys/fs/cgroup
none            1.9G   76K  1.9G   1% /mnt/wslg/versions.txt
none            1.9G   76K  1.9G   1% /mnt/wslg/doc
C:\             136G   67G   70G  49% /mnt/c
D:\              39G   17G   23G  43% /mnt/d
E:\              64G   23G   42G  35% /mnt/e
snapfuse        128K  128K     0 100% /snap/bare/5
snapfuse         74M   74M     0 100% /snap/core22/1663
snapfuse         92M   92M     0 100% /snap/gtk-common-themes/1535
snapfuse         45M   45M     0 100% /snap/snapd/23258
snapfuse         74M   74M     0 100% /snap/core22/1722
snapfuse        132M  132M     0 100% /snap/ubuntu-desktop-installer/1286
snapfuse        132M  132M     0 100% /snap/ubuntu-desktop-installer/1276
snapfuse         39M   39M     0 100% /snap/snapd/21759
+ free -g
               total        used        free      shared  buff/cache   available
Mem:               3           0           3           0           0           3
Swap:              1           0           1
+ nproc

``
