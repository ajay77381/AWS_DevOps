

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
