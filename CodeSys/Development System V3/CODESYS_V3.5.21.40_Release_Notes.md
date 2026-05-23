[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS V3.5 SP21 Patch 4

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
CDS-95580 | Bug | CLONE - Compiler: Type of lazy variable cannot be inferred inside of pragma statement | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.21.40  
The first use of the variable in the IF statement now determines the type. If the variable is used in ELSE with a different type, there will be compilation errors.  
CDS-95579 | Bug | CLONE - About Dialog: Unhandled exception when displaying details of plugin of unsigned package | Fixed |   
CDS-95563 | Bug | CLONE - CmpUserObjectsDBFile: Loading the object DB, incorrectly checks and truncates the object name to USERMGR_MAX_GROUPNAME_LEN | Fixed | [[GENERAL]] Accident caused by CDS-94899 in V3.5.21.30.  
CDS-95515 | Bug | CLONE - CmpRedundancy: Standalone/Standalone after reboot of active linux machine | Fixed |   
CDS-95514 | Bug | CLONE - Massive CPU usage after device is added | Fixed |   
CDS-95501 | Bug | CLONE - [3SLicense.library] Resync license before demo mode expires for feature licenses | Fixed |   
CDS-95500 | Improvement | CLONE - Add new 3slicense library version 3.5.22.0 to library resolution | Fixed |   
CDS-95468 | Bug | CLONE - Combination of targetsettings "retain-in-cycle" and "report-retain-persistent-update-in-cycle" leads to invalid retain__updated() calls | Fixed |   
CDS-95439 | Bug | CLONE - TargetVisu: Security issues in Qt versions before 6.9.3 | Fixed |   
CDS-95438 | Bug | CLONE - SVG-Renderer: Security issues in OSS versions before (libxml2 2.15.1, libcurl 8.16.0) | Fixed |   
CDS-95437 | Bug | CLONE - Runtime logger files do not work on pathlength >31 | Fixed | [[GENERAL]]  
There are different ways to specify now the filepath of a logger:  
  
1\. Placeholder "$logfiles$":  
The placeholder "$logfiles$" is designed for this usecase.  
To specify a path where the logfiles have to be saved, one can use the following configuration:  
[SysFile]  
PlaceholderFilePath.<NextFreeIdx>=<Path>, $logfiles$  
  
2\. Relative or absolute filepath in logger name setting:  
You can specify and relative or absolute filepath in the logger name setting:  
[CmpLog]  
Logger.0.Name=./codesys/codesyscontrol.log  
Or:  
[CmpLog]  
Logger.0.Name=/var/log/codesys/codesyscontrol.log  
  
3\. Combination of 1. and 2.  
You can combine the placeholder filepath and relative filepath for a logger:  
[SysFile]  
PlaceholderFilePath.<NextFreeIdx>=/var/log, $logfiles$  
  
[CmpLog]  
Logger.0.Name=./codesys/codesyscontrol.log  
Logger.1.Name=./mylogger/mylogger.log  
CDS-95436 | Bug | CLONE - CmpOpenSSL: Security issues in OpenSSL versions before 3.2.6 | Fixed |   
CDS-95435 | Bug | CLONE - CODESYSControl: Security issues in Expat versions before 2.7.3 | Fixed |   
CDS-95432 | Bug | CLONE - Compare View exception if arbitrary compare is selected for different editors | Fixed |   
CDS-95431 | Bug | CLONE - Precompile error if a subordinate library is installed in the Lib Repository while project is opened | Fixed |   
CDS-95430 | Bug | CLONE - Ladder + LAZY type: missing type errors hidden behind lazy errors | Won't Fix | [[GENERAL]]  
This issue is a minor improvement in wording of errors for lazy variables. I will not be patched, since it is no critical error or a regression.  
CDS-95357 | Bug | CLONE - BACnet: BACstack Loongson segfault within send_request_to_tsm | Fixed |   
CDS-95356 | Bug | CLONE - OPCUAServer: Crash if several clients are connected and connection is interrupted multipe times | Fixed |   
CDS-95355 | Improvement | CLONE - Linux runtimes: allow for 16 CAN interfaces instead of 12 | Fixed |   
CDS-95354 | Bug | CLONE - Using DUT declaration in POU leads to crash in tabular view | Fixed |   
CDS-95353 | Bug | CLONE - Project Inspection: Suppress unwanted AddOn installation prompts when opening existing projects | Fixed | [[GENERAL]]  
Add customization to remove addOn in project inspection.  
The function is called with the package guid and should return false if the package should not be listed as a required addOn.  
  
Section: InstallerIntegration  
Key: FilterAddOnGuid  
Type: Func<Guid, bool>  
CDS-95352 | Bug | CLONE - Codesys freeze after import xml project without softmotion package | Fixed | [[GENERAL]]   
To avoid this error, the use of IRequiredTypeGuidProvider2 is required  
CDS-95350 | Bug | CLONE - Performance Onlinechange: Targetsetting "report-retain-persistent-update-in-cycle" is making problems | Fixed | [[GENERAL]]  
With Compiler version >= 3.5.21.40  
the performance of online change may improve a lot and the performance of generate code may improve significantly for targets with"codegenerator\\\report-retain-persistent-update-in-cycle".  
CDS-95349 | Bug | CLONE - CmpGwClientImpl: Investigate PLCHandler deadlock in gateway v3 communication | Won't Fix | [[GENERAL]]  
No fix for deadlock available.  
CDS-95223 | Bug | CLONE - LibManObject: Error when removing objects referenced by RequiredLibraries | Fixed | [[GENERAL]]  
CODESYS Communication 4.7.0.0 is also required  
CDS-95148 | Bug | CLONE - [Project Metrics] Task Group Assignment doesn't detekts Task Groups | Fixed |   
CDS-95067 | Bug | CLONE - RTS: Security issues in sqlite versions before 3.50.4 | Fixed |   
CDS-95036 | Bug | CLONE - Trace from VAR_INST no longer works with SP21 compiler | Fixed |   
CDS-94962 | Bug | CLONE - CmpOPCUAClient: RaceCondition in varions state machines | Fixed |   
CDS-94920 | Bug | CLONE - Library Parameters: ILibManItem3.GetParameterValue does not work anymore. | Won't Fix | [[GENERAL]]  
The risc for this patch is just to high, we decided to move this fix back to 3.5 SP22.  
CDS-94826 | Bug | CLONE - Compiler, M4 : IEC interface type defined after usage | Fixed | [GENERAL]]  
CODESYS 3.5.21.40  
CDS-94606 | Bug | CLONE - IntelliSense: IntelliSense may not be shown/drawn properly | Cannot Reproduce | [[GENERAL]]  
Currently we are not able to reproduce this issue, therefore we cannot patch the problem.  
  
 

CODESYS AddOns  |  Version   
---|---  
CODESYS Automation Server Connector | 1.36.0.0  
CODESYS Base Libraries | 4.0.1.0  
CODESYS SoftMotion | 4.19.0.0  
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
CODESYS Safety Support | 4.0.0.0  
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
CODESYS PROFINET | 4.7.1.0  
CODESYS Scripting | 4.2.0.0  
CODESYS Recipes | 4.6.0.0  
CODESYS Embedded Runtime Extension | 4.1.0.0  
CODESYS Device Reader | 4.0.0.0  
CODESYS Visualization Support | 4.6.0.0  
CODESYS Visualization | 4.8.1.0  
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

© 2025 CODESYS GmbH  | A member of the CODESYS Group 
