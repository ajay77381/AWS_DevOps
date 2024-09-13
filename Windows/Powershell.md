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

 $start_timer = Get-Date
 Do {
    $current_time = Get-Date
    ping google.com -n 1 | Select-String "Reply" | foreach $_ { $a = Get-Date; $a.ToString() + " " + $_ } | Out-File -Append -Encoding UTF8 -FilePath  $log_file
    # normally the output of New-TimeSpan is a String but you need an Integer to be able to compare it
    $running_minutes = [int]((New-TimeSpan –Start $start_timer –End $current_time).minutes) 
    $running_seconds = [int]((New-TimeSpan –Start $start_timer –End $current_time).seconds) 
    Write-Output  "Running for: $($running_minutes)m:$($running_seconds)s" | Out-File -Append -Encoding UTF8 -FilePath  $log_file
 } Until ($running_minutes -ge $limit_in_minutes)
