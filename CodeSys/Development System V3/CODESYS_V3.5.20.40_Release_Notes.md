[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS V3.5 SP20 Patch 4

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
CDS-91541 | Improvement | CLONE - [TS_LicensingCodemeter_Network]: Create linux qs target which supports networklicensing | Fixed |   
CDS-91533 | Bug | CLONE - Compile error C0032 from library with no error on lib-check | Fixed |   
CDS-91463 | Bug | CLONE - CmpLog/SysFile: Logmessages in file have a unexpected trailing NULL char | Fixed |   
CDS-91401 | Bug | CLONE - CmpIoMgr: cleanup Buscycle semaphore in case of exception (of IoDrv) | Won't Fix | [[GENERAL]]  
Removed from Patch 4 because of VxWorks TS_Runtime errors.  
CDS-91400 | Bug | CLONE - SysTask / SysTaskLinux: rework end of tasks (also musl libc) | Won't Fix | [[GENERAL]]  
Removed from Patch 4 because of technical risks.  
CDS-91379 | Bug | CLONE - Security issues in CodeMeter versions before 8.20 | Fixed |   
CDS-91378 | Bug | CLONE - Security issues in WibuCmNet versions before 8.20 | Fixed | [[GENERAL]]  
WibuCmNet has been updated to 8.20.6539.500.  
CDS-91354 | Bug | CLONE - CmpRedundancy.library: Remove license request to productcode=0 | Fixed |   
CDS-91336 | Bug | CLONE - TargetVisu: Security issues in Qt versions before 6.7.3 | Fixed |   
CDS-91335 | Bug | CLONE - SVG-Renderer: Security issues in OSS versions before (libxml2 2.13.4, libcurl 8.10.1, Cairo 1.18.2, libpng 1.6.44, libjpeg-turbo 3.0.4) | Fixed |   
CDS-91334 | Bug | CLONE - CODESYSControl: Security issues in Expat versions before 2.6.3 | Fixed |   
CDS-91333 | Bug | CLONE - CmpOpenSSL: Security issues in OpenSSL versions before 3.2.3 | Fixed |   
CDS-91332 | Bug | CLONE - Download ends with an “Invalid result package”. | Cannot Reproduce |   
CDS-91331 | Bug | CLONE - M4 Export - Order of typedefs in M4 unstable (for Properties) | Fixed |   
CDS-91330 | Bug | CLONE - FB with EN/ENO has compile errors if used in a Transition | Fixed |   
CDS-91329 | Bug | CLONE - Security issues in System.Data.SQLite.Core versions before 1.0.119.0 containing sqlite 3.46.1 | Fixed |   
CDS-91275 | Bug | CLONE - ObjectManager: Profile information is just limited to V3 projects | Fixed | [[GENERAL]]  
New interface IProjectFormatProfileSupport has been introduced.  
CDS-91274 | Bug | CLONE - PLCopenXML import does not work as expected | Fixed |   
CDS-91273 | Bug | CLONE - Persistent Variables: Data type of the mapped variable does not match the original data type | Won't Fix | [[GENERAL]]  
To fix the issue a substantial rework in the compiler was necessary. Two regression issues occured. On the other hand, there is a workaround to avoid the problem.  
A patch without full regression testing is too dangerous.  
CDS-91272 | Bug | CLONE - CmpOPCUAClient: Crash when server closes socket before responses of discovery service returns | Fixed |   
CDS-91225 | Improvement | CLONE - IEC task start time: Configuration from IEC code | Won't Fix | [[GENERAL]]  
\- New IEC CmpIecTask.library functions available to set and get IEC task offset  
\- Only supported for linux targets yet! Has no effect on other platforms!  
  
FUNCTION IecTaskSetStartOffset : RTS_IEC_RESULT  
VAR_INPUT  
/// IEC task name  
sIecTaskName : STRING;  
/// Start offset in milliseconds from calculated task start  
startOffsetUs : DINT;  
END_VAR  
CDS-91210 | Bug | CLONE - Simulation: Wrong device identification is used for reading custom online device/application guids | Fixed |   
CDS-91209 | Bug | CLONE - compile_m4.py: Convert m4 => h: misplaced #endif of #ifdef CPLUSPLUS | Fixed |   
CDS-91203 | Bug | CLONE - Linux: Exception in SysProcessExecuteCommand2 | Fixed |   
CDS-91202 | Improvement | CLONE - CODESYSControl ComponentManager: safe mode should be configurable, disable if required | Fixed | [[GENERAL]]  
Added features to specify the behavior of the safemode:  
\- SafeMode_Shutdown - If the safemode is triggered, the runtime will shut down in the next comm cycle.  
\- SafeMode_Disable - The safemode does not have any effect. But still, a log message with LOG_EXCEPTION is sent.  
CDS-91201 | Bug | CLONE - SysCpuHandling X64 Windows: mitigation for split-lock effect needed in SysCpuTestAndSetBit() | Fixed |   
CDS-91169 | Bug | CLONE - Deviceobject: Import of Default values for array does not work | Fixed |   
CDS-91168 | Bug | CLONE - CmpRedundancy : Mode SIMULATION (forced by setting) cannot be left | Fixed |   
CDS-91164 | Bug | CLONE - CODESYS Control Runtime: Communication channels are not freed in rare cases | Fixed |   
CDS-91159 | Bug | CLONE - m4 Export : IEC construct ALIAS / Type not supported | Fixed |   
CDS-91144 | Bug | CLONE - Wrong value is monitored when using GVL with same name in pool and app | Won't Fix | [[GENERAL]]  
To many changes area required for this fix, since having multiple GVLs with the same name and same variables is untypical and the workaround makes the project easier to understand anyway, we decided to not patch this issue.  
CDS-91096 | Bug | CLONE - SysCpuHandling X64 VxWorks: mitigation for split-lock effect needed in atomic functions | Cannot Reproduce |   
CDS-91095 | Bug | CLONE - CmpRedundancy: Race condition in exception handling during startup | Fixed |   
CDS-91094 | Bug | CLONE - SysCpuHandling X64 RTE: mitigation for split-lock effect needed in SysCpuTestAndSetBit() | Fixed |   
CDS-91093 | Bug | CLONE - SysCpuHandling X64 Linux: mitigation for split-lock effect needed in atomic functions | Fixed |   
CDS-91075 | Improvement | CLONE - Use Geometry() of display directly without rotation | Fixed |   
CDS-91074 | Bug | CLONE - Linux: sporadic Access Violation on Reset after OS Exception | Duplicate | [[GENERAL]]  
Duplicate of CDS-91400  
CDS-91073 | Bug | CLONE - Vxworks (LLVM, X86) : When using IEC marker (exception info) a bad register save area is used | Won't Fix | [[GENERAL]]  
Is reverted because of the upcoming regression CDS-91734.  
This jira could be isolated as the originator of the regression!  
CDS-91072 | Bug | CLONE - CmpCodeMeter: Disconnect and connect a CmRuntime does not reconnect licenses | Fixed |   
CDS-91027 | Bug | CLONE - Confusing error message for online change of variable type at direct location | Fixed | [[GENERAL]]  
Fixed with compiler version >= 3.5.20.40  
CDS-91026 | Bug | CLONE - Compiler: Compile error on Online Change when adding variable to FB which contains array with variable length | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.40  
CDS-90901 | Improvement | CLONE - License Metrics Screen: must warn about other potentially required licenses | Fixed |   
CDS-90900 | Bug | CLONE - Different views and instances while monitoring, no data online | Fixed |   
CDS-90899 | Bug | CLONE - Change to tabular view ends in exception when three backslashes are used for comments | Fixed |   
CDS-90898 | Bug | CLONE - Method bigger 80000 lines throws an exception | Fixed |   
CDS-89676 | Bug | CLONE - [Proxy] CDS crash if you use Proxy with certificates | Fixed |   
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2024 CODESYS GmbH  | A member of the CODESYS Group 
