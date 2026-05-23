[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Product: CODESYS V3.5 SP19 Patch 5

Key  |  Issue Type  |  Summary  |  Resolution  |  Release Note   
---|---|---|---|---  
CDS-87569 | Bug | CLONE - DeviceObject: ChannelMapping for Safety-Exchange Variables invalid | Fixed |   
CDS-87560 | Bug | CLONE - DeviceObject: ChannelMapping for Safety-Exchange Variables invalid | Duplicate |   
CDS-87447 | Bug | CLONE - ProjectInfoEditor: 2 checkboxes not visible | Fixed |   
CDS-87405 | Bug | CLONE - CmpBlkDrvTcp: EnableServer with LocalAccessOnly does not work anymore | Fixed | [[GENERAL]]  
Caused by CDS-86078 CmpBlkDrvTcp: Improve ethernet configuration options.  
CDS-87340 | Bug | CLONE - Exception on logout when using IControlledExternalEditorView2 | Fixed |   
CDS-87331 | Bug | CLONE - OPCServer: Very rare semaphore deadlock possible | Fixed |   
CDS-87329 | Bug | CLONE - SysFileLinux: Linux SysFileCopy_ check dst for valid filename | Fixed | [[GENERAL]]  
For more details see Advisory 2023-11, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=18027&token=43109051cf95d3445bc616e4efb8414336ebcc47&download=  
CDS-87256 | Improvement | CLONE - Retains: Support Shm custom device file | Fixed | [[GENERAL]]  
Retains can now be stored in a configurable location.  
This feature cannot be used simultaniously with retain in shm.  
  
Example for configuration:  
  
[CmpApp]  
RetainType.Applications=InSRAM  
  
[CmpRetain]  
Retain.SRAM.Size=0x10000  
  
[SysShm]  
Linux.RetainPath=/dev/nv01  
(Or a local path for testing, this file must be allocated with a corresponding size or larger before: )  
Linux.RetainPath=/var/run/retains  
CDS-87231 | Bug | CLONE - Internal error on Online Change after Reload project | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.19.50  
CDS-87230 | Improvement | CLONE - PlcHandler Linux Arm: Support SoftFloat | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
The linux arm (soft float) binary requires minimum march=armv6, as the atomic builtin "compare and swap" is required for proper functionality.  
CDS-87190 | Bug | CLONE - DeviceObject: Mapping for safety device without safety mapping application does not work as expected with PN device | Fixed |   
CDS-87145 | Improvement | CLONE - Improve codesize output message after Compiler | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.50  
CDS-87099 | Bug | CLONE - CmpUserMgr: admin access rights get lost with update from 3.5.15.x to version >=3.5.18.x | Fixed |   
CDS-87092 | Bug | CLONE - IEC task does not start after online change, Task Monitoring Status not shown | Fixed | [[COMPATIBILITY_INFORMATION-EndUser]]  
Sleep time of freewheeling tasks are limited now, if cycle time is very high!  
So we limit the sleep time to a maximum of:  
5 * average cycle time * number of freewheeling tasks  
CDS-87091 | Bug | CLONE - PLCHandler Interface ARTI: Login into PLC with Motorola byte order is not possible anymore | Fixed |   
CDS-87081 | Bug | CLONE - Linux SocketCan: removing CAN cable may cause 100% CPU load | Won't Fix | [[GENERAL]]  
CmpSocketCANDrv requires a proper bus off error frame to handle a removed can cable properly. Specific low level can errors (only protocol error) does not signal error situation.  
Log message is valid and must be shown in this error case.  
CDS-87065 | Bug | CLONE - CmpOPCUAProviderAlarmConfiguration: Events are reported three times | Fixed |   
CDS-87058 | Bug | CLONE - OPC Configurator: Checkbox value of 'Motorola Byteorder' is not saved | Fixed |   
CDS-87001 | Bug | CLONE - CmpUserMgr: Admin can not change password for user created with "Password can be changed by user" unselected (RTS-Part) | Fixed |   
CDS-86973 | Bug | CLONE - Online Change: Project generates Internal Error 2 after adding a variable | Cannot Reproduce | [[GENERAL]]  
duplicates CDS-87126, already fixed with SP 19 Patch 4  
CDS-86952 | Bug | CLONE - SysProcessLinux: incompatible change of return value of SysProcessExecuteCommand function | Fixed | [[COMPATIBILITY_INFORMATION]]  
SysProcessExecuteCommand returns the exitcode of the subprocess. SysProcessExecuteCommand2 also fills number of read bytes, even in case of error.  
CDS-86951 | Bug | CLONE - CmpOpenSSL: Update OpenSSL to version 3.1.3 | Fixed | [[COMPATIBILITY_INFORMATION]]  
OpenSSL 3.1. has less performance for some functions then OpensSL 1.1. because of improved security algorithms. But it is better than 3.0.  
CDS-86949 | Bug | CLONE - Device User Management: Import of user “Owner” leads to exception when entering several wrong passwords | Fixed |   
CDS-86941 | Bug | CLONE - CmpOPCUAProviderIecVarAccess: Too much memory is allocated for Array of STRING monitored Items | Fixed |   
CDS-86921 | Bug | CLONE - Context menu stops working sometimes | Fixed |   
CDS-86769 | Bug | CLONE - Compiler: Error C0230 when accessing a enum with the __POOL operator | Fixed |   
CDS-86766 | Bug | CLONE - Compare: Unhandled exception after compare for different devices in tab "Backup and Restore" or "Log" | Fixed | [[KNOWN_LIMITATIONS]]  
DeviceEditors opened from a ProjectCompare will no longer cause unhandled exceptions in the described szenario.  
However if no online device for such an editor exists, it might have reduced functionality, show an error message or simply not show information for certain tab pages.  
CDS-86765 | Bug | CLONE - Compile: VAR GENERIC CONSTANT not working in METHOD | Fixed | [[GENERAL]]  
Works now with Compilerversion >= 3.5.19.50  
CDS-86679 | Bug | CLONE - CmpOpenSSL: Update OpenSSL to version 3.0.10 | Fixed |   
CDS-86557 | Bug | CLONE - Windows: sysdefines.h: #ifdef WIN32_LEAN_AND_MEAN is missing | Fixed |   
CDS-86118 | Bug | CLONE - CmpOpenSSL: Update OpenSSL to version 3.0.5 (LTS) | Fixed |   
CDS-85663 | Improvement | CLONE - CmpCodeMeter: Update CodeMeter Embedded SDK to latest version 2.61 | Fixed |   
CDS-85426 | Improvement | CLONE - RTE: Support of App Based licenses | Fixed |   
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2023 CODESYS GmbH  | A member of the CODESYS Group 
