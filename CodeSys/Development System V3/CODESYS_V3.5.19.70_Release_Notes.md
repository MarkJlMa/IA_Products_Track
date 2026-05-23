[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Product: CODESYS V3.5 SP19 Patch 7

Key  |  Issue Type  |  Summary  |  Resolution  |  Release Note   
---|---|---|---|---  
CDS-89743 | Bug | CLONE - TS_Runtime Linux: Test fails with several errors on Linux x86 | Fixed | [[GENERAL]]  
Accident caused by CDS-85986.  
CDS-89674 | Bug | CLONE - RTE: Change Operating Mode does sometimes leads to rejection by CM | Fixed |   
CDS-89609 | Bug | CLONE - Embedded SizeCheck fails on Bookworm build host | Won't Fix | [[GENERAL]]  
Wont fix cause: this is not relevant for SP19 branch, as this problem does not occur here!  
CDS-89513 | Bug | CLONE - Linux SysProcessExecuteCommand(-2) does not close the used pipe if an error occurs | Fixed |   
CDS-89345 | Bug | CLONE - [Build] pt-br and tr resources are missing in SDK | Fixed |   
CDS-89300 | Bug | CLONE - Crash while change setting "Behavior for outputs in stop" | Duplicate | [[GENERAL]]  
Duplicate entry for CDS-87648 released with SP19 Patch 6  
CDS-89241 | Bug | CLONE - RTE: incorrect PN-CIFX-Communication with Wago Slave | Fixed |   
CDS-89227 | Bug | CLONE - OnlineChange ist not possible after closing project because of changes in IoConfig_Globals_ModuleList | Fixed |   
CDS-89226 | Bug | CLONE - Linux x64: SIGILL terminates runtime | Fixed |   
CDS-89169 | Bug | CLONE - Linux: Compile errors when HilscherCifxLib Feature is used | Fixed |   
CDS-89140 | Bug | CLONE - Linux: SysFileCopy doesn't work | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
SysFileCopy internally uses SysProcessLinux -> this uses posix_spawn.  
For old libc Versions (< 2.24) posix_spawn uses fork() instead of vfork().  
This is now avoided by setting the flag "USEVFORK" for posix_spawn.  
CDS-89136 | Bug | CLONE - CmpIecTask: Crash can occur because IecTaskDelete2() is called twice with RSMUtility.library | Fixed |   
CDS-89101 | Bug | CLONE - CmpRetain: Retain file from SP12 cannot be loaded with bootapplication SP19 | Fixed |   
CDS-89085 | Bug | CLONE - Compile: Internal error 2 during OnlineChange | Fixed |   
CDS-89082 | Bug | CLONE - RTE: OEM licensing does not work | Fixed |   
CDS-89079 | Bug | CLONE - Security issues in CodeMeter versions before 8.0 | Fixed |   
CDS-89076 | Bug | CLONE - RTE: Control RTE SL license is not working on the UFC Container | Fixed | [[COMPATIBILITY_INFORMATION-EndUser]]  
RTE runtime licenses are working now on WIBU UFC container!  
If you use an older RTE version, you can only use a runtime license on a legacy cmact container (firmcode=5000304)  
CDS-89058 | Bug | CLONE - CmpRedundancy: Possible AccessViolation due to skipped EventPost for vfinit | Fixed |   
CDS-89011 | Bug | CLONE - RTE: SysEthernet-drivers: CmpEt1000Drv: The intel driver periodically scans for a link in case no cable plugged and blocks CPU too long. | Fixed |   
CDS-88996 | Improvement | CLONE- [Setup] Update CODESYS Installer to 2.2.2 | Fixed |   
CDS-88977 | Bug | CLONE - CmpOpenSSL: Endless loop creating key pair on Linux ARM targets | Fixed |   
CDS-88884 | Bug | CLONE - [Setup] Problems, if CodeMeter Runtime 8.0 is already installed | Fixed |   
CDS-88874 | Bug | CLONE - CmpApp: Improve license exception logmessage if DevDesc or CDS compiler is too old | Fixed |   
CDS-88873 | Bug | CLONE - [RTS Online Help]: Endless recursion occurred after entering a search text | Fixed |   
CDS-88845 | Bug | CLONE - SysSocketLinux.c : For QNX the UpdateNetworkAdapterInfo( ) causes cyclically CPU performance peak | Fixed | A new setting is available to disable the cyclic update of the default gateway, while still initializing it once:  
  
[SysSocket]  
DisableGetDefaultGateway=1  
  
In This case, the event EVTPARAM_SysSocket_GetAdditionalAdapterInfo can still be used to update the default gateway at runtime.  
CDS-88783 | Bug | CLONE - CmpRedundancy: AutoSyncEnabled setting doesn't cover re-sync after receiving delayed messages | Fixed |   
CDS-88771 | Bug | CLONE - Shell, pinf command: Changing the application with/without project info POU leads to an exception | Fixed |   
CDS-88543 | Bug | CLONE - Symbolconfig: Odd behaviour related to symbol file access to variable | Won't Fix | [[GENERAL]]  
Affected feature has been moved to the communication Add-on and has an independent release cycle.  
CDS-88526 | Bug | CLONE - Wrong Code for x64 codegenerator for try-catch statement with CONCAT | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.70  
CDS-87856 | Bug | CLONE - Persistent variables: wrong error message for persistent variable of library of complex type | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.70  
The hastype pragma only performed a string comparision of the variable-type and the passed type. This is obviously wrong and leads to problems with any kind of qualified constants or types. So this this behavior was deliberately changed.  
CDS-87818 | Bug | CLONE - CDS: Opening CODESYS without second monitor - CODESYS not visible | Fixed |   
CDS-87700 | Bug | CLONE - Setup: Silent execution indicates success if an error during package installation | Fixed |   
CDS-87697 | Bug | CLONE - SysTask: SysTaskExit, SysTaskDestroy, SysTaskEnd, SysTaskSetInterval: OS implementations incorrect | Won't Fix | [[GENERAL]]  
Issue will not be patched to SP19, since CDS-87837 as part of SP19 Patch 6 already fixes the most critical aspect of the bug.  
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2024 CODESYS GmbH  | A member of the CODESYS Group 
