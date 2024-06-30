# Abused Windows API Calls

| **API Call**                     | **Description**                                              | **Example**                                                      |
|----------------------------------|--------------------------------------------------------------|------------------------------------------------------------------|
| **`CreateProcess`**             | Creates a new process and its primary thread.              | `CreateProcess(NULL, "C:\\path\\to\\malicious.exe", NULL, NULL, FALSE, 0, NULL, NULL, &startupInfo, &processInfo)` |
| **`WinExec`**                    | Executes a specified command.                              | `WinExec("C:\\path\\to\\malicious.exe", SW_HIDE)`                |
| **`ShellExecute`**             | Opens or executes a specified file.                        | `ShellExecute(NULL, "open", "C:\\path\\to\\malicious.exe", NULL, NULL, SW_HIDE)` |
| **`LoadLibrary`**               | Loads a DLL into the address space of the calling process. | `LoadLibrary("C:\\path\\to\\malicious.dll")`                     |
| **`GetProcAddress`**           | Retrieves the address of an exported function or variable from a DLL. | `GetProcAddress(hModule, "MaliciousFunction")`                  |
| **`VirtualAlloc`**             | Reserves or commits a region of memory.                     | `VirtualAlloc(NULL, size, MEM_COMMIT, PAGE_EXECUTE_READWRITE)` |
| **`WriteProcessMemory`**       | Writes data to the memory of another process.               | `WriteProcessMemory(hProcess, address, data, size, &bytesWritten)` |
| **`ReadProcessMemory`**        | Reads data from the memory of another process.              | `ReadProcessMemory(hProcess, address, buffer, size, &bytesRead)` |
| **`CreateRemoteThread`**       | Creates a thread in the address space of another process.   | `CreateRemoteThread(hProcess, NULL, 0, remoteFunction, NULL, 0, NULL)` |
| **`OpenProcess`**              | Opens an existing process object.                           | `OpenProcess(PROCESS_ALL_ACCESS, FALSE, processId)`             |
| **`GetWindowsDirectory`**      | Retrieves the path of the Windows directory.                | `GetWindowsDirectory(buffer, MAX_PATH)`                          |
| **`RegOpenKeyEx`**             | Opens the specified registry key.                           | `RegOpenKeyEx(HKEY_CURRENT_USER, "Software\\Malicious", 0, KEY_READ, &hKey)` |
| **`RegSetValueEx`**           | Sets the data for a specified registry key.                  | `RegSetValueEx(hKey, "ValueName", 0, REG_SZ, data, dataSize)`   |
| **`RegCreateKeyEx`**           | Creates a new registry key or opens an existing one.        | `RegCreateKeyEx(HKEY_CURRENT_USER, "Software\\Malicious", 0, NULL, REG_OPTION_NON_VOLATILE, KEY_SET_VALUE, NULL, &hKey, &disposition)` |
| **`CreateFile`**               | Creates or opens a file or I/O device.                       | `CreateFile("C:\\path\\to\\file.txt", GENERIC_WRITE, 0, NULL, CREATE_ALWAYS, FILE_ATTRIBUTE_NORMAL, NULL)` |
| **`ReadFile`**                 | Reads data from a file or I/O device.                        | `ReadFile(hFile, buffer, bufferSize, &bytesRead, NULL)`         |
| **`WriteFile`**                | Writes data to a file or I/O device.                         | `WriteFile(hFile, data, dataSize, &bytesWritten, NULL)`         |
| **`DeleteFile`**               | Deletes an existing file.                                    | `DeleteFile("C:\\path\\to\\malicious.exe")`                      |
| **`CreateDirectory`**         | Creates a new directory.                                    | `CreateDirectory("C:\\path\\to\\new\\directory", NULL)`        |
| **`SetFileAttributes`**       | Sets the attributes of a file or directory.                  | `SetFileAttributes("C:\\path\\to\\file.txt", FILE_ATTRIBUTE_HIDDEN)` |
| **`MoveFile`**                 | Moves a file or renames a file or directory.                | `MoveFile("C:\\path\\to\\file.txt", "C:\\path\\to\\newfile.txt")` |
| **`GetSystemInfo`**           | Retrieves information about the current system.             | `GetSystemInfo(&systemInfo)`                                    |
| **`CreateService`**           | Creates a service object.                                   | `CreateService(hSCManager, "ServiceName", "DisplayName", SERVICE_ALL_ACCESS, SERVICE_WIN32_OWN_PROCESS, SERVICE_AUTO_START, SERVICE_ERROR_NORMAL, "C:\\path\\to\\service.exe", NULL, NULL, NULL, NULL, NULL)` |
| **`StartService`**            | Starts a service.                                          | `StartService(hService, 0, NULL)`                               |
| **`ControlService`**         | Sends a control request to a service.                        | `ControlService(hService, SERVICE_CONTROL_STOP, &serviceStatus)` |
| **`EnumServicesStatus`**     | Enumerates services that are installed on the system.       | `EnumServicesStatus(hSCManager, SERVICE_WIN32, SERVICE_STATE_ALL, serviceStatus, buffer, bufferSize, &bytesNeeded, &servicesReturned, &resumeHandle, NULL)` |
| **`GetModuleHandle`**       | Retrieves a module handle for the specified module.         | `GetModuleHandle("kernel32.dll")`                               |
| **`GetModuleFileName`**     | Retrieves the full path of the executable file of a specified module. | `GetModuleFileName(hModule, buffer, bufferSize)`                |
| **`GetCurrentProcessId`**   | Retrieves the process identifier of the calling process.    | `GetCurrentProcessId()`                                         |
| **`GetTickCount`**          | Retrieves the number of milliseconds that have elapsed since the system was started. | `GetTickCount()`                                                |
| **`CreateRemoteThreadEx`**  | Creates a thread in the address space of another process (Extended). | `CreateRemoteThreadEx(hProcess, NULL, 0, remoteFunction, NULL, 0, NULL, NULL)` |

