New-Item cmdlet is used to create a directory by passing the path using -Path as path of the directory and -ItemType as Directory.

## In this example, we'll create a folder in D:\Temp\ with name "Test Folder"

``
New-Item -Path 'D:\temp\Test Folder' -ItemType Directory
``
### In this example, we'll create a file in D:\Temp\Test Folder with name "Test File.txt"
Type the following command in PowerShell ISE Console

``New-Item -Path 'D:\temp\Test Folder\Test File.txt' -ItemType File
``
