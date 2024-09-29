
Powershell syntex-

![image](https://github.com/user-attachments/assets/3bc723d5-ed35-43ab-a573-f1cb4e43a287)

As-
 Get-Service -Name "Bits"

Even i don't give name, i would be able to see the output.
like- 

PS C:\Users\test> Get-Service


Status   Name               DisplayName
------   ----               -----------
Stopped  AarSvc_685fdf4     Agent Activation Runtime_685fdf4

Running  AdobeARMservice    Adobe Acrobat Update Service

Stopped  AJRouter           AllJoyn Router Service

Stopped  ALG                Application Layer Gateway Service

Stopped  AppIDSvc           Application Identity

Running  Appinfo            Application Information

Stopped  AppMgmt            Application Management

Stopped  AppReadiness       App Readiness

Stopped  AppVClient         Microsoft App-V Client

Running  AppXSvc            AppX Deployment Service (AppXSVC)

Stopped  AssignedAccessM... AssignedAccessManager Service

Running  AudioEndpointBu... Windows Audio Endpoint Builder

Running  Audiosrv           Windows Audio

- What will happen if we add the name. We'll be able to know about a particular service.

- If we want to know, what are the other command related to get then we can use below command to know?

Get-Command -Name "Get-Service" -Syntax

PS C:\Users\test> Get-Command -Name "Get-Service" -Syntax

Get-Service [[-Name] <string[]>] [-ComputerName <string[]>] [-DependentServices] [-RequiredServices] [-Include <string[]>] [-Exclude <string[]>] [<CommonParameters>]

Get-Service -DisplayName <string[]> [-ComputerName <string[]>] [-DependentServices] [-RequiredServices] [-Include <string[]>] [-Exclude <string[]>] [<CommonParameters>]

Get-Service [-ComputerName <string[]>] [-DependentServices] [-RequiredServices] [-Include <string[]>] [-Exclude <string[]>] [-InputObject <ServiceController[]>] [<CommonParameters>]

PS C:\Users\test>

As we are able to see dual square bracket it mean that are optional. As we call positonal parameter such as prameter and these come alway in first.



- If we want to know how many 
PS C:\Users\test> Get-Command -Noun "Service"

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Cmdlet          Get-Service                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          New-Service                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Restart-Service                                    3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Resume-Service                                     3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Set-Service                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Start-Service                                      3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Stop-Service                                       3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Suspend-Service                                    3.1.0.0    Microsoft.PowerShell.Management


PS C:\Users\test>

If we want to know how many commands are available in which copy come in ver then we can use below commands-


PS C:\Users\test> Get-Command -Verb "Copy"

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Function        Copy-NetFirewallRule                               2.0.0.0    NetSecurity
Function        Copy-NetIPsecMainModeCryptoSet                     2.0.0.0    NetSecurity
Function        Copy-NetIPsecMainModeRule                          2.0.0.0    NetSecurity
Function        Copy-NetIPsecPhase1AuthSet                         2.0.0.0    NetSecurity
Function        Copy-NetIPsecPhase2AuthSet                         2.0.0.0    NetSecurity
Function        Copy-NetIPsecQuickModeCryptoSet                    2.0.0.0    NetSecurity
Function        Copy-NetIPsecRule                                  2.0.0.0    NetSecurity
Cmdlet          Copy-Item                                          3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Copy-ItemProperty                                  3.1.0.0    Microsoft.PowerShell.Management





PS C:\Users\test> Get-Command -Noun "Service"

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Cmdlet          Get-Service                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          New-Service                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Restart-Service                                    3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Resume-Service                                     3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Set-Service                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Start-Service                                      3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Stop-Service                                       3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Suspend-Service                                    3.1.0.0    Microsoft.PowerShell.Management


PS C:\Users\test>

- If i want to see the all alias then we can use below commands.

  
PS C:\Users\test> Get-Command -CommandType "Alias"

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Alias           % -> ForEach-Object
Alias           ? -> Where-Object
Alias           ac -> Add-Content
Alias           Add-AppPackage                                     2.0.1.0    Appx
Alias           Add-AppPackageVolume                               2.0.1.0    Appx
Alias           Add-AppProvisionedPackage                          3.0        Dism
Alias           Add-ProvisionedAppPackage                          3.0        Dism
Alias           Add-ProvisionedAppxPackage                         3.0        Dism
Alias           Add-ProvisioningPackage                            3.0        Provisioning
Alias           Add-TrustedProvisioningCertificate                 3.0        Provisioning
Alias           algm ->                                            1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           Apply-WindowsUnattend                              3.0        Dism
Alias           asnp -> Add-PSSnapin
Alias           blsmba ->                                          2.0.0.0    SmbShare
Alias           cat -> Get-Content
Alias           cd -> Set-Location
Alias           CFS -> ConvertFrom-String                          3.1.0.0    Microsoft.PowerShell.Utility
Alias           chdir -> Set-Location
Alias           clc -> Clear-Content
Alias           clear -> Clear-Host
Alias           clhy -> Clear-History
Alias           cli -> Clear-Item
Alias           clp -> Clear-ItemProperty
Alias           cls -> Clear-Host
Alias           clv -> Clear-Variable
Alias           cmpcfg ->                                          1.1        PSDesiredStateConfiguration
Alias           cnsn -> Connect-PSSession
Alias           compare -> Compare-Object
Alias           copy -> Copy-Item
Alias           cp -> Copy-Item
Alias           cpi -> Copy-Item
Alias           cpp -> Copy-ItemProperty
Alias           cssmbo ->                                          2.0.0.0    SmbShare
Alias           cssmbse ->                                         2.0.0.0    SmbShare
Alias           curl -> Invoke-WebRequest
Alias           cvpa -> Convert-Path
Alias           dbp -> Disable-PSBreakpoint
Alias           del -> Remove-Item
Alias           diff -> Compare-Object
Alias           dir -> Get-ChildItem
Alias           Disable-PhysicalDiskIndication                     2.0.0.0    Storage
Alias           Disable-StorageDiagnosticLog                       2.0.0.0    Storage
Alias           Dismount-AppPackageVolume                          2.0.1.0    Appx
Alias           dlu ->                                             1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           dnsn -> Disconnect-PSSession
Alias           dsmbd ->                                           2.0.0.0    SmbShare
Alias           ebp -> Enable-PSBreakpoint
Alias           echo -> Write-Output
Alias           elu ->                                             1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           Enable-PhysicalDiskIndication                      2.0.0.0    Storage
Alias           Enable-StorageDiagnosticLog                        2.0.0.0    Storage
Alias           epal -> Export-Alias
Alias           epcsv -> Export-Csv
Alias           epsn -> Export-PSSession
Alias           erase -> Remove-Item
Alias           esmbd ->                                           2.0.0.0    SmbShare
Alias           etsn -> Enter-PSSession
Alias           exsn -> Exit-PSSession
Alias           fc -> Format-Custom
Alias           fhx -> Format-Hex                                  3.1.0.0    Microsoft.PowerShell.Utility
Alias           fimo ->                                            1.0.0.1    PowerShellGet
Alias           fl -> Format-List
Alias           Flush-Volume                                       2.0.0.0    Storage
Alias           foreach -> ForEach-Object
Alias           ft -> Format-Table
Alias           fw -> Format-Wide
Alias           gal -> Get-Alias
Alias           gbp -> Get-PSBreakpoint
Alias           gc -> Get-Content
Alias           gcai ->                                            1.0.0.0    CimCmdlets
Alias           gcb -> Get-Clipboard                               3.1.0.0    Microsoft.PowerShell.Management
Alias           gcfg ->                                            1.1        PSDesiredStateConfiguration
Alias           gcfgs ->                                           1.1        PSDesiredStateConfiguration
Alias           gci -> Get-ChildItem
Alias           gcim ->                                            1.0.0.0    CimCmdlets
Alias           gcls ->                                            1.0.0.0    CimCmdlets
Alias           gcm -> Get-Command
Alias           gcms ->                                            1.0.0.0    CimCmdlets
Alias           gcs -> Get-PSCallStack
Alias           gdr -> Get-PSDrive
Alias           Get-AppPackage                                     2.0.1.0    Appx
Alias           Get-AppPackageDefaultVolume                        2.0.1.0    Appx
Alias           Get-AppPackageLastError                            2.0.1.0    Appx
Alias           Get-AppPackageLog                                  2.0.1.0    Appx
Alias           Get-AppPackageManifest                             2.0.1.0    Appx
Alias           Get-AppPackageVolume                               2.0.1.0    Appx
Alias           Get-AppProvisionedPackage                          3.0        Dism
Alias           Get-DiskSNV                                        2.0.0.0    Storage
Alias           Get-Language                                       1.0        LanguagePackManagement
Alias           Get-PhysicalDiskSNV                                2.0.0.0    Storage
Alias           Get-PreferredLanguage                              1.0        LanguagePackManagement
Alias           Get-ProvisionedAppPackage                          3.0        Dism
Alias           Get-ProvisionedAppxPackage                         3.0        Dism
Alias           Get-StorageEnclosureSNV                            2.0.0.0    Storage
Alias           Get-SystemLanguage                                 1.0        LanguagePackManagement
Alias           ghy -> Get-History
Alias           gi -> Get-Item
Alias           gin -> Get-ComputerInfo                            3.1.0.0    Microsoft.PowerShell.Management
Alias           gip ->                                             1.0.0.0    NetTCPIP
Alias           gjb -> Get-Job
Alias           gl -> Get-Location
Alias           glcm ->                                            1.1        PSDesiredStateConfiguration
Alias           glg ->                                             1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           glgm ->                                            1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           glu ->                                             1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           gm -> Get-Member
Alias           gmo -> Get-Module
Alias           gp -> Get-ItemProperty
Alias           gps -> Get-Process
Alias           gpv -> Get-ItemPropertyValue
Alias           group -> Group-Object
Alias           grsmba ->                                          2.0.0.0    SmbShare
Alias           gsmba ->                                           2.0.0.0    SmbShare
Alias           gsmbb ->                                           2.0.0.0    SmbShare
Alias           gsmbc ->                                           2.0.0.0    SmbShare
Alias           gsmbcc ->                                          2.0.0.0    SmbShare
Alias           gsmbcn ->                                          2.0.0.0    SmbShare
Alias           gsmbd ->                                           2.0.0.0    SmbShare
Alias           gsmbgm ->                                          2.0.0.0    SmbShare
Alias           gsmbm ->                                           2.0.0.0    SmbShare
Alias           gsmbmc ->                                          2.0.0.0    SmbShare
Alias           gsmbo ->                                           2.0.0.0    SmbShare
Alias           gsmbs ->                                           2.0.0.0    SmbShare
Alias           gsmbsc ->                                          2.0.0.0    SmbShare
Alias           gsmbscm ->                                         2.0.0.0    SmbShare
Alias           gsmbse ->                                          2.0.0.0    SmbShare
Alias           gsmbsn ->                                          2.0.0.0    SmbShare
Alias           gsmbt ->                                           2.0.0.0    SmbShare
Alias           gsmbw ->                                           2.0.0.0    SmbWitness
Alias           gsn -> Get-PSSession
Alias           gsnp -> Get-PSSnapin
Alias           gsv -> Get-Service
Alias           gtz -> Get-TimeZone                                3.1.0.0    Microsoft.PowerShell.Management
Alias           gu -> Get-Unique
Alias           gv -> Get-Variable
Alias           gwmi -> Get-WmiObject
Alias           h -> Get-History
Alias           history -> Get-History
Alias           icim ->                                            1.0.0.0    CimCmdlets
Alias           icm -> Invoke-Command
Alias           iex -> Invoke-Expression
Alias           ihy -> Invoke-History
Alias           ii -> Invoke-Item
Alias           Initialize-Volume                                  2.0.0.0    Storage
Alias           inmo ->                                            1.0.0.1    PowerShellGet
Alias           ipal -> Import-Alias
Alias           ipcsv -> Import-Csv
Alias           ipmo -> Import-Module
Alias           ipsn -> Import-PSSession
Alias           irm -> Invoke-RestMethod
Alias           iru ->                                             1.0.0.0    AppBackgroundTask
Alias           ise -> powershell_ise.exe
Alias           iwmi -> Invoke-WmiMethod
Alias           iwr -> Invoke-WebRequest
Alias           kill -> Stop-Process
Alias           lp -> Out-Printer
Alias           ls -> Get-ChildItem
Alias           man -> help
Alias           md -> mkdir
Alias           measure -> Measure-Object
Alias           mi -> Move-Item
Alias           mount -> New-PSDrive
Alias           Mount-AppPackageVolume                             2.0.1.0    Appx
Alias           move -> Move-Item
Alias           Move-AppPackage                                    2.0.1.0    Appx
Alias           Move-SmbClient                                     2.0.0.0    SmbWitness
Alias           mp -> Move-ItemProperty
Alias           msmbw ->                                           2.0.0.0    SmbWitness
Alias           mv -> Move-Item
Alias           nal -> New-Alias
Alias           ncim ->                                            1.0.0.0    CimCmdlets
Alias           ncms ->                                            1.0.0.0    CimCmdlets
Alias           ncso ->                                            1.0.0.0    CimCmdlets
Alias           ndr -> New-PSDrive
Alias           ni -> New-Item
Alias           nlg ->                                             1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           nlu ->                                             1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           nmo -> New-Module
Alias           npssc -> New-PSSessionConfigurationFile
Alias           nsmbgm ->                                          2.0.0.0    SmbShare
Alias           nsmbm ->                                           2.0.0.0    SmbShare
Alias           nsmbs ->                                           2.0.0.0    SmbShare
Alias           nsmbscm ->                                         2.0.0.0    SmbShare
Alias           nsmbt ->                                           2.0.0.0    SmbShare
Alias           nsn -> New-PSSession
Alias           nv -> New-Variable
Alias           nwsn ->                                            2.0.0.0    PSWorkflow
Alias           ogv -> Out-GridView
Alias           oh -> Out-Host
Alias           Optimize-AppProvisionedPackages                    3.0        Dism
Alias           Optimize-ProvisionedAppPackages                    3.0        Dism
Alias           Optimize-ProvisionedAppxPackages                   3.0        Dism
Alias           pbcfg ->                                           1.1        PSDesiredStateConfiguration
Alias           pfn ->                                             1.0.0.0    AppBackgroundTask
Alias           popd -> Pop-Location
Alias           ps -> Get-Process
Alias           pumo ->                                            1.0.0.1    PowerShellGet
Alias           pushd -> Push-Location
Alias           pwd -> Get-Location
Alias           r -> Invoke-History
Alias           rbp -> Remove-PSBreakpoint
Alias           rcie ->                                            1.0.0.0    CimCmdlets
Alias           rcim ->                                            1.0.0.0    CimCmdlets
Alias           rcjb -> Receive-Job
Alias           rcms ->                                            1.0.0.0    CimCmdlets
Alias           rcsn -> Receive-PSSession
Alias           rd -> Remove-Item
Alias           rdr -> Remove-PSDrive
Alias           Remove-AppPackage                                  2.0.1.0    Appx
Alias           Remove-AppPackageVolume                            2.0.1.0    Appx
Alias           Remove-AppProvisionedPackage                       3.0        Dism
Alias           Remove-EtwTraceSession                             1.0.0.0    EventTracingManagement
Alias           Remove-ProvisionedAppPackage                       3.0        Dism
Alias           Remove-ProvisionedAppxPackage                      3.0        Dism
Alias           Remove-ProvisioningPackage                         3.0        Provisioning
Alias           Remove-TrustedProvisioningCertificate              3.0        Provisioning
Alias           ren -> Rename-Item
Alias           ri -> Remove-Item
Alias           rjb -> Remove-Job
Alias           rksmba ->                                          2.0.0.0    SmbShare
Alias           rlg ->                                             1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           rlgm ->                                            1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           rlu ->                                             1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           rm -> Remove-Item
Alias           rmdir -> Remove-Item
Alias           rmo -> Remove-Module
Alias           rni -> Rename-Item
Alias           rnlg ->                                            1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           rnlu ->                                            1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           rnp -> Rename-ItemProperty
Alias           rp -> Remove-ItemProperty
Alias           rsmbb ->                                           2.0.0.0    SmbShare
Alias           rsmbc ->                                           2.0.0.0    SmbShare
Alias           rsmbgm ->                                          2.0.0.0    SmbShare
Alias           rsmbm ->                                           2.0.0.0    SmbShare
Alias           rsmbs ->                                           2.0.0.0    SmbShare
Alias           rsmbscm ->                                         2.0.0.0    SmbShare
Alias           rsmbt ->                                           2.0.0.0    SmbShare
Alias           rsn -> Remove-PSSession
Alias           rsnp -> Remove-PSSnapin
Alias           rtcfg ->                                           1.1        PSDesiredStateConfiguration
Alias           rujb -> Resume-Job
Alias           rv -> Remove-Variable
Alias           rvpa -> Resolve-Path
Alias           rwmi -> Remove-WmiObject
Alias           sacfg ->                                           1.1        PSDesiredStateConfiguration
Alias           sajb -> Start-Job
Alias           sal -> Set-Alias
Alias           saps -> Start-Process
Alias           sasv -> Start-Service
Alias           sbp -> Set-PSBreakpoint
Alias           sc -> Set-Content
Alias           scb -> Set-Clipboard                               3.1.0.0    Microsoft.PowerShell.Management
Alias           scim ->                                            1.0.0.0    CimCmdlets
Alias           select -> Select-Object
Alias           set -> Set-Variable
Alias           Set-AppPackageDefaultVolume                        2.0.1.0    Appx
Alias           Set-AppPackageProvisionedDataFile                  3.0        Dism
Alias           Set-AutologgerConfig                               1.0.0.0    EventTracingManagement
Alias           Set-EtwTraceSession                                1.0.0.0    EventTracingManagement
Alias           Set-PreferredLanguage                              1.0        LanguagePackManagement
Alias           Set-ProvisionedAppPackageDataFile                  3.0        Dism
Alias           Set-ProvisionedAppXDataFile                        3.0        Dism
Alias           Set-SystemLanguage                                 1.0        LanguagePackManagement
Alias           shcm -> Show-Command
Alias           si -> Set-Item
Alias           sl -> Set-Location
Alias           slcm ->                                            1.1        PSDesiredStateConfiguration
Alias           sleep -> Start-Sleep
Alias           slg ->                                             1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           sls -> Select-String
Alias           slu ->                                             1.0.0.0    Microsoft.PowerShell.LocalAccounts
Alias           sort -> Sort-Object
Alias           sp -> Set-ItemProperty
Alias           spjb -> Stop-Job
Alias           spps -> Stop-Process
Alias           spsv -> Stop-Service
Alias           ssmbb ->                                           2.0.0.0    SmbShare
Alias           ssmbcc ->                                          2.0.0.0    SmbShare
Alias           ssmbp ->                                           2.0.0.0    SmbShare
Alias           ssmbs ->                                           2.0.0.0    SmbShare
Alias           ssmbsc ->                                          2.0.0.0    SmbShare
Alias           start -> Start-Process
Alias           stz -> Set-TimeZone                                3.1.0.0    Microsoft.PowerShell.Management
Alias           sujb -> Suspend-Job
Alias           sv -> Set-Variable
Alias           swmi -> Set-WmiInstance
Alias           tcfg ->                                            1.1        PSDesiredStateConfiguration
Alias           tee -> Tee-Object
Alias           tid ->                                             1.0.0.0    AppBackgroundTask
Alias           TNC ->                                             1.0.0.0    NetTCPIP
Alias           trcm -> Trace-Command
Alias           type -> Get-Content
Alias           udsmbmc ->                                         2.0.0.0    SmbShare
Alias           ulsmba ->                                          2.0.0.0    SmbShare
Alias           upcfg ->                                           1.1        PSDesiredStateConfiguration
Alias           upmo ->                                            1.0.0.1    PowerShellGet
Alias           wget -> Invoke-WebRequest
Alias           where -> Where-Object
Alias           wjb -> Wait-Job
Alias           write -> Write-Output
Alias           Write-FileSystemCache                              2.0.0.0    Storage


-Suppose we want to know the alias of clear host then we can use below command-


PS C:\Users\test> Get-Alias -Definition "Clear-Host"

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Alias           clear -> Clear-Host
Alias           cls -> Clear-Host


PS C:\Users\test>

PS C:\Users\test> Get-Command -Name "Get-Alias" -Syntax

Get-Alias [[-Name] <string[]>] [-Exclude <string[]>] [-Scope <string>] [<CommonParameters>]

Get-Alias [-Exclude <string[]>] [-Scope <string>] [-Definition <string[]>] [<CommonParameters>]

PS C:\Users\test>


