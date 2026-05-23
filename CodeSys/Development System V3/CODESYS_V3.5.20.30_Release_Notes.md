[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS V3.5 SP20 Patch 3

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
CDS-90934 | Bug | CLONE - CmpCodeMeter: Disconnect and connect a CmRuntime does not reconnect licenses | Cannot Reproduce | [[GENERAL]]  
Issue cannot be reproduced.  
CDS-90918 | Bug | CLONE - M4 Export - Order of typedefs in M4 file is unstable for interface sub-elements | Fixed |   
CDS-90916 | Bug | CLONE - PLCopenXML with AddDataProvider can't export explicit connector types | Fixed |   
CDS-90896 | Bug | CLONE - Update Compiler Version: wrong order of execution | Fixed |   
CDS-90874 | Bug | CLONE - Compile: Internal error 2 during OnlineChange | Fixed | [[GENERAL]]  
Fixed for CompilerVersion >= 3.5.20.30  
CDS-90872 | Bug | CLONE - Precompile error - data type conversion | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.30  
CDS-90871 | Bug | CLONE - IntelliSense not working at Conversion Function | Won't Fix | [[GENERAL]]  
An open regression prevents the patch integration.  
CDS-90783 | Improvement | CLONE - CmpCodeMeter: Online Service to transport UsagePeriod, ExpirationTime and MaintenancePeriod of licenses | Fixed |   
CDS-90742 | Bug | CLONE - Security issues in CodeMeter versions before 8.10a | Won't Fix | [[GENERAL]]  
Due to an bug in version 8.10a of the CodeMeter runtime, the update will not be carried out.  
CDS-90735 | Bug | CLONE - [Dev+Test] Transition Object: erroneuos code for SFC analyzation | Fixed |   
CDS-90734 | Bug | CLONE - Project Compare: Clicking Backspace leads to exception | Fixed |   
CDS-90732 | Improvement | CLONE - PROFIsafe: Interface for Data Exchange | Fixed |   
CDS-90710 | Improvement | CLONE - SysSocketLinux: replace select with poll | Fixed | [[GENERAL]]  
  
On Linux select is limited to less than 1024 file descriptors.   
Because of that we added the Option to use poll() for SysSocketSelect which does not have these limitations.   
  
Per default select() will be used.  
  
There is a new setting to switch to the new Implementation using poll():  
  
/**  
* <category>Settings</category>  
* <type>Int</type>  
* <description>  
* You can specify whether select() or poll() should be used for SysSocketSelect. On Linux select is limited to less than 1024 file descriptors.  
* 0: Use poll()  
* 1(DEFAULT): Use select()  
* </description>  
*/  
CDS-90636 | Bug | CLONE - Gateway SysTray: Config mode cannot be activated - hint for manual activation necessary | Fixed |   
CDS-90613 | Bug | CLONE - Compiler: Changed initial values of VAR_Inst are not updated on Download | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.30  
CDS-90607 | Bug | CLONE - SysTaskVxWorks.c : Add NULL pointer check | Fixed |   
CDS-90606 | Bug | CLONE - Generate Code: Generate Code leads to freeze for project with specific ST POU with 6700 lines of code | Fixed |   
CDS-90605 | Improvement | CLONE - ComponentManager: Probe for latest GAC version if exact is missing | Won't Fix | [[GENERAL]]  
After investigation, the problem which led to this clone-issue is not associated with the component manager. Therefore, this a clone-issue is not required any more.  
CDS-90604 | Bug | CLONE - Non-escaped characters in description field causes import/export of csv to fail | Fixed |   
CDS-90558 | Improvement | CLONE - [Object Manager] Report unconsolidated changes to the project format | Fixed | [[GENERAL]]  
IProjectFormat2 interface has been introduce to process an unconsolidated list of changes.  
CDS-90557 | Bug | CLONE - CmpIecVarAccess: Possible very rare crash when writing values during OnlineChange | Fixed |   
CDS-90549 | Bug | CLONE - CmpWebServer: WebServerReadRequest() - Exception caused, if the number of bytes read is -1 | Fixed | [[GENERAL]]  
For more details see CODESYS Security Advisory 2024-05, which is available on the CODESYS website:  
https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=18604&token=d5e1e2820ee63077b875b3bb41014b1f102e88a3&download=  
CDS-90548 | Bug | CLONE - LibMan, Scripting: call of add_placeholder results in Namespace set to NOTIMPLEMENTEDBYDEVICE | Won't Fix | [[GENERAL]]  
This is a scripting issue and can only be fixed in the scripting package.  
CDS-90531 | Improvement | CLONE - CmpRetain: Setting needed to clear SRAM once at startup | Fixed | [[GENERAL]]  
\- New setting to initialize SRAM at next bootup:  
[CmpRetain]  
Retain.SRAM.InitAtFirstBoot=1  
=>Is set to 0 after first reboot!  
  
\- If bootproject is not an offline bootproject (a bootproject copied from another PLC), you have to specify a second setting, that the RETAINs must be initialized:  
[CmpApp]  
Bootproject.RetainMismatch.Init=1  
CDS-90530 | Bug | CLONE - RepositoryLocation.ini: Relative paths are not working after project open | Fixed |   
CDS-90529 | Bug | CLONE - CmpIecTask C++ Runtime: IEC exception calling IecTaskGetWatchdogHitCount from IEC | Fixed |   
CDS-90476 | Bug | CLONE - Runtime Toolkit Templates - Linux Makefile(s) incomplete and not working | Fixed |   
CDS-90475 | Bug | CLONE - Resolve conflict crash codesys when use 3-way merge view | Fixed |   
CDS-90474 | Improvement | CLONE - [PackageManagerCLI] Support signing packages with certificate thumbprint | Fixed | [[GENERAL]]  
PackageManagerCLI does now support the signing of packages with a certificate from the certificate store of the current user.  
CDS-90473 | Bug | CLONE - CmpApp: Timeout at OnlineChange is not handled correctly | Fixed |   
CDS-90472 | Bug | CLONE - LibDoc: Malformed table error cannot be identified | Fixed |   
CDS-90357 | Bug | CLONE - Security issues in CodeMeter versions before 8.10a | Duplicate | [[GENERAL]]  
Duplicates CDS-90742  
CDS-90356 | Improvement | CLONE - CmpLog: Support of dynamic logger string length | Fixed |   
CDS-90270 | Bug | CLONE - Security issues in WibuCmNet versions before 8.10a | Fixed | [[GENERAL]]  
CODESYS uses now the version 8.10a of the WibuCmNet assembly.  
CDS-90204 | Improvement | CLONE - CmpIecVarAccess: Setting to limit the number of variable lists | Fixed |   
CDS-90203 | Bug | CLONE - Import PLCOpenXML: Importing a function block with VAR_GENERIC leads to error | Fixed |   
CDS-90202 | Bug | CLONE - VxWorks: High cpu load caused by SysEthernetGetPortConfigAndStatus() | Fixed | [[GENERAL]]  
Settings are now read only once at first call of SysEthernetGetPortConfigAndStatus()  
CDS-90162 | Bug | CLONE - CmpDevice session timouts for SIL3 protocol handler | Fixed |   
CDS-90161 | Improvement | CLONE - Prepare Value Dialog: Insert a String without ' at the begin and end does not work | Fixed |   
CDS-90158 | Bug | CLONE - Compiler: Internal error in CompilerPhase2_AfterTypification.CheckCallRecursionRecursive | Fixed | Compiler Version >= 3.5.20.30  
CDS-90126 | Improvement | CLONE - SysMemVxWorks.c : Remove or adapt superflous log message | Fixed |   
CDS-90029 | Improvement | CLONE - API or Hook needed to replace the CODESYS message "Selected target system is different from the connected device....." | Fixed | [[GENERAL]]  
Added a new Customization Hook with Section="OnlineManager" and Key="TargetMismatchHandler" and Type=Func<_3S.CoDeSys.Core.Online.TargetMismatchException2, bool>.  
Instead of showing an error message, perform custom behavior for a TargetMismatchException. Return true, if the exception was handled. Return false, if the original error message should be displayed.  
CDS-89968 | Improvement | CLONE - RunTime Security: Add logs when there are errors with application Signing or Encryption | Fixed |   
CDS-89749 | Improvement | CLONE - CmpIecTask: Add counters for lost cycles in Task_Desc structure | Fixed | [[GENERAL]]  
\- New C- and IEC interface functions to get lost cycle counters:  
RTS_RESULT CDECL IecTaskGetOmittedCycleCounters(RTS_HANDLE hIecTask, IecTaskOmittedCycleCounters *pOmittedCycleCounters);  
\- Worked only on targets with full CmpSchedule and the activated feature "IecTask.OmittedCycleInfos.xml"  
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2024 CODESYS GmbH  | A member of the CODESYS Group 
