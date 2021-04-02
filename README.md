# MMFCodeInjection

This technique leverages [File Mapping](https://docs.microsoft.com/en-us/windows/win32/memory/file-mapping) and APC(s) to execute shellcode into another process. By leveraging file mapping we would not have to use various functions such as VirtualAllocEx and WriteProcessMemory to copy the shellcode into the remote process but instead we can just use QueueUserAPC to call the functions we want to reference and execute the shellcode in the file we want. 
