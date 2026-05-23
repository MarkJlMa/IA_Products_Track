[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Product: CODESYS V3.5 SP19 Patch 2

Key  |  Issue Type  |  Summary  |  Resolution  |  Release Note   
---|---|---|---|---  
CDS-86288 | Bug | CLONE - GUID Object error, when performing a 'clean all' operation with a open common library element element | Fixed |   
CDS-86207 | Bug | CLONE - RTE: SysEthernet: CmpEt1000Drv: i219 LM does not work correctly . | Fixed |   
CDS-86153 | Bug | CLONE - SymbolConfiguration: Exception while accessing a variable of packed structure (with pack_mode:1 attribute) | Won't Fix | [[GENERAL]]  
Cannot be fixed in CODESYS and must be fixed in the Communication Addon since the symbol configuration is located there. (COMM-625)  
CDS-86150 | Bug | CLONE - AppBasedLicenses: Validation failed at standard onlinechange | Fixed |   
CDS-86148 | Bug | CLONE - TextDocument: Empty ST after opening an SP17 project and directly using "Save as..." without modification | Fixed |   
CDS-86128 | Bug | CLONE - Compiler: "C0032: Cannot convert type 'DINT' to type 'INT'" message appears with customer project | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.20  
CDS-86084 | Bug | CLONE - DeviceObject: upgrade storage format window is shown by mistake | Fixed |   
CDS-86062 | Bug | CLONE - Devices Repository: Install-Device-Description (Automatic detection) always uses default converter | Fixed |   
CDS-86061 | Bug | CLONE - Intellisense does not work properly with variables written after a bracket | Fixed |   
CDS-86032 | Bug | CLONE - ST: For each new line, which is entered within a region, an increased number of tabs is added | Fixed |   
CDS-86007 | Bug | CLONE - RTE: No Link with 4-Wire Ethernet Cable | Fixed |   
CDS-85990 | Bug | CLONE - SVG-Renderer: Update OSS to latest versions (libcurl 8.1.2) | Fixed |   
CDS-85989 | Bug | CLONE - WebBrowserIntegration: LibDoc not shown in LibMan with OEM customized homepage | Fixed |   
CDS-85988 | Bug | CLONE - WebBrowserIntegration/Store: Without network CPU load goes to 100% | Fixed |   
CDS-85987 | Bug | CLONE - Compile: Internal error occurs during build | Fixed | [[GENERALL]]  
Compiler Version >= 3.5.19.20  
CDS-85986 | Bug | CLONE - CODESYS Control: Authenticated DoS vulnerabilities in CODESYS protocol servers | Fixed | [[GENERAL]]  
For more details see Advisory 2022-05, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17765&token=04e117e1408fdb8e02b4bc821aa3be819668aef4&download=  
CDS-85977 | Bug | CLONE - Build error C0332 without explainable reason | Fixed | [[GENERAL]]  
With the target setting "codegenerator\\\check-multiple-task-output-write" a check is performed whether the same byte is updated in different tasks.  
This check was wrong and could produce wrong error messages without clear indication.  
The only workaround is not to use the target setting.  
With this bugfix and Compiler Version >= 3.5.19.20, the check should be working as intended.  
CDS-85975 | Bug | CLONE - NetVar: Variables of extended types are not transmitted | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.2  
CDS-85857 | Bug | CLONE - App Based License: __ValidateLicenseMetrics is not called in onlinechange | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.20 and runtime version >= 3.5.19.20  
CDS-85851 | Bug | CLONE - RTS, Targetvisu: Memory leak in Overlay-Targetvisu | Fixed |   
CDS-85845 | Improvement | CLONE - CmpCodeMeter: minimal required version of CodeMeter Runtime should be configurable | Fixed |   
CDS-85809 | Bug | CLONE - Project Import: Command does not work, if InstallerIntegration plugin is missing | Fixed |   
CDS-85800 | Improvement | CLONE - CmpIecVarAccess: Add new API RTS_BOOL IecVarAccIsReference | Fixed |   
CDS-85787 | Bug | CLONE - Edit Object (offline): Command does not work – modification not possible | Fixed |   
CDS-85786 | Bug | CLONE - Notification Center: Potential remote code execution | Fixed | [[GENERAL]]  
For more details see Advisory 2022-07, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17767&token=7ed2d9324eff98a0a319c455d0256dc7627c705e&download=  
CDS-85766 | Bug | CLONE - DeviceObject: Exception in method LanguageModelMgr_CodeChanged when called within non primary project | Fixed |   
CDS-85765 | Bug | CLONE - Generate Code: DINT variable initialization via constants multiplication leads to build error | Duplicate | [[GENERAL]]  
Duplicate of CDS-86128  
CDS-85764 | Bug | CLONE - Generate Code: Internal error on project | Duplicate | [[GENERAL]]  
Duplicate of CDS-86128  
CDS-85759 | Bug | CLONE - Runtime: Exceptions in (asynchronous) GlobalInit handled incompletely | Fixed |   
CDS-85742 | Bug | CLONE - Flow Control does not work with instances called in different tasks | Won't Fix | [[GENERAL]]  
For flow control, it is necessary to know in which task the code to flow is running. The compiler calculates for each variable in which tasks it is accessed. An array however, is only one variable and if the individual elements in an array are accessed in different tasks, this will be considered to be a property of the array to be accessed in different tasks.  
Typically an array element is accessed within a loop with loop index variable i, and it is not possible to derive individual task accesses for each element in an array.  
If you have an array with elements that are only used explicitly with concrete indices 1, 2, 3, then you should consider using individual variables.  
However, CDS-85927 adresses this problem. With this issue, the user is prompted to select a task for flow control, and they can change the task to flow a POU.  
CDS-85738 | Bug | CLONE - Project Information, Last Saved with: the entry "Last Saved with" is only updated at Save As, but not at Save | Fixed | [[GENERAL]]  
This fix just replaces the string "Last saved with" with "Storage format" in the UI. The value will not be changed because the value displays the storage format and has no direct relationship to the exact version of CODESYS that was used for saving the file for the last time. There will be an additional documentation for this in the online help to clarify the situation for the end user (CDS-86082).  
CDS-85695 | Bug | CLONE - Linux SysOut / SysFile: wrong log class in LogAdd2 leads to unnecessary log messages | Fixed |   
CDS-85691 | Bug | CLONE - CmpApp: Reset on breakpoint w/o finish cycle leads to watchdog exception | Fixed | [[GENERAL]]  
Accident because of CDS-76248  
CDS-85689 | Improvement | CLONE - NBS: Provide a PingRequest function block | Fixed |   
CDS-85612 | Bug | CLONE - SysCpuMulticore linux: Crash in case of restricted cores with cgroups/containers | Fixed |   
CDS-85609 | Bug | CLONE - CmpMonitor2: Value of Device Parameters > 768 Bytes is invalid | Fixed |   
CDS-85608 | Bug | CLONE - Visu: Input Assistant shows local variables of abstract function block marked with „conditionalshow_all_locals” | Won't Fix | [[GENERAL]]  
This issue will not be fixed for 3.5.19.20 because the problem is located in the AddOn CODESYS Visualization. Therefore the bugfix will be released with the fix version of VIS-3237  
CDS-85606 | Improvement | CLONE - CmpMemGC: SystemTrace needed to check memory consumption on runtime per component | Fixed | [[COMPATIBILITY_INFORMATION-EndUser]]  
Memory trace can be activated with the following setting in the cfg-file:  
[CmpMemGC]  
EnableMemTrace=1  
  
=>You can upload a device trace named "MemGCTrace" to see global heap memory usage, delta global heap memory usage and heap memory usage per component:  
\- Add a trace object right under the device  
\- Menu command "Trace\Upload trace"  
\- Select "MemGCTrace"  
\- Command "Upload"  
  
[[COMPATIBILITY_INFORMATION-OEM]]  
Trace code can be disabled with the following compiler switch:  
#define MEMGC_DISABLE_MEM_TRACE  
CDS-85605 | Bug | CLONE - Boot Application: Switching application from unencrypted to encrypted does not provoke Boot App update | Fixed |   
CDS-85595 | Bug | CLONE - CmpTraceMgr: Missing Trace entries | Won't Fix | [[GENERAL]]  
Investigation shows that there are no lost values in trace buffer but a delayed entry. But this is not a problem of the runtime system and there is no chance to check this.  
CDS-85589 | Improvement | CLONE - Enable usage of memory reserve for POUs allocatable using __NEW | Fixed |   
CDS-85588 | Bug | CLONE - It is no longer possible to set constant variables in the libraries via python script | Won't Fix | [[GENERAL]]  
Issue will be fixed in a new scripting release, so no patch is necessary.  
CDS-85554 | Improvement | CLONE - Fast online change: compile errors might prevent consequent fast online changes | Won't Fix | [[GENERAL]]  
Though the problem seems simple, the changes needed to fix it are too complex to safely patch.  
CDS-85501 | Bug | CLONE - Breakpoint cannot be set/removed in method of nested libraries | Won't Fix | [[GENERAL]]  
The problem is not new and only occurs in very special circumstances. There is a simple workaround since breakpoints can be set / removed with the breakpoint view.  
On the other hand, to fix the bug the code needed to be reworked in several files. The danger of accidents is high. A patch without full test would be risky => won't fix  
CDS-85492 | Bug | CLONE - Installer Integration: Resolving path to installer executables considers working directory | Fixed | [[GENERAL]]  
For more details see Advisory 2022-06, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17766&token=667d36292e99e6f6b7eb8c0b4a86d27137c31f98&download=  
CDS-85491 | Bug | CLONE - IoDrvSafetySP: with some projects the logical exchange GVL do not exchange data | Fixed |   
CDS-85461 | Bug | CLONE - Compile error unitialized variable after update to 3.5.18.0 | Fixed | [[GENERAL]]  
The use of a reference or a pointer or an interface to an uninitialized variable to initialize a variable will produce a warning with Compilerversion >= 3.5.19.20  
So in some cases (interfaces) existing projects may produce now a warning instead of an error. In other cases (pointer, references) existing projects may now produce new warnings.  
CDS-85460 | Bug | CLONE - Frame: No Trace values shown on Logout when Trace window undocked | Fixed |   
CDS-85459 | Bug | CLONE - CmpSessionInformation: Integration into FW based on C++ RunTime does not work | Fixed |   
CDS-85455 | Bug | CLONE - Property call returns wrong value if Property contains CASE with empty ELSE branch | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.20  
CDS-85412 | Improvement | CLONE - SysCpuHandlingLinux.c: ARM32/THUMB/??/ does not build with GCC11 | Fixed |   
CDS-85411 | Bug | CLONE - Using "INTERNAL" in declaration and using tabular view works not correct | Fixed |   
CDS-85407 | Bug | CLONE - Targetvisu, Overlay: mouse click executed within the wrong image object | Fixed |   
CDS-85153 | Bug | CLONE - Access Violation in EtherCAT_Task if network is set down | Fixed |   
CDS-85139 | Bug | CLONE - Project Compare: Invalid GUID exception, when comparing 2 independent projects, where the right one contains a Trace | Won't Fix | [[GENERAL]]  
Won't fix because the behaviour (opening editor of object of compared project) is "as designed" (introduced with CDS-51949) and the problem must be fixed in the Trace addon  
CDS-84746 | Improvement | CLONE - Scan Network/Communication Editor: Allow disabling Update non matching devices use case | Fixed |   
CDS-84600 | Bug | CLONE - Importing Project User Rights is vulnerable to brute force attack | Fixed | [[GENERAL]]  
For more details see Advisory 2022-08, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17768&token=9d206ea9e0449cd9d3ee60d5179d2761dad2d2dd&download=  
CDS-83797 | Bug | CLONE - IecCoreSetOverwrite event doesn't work anymore | Fixed |   
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2023 CODESYS GmbH  | A member of the CODESYS Group 
