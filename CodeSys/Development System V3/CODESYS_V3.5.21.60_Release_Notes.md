[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS V3.5 SP21 Patch 6

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
CDS-97859 | Bug | CLONE - DeviceObject: Update device removes manual change | Fixed |   
CDS-97856 | Bug | CLONE - Compiler: Property with only Set accessor of type REFERENCE TO struct leads to compile error | Fixed |   
CDS-97703 | Bug | CLONE - User Management, Import: Import leads to endless Credential prompt with disabled Device User Management | Fixed |   
CDS-97700 | Bug | CLONE - CmpOPCUAServer, CmpOPCUAStack: Harden AuditLogs against specifiers placed in user defined text | Fixed | [[GENERAL]]  
For more details see CODESYS Security Advisory 2026-03, which is available on the CODESYS website:  
https://api-www.codesys.com/fileadmin/user_upload/CODESYS_Group/Ecosystem/Up-to-Date/Security/Security-Advisories/Advisory2026-03_CDS-95911.pdf  
CDS-97699 | Bug | CLONE - CmpAuditLog: Format specifiers can lead to DOS | Fixed | [[GENERAL]]  
For more details see CODESYS Security Advisory 2026-03, which is available on the CODESYS website:  
https://api-www.codesys.com/fileadmin/user_upload/CODESYS_Group/Ecosystem/Up-to-Date/Security/Security-Advisories/Advisory2026-03_CDS-95911.pdf  
CDS-97584 | Bug | CLONE - Internal error and compile error when calling functions with ANY inputs | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.21.60  
CDS-97532 | Bug | CLONE - Compile: Access Violation with __Currenttask-Operator | Fixed |   
CDS-97528 | Bug | CLONE - CmpSchedule: Unexpected Watchdog Timeout exceptions | Fixed |   
CDS-97523 | Bug | CLONE - LacUtil: Exception during LAC installation prevents references from being installed | Fixed | [[GENERAL]]  
The LacUtil executable now features improved error handling for reference installations. If an error occurs in this context, the return value 3 will be returned.  
Since the original issue was caused by a referenced GAC installation that resulted in a target path exceeding 260 characters, LacUtil is now capable of handling long paths correctly.  
  
[[KNOWN_LIMITATIONS]]  
LACUtil.exe will not start if the path <RootFolder>\LacBinaries\GAC_MSIL\Utilities\3.5.23.0__83380e73b2486719\Utilities.dll is longer than 260 characters. .Net internal loading from redirected paths does not work with long paths as well.  
  
[[COMPATIBILITY_INFORMATION]]  
LACUtil.exe now has new dependencies on Utilities.dll and PInvoke.dll, according to the assembly redirects placed in the LacBinaries folder.  
LACUtil.exe works well within the Common directory. If it is used outside a CODESYS installation, both referenced DLLs must be copied along as well. Additionally, the LACUtil.exe.config file must be deleted.  
CDS-97520 | Bug | CLONE - Project Compare: Commit Device Changes makes Device unusable | Won't Fix | [[GENERAL]]  
Too risky for a patch as changes in device object is required. Without a full regression test it is to dangerous -> won't fix  
CDS-97470 | Bug | CLONE - Library Manager: Documentation shows BLACK background and text when Windows color set to Dark | Fixed |   
CDS-97462 | Bug | CLONE - Incorrect message in the use case that a device does not support any boot project at all | Fixed | [[GENERAL]]  
The additional warning introduced for CDS-85812 will no longer be shown for devices that do not support a boot application.  
It will also not be shown when the simulation mode is active for a device.  
CDS-97460 | Bug | CLONE - Message View: Project with EnternetIP leads to exception | Fixed |   
CDS-97458 | Bug | CLONE - SymbolConfig: OnlineChange fails due to changes in the SymbolConfig | Won't Fix | [[GENERAL]]  
Won't fix. The original issue CDS-95679 does not contain any relevant source changes, there is nothing to patch here.  
  
The project reports three instance of "Internal Error 2" during OnlineChange:  
One instance was fixed with CDS-95522 in CODESYS 3.5 SP22 and has been patched into CODESYS 3.5 SP21 Patch 5 with with CDS-97034.  
  
The two remaining issues have been fixed with CDS-95448 in CODESYS 3.5 SP22 which relies on a major rework of the compile process in SP22 and cannot be backported to SP21.  
  
Workaround:  
The release note of CDS-95448 describes a workaround: Avoid using ANY-type conversion operators for initial value declarations.  
For this specific case: The library diagutil, 1.3.10.5 contains several functions where VAR_INPUT cSeparator is initialized using an ANY_TO_BYTE expression:  
cSeparator : BYTE := ANY_TO_BYTE(';');  
Change this to  
cSeparator : BYTE := 59; // semicolon  
  
Please note that STRING_TO_BYTE does not convert characters to ASCII bytes. Instead it tries to parse a number from a string (similar to STRING_TO_INT).  
CDS-97271 | Bug | CLONE - CmpOPCUAServer: Crash if CloseSession (or another service) is called before ActivateSession has finished | Fixed |   
CDS-97215 | Improvement | CLONE - DeviceRepository: internal speed improvements | Fixed |   
CDS-97208 | Bug | CLONE - VxWorks 7 : Imbalance of handling reference counts for END devices | Fixed |   
CDS-97202 | Bug | CLONE - CmpHilscherCIFX : Check customer feedback and fixes for message handling problems | Won't Fix | [[GENERAL]]  
Requested patch cannot be integrated:  
\- Caused errors in CODESYS fieldbus regressions tests  
\- Customer errors cannot be reproduced in our environment  
CDS-97098 | Improvement | CLONE - AddOn Check for PLCNext module should be removed | Fixed |   
CDS-96812 | Improvement | CLONE - [Project Inspection] Possibility to modify add-ons for creating a new installation | Fixed | [[GENERAL]]   
Two new OEMCustomization Hooks  
1\. Filter to modify required add-ons  
Section: InstallerIntegration;   
Key: FilterRequiredAddOns;   
Data Type: Func<IEnumerable<IAddOnInformation>, IEnumerable<IAddOnInformation>>  
  
2\. Filter to modify optional add-ons  
Section: InstallerIntegration;   
Key: FilterOptionalAddOns;   
Data Type: Func<IEnumerable<IAddOnInformation>, IEnumerable<IAddOnInformation>>  
  
The first parameter of the Func<> is the original list determined by project inspection, where the return value is the modified (or cleared) list.  
CDS-96158 | Bug | CLONE - DeviceEditor: additional empty IO-Mapping page is shown | Fixed |   
  
 

CODESYS AddOns  |  Version   
---|---  
CODESYS Automation Server Connector | 1.38.0.0  
CODESYS Base Libraries | 4.0.1.0  
CODESYS SoftMotion | 4.20.2.0  
CODESYS Security Agent | 1.4.0.0  
CODESYS C Code Integration | 4.0.0.0  
CODESYS Core Dump | 4.2.0.0  
CODESYS Code Generator ARM | 4.0.3.0  
CODESYS Code Generator ARM64 | 4.0.1.0  
CODESYS Code Generator Blackfin | 4.0.0.0  
CODESYS Code Generator Cortex M3 | 4.0.2.0  
CODESYS Code Generator PowerPC | 4.0.2.0  
CODESYS Code Generator RX | 4.0.0.0  
CODESYS Code Generator SH | 4.0.0.0  
CODESYS Code Generator TIC28x | 4.0.0.0  
CODESYS Code Generator TriCore | 4.0.1.0  
CODESYS Compiler Versions Archive | 4.0.0.0  
CODESYS Communication | 4.7.0.0  
CODESYS RISC Front End | 4.0.2.0  
CODESYS Target Settings Export | 4.0.0.0  
CODESYS Trace | 4.3.0.0  
CODESYS IO-Link | 4.3.0.0  
CODESYS Safety Support | 4.1.0.0  
CODESYS Redundancy | 4.2.0.0  
CODESYS NetX | 4.0.0.0  
CODESYS Memory Tools | 4.1.0.0  
CODESYS Modbus | 4.5.0.0  
CODESYS Ethernet Adapter | 4.2.0.0  
CODESYS EtherCAT | 4.10.0.0  
CODESYS CANopen | 4.3.0.0  
CODESYS EDS Import | 4.3.0.0  
CODESYS EtherNetIP | 4.8.0.0  
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
CODESYS LD FBD | 4.6.0.0  
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
