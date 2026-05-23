[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS V3.5 SP22 Patch 2

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
CDS-98093 | Bug | CLONE - SVG-Renderer: Security issues in OSS versions before (Libxml2 2.15.3, libpng 1.6.58, libcurl 8.20.0, zlib 1.3.2) | Duplicate |   
CDS-97998 | Improvement | CLONE - [Setup]: Replace package "CODESYS Redundancy" with "CODESYS Redundancy Configuration"" | Fixed |   
CDS-97985 | Improvement | CLONE - Transition Object: Allow external handling of Analyzation Feature | Fixed |   
CDS-97963 | Bug | CLONE - Linux: Compile error if SYSMEM_EXTERNAL is defined | Fixed |   
CDS-97962 | Bug | CLONE - Compiler: Suppression of warnings does not correctly work for precompile | Fixed |   
CDS-97961 | Improvement | CLONE - GfxEdControl: Enable Horizontal Scrolling with <Shift> \+ Mouse Wheel in the Editor Window | Fixed | [[KNOWN_LIMITATIONS]]  
The improvement will become effective in the affected graphical editors only with a future update that adds the corresponding support.  
CDS-97951 | Bug | CLONE - SVG-Renderer: Security issues in OSS versions before (Libxml2 2.15.3, libpng 1.6.57, libcurl 8.19.0, zlib 1.3.2) | Fixed |   
CDS-97949 | Bug | CLONE - [Installation Migration] Backup uninstalls package references | Fixed | [[GENERAL]]  
During installation migration the retained packages will be uninstalled without reference uninstallation.  
CDS-97948 | Bug | CLONE - DeviceObject: Bit-Channels at device are not created when the EtherCAT-Master is plugged into a Slot | Fixed |   
CDS-97929 | Bug | CLONE - CmpRedundancy: AutoSync unexpected behavior in special case | Fixed |   
CDS-97916 | Bug | CLONE - Ignore Retain on bootup for secondary PLC | Fixed |   
CDS-97915 | Bug | CLONE - CmpRedundancy: AutoSync always forces PLC_ID2 to standby | Fixed |   
CDS-97889 | Bug | CLONE - CODESYSControl: Security issues in Expat versions before 2.7.5 | Fixed |   
CDS-97888 | Bug | CLONE - CmpOpenSSL: Security issues in OpenSSL versions before 3.5.6 | Fixed |   
CDS-97887 | Bug | CLONE - Persistent Variable behavior changed on SP21 when clean all: Data deleted without notice to user | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.22.20  
CDS-97886 | Bug | CLONE - Compile: Internal Error with Initialization 1.0 / 0.0 | Fixed |   
CDS-97864 | Bug | CLONE - Compiler: Property with only Set accessor of type REFERENCE TO struct leads to compile error | Fixed |   
CDS-97863 | Bug | CLONE - Exception with TICKU.GetElapsedTimeInUSec | Fixed |   
CDS-97862 | Bug | CLONE - IConstantEvaluator.Evaluate is not working as before. | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.20  
CDS-97861 | Bug | CLONE - Deleting objects from LibraryProjects doesnt work in go! | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.2  
CDS-97858 | Bug | CLONE - Engine: Crash to desktop (stack overflow) in certain scenario | Fixed | [[GENERAL]]  
Fixed crash from a stack overflow. It is caused by calling IEngine.InvokeInPrimaryThread(Delegate, false) from the primary thread too many times in a short time frame.  
CDS-97857 | Bug | CLONE - RawSTParser: Error parsing string with special characters | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.20  
CDS-97843 | Bug | CLONE - CmpRetain: Retain area is not initialized on download, when using Retain.DoubleBufferEnabled. Resulting in loss of retains | Fixed |   
CDS-97746 | Bug | CLONE - CmpCodeMeter: infinite loop if more than 16 Wibu Containers on hardware | Fixed |   
CDS-97744 | Bug | CLONE - Compiler: double allocation of retain and persistent variables when retain in cycle is used | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.22.20  
CDS-97704 | Bug | CLONE - User Management, Import: Import leads to endless Credential prompt with disabled Device User Management | Fixed |   
CDS-97702 | Bug | CLONE - RawST: Issues if two objects have the same name | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.20  
CDS-97701 | Bug | CLONE - Precompile context, FindSubelements throws an NullReferenceException in customer specific library | Fixed |   
CDS-97651 | Bug | CLONE - Disconnect Edge Gateway not possible, because the Edge Gateway instance may crash | Fixed |   
CDS-97608 | Improvement | CLONE - CmpRedundancy: Add tag in online service to transmit redundancy error | Fixed |   
CDS-97607 | Bug | CLONE - RawSTParser: implicit symbols cannot be used in implementation | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.20  
CDS-97585 | Bug | CLONE - Internal error and compile error when calling functions with ANY inputs | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.22.20  
CDS-97533 | Bug | CLONE - Compile: Access Violation with __Currenttask-Operator | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.20  
We could analyse the situation of the crash and found that a reference from a function using the __CurrentTask-operator and an implicit function necessary to detect the current task id got lost. This situation probably occurs after a special combination of online changes. We were not able to reproduce the problem, though.  
We try to fix the problem by moving the cross refernce-linking to an earlier compile stage and are confident, that the situation will no longer occur.  
CDS-97531 | Bug | CLONE - Linux SysProcessExecuteCommand2: sporadic Exception (SIGABRT) | Fixed |   
CDS-97524 | Bug | CLONE - LacUtil: Exception during LAC installation prevents references from being installed | Fixed | [[GENERAL]]  
The LacUtil executable now features improved error handling for reference installations. If an error occurs in this context, the return value 3 will be returned.  
Since the original issue was caused by a referenced GAC installation that resulted in a target path exceeding 260 characters, LacUtil is now capable of handling long paths correctly.  
  
[[KNOWN_LIMITATIONS]]  
LACUtil.exe will not start if the path <RootFolder>\LacBinaries\GAC_MSIL\Utilities\3.5.23.0__83380e73b2486719\Utilities.dll is longer than 260 characters. .Net internal loading from redirected paths does not work with long paths as well.  
  
[[COMPATIBILITY_INFORMATION]]  
LACUtil.exe now has new dependencies on Utilities.dll and PInvoke.dll, according to the assembly redirects placed in the LacBinaries folder.  
LACUtil.exe works well within the Common directory. If it is used outside a CODESYS installation, both referenced DLLs must be copied along as well. Additionally, the LACUtil.exe.config file must be deleted.  
CDS-97522 | Improvement | CLONE - [LongPath Utilities] Support long paths for time operations | Fixed |   
CDS-97521 | Bug | CLONE - Project Compare: Commit Device Changes makes Device unusable | Won't Fix | [[GENERAL]]  
Too risky for a patch as changes in device object is required. Without a full regression test it is to dangarous -> won't fix  
CDS-97469 | Bug | CLONE - CmpSchedule: Unexpected Watchdog Timeout exceptions | Fixed |   
CDS-97463 | Bug | CLONE - Incorrect message in the use case that a device does not support any boot project at all | Fixed | [[GENERAL]]  
The additional warning introduced for CDS-85812 will no longer be shown for devices that do not support a boot application.  
It will also not be shown when the simulation mode is active for a device.  
CDS-97461 | Bug | CLONE - Message View: Project with EnternetIP leads to exception | Fixed |   
CDS-97457 | Bug | CLONE - Compiler/Codex86-64: Internal error, Null Reference Exception compiling project assigning to __SYSTEM.VAR_INFO in input | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.20  
CDS-97456 | Bug | CLONE - IntelliSense: REF= does not work correctly with intellisense | Fixed |   
CDS-97454 | Bug | CLONE - AutoDeclare SmartTags are not correctly displayed for instance variables | Fixed |   
CDS-97124 | Bug | CLONE - WebVisu: Connection refused caused by cached redirect responses in the browser | Fixed |   
CDS-97123 | Bug | CLONE - DynamicTextChangeLanguage does not update the language in the visu | Won't Fix | [[GENERAL]]  
[[COMPATIBILITY_INFORMATION]]  
With CODESYS V3.5 SP20 we have introduced the feature client independent language switching (see CDS-42991 Visu, WebVisu: The language in the visualization should be clientspecific)  
  
The function CmpDynamicText.DynamicTextChangeLanguage cannot be used anymore to correctly update the language in the visualization.  
  
Instead assignments to VisuElems.CURRENTLANGUAGE must be used:  
VisuElems.CURRENTLANGUAGE := sNewLanguage; // Switches the language in all visualization clients  
CDS-97099 | Improvement | CLONE - AddOn Check for PLCNext module should be removed | Fixed |   
CDS-97097 | Bug | CLONE - CmpHilscherCIFX: Exception in GlobalInit if wrong card is configured | Fixed |   
CDS-97016 | Bug | CLONE - IntelliSense: Does not work correctly in array declarations | Fixed |   
CDS-97015 | Bug | CLONE - PLCOpen Import: Importing a xml exported from a LD POU results in compile warnings or import failing | Won't Fix | [[GENERAL]]  
This issue was fixed within the LDFBD addon with LDFBD-461. So there is nothing more to do for it in essentials.  
CDS-96159 | Bug | CLONE - Editor: Login leads to a nervous and flickering declaration part | Won't Fix | [[GENERAL]]  
This issue was rated as too risky for the current patch  
  
 

CODESYS AddOns  |  Version   
---|---  
CODESYS Automation Server Connector | 1.38.0.0  
CODESYS Base Libraries | 4.0.1.0  
CODESYS SoftMotion | 4.20.2.0  
CODESYS Security Agent | 1.4.0.0  
CODESYS Core Dump | 4.2.0.0  
CODESYS Code Generator ARM | 4.0.3.0  
CODESYS Code Generator ARM64 | 4.0.1.0  
CODESYS Code Generator Cortex M3 | 4.0.2.0  
CODESYS Code Generator PowerPC | 4.0.2.0  
CODESYS Code Generator TriCore | 4.0.1.0  
CODESYS Compiler Versions Archive | 4.0.0.0  
CODESYS Communication | 4.7.0.0  
CODESYS RISC Front End | 4.0.2.0  
CODESYS Target Settings Export | 4.0.0.0  
CODESYS Trace | 4.4.0.0  
CODESYS IO-Link | 4.3.0.0  
CODESYS Safety Support | 4.1.0.0  
CODESYS Redundancy Configuration | 4.3.0.0  
CODESYS NetX | 4.1.0.0  
CODESYS Memory Tools | 4.1.0.0  
CODESYS Modbus | 4.5.1.0  
CODESYS Ethernet Adapter | 4.2.0.0  
CODESYS EtherCAT | 4.11.0.0  
CODESYS CANopen | 4.3.0.0  
CODESYS EDS Import | 4.3.0.0  
CODESYS EtherNetIP | 4.9.0.0  
CODESYS PROFIBUS | 4.2.0.0  
CODESYS SAE J1939 | 4.2.0.0  
CODESYS PROFINET | 4.7.2.0  
CODESYS Scripting | 4.2.0.0  
CODESYS Recipes | 4.7.0.0  
CODESYS Embedded Runtime Extension | 4.1.0.0  
CODESYS Device Reader | 4.0.0.0  
CODESYS Visualization Support | 4.7.0.0  
CODESYS Visualization | 4.9.1.0  
CODESYS CFC | 4.5.0.0  
CODESYS Application Composer | 4.4.0.0  
CODESYS LD FBD | 4.7.0.0  
CODESYS SFC | 4.4.0.0  
CODESYS Ladder | 1.2.0.0  
CODESYS Usage Analysis | 1.2.0.0  
CODESYS String Libraries | 4.1.0.0  
CODESYS Library Dependency Inspection | 1.1.0.0  
CODESYS Math Libraries | 4.0.0.0  
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2026 CODESYS GmbH  | A member of the CODESYS Group 
