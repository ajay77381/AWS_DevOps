New-Item cmdlet is used to create a directory by passing the path using -Path as path of the directory and -ItemType as Directory.

## In this example, we'll create a folder in D:\Temp\ with name "Test Folder"

``
New-Item -Path 'D:\temp\Test Folder' -ItemType Directory
``
### In this example, we'll create a file in D:\Temp\Test Folder with name "Test File.txt"
Type the following command in PowerShell ISE Console

``New-Item -Path 'D:\temp\Test Folder\Test File.txt' -ItemType File
``

For show the version of powershell-

``PSVersionTable
``
For show the running and stopped service?

``Get-Service
``

## powershell ping continous for specific duration and save log
 # 1 minute
 $limit_in_minutes = 1
 # path to log
 $log_file = '<path_to_log>\time.log'
 # clear the log file before running again
 fc > $log_file

````
 $start_timer = Get-Date
 Do {
    $current_time = Get-Date
    ping google.com -n 1 | Select-String "Reply" | foreach $_ { $a = Get-Date; $a.ToString() + " " + $_ } | Out-File -Append -Encoding UTF8 -FilePath  $log_file
    # normally the output of New-TimeSpan is a String but you need an Integer to be able to compare it
    $running_minutes = [int]((New-TimeSpan –Start $start_timer –End $current_time).minutes) 
    $running_seconds = [int]((New-TimeSpan –Start $start_timer –End $current_time).seconds) 
    Write-Output  "Running for: $($running_minutes)m:$($running_seconds)s" | Out-File -Append -Encoding UTF8 -FilePath  $log_file
 } Until ($running_minutes -ge $limit_in_minutes)

`````

1.1. What is PowerShell?

- PowerShell is a command-line shell.
- PowerShell is a scripting environment.
- PowerShell is an automation engine.

These are all part of the answer. We prefer to say PowerShell is a tool you can use to manage your Microsoft-based machines and applications that programs consistency into your management process. The tool is attractive to administrators and developers in that it can span the range of command line, simple and advanced scripts, to real programs.

 Basic expressions and variables
``PS> 2+2
``
4

Notice as soon as you typed the expression, the result was calculated and displayed. It wasn’t necessary to use any kind of print statement to display the result. It’s important to remember whenever an expression is evaluated, the result of the expression is output, not discarded. PowerShell supports most of the basic arithmetic operations you’d expect, including floating point.

PS> (2+2)*3/7 > c:\foo.txt
PS> Get-Content c:\foo.txt
1.71428571428571

Saving expressions into files is useful; saving them in variables is more useful:

PS> $n = (2+2)*3
PS> $n
12

PS> $n / 7
1.71428571428571


https://www.youtube.com/watch?v=BVzKmZT7z_o&list=PLcj5HCtrio7Ep6tfPNxhACkCEuCMZe95x



Powershell


Rename-NetAdapter -Name Ethernet -NewName eh


To know the interface name-

Get-NetAdapter 

Assign ip address by powershell-

New-NetIPAddress -InterfaceIndex 15 -IPAddress 10.0.0.40 -PrefixLength 8 -DefaultGateway 10.0.0.0


 




