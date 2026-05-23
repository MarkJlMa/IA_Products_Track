[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Product: CODESYS V3.5 SP19 Patch 3

Key  |  Issue Type  |  Summary  |  Resolution  |  Release Note   
---|---|---|---|---  
CDS-87005 | Bug | CLONE - [Setup] OPC Server DA cannot be installed if newer Gateway V2.3 is already installed | Fixed |   
CDS-86759 | Bug | CLONE - Declaration editor: Variables grayed out in declaration part of SFC POU in offline mode | Fixed |   
CDS-86742 | Bug | CLONE - CmpRedundancy: Race condition sporadically occurs when setting up the redundancy | Fixed |   
CDS-86734 | Improvement | CLONE - DeviceCommunicationEditor: Extend the API of the device license activation to allow selecting the container for the activation | Won't Fix | [[GENERAL]]  
Patch contains too many incompatibilities  
CDS-86726 | Improvement | CLONE - Device Communication Editor: Update Wibu Gateways | Won't Fix | [[GENERAL]]  
Patch contains too many incompatibilities  
CDS-86724 | Improvement | CLONE - License Manager: Update Wibu Gateways | Won't Fix | [[GENERAL]]  
Patch contains too many incompatibilities  
CDS-86722 | Bug | CLONE - Compiler: Wrong Compiler Message C0032 is created | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.30  
CDS-86707 | Bug | CLONE - SysProcessLinux: possible endless loop in SysProcessExecuteCommand | Fixed |   
CDS-86697 | Bug | CLONE - Linux Targetvisu Webbrowser Element: Stack Overflow causes Exception | Fixed |   
CDS-86684 | Bug | CLONE - Rebuild before Login after online change | Fixed |   
CDS-86680 | Bug | CLONE - License terms for Evergreen Webview2 installation are not complete | Fixed | [[GENERAL]]  
Microsoft Edge WebView2 runtime is no longer installed with CODESYS. The user has to download it from https://developer.microsoft.com/en-us/microsoft-edge/webview2 and confirm the license terms.  
We have disabled Microsoft Defender SmartScreen as described by Microsoft.  
  
The CODESYS Visualization add-on included in the installation uses the software Microsoft Defender SmartScreen. Thus, your information is collected and transmitted to Microsoft. For details, see the Microsoft privacy statement at https://aka.ms/privacy and the Microsoft Edge privacy whitepaper at https://learn.microsoft.com/en-us/microsoft-edge/privacy-whitepaper#smartscreen  
CDS-86670 | Improvement | CLONE - Online: Password should be cleared if LoginDialog is idle for some time | Fixed | [[GENERAL]]  
The Dialog to provide credentials for a authentication on a device will now reset the entered password after 2 minutes. The OK button will also be disabled in this case until the user reenters credentials.  
CDS-86656 | Bug | CLONE - Update CodeMeter runtime to version V7.60c | Fixed | [[GENERAL]]  
For more details see Advisory 2023-10, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17809&token=c3b4e3ec4956099de26f0c6caf194d1ba341040a&download=  
CDS-86624 | Improvement | CLONE - Online: User credentials have to be re-entered after automatic logout from PLC | Fixed |   
CDS-86606 | Improvement | CLONE - Package Manager: Write tags and language model version into package db | Fixed | [[GENERAL]]  
Tags and LanguageModelVersion of Packages are now written to the PackageDB. Tags and LanguageModelVersion are now exposed in an Interface.  
CDS-86605 | Bug | CLONE - Compile: C0072 generated in case of REF Property passed to VAR_IN_OUT of method | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.19.30  
CDS-86601 | Improvement | CLONE - Package Manager: Use packed package for archiving | Fixed | [[GENERAL]]  
Use original package for archiving  
CDS-86592 | Improvement | CLONE - DeviceObject: improve saving Parametercache files | Fixed |   
CDS-86534 | Bug | CLONE - Generate Code: Compiler error because of global_init_slot after project update | Cannot Reproduce | [[GENERAL]]  
Fixed with CDS-82727 for SP 19 Patch 2  
CDS-86532 | Bug | CLONE - FBD: Division by zero leads to an unhandled CDS exception | Fixed | [[GENERAL]]  
An OnlineExpressionException is no longer thrown in case of a division by 0.  
The value NaN is returned in this case  
CDS-86525 | Bug | CLONE - No recompilation done when resetting a modified address in IO Mapping | Fixed |   
CDS-86524 | Bug | CLONE - CmpApp: Bootproject must never be renamed or deleted in case of an exception | Fixed | [[COMPATIBILITY_INFORMATION-EndUser]]  
Behavior of existing setting has changed:  
[CmpApp]  
Bootproject.InvalidateNever=1  
=>[Default=1]: The bootproject should never be invalidated or deleted after an exception!  
  
Bootproject is now never deleted or renamed in any case of an exception:  
\- Previously, the bootproject was deactivated after an exception in non IEC tasks!  
\- The bootproject was deleted after an exception in an IO-driver during configuration phase!  
CDS-86523 | Bug | CLONE - PLCHandler: Access violation occurs in ResolveIpAddressCallback after PLCComBase3 destruction | Fixed |   
CDS-86496 | Bug | CLONE - OnlineHelp: Outdated Offline Help is triggered by "F1" if PING is disabled by IT department | Fixed |   
CDS-86468 | Bug | CLONE - CmpDynamicTextSym: Unnecessary large memory allocation in HashtableOpen | Fixed |   
CDS-86462 | Bug | CLONE - LibMan: Detail and documentation view windows do not work correctly after switching to another library | Fixed |   
CDS-86443 | Improvement | CLONE - Package Manager: Prohibit the installation of older packages | Fixed | [[GENERAL]]  
Prohibit the installation of older packages.  
The installation of older packages must be explicitly allowed.  
Either by means of the package tag "AllowOlderVersions" or an OEM customization.  
CDS-86393 | Bug | CLONE - Virusscanner, Codesys Addons: Installing can lead to "process cannot access the file 'CurrentInstall.log' " message | Fixed | [[GENERAL]]  
Log will be hold in memory instead of writing to disc.  
CDS-86392 | Bug | CLONE - Library: Documentation not shown on double click on function block from LD / FBD / CFC | Fixed |   
CDS-86377 | Improvement | CLONE - DeviceObject: add flag for safety input and outputs to skip swapping of io channels | Fixed | [[GENERAL]]  
Compiler version >= 3.5.19.30 required  
CDS-86376 | Bug | CLONE - PLCHandler VxWorks Source Delivery: Files are missing | Fixed |   
CDS-86329 | Bug | CLONE - Updating an package can lead to break of dependency (PackageReference) | Fixed | [[GENERAL]]  
Existing package reference constraints will now be checked before a new package will be installed. If the new one would break a reference an error will be shown.  
CDS-86300 | Bug | CLONE - APUnitTestFramework should resolve interface dependencies of loaded plugins in their respective target | Fixed | [[GENERAL]]  
ApUnittestFramework uses the plugin cache file of the target for test execution.  
CDS-86286 | Bug | CLONE - Compile: VAR_GENERIC CONSTANT not working in compiled libraries | Fixed | [[GENERAL]]  
a type declaration using a generic type will be saved for Compiler Version >= 3.5.19.30  
CDS-86285 | Bug | CLONE - CmpOPCUAServer: Calculation for mempool extension is incorrect for PublishRequests and Subscriptions | Fixed |   
CDS-86260 | Bug | CLONE - Targetvisu, Overlay: High load in certain customer project | Won't Fix | [[GENERAL]]  
This issue will not be fixed for 3.5.19.30 because the problem is located in the AddOn CODESYS Visualization. Therefore the bugfix will be released with the fix version of VIS-3302  
CDS-86259 | Bug | CLONE - LWIP: Update to latest version 2.1.3 | Fixed |   
CDS-86258 | Bug | CLONE - Package Manager: Missing menu items in standard menu option files after package installation | Fixed |   
CDS-86200 | Bug | CLONE - IoDrvTemplate: No driver found | Won't Fix | [[GENERAL]]  
Templates will not be patched to older versions.  
CDS-86199 | Bug | CLONE - Watchlist: Exception "too many items added" when opening library method in online mode | Fixed |   
CDS-86198 | Bug | CLONE - [MessageView] Messages added during Engine initialization are not shown | Fixed | [[GENERAL]]  
Adding messages to the MessageStorage before UIReady is now working properly  
CDS-86197 | Bug | CLONE - CmpIecVarAccess: Use IecVarAccGetAccessRights instead of IecVarAccessGetAccessRights2 to serialze type members | Fixed |   
CDS-86179 | Bug | CLONE - Device User Management: Option “Password must be changed at first login” is not working | Fixed |   
CDS-86178 | Bug | CLONE - Device User Management: Admin can not change password for user created with “Password can be changed by user” unselected | Fixed | [[GENERAL]]  
This issue fixes a problem in the IDE so that it works again for older runtime systems (e.g. SP15). For a full fix for newer runtime systems, an additional fix on the runtime side needs to be patched (CDS-86419).  
CDS-86157 | Bug | CLONE - Compiler, Cross references: Null reference exceptions possible when forcing early cross references | Fixed |   
CDS-86156 | Improvement | CLONE - WebBrowser: Update to Microsoft.Web.WebView2 V1.0.1823.32 | Fixed |   
CDS-86147 | Improvement | CLONE - CmpIecTask: IEC call of IecTaskDeleteInternalAsync() with parameters from stack can lead to stack overwrite | Fixed |   
CDS-86146 | Bug | CLONE - RSM Utility Library: Wrong parameter usage of IecTaskDelete3 | Fixed |   
CDS-86102 | Improvement | CLONE - CODESYS Control: Add a log message, if a file access is denied by ForceIecFilePath | Fixed |   
CDS-86101 | Bug | CLONE - CmpApp: Log error needed for AppBasedLicenses if metrics in bootproject exceeds license | Fixed |   
CDS-86085 | Improvement | CLONE - Package Manager: Blacklist old PDE versions | Fixed | [[GENERAL]]  
[[COMPATIBILITY_INFORMATION]]  
The following add-ons have been blacklisted due to upcoming compatibility issues.  
CODESYS UML < 4.3.0.0  
CODESYS SVN < 4.5.0.0  
CODESYS Static Analysis < 4.4.3.0  
CODESYS Test Manager < 5.1.0.0  
CODESYS Profiler < 2.2.0.0  
CODESYS GIT < 1.3.0.0  
CODESYS Application Composer Single License < 4.2.0.0  
CODESYS Visu Elem Toolkit < 4.3.0.0  
CDS-86078 | Improvement | CLONE - CmpBlkDrvTcp: Improve ethernet configuration options | Fixed | [[COMPATIBILITY_INFORMATION]]  
[[COMPATIBILITY_INFORMATION-OEM]]  
The setting BLKDRVTCPKEY_STRING_LOCALADDRESS is now deprecated and only kept for compatibility reasons. It is replaced by the new setting BLKDRVTCPKEY_STRING_NETWORK_ADAPTER.  
See CmpBlkDrvItf.h for details.  
CDS-86077 | Improvement | CLONE - CmpWebServer: Improve ethernet configuration options | Fixed |   
CDS-86068 | Bug | CLONE - Open Project: Crash while opening NVL project | Fixed |   
CDS-86067 | Improvement | CLONE - Logout IDE from PLC after configurable time of inactivity | Fixed | [[GENERAL]]  
Added new option page "Online"  
* New Setting "Force disconnect from device after time of inactivity"  
  
Added new startup parameter "ForceDisconnectAfterInactivity", which overrides the new setting:  
* --ForceDisconnectAfterInactivity="2000" (Will perform a force logout after 2000 seconds of inactivity. The specified time will be clamped to the range of 10-10800)  
* --ForceDisconnectAfterInactivity="0" (Will disable the new setting)   
  
Note that the inactivity is tracked by mouse/keyboard events that are local to CODESYS. This means that CODESYS running on a second monitor will force a disconnect even if the user is busy typing inside another application on the primary monitor. However, simply moving the mouse across the CODESYS UI without any clicking will reset the inactivity.  
CDS-86060 | Bug | CLONE - Fast online change: Not working in certain circumstances | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.19.30  
CDS-86031 | Bug | CLONE - CmpEventMgr: Exception in IEC Callback leads to timeout and inconsistent state | Fixed |   
CDS-86030 | Improvement | CLONE - RTE / CmpET1000Drv: Extend driver to support new generation eth chips like i225/i226 | Fixed |   
CDS-85763 | Bug | CLONE - SIGABRT on Reset Cold with MODBUS Slave | Fixed |   
CDS-85737 | Bug | CLONE - Option Files: Files end up in the same folder in customized installation | Won't Fix | [[GENERAL]]  
This issue is too risky to be cloned to a patch without a full regression test and without a larger community testing it before the release. See risk analysis for more information.  
CDS-85503 | Bug | CLONE - IecVarAccess: Consistent read blocks sporadically the IEC tasks for 1s | Fixed |   
CDS-84417 | Bug | CLONE - CmpIoMgr.c : Issues causing crash after few Run->Halt->Reset cycles | Fixed |   
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2023 CODESYS GmbH  | A member of the CODESYS Group 
