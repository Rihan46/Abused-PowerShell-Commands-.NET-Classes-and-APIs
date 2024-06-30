# Abused .NET Classes in PowerShell

| **.NET Class**                           | **Description**                                                | **Example**                                                      |
|------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------|
| **`System.Net.WebClient`**               | Provides methods for sending data to and receiving data from a resource identified by a URI. | `$webClient = New-Object System.Net.WebClient`                    |
| **`System.Net.HttpWebRequest`**         | Provides a way to interact with HTTP requests and responses.  | `$request = [System.Net.HttpWebRequest]::Create("http://example.com")` |
| **`System.Net.Http.HttpClient`**        | Sends HTTP requests and receives HTTP responses.             | `$client = New-Object System.Net.Http.HttpClient`                |
| **`System.Diagnostics.Process`**       | Provides Start, Stop, and query functionalities for system processes. | `[System.Diagnostics.Process]::Start("notepad.exe")`            |
| **`System.IO.File`**                    | Provides static methods for creating, copying, deleting, and moving files. | `[System.IO.File]::ReadAllText("C:\path\to\file.txt")`           |
| **`System.IO.Stream`**                  | Abstract base class for data streams.                         | `$stream = [System.IO.Stream]::Null`                            |
| **`System.IO.MemoryStream`**            | Provides a stream for reading and writing to memory.         | `$memoryStream = New-Object System.IO.MemoryStream`             |
| **`System.Reflection.Assembly`**       | Provides methods for loading and querying .NET assemblies.   | `[System.Reflection.Assembly]::Load("System.Core")`             |
| **`System.Security.Cryptography.Aes`** | Provides methods for symmetric encryption and decryption.     | `$aes = [System.Security.Cryptography.Aes]::Create()`           |
| **`System.Management.Automation.PSCustomObject`** | Represents a generic object for use with PowerShell.        | `$obj = New-Object PSCustomObject`                             |
| **`System.Management.Automation.PowerShell`** | Provides methods for running and managing PowerShell commands. | `$powershell = [System.Management.Automation.PowerShell]::Create()` |
| **`System.Net.Sockets.TcpClient`**     | Provides methods for TCP network connections.                 | `$tcpClient = New-Object System.Net.Sockets.TcpClient`           |
| **`System.Net.Sockets.UdpClient`**     | Provides methods for UDP network connections.                 | `$udpClient = New-Object System.Net.Sockets.UdpClient`           |
| **`System.Net.Dns`**                    | Provides methods for host name resolution.                    | `[System.Net.Dns]::GetHostEntry("example.com")`                 |
| **`System.IO.Compression.ZipArchive`** | Provides methods for compressing and decompressing files.     | `$archive = [System.IO.Compression.ZipArchive]::new($stream, [System.IO.Compression.ZipArchiveMode]::Create)` |
| **`System.IO.Compression.GZipStream`** | Provides methods for compressing and decompressing streams using GZip. | `$gzipStream = New-Object System.IO.Compression.GZipStream($stream, [System.IO.Compression.CompressionMode]::Compress)` |
| **`System.Net.NetworkInformation.Ping`** | Provides methods for sending ICMP echo requests.             | `$ping = New-Object System.Net.NetworkInformation.Ping`          |
| **`System.Security.Principal.WindowsIdentity`** | Represents a Windows user identity.                         | `[System.Security.Principal.WindowsIdentity]::GetCurrent()`      |
| **`System.Management.ManagementObjectSearcher`** | Provides a way to query WMI classes and instances.         | `$searcher = New-Object System.Management.ManagementObjectSearcher("SELECT * FROM Win32_ComputerSystem")` |
| **`System.Diagnostics.EventLog`**      | Provides methods for working with event logs.                 | `$log = [System.Diagnostics.EventLog]::new("Application")`     |
| **`System.Net.Mail.SmtpClient`**       | Provides methods for sending email messages.                 | `$smtp = New-Object System.Net.Mail.SmtpClient("smtp.example.com")` |
| **`System.Diagnostics.EventLog`**      | Provides methods for working with event logs.                 | `$eventLog = [System.Diagnostics.EventLog]::new("Application")` |
