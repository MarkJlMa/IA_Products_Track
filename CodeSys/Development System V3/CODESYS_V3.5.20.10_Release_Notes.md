[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS V3.5 SP20 Patch 1

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
CDS-89956 | Bug | CLONE - ABL / CmpOPCUAProviderIecVarAccess: "Communication <xyz>" license locked without using symbolconfig | Fixed |   
CDS-89815 | Bug | CLONE - Static Analysis error SA0003: "Empty statement" is reported for correctly implemented transition objects | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.10  
CDS-89812 | Bug | CLONE - OnlineChange: Potential memory overwrite after OnlineChange | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.10  
CDS-89777 | Improvement | CLONE - Setup: Working Directory for Simulation should be in the user profile | Fixed | [[GENERAL]]  
The working directory for the simulation is now %APPDATA%/CODESYS/Simulation.  
CDS-89748 | Bug | CLONE - Precompile errors C0046, C0004, C0080 with applications with Modbus and GPIO's | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.1  
CDS-89707 | Improvement | CLONE - [Object Manager] Support loading project from url | Fixed | [[GENERAL]]  
New interface IProjectLocalPathProvider has been introduced.  
CDS-89626 | Bug | CLONE - CmpLog: ISO 8601 local time, timezone offset for JST is wrong on Linux | Fixed |   
CDS-89625 | Bug | CLONE - UA-AnsiC: Decoding of huge Arrays leads to memory overwrite | Fixed | [[GENERAL]]  
Workaround: Starting from version 3.5.15.0 of the affected products, the incorrect calculation of the buffer size can be avoided if the maximum supported array length of the OPC UA stack of the CODESYS Control runtime system is limited to a value of 10129639 or less.  
  
This can be achieved by adding the following setting in the CODESYS runtime configuration file (e.g. CODESYSControl.cfg):  
[CmpOPCUAStack]  
Stack.MaxArrayLenth=10129639   
  
For more details see CODESAYS Security Advisory 2024-03, which is available on the CODESYS website:  
https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=18355&token=e3e5a937ce72602bec39718ddc2f4ba6d983ccd1&download=  
CDS-89620 | Bug | CLONE - Project recovery cannot be used if codesys is started with project given as command line argument | Fixed |   
CDS-89611 | Improvement | CLONE - Package Manager: Allow installation of older package version | Fixed | [[GENERAL]]  
The prohibition to install older packages over newer ones has been revised. It is again possible to install older versions over newer ones (as it was possible before SP19 Patch 3). The only exception is the CODESYS Licensen Provider Enabler add-on.  
CDS-89610 | Bug | CLONE - Embedded SizeCheck fails on Bookworm build host | Fixed |   
CDS-89512 | Bug | CLONE - Linux SysProcessExecuteCommand(-2) does not close the used pipe if an error occurs | Fixed |   
CDS-89473 | Bug | CLONE - RTS: Security issues in sqlite versions before 3.45.2 | Fixed |   
CDS-89472 | Bug | CLONE - SVG-Renderer: Security issues in OSS versions before (libcurl 8.7.1, zlib 1.3.1, libxml2 2.12.6, Cairo 1.18.0, pixman 0.43.4, libpng 1.6.43, libjpeg-turbo 3.0.2) | Fixed |   
CDS-89471 | Bug | CLONE - Linux RemoteTargetvisu Client (RTV) QT6 : compile errors | Fixed |   
CDS-89470 | Improvement | CLONE - CmpApp: Support network licenses | Fixed |   
CDS-89469 | Improvement | CLONE - CmpCodeMeter: Support network licenses | Fixed |   
CDS-89468 | Improvement | CLONE - ComponentManager: Support network licenses | Fixed |   
CDS-89467 | Bug | CLONE - CODESYSControl: Security issues in Expat versions before 2.6.2 | Fixed |   
CDS-89466 | Bug | CLONE - Compiler: Crash when a Exception occurs in the codeoptimizer | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-89464 | Bug | CLONE - Online mode: "Value" column may be empty after login or is surely empty when switching to "Tabular view" and back to "Textual view" | Fixed |   
CDS-89460 | Bug | CLONE - Compiler: Compile error in existing visu project | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.21.0  
CDS-89389 | Bug | CLONE - SynEdControl: Possibility to suppress special keys | Fixed |   
CDS-89387 | Bug | CLONE - Setup: CODESYS Control Win V3: Move working directory to %APPDATA% | Fixed | [[GENERAL]]  
For more information, see the documentation "CODESYS Installation Extended OEM Adaptions" and CODESAYS Security Advisory 2024-02, which is available on the CODESYS website:https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=18354&token=f3e92a942c3a2f90c272a5ded7598c6a0b5f4924&download=  
CDS-89318 | Improvement | CLONE - TargetSetting - codegenerator/operating-system: Only supported value "Linux" | Fixed | [GENERAL]]  
There is a new target setting "codegenerator\\\systemv-calling-convention".  
For x86-64 code generation only: Use the System V calling conventions.  
Is automatically switched on for codegenerator\\\operating-system='Linux'"  
CDS-89317 | Bug | CLONE - PLCHandler: Wrong PlcSymbolDesc for struct members with DontExpandComplexTypeArrays activated | Fixed |   
CDS-89304 | Bug | CLONE - C0094: Double-click on compiler error does not lead to the error location | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.10  
CDS-89303 | Bug | CLONE - Attribute To_String : not working for enum on VAR_IN_OUT | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.10  
CDS-89236 | Bug | CLONE - CmpRedundancy: AutoSyncEnabled setting doesn't cover re-sync after receiving delayed messages | Fixed |   
CDS-89229 | Bug | CLONE - LongPathFile Exception does not name the file | Fixed | [[GENERAL]]  
IOException names affected file  
CDS-89228 | Bug | CLONE - OnlineChange ist not possible after closing project because of changes in IoConfig_Globals_ModuleList | Fixed |   
CDS-89182 | Improvement | CLONE - MultiCore / VxWorks : CPU load (SysMCGetLoad) implementation | Fixed | [[GENERAL]]  
SysCpuMulticore on VxWorks "SysMCGetLoad_" is now marked as "weak", so own implementations can overload this function.  
CDS-89172 | Improvement | CLONE - CmpRetain: Implement Double Buffering | Fixed | [[GENERAL]]  
CmpRetain now provides a new doublebuffer mechanism for InSRAM/InSHM configurations. Prerequisites: device description targetsetting: report-retain-persistent-update-in-cycle must be set to 1,  
and runtime configuration must be using InSRAM/InSHM and new setting "Retain.DoubleBufferEnabled=1"  
Two new events are also provided. For detailed expert usage see example/template component CmpRetainEvents.  
CDS-89170 | Bug | CLONE - Linux: Compile errors when HilscherCifxLib Feature is used | Fixed |   
CDS-89168 | Bug | CLONE - CODESYS Control Win V3: Low privileged Windows users can modify files in working folder | Fixed | [[GENERAL]]  
The working directories of the affected products are moved to "%APPDATA%\CODESYS\", which is usually located in C:\Users\<user>\AppData\CODESYS\ and can only be accessed by the respective user.  
  
If the PLC is started with the "CODESYS Control Win SysTray PLC Control", it runs in the Windows user account "LocalSystem" and therefore the effective working directory is "C:\Windows\system32\config\systemprofile\AppData\Roaming\CODESYS\" or C:\Windows\SysWOW64\config\systemprofile\AppData\Roaming\CODESYS\\. An administrator account is required to access these folders.   
  
At startup, before the working directory is set, the "CODESYSControlService.exe" and the "GatewayService.exe" write log messages to the Windows Event Log. These can be read in the Windows Event Viewer under "Windows Logs" > "Application" under the details of the logged event.  
  
For more details see CODESAYS Security Advisory 2024-02, which is available on the CODESYS website:https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=18354&token=f3e92a942c3a2f90c272a5ded7598c6a0b5f4924&download=  
  
[COMPATIBILITY_INFORMATION]  
The secured working directory of the ControlWin might have some effects on the behaviour of existing projects using certain features when the ControlWin is executed as a system service:  
* Using ActiveX-Controls in the Targetvisu: If a used ActiveX-Control accesses files from the ControlWin working directory the following effects have to be considered:  
** Readonly access to files is still possible if these are located within $PlcLogic$/$visu$  
** Modifications of these files by the runtime system are not visible to the ActiveX-Control within the Targetvisu  
** Access to files in the working environment outside $PlcLogic$/$visu$ is not possible  
** Workaround: Either locate the according files within $PlcLogic$/$visu$ or run the ControlWin as Windows-User and not as a system service  
* Filetransfer-Feature of the Targetvisu: Filetransfers using the according visualization feature (not streaming) between the Targetvisu and the runtime system no longer work  
** Workaround: Run the ControlWin as Windows-User and not as a system service  
* Placeholder directory redirection for $visu$ or $PlcLogic$/$visu$: Targetvisu will not work correctly and an according log message will be generated  
** Workaround: Remove the placeholder directory redirection or run the ControlWin as Windows-User and not as a system service  
CDS-89141 | Bug | CLONE - Linux: SysFileCopy doesn't work | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
SysFileCopy internally uses SysProcessLinux -> this uses posix_spawn.  
For old libc Versions (< 2.24) posix_spawn uses fork() instead of vfork().  
This is now avoided by setting the flag "USEVFORK" for posix_spawn.  
CDS-89137 | Bug | CLONE - ST Editor System.ArgumentOutOfRangeException | Fixed |   
CDS-89102 | Bug | CLONE - CmpRetain: Retain file from SP12 cannot be loaded with bootapplication SP19 | Fixed |   
CDS-89096 | Bug | CLONE - CmpRedundancy: Possible AccessViolation due to skipped EventPost for vfinit | Fixed |   
CDS-89083 | Bug | CLONE - RTE: OEM licensing does not work | Fixed |   
CDS-89081 | Bug | CLONE - Crash while change setting "Behavior for outputs in stop" | Duplicate | [[GENERAL]]  
This issue duplicates CDS-87637 released with SP20.  
CDS-89080 | Improvement | CLONE - Login dialogs: Improve text of dialogs | Fixed |   
CDS-89078 | Bug | CLONE - Compile: Internal error 2 during OnlineChange | Fixed |   
CDS-89045 | Improvement | CLONE - OPC UA Server: Add additional RtsX509AltName(s) with IpAddress(es) to Certificate | Fixed | [[GENERAL]]  
There is a new security Setting for the OPC UA Server which allows the configuration of IPs used within the OPC UA servers certificate.  
  
[CmpOPCUAServer]  
SECURITY.CertificateIpAddresses  
CDS-88956 | Improvement | CLONE - SysEthernetLinux: Blink Ethernet Adapter LEDs for Linux | Fixed |   
CDS-88955 | Improvement | CLONE - Profinet Certification: Blink Ethernet Adapter LEDs | Fixed | [[GENERAL]] This function causes the orange LED of an Ethernet adapter specified via the Mac address to blink for a certain period of time. The function is only available with certain hardware and only in certain operating systems.  
CDS-88943 | Bug | CLONE - Controls: Deadlock in text editors freezes brand-labelled IDE | Fixed |   
CDS-88875 | Bug | CLONE - Transition Object: wrong language model when Analyzation is activated | Fixed | [[GENERAL]]  
Compiler version higher or equal 3.5.20.10 required.  
In cases where a transition implementation produces multiple statement an explicit assignment to a transition output variable is required, otherwise a new compiler message will be generated.  
CDS-88860 | Bug | CLONE - Possible exception in TabbedViewManager.LoadViews | Fixed |   
CDS-88852 | Bug | CLONE - LibMan: Hidden Library Parameters get reset, when using Library Parameter Editor | Fixed |   
CDS-88851 | Bug | CLONE - LibMan: Library Parameter Editor stores parameter values with incorrect key | Fixed |   
CDS-88850 | Bug | CLONE - Generate Code: Nested structured size not calculated correctly | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.10  
CDS-88849 | Bug | CLONE - Compiler: Internal Error when using GVL Properties | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.10  
CDS-88848 | Bug | CLONE - Unexpected folders are created on connecting to controller | Fixed |   
CDS-88846 | Bug | CLONE - Monitoring: For an FB with a BOOL VAR_IN_OUT “Value of the expression cannot be retrieved” gets shown | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.10  
CDS-88787 | Improvement | CLONE - Linux: SysTaskLinux: sync/starttime mechanism for cyclic SysTasks via setting | Fixed |   
CDS-88785 | Improvement | CLONE - UI: Pause some UI updates while lengthy operations are running | Fixed |   
CDS-88784 | Bug | CLONE - M4 Export: arrays of variable size used in methods are not exported correctly | Fixed | [[GENERAL]]  
CODESYS 3.5.20.1  
CDS-88769 | Bug | CLONE - Find/Replace: some Hot Key Control not working when window is docked | Fixed |   
CDS-88626 | Improvement | CLONE - Message View: Showing the message automatically when messages are added should be suppressable | Fixed | [[GENERAL]]  
There is a new OEMCustomization entry which prevents the message view popup:   
  
Section: MessageView  
Key: SuppressViewOpening  
Type: Boolean  
Effective value: true  
CDS-87124 | Bug | CLONE - Online change: Persistent Variable become 0 after full download application a few times | Won't Fix | [[GENERAL]]  
Error is caused in customer firmware and not in runtime system!  
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2024 CODESYS GmbH  | A member of the CODESYS Group 
