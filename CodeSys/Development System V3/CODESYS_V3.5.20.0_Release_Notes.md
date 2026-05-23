[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS V3.5 SP20

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
CDS-89143 | Bug | Reset Warm on RTE MC ends in deadlock | Fixed |   
CDS-89053 | Bug | RTE: incorrect PN-CIFX-Communication with Wago Slave | Fixed |   
CDS-89033 | Bug | CmpOPCUAProviderIecVarAccess: Array of ENUM can not be written | Duplicate | [[GENERAL]]  
Duplicates CDS-86257  
CDS-88995 | Improvement | [Setup] Update CODESYS Installer to 2.2.2 | Fixed | [[GENERAL]]  
Updated CODESYS Installer to 2.2.2  
CDS-88994 | Improvement | [Setup] Update CODESYS Installer to 2.2.2 | Duplicate | [[GENERAL]]  
Duplicates CDS-88995  
CDS-88983 | Bug | RTE: Control RTE SL license is not working on the UFC Container | Fixed | [[COMPATIBILITY_INFORMATION-EndUser]]  
RTE runtime licenses are working now on WIBU UFC container!  
If you use an older RTE version, you can only use a runtime license on a legacy cmact container (firmcode=5000304)  
CDS-88957 | Improvement | [RTS OnlineHelp] Update and correct manual | Fixed |   
CDS-88915 | Bug | TargetVisu: Security issues in Qt versions before 6.6.2 | Fixed |   
CDS-88847 | Bug | [Setup] Problems, if CodeMeter Runtime 8.0 is already installed | Fixed |   
CDS-88841 | Bug | Crash while display constant | Duplicate | [[GENERAL]]  
This issue is a duplicate of CDS-86008. The exception is fixed with a compile error in such a special case.  
CDS-88808 | Bug | OPC Server DA: Sporadic exceptions during heavy connection tests with Gateway V2.3 | Won't Fix | [[GENERAL]]  
The issue was caused by the Gateway client V2.3 and is not a bug in the CODESYS OPC Server DA. See LCDS-420.  
CDS-88789 | Bug | RTE: Control RTE MC SL license not working any more | Fixed |   
CDS-88764 | Bug | VISU: Exception when using a constant in visualization. | Duplicate | [[GENERAL]]  
This issue duplicates CDS-86008.  
CDS-88747 | Bug | CmpApp: Improve license exception logmessage if DevDesc or CDS compiler is too old | Fixed |   
CDS-88728 | Bug | [RTS Online Help]: Endless recursion occurred after entering a search text | Fixed |   
CDS-88625 | Improvement | [Setup] Update CODESYS Installer to 2.2.1 | Fixed | [[GENERAL]]  
Updated CODESYS Installer to 2.2.1  
CDS-88574 | Bug | PLCHandler: Linux: Disconnect blocks for several seconds when exiting old update threads | Fixed |   
CDS-88569 | Improvement | VxWorks - QS target - make runtime smaller for VxWorks-X86-PacDrive-02 | Fixed |   
CDS-88559 | Bug | CLONE - Wrong Code for x64 codegenerator for try-catch statement with CONCAT | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-88522 | Bug | CmpCodeMeter: AppBasedLicenses are not released if last application is deleted | Fixed |   
CDS-88519 | Bug | Device, Login: Display issue with Device User Logon dialog for different languages | Cannot Reproduce |   
CDS-88489 | Bug | CmpOpenSSL: include "CmpOpenSSLInternal.h" missing in OpenSSLMultitasking.c | Fixed |   
CDS-87864 | Bug | Fast online change is not executed when adding call to existing function block instance | Duplicate | [[GENERAL]]  
duplicates CDS-86340  
CDS-87850 | Bug | CmpOpenSSL: Endless loop creating key pair on Linux ARM targets | Fixed |   
CDS-87837 | Bug | SysTaskLinux: Add missing SysTaskSetDeleted in SysTaskEnd | Won't Fix | [[GENERAL]]  
Wont fix as the original problem will be solved in PLCHandler.  
CDS-87829 | Bug | OPCUA memory leak when connecting <-> disconnecting | Cannot Reproduce | [[GENERAL]]  
The observed behavior is as expected. The OPC UA Server allocates some resources upon the first connect or extends them if many connections are needed. The memory is not freed up, because it is reused by the OPC UA Server on new connections.  
CDS-87824 | Improvement | RTE: Update Windows target platform version to Win10 | Fixed |   
CDS-87801 | Improvement | BACnet: BACstack - update to BACstack V25.1.42.1 | Fixed |   
CDS-87800 | Bug | StaticAnalysisManager: Running SAN on Application with Visualization leads to SAN messages from Visu Manager | Fixed |   
CDS-87786 | Improvement | 3SLicense: set demo time for features to 2h and harmonize it with the runtime demo time | Fixed |   
CDS-87779 | Bug | DeviceRepository: stack overflow with new ESI file | Fixed |   
CDS-87774 | Bug | CmpOPCUAClient: Crash if Subscription is deleted before CreateMonitoredItemsResponse is received | Fixed |   
CDS-87768 | Bug | Localization: License overage message window contains a typo | Duplicate |   
CDS-87766 | Improvement | CmpOPCUAStack: Sort types and functions according to usage | Fixed |   
CDS-87758 | Bug | Linux / Arm64: AccessViolation and exception during shutdown or reboot of system | Duplicate |   
CDS-87754 | Bug | Security issues in CodeMeter versions before 8.0 | Fixed |   
CDS-87752 | Bug | Linux: SysTaskLinux: SysTaskSuspend/Resume remove valgrind warning about not initialized variable sigvalue | Fixed |   
CDS-87743 | Improvement | CmpCodeMeter: Find and occupy matching featurecode by firmcode+productcode+featuremap | Fixed |   
CDS-87742 | Bug | CmpOpenSSL: Security issues in OpenSSL versions before 3.1.4 | Fixed |   
CDS-87739 | Bug | SVG-Renderer: Update OSS to latest versions (libcurl 8.4.0, libjpeg-turbo 3.0.1, libxml2 2.12.1) | Fixed | [[GENERAL]]  
Updated libcurl.dll to version 8.4.0  
Updated libxml2.dll to version 2.12.1  
Updated libjpeg-turbo to 3.0.1  
CDS-87728 | Bug | Compiler: Null reference exception from locator if using method with any type | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-87716 | Bug | BACnet: BACstack (2) server side read of Device.Active_Cov_Subscriptions (and eventually other internally generated) properties does fail with BACET_STATUS_BACNET_ERROR | Cannot Reproduce |   
CDS-87714 | Improvement | Create API SysSockGetFQDN | Fixed |   
CDS-87706 | Bug | Compiler: Result of __MAXOFFSET might be incorrect | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-87684 | Bug | Warning Failed to load compile info.... Unknown tag Case2 | Fixed |   
CDS-87682 | Bug | Compiler: GVL with the same name, the same variable but different initialization value in lib and project | Won't Fix | [[GENERAL]]  
This behaviour is as designed, names from the pool are shadowed by application libraries, to access values in the pool the __POOL Scope qualifier can be used.  
CDS-87664 | Improvement | SysSem: add enhanced lock debug feature (log output) for SysSemEnter | Fixed |   
CDS-87652 | Bug | TextEditors, SmartCoding: Insert with Namespace leads to insertion of two dots | Duplicate |   
CDS-87649 | Improvement | Include Pragmastatements in white parse trees | Fixed |   
CDS-87644 | Bug | Wrong code with attribute 'pack_mode' and variable index access | Fixed | [[GENERAL]]  
Requires:  
\- Compilerversion >= 3.5.20.0  
\- RiscFrontend PlugIn >= 4.0.2.0  
  
See also RISCFE-26  
CDS-87642 | Bug | Nullreference exception in precompile | Fixed |   
CDS-87641 | Bug | Wrong location in information dialog for licensed software metrics | Fixed |   
CDS-87639 | Bug | Runtime docu: CmpBlkDrvItf: Settings are not exported | Duplicate |   
CDS-87637 | Bug | DeviceObject: Changing PLC settings results in an unhandled exception of CODESYS | Fixed |   
CDS-87636 | Bug | VFTable and FPVariables might not be initialized with enabled multithreading | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-87619 | Bug | CmpIecTask: Crash can occur because IecTaskDelete2() is called twice with RSMUtility.library | Fixed |   
CDS-87612 | Bug | Compiler: Calcucations with REFERENCE TO DATE not possible | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-87599 | Improvement | Enable Legacy Cross Reference List to ask about visibility of nodes | Fixed |   
CDS-87598 | Bug | LibMan: If some libraries are added, not all placeholders can be resolved | Fixed |   
CDS-87583 | Improvement | CAA Device Diagnosis: Update company name | Fixed |   
CDS-87581 | Improvement | UDP: Update company name | Fixed |   
CDS-87571 | Improvement | Project Settings dialog: change checkbox text | Fixed |   
CDS-87567 | Improvement | Linux: SysSemLinux should provide a debug mechanism for hard semaphore locks | Duplicate |   
CDS-87564 | Bug | IoDrvSafetySP: Driver cannot handle Unaligned IO-Data | Fixed |   
CDS-87553 | Bug | X86-64 codegeneration: Internal error with c++_compatible attribute and enum data type | Fixed |   
CDS-87550 | Bug | DeviceObject: ChannelMapping for Safety-Exchange Variables invalid | Fixed |   
CDS-87546 | Improvement | NetVarUdp: Change author | Fixed |   
CDS-87541 | Bug | IecTaskCreate: Possible access violation in self created IEC-Task | Fixed | [[COMPATIBILITY_INFORMATION]] The members 'bResult' and 'bDummy1' of the struct 'IEC_CYCLE_STRUCT' in the system library 'CmpIecTask' have been removed. The members of this struct, which is used to set up the task entry function of an IEC task in IEC code, were never evaluated, so their use was pointless anyway.  
CDS-87537 | Bug | CODESYSControl with CodeMeter Embedded: CmAct folder is not accessible via filetransfer | Fixed | [[COMPATIBILITY_INFORMATION]]  
This change only affects runtime products using CodeMeter Embedded for Wibu licensing.  
The folder "cmact_licenses" containing all license information will now be visible in the root folder of the CODESYS filetransfer in order to simplify the access for backup and restore of the licenses.  
The old invisible ".cmact_licenses" folder will be moved to "cmact_licenses" at startup of the new runtime.  
CDS-87536 | Bug | CmpX509CertItf: Unions are described as structure in itf description | Fixed |   
CDS-87535 | Improvement | 3SLicense: rename vendor to "CODESYS" | Fixed |   
CDS-87534 | Improvement | StringUtils: Change author | Fixed |   
CDS-87533 | Improvement | SharedData Utilities for MultiCore: Change author and company | Fixed |   
CDS-87532 | Improvement | RSM Utility: Change author and company | Fixed |   
CDS-87531 | Improvement | CAA Net Base Services: Change author | Fixed |   
CDS-87530 | Improvement | Change author of CmpOPCUAProviderAlarmConfiguration to CODESYS Development GmbH | Fixed |   
CDS-87528 | Improvement | Package Manager: Resolve REPOSITORY_LOCATION from RepositoryLocations ini | Fixed |   
CDS-87513 | Bug | CmpCodeMeter: Possible memory leak on CmEmbedded | Fixed |   
CDS-87511 | Bug | IntelliSense inserts "." twice | Fixed |   
CDS-87456 | Bug | Compile error C0536 | Won't Fix | [[GENERAL]]  
No local variables of methods are allowed to be used for the initialization of instance variables. The variables are not known in the scope of the function block or the FB_INIT method but only within the method itself. This also applies to constants that are defined in methods.  
=> Won't fix  
CDS-87454 | Bug | DeviceObject: creating task mapping list takes a long time | Fixed |   
CDS-87453 | Bug | Support rebranded libraries in unbound placeholder resolution | Fixed |   
CDS-87443 | Bug | FB in persistent memory leads to asymmetric calls of FB_Init/FB_Exit | Duplicate | [[GENERAL]]  
Duplicates CDS-87427  
CDS-87436 | Bug | Missing checkboxes in Project Information dialog | Duplicate |   
CDS-87434 | Bug | Linux / SysEthernet: Global Tap device closed when any raw ethernet port is closed | Fixed | [[GENERAL]]  
It is now possible to configure which network adapter should be used for EoE communication through the setting  
  
[SysEthernet]  
Linux.EoEAdapter=<AdapterName>  
  
It not set, the first ethernet adapter will enable EoE, the last one disables it.  
CDS-87429 | Bug | NullReference Exeption LoadLiteral(...) | Duplicate | [[GENERAL]]  
Duplicates CDS-86612  
CDS-87427 | Bug | Call of FB_Exit for Retain FB Instance in Reset Warm | Fixed | [[GENERAL]]  
The compiler will now produce a new warning if an FB_Exit is to be called on a function block instance in retain memory.  
A fix of the problem would need a new FB_Exit with a parameter bExitRetain similar to the parameter of FB_Init and changes in the runtime to call the exit function with the correct parameter values. Such a change is not planned at the moment.  
CDS-87409 | Bug | CmpFileTransferSrv: FileTransferServiceHandler() doesn't handle result of BTagWriterFinish() | Fixed |   
CDS-87408 | Bug | CmpOPCUAStack Implementation: All functions have set the property "Link always" | Fixed |   
CDS-87407 | Improvement | Engine, AppBasedLicenses: Check the LicensedCodeExclusionFilter when providing metrics | Fixed |   
CDS-87403 | Improvement | LibraryManager: In the Placeholder dialog, a "Sort" option for each column should be possible to sort the entries | Fixed |   
CDS-87401 | Bug | data recursion and the {attribute 'enable_dynamic_creation'} may crash IDE | Cannot Reproduce | [[GENERAL]]  
Cannot reproduced with compilerversion 3.5.20.0  
CDS-87400 | Improvement | Update UA AnsiC Stack to latest versions of the UA Specification | Fixed |   
CDS-87395 | Bug | Device Object: No compiler warning when using Symbolic Access and IO mapping simultaneously | Fixed |   
CDS-87393 | Bug | Device, PlcOpenXML Import: Importing a module via context menu is possible, even the parent source and target device IDs are different | Fixed | -  
CDS-87386 | Bug | Create new POU dialog: Crash when inserting an FB that expands itself | Fixed |   
CDS-87382 | Bug | BACnet: BACstack (2) - Calendar add wildcard date range (monday to friday or similiar) does fail | Cannot Reproduce |   
CDS-87375 | Bug | Correct definition for CLASSID_IecCodeEnd | Fixed |   
CDS-87372 | Improvement | LanguageModelBuilderHelper in LanguageModelUtilities does not work with Backtick identifiers | Fixed |   
CDS-87371 | Improvement | PLCHandler: Add PLCHandlerDeleteFile() and PLCHandlerRenameFile() functions | Fixed |   
CDS-87337 | Bug | Project Inspection: Missing addon(s) dialog suggest SoftMotion for a project with EtherCAT Safety Module | Fixed |   
CDS-87330 | Bug | Exception on logout when using IControlledExternalEditorView2 | Fixed |   
CDS-87327 | Bug | OPCUA Server: Error during initialization, if CmpUserMgr is missing, Crash during runtime | Fixed |   
CDS-87317 | Bug | CmpOPCUAStack: OpcUa_String_StrnCmp does not compare properly | Fixed |   
CDS-87312 | Bug | CAA Net Base Service: TCP client hangs with CAA_NETBASESERVICES_USE_ASYNCMGR enabled. | Fixed |   
CDS-87307 | Bug | VxWorks : Adaptions required for VxWorks 23.09 | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
Only for VxWorks: function PlcStart now returns NULL in case of ERROR, or a valid task id in case of success.  
CDS-87304 | Bug | Device, TaskDeployment: Enable Symbolic Access for IOs is not considered by Task Deployment and IO Mapping | Won't Fix | [[GENERAL]]  
The task deployment is correct as no mapping is set and therefore no existing variable neither the IEC address is used.   
Only the symbolic access is used but this is not shown in the task deployment  
-> Won't fix  
CDS-87303 | Improvement | CmpOPCUAServer: Make use of API CertStoreRegister2 to provide compatibility of Basic constraints are set to false | Fixed | [[COMPATIBILITY_INFORMATION]]  
Self-Signed certificates of the OPC UA Server will have set the basicConstraints field to cA:FALSE by default. This takes only affect, if the certificates are recreated. However, this may be not compatible with all UA Clients. If such a situation occurs you can add the fields back using the security setting CmpOPCUAServer.CreateWithCAFlag  
CDS-87300 | Bug | Device Object: Symbolic Access leads to Compile warnings | Duplicate |   
CDS-87299 | Bug | Compiler: Internal error during generate code when using property and check function | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-87298 | Bug | Compiler: The pack mode 4 is ignored for 64-Bit processors | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-87295 | Bug | Breakpoints: Breakpoint in subordinate library opens new editor when breakpoint is hit | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce with compilerversion 3.5.20.0  
CDS-87294 | Bug | IDE Crashes without warning when testing a library with a breakpoint at an instance of a called function block | Cannot Reproduce |   
CDS-87293 | Bug | Setup: Silent execution indicates success if an error during package installation | Fixed |   
CDS-87288 | Bug | BACnet: BACstack (2) properties set to BACNET_ACCESS_HIDDEN reply READ_ACCESS_DENIED instead UNKNOWN_PROPERTY | Cannot Reproduce |   
CDS-87285 | Improvement | [Setup] Sandbox light: install the repositories in a separate path | Fixed | [[GENERAL]]  
If the CDS_SEPARATE_REPO property is set to 1, the setup installs the repositories in a separate path. This path is deleted on uninstallation.  
The default value for the property is 0, so the repositories continue to be installed in the default folder %PROGRAMDATA%\CODESYS.  
For more information see the documentation "CODESYS Installation Extended OEM Adaptions" and CODESYS Installation OEM Adaptions"  
CDS-87282 | Improvement | BACnet: BACstack2 - update to BACstack V25.1.38.1 | Fixed |   
CDS-87281 | Improvement | SysEthernetLinux: Add support for a custom QDISC bypass mode | Fixed |   
CDS-87280 | Bug | Compile: Compile errors (C0077 unknown type) with image pool in sub-library | Fixed |   
CDS-87261 | Bug | ProjectInfoEditor: 2 checkboxes not visible | Fixed |   
CDS-87233 | Improvement | BACnet: BACstack2 - update to BACstack V25.1.37.1 | Fixed |   
CDS-87232 | Bug | VxWorks : New X86 micorarchitecture variant required (sysdefines.h) | Fixed |   
CDS-87226 | Improvement | BACnet: BACstack2 - update to BACstack V25.1.35.1 | Fixed |   
CDS-87223 | Improvement | BACnet2: CmpBACnet2 - add BACnetLoopEnablePidAlgorithm | Cannot Reproduce |   
CDS-87213 | Bug | [OPC UA SERVER] NVL list is not visible in UA Expert | Cannot Reproduce |   
CDS-87209 | Bug | SysFileLinux: Linux SysFileCopy_ check dst for valid filename | Fixed | [[GENERAL]]  
For more details see Advisory 2023-11, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=18027&token=43109051cf95d3445bc616e4efb8414336ebcc47&download=  
CDS-87207 | Bug | BACnet: BACstack (2) - Global Group resize of Group_Members triggered by write to Group_Members[0] doesnt copy Group_Members to Present_Value | Cannot Reproduce |   
CDS-87205 | Bug | ST: Missing Intellisense proposal | Fixed |   
CDS-87201 | Bug | Internal error on Online Change after Reload project | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.20.0  
CDS-87200 | Bug | CmpOPCUAServer: Loading of intermediate certificates does only work after reboot, not on filetransfer | Fixed |   
CDS-87198 | Bug | Project Inspection create excpetion if no packages is selected to install | Fixed |   
CDS-87196 | Improvement | PlcHandler Linux Arm: Support SoftFloat | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
The linux arm (soft float) binary requires minimum march=armv6, as the atomic builtin "compare and swap" is required for proper functionality.  
CDS-87178 | Bug | DeviceObject: Mapping for safety device without safety mapping application does not work as expected with PN device | Fixed |   
CDS-87176 | Improvement | SysFileLinux: SysFileSetPos / SysFileGetPos unable to handle file offsets > 2^31-1 (2GB) | Fixed |   
CDS-87143 | Bug | ProjectRecovery: Recovery is not offered if there are several recovery files present | Fixed |   
CDS-87141 | Improvement | Improve codesize output message after Compiler | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-87137 | Bug | Persistent variables: wrong error message for persistent variables | Fixed |   
CDS-87134 | Bug | SlotDevices: Moving a slot device may fail when using project structure API | Won't Fix | [[GENERAL]]  
This behavior is as expected,. Slot devices must not be movable, as only devices are plugged or unplugged into a slot but the slot itself must remain in the device tree.  
CDS-87132 | Bug | BACnet: BACstack (2) - can't create Access Door with Audit_Priority_Filter existent | Cannot Reproduce |   
CDS-87122 | Bug | Compiler: Display of the wrong tooltip for methods | Fixed |   
CDS-87113 | Bug | Compile error C0032 if use TO_LREAL with an input type POINTER TO TIME | Cannot Reproduce | [[GENERAL]]  
There is no compile error for the statement "lrValue := TO_LREAL(pTime^)/1000.0;" when all other errors are removed.  
CDS-87104 | Bug | Force: Wrong current/prepared value are shown, when monitoring REAL data type through Address (without the use of a Variable Binding) | Fixed |   
CDS-87100 | Bug | IEC task does not restart when multiple breakpoints are held in a multiple IEC task | Fixed |   
CDS-87087 | Bug | OnlineCommands: "ShowCompileChangeDetailsCommand" displays exception for safety applications | Fixed |   
CDS-87082 | Bug | PLCHandler Interface ARTI: Login into PLC with Motorola byte order is not possible anymore | Fixed | [[GENERAL]]  
Accident caused by CDS-81289.  
CDS-87077 | Improvement | CmpUserMgr: Fix typos in interface | Fixed |   
CDS-87073 | Bug | PLCHandler: Unknown access right 'n' reports if the variable is of type 'data structure' | Duplicate | [[GENERAL]]  
Duplicates CDS-86193  
CDS-87070 | Bug | Compiler: Internal error when using instance-path with a library that contain a variable with the same name as the library | Fixed |   
CDS-87062 | Bug | Compiler, Precompile: No type in local variable's initial value in pool | Fixed |   
CDS-87061 | Bug | 'Go to definition' shows wrong content of gvl in online mode | Fixed |   
CDS-87027 | Improvement | [Technical Debt] LibManObject, Refactor LibraryLoader.GetCachedDependencies | Cannot Reproduce | [[GENERAL]]  
Already done with CDS-79915  
CDS-87025 | Improvement | LibManObject: Better handling of unknown objects in method GetCachedDependencies | Fixed |   
CDS-87015 | Bug | CmpDeviceSrv: Service GET_TARGET_IDENT doesn't update session timeout | Fixed |   
CDS-87013 | Improvement | CmpOPCUAServerItf: Inform user that only alpha-2 code is a valid country input | Fixed |   
CDS-87004 | Bug | Excluding an explicit connector from build may result in compile errors | Fixed |   
CDS-86994 | Improvement | Device Editor: Renaming of IEC Object should open refactoring dialog | Fixed |   
CDS-86992 | Bug | PLCOpenXML: DeviceObject.xsd does not fit with the real implementation | Fixed | -  
CDS-86989 | Bug | OPC Configurator: Checkbox value of 'Motorola Byteorder' is not saved | Fixed |   
CDS-86986 | Bug | DeviceScan: Error "Axis could not be added" popup when scan and ‘Copy Before’ EtherCAT Slave with CiA402 Axis | Fixed |   
CDS-86985 | Bug | Compiler: "internal error" when re-opening an existing CODESYS project | Fixed |   
CDS-86966 | Improvement | Device-Information Dialog: display filename of native device description | Fixed |   
CDS-86963 | Bug | Force for Real value may not possible on devices | Fixed |   
CDS-86959 | Bug | CmpUserMgr: admin access rights get lost with update from 3.5.15.x to version >=3.5.18.x | Fixed |   
CDS-86958 | Bug | [Installer+InstallerAppDomainManager] Precalculated interface checksums are different with Czech OS | Fixed | [[GENERAL]]  
Having a different culture set than de could lead to wrong checksums on plugins. The checksums are now calculated culture-independent.  
CDS-86954 | Improvement | Child applications: Disable the possibility to add child applications using the "Add object" command | Fixed |   
CDS-86945 | Bug | Licensed Software Metrics, CodeSize: Codesize calculation can be disabled with message_guid attribute | Fixed |   
CDS-86943 | Bug | SysProcessLinux: incompatible change of return value of SysProcessExecuteCommand function | Fixed | [[COMPATIBILITY_INFORMATION]]  
SysProcessExecuteCommand returns the exitcode of the subprocess. SysProcessExecuteCommand2 also fills number of read bytes, even in case of error.  
CDS-86937 | Bug | misspelling in this message, "The default value for a VAROUPUT ... | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-86934 | Bug | SysModuleLinux: dlerror resets error string and must not be used several times | Fixed |   
CDS-86932 | Bug | PreCompile error "NetVarUDP library is not valid" is reported selecting a GVL | Fixed |   
CDS-86931 | Bug | Compiler: Global variable inside a library initialized by a calculation returns a wrong value | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-86929 | Bug | CmpOpenSSL: Update OpenSSL to version 3.1.3 | Fixed | [[COMPATIBILITY_INFORMATION]]  
OpenSSL 3.1. has less performance for some functions then OpensSL 1.1. because of improved security algorithms. But it is better than 3.0.  
CDS-86922 | Bug | VxWorks : Function SysSockGetHostByName() returns error | Fixed |   
CDS-86916 | Bug | Device User Management: Import of user “Owner” leads to exception when entering several wrong passwords | Fixed |   
CDS-86912 | Bug | Context menu stops working sometimes | Fixed |   
CDS-86911 | Bug | Go to Definition: Jumps to wrong position in library manager | Fixed |   
CDS-86910 | Bug | Library Manager: Unhandled exception when opening the library parameter dialog | Fixed |   
CDS-86896 | Bug | Task Configuration: When adding a system event, libraries might be inserted with "*" | Fixed |   
CDS-86893 | Bug | IEC task does not start after online change, Task Monitoring Status not shown | Fixed | [[COMPATIBILITY_INFORMATION-EndUser]]  
Sleep time of freewheeling tasks are limited now, if cycle time is very high!  
So we limit the sleep time to a maximum of:  
5 * average cycle time * number of freewheeling tasks  
CDS-86892 | Improvement | CmpSIL2: Interface to read GUIDs from bootproject before startup (companion) | Fixed |   
CDS-86891 | Bug | Compile: C0032 Build Error in case of VAR_RETAIN array declaration on retain-in-cycle PLC | Fixed |   
CDS-86890 | Bug | NBS: Resetting of EventSet for background tasks, linux arm64, does not work | Fixed |   
CDS-86879 | Bug | Online Change: Project generates Internal Error 2 after adding a variable | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-86869 | Improvement | Compiler: Cleanup the compile options dialog | Fixed |   
CDS-86868 | Improvement | Compile Options: Enable UTF8 Encoding for Strings for new projects by default | Fixed | [[GENERAL]]  
All templates used in CODESYS (Essentials) create a new project with the option UTF8-Encoding switched on.  
CDS-86865 | Improvement | RTS Online Help: Status task is missing in IEC task management chapter | Fixed |   
CDS-86844 | Improvement | [PackageManagement] OEM Customization to define list of packages which should not be migrated | Fixed | [[GENERAL]]  
OEM customers are able to define own package to retain within shared essentials during the migration process via OEMCustomization hook:  
Section: PackageManager  
Key: RetainPackages  
Value: Tuple<Guid,Version>[]  
CDS-86843 | Improvement | CPLCComBase3::Login(): Log error more specific | Fixed |   
CDS-86840 | Improvement | DeviceRepository: Install missing devices by AP Interface | Fixed |   
CDS-86763 | Improvement | Licensed Software Metrics: MultiCore feature not shown | Fixed |   
CDS-86758 | Improvement | Compiler: Remove static variable s_unusedStatements in Services.Helper | Fixed |   
CDS-86757 | Improvement | Compiler: Extend ICompileHelper4.GetUnusedStatementPositions interface | Fixed | [[GENERAL]]  
New interface ILMPreCompileSmartCodingService5 with method GetUnusedStatementPositions(Guid, ISignature, EPouScopeFlags)  
New enumeration EPouScopeFlags with values   
\- Declaration  
\- Implementation  
CDS-86741 | Bug | PLC settings: Linux SL disable diagnosis for devices requires clean all | Fixed |   
CDS-86738 | Bug | CmpOPCUAProviderIecVarAccess: Too much memory is allocated for Array of STRING monitored Items | Fixed |   
CDS-86737 | Bug | DeviceEditor: sometimes editor pages are doubled | Fixed |   
CDS-86735 | Bug | Declaration editor: Variables grayed out in declaration part of SFC POU in offline mode | Fixed | [[GENERAL]]  
Graying out code in the declaration part has been deactivated and will be reworked in SP20 along with CDS-86757.  
CDS-86728 | Bug | Device, Editor: Still inconsistent behaviour for upper and lower limits of range types | Cannot Reproduce | [[GENERAL]]  
Test with V3.5 SP19 Patch 2. The negative value is as requested automatically changed to the minimum value of the range. No window is shown.  
Cannot reproduce  
CDS-86727 | Bug | Add device and simultaneously close the dialog generate an unhandled exception crash | Fixed |   
CDS-86721 | Bug | RTE: Change Operating Mode does sometimes leads to rejection by CM | Fixed |   
CDS-86713 | Bug | OnCodeChanged is wrongly triggered on every login | Fixed | [[GENERAL]]  
If the last generated code does not match the code on the device, but the content of the project matches the code on the device, and a login is performed. The last generated code will be changed to the code on the device and a OnCodeChanged event will be triggerd  
CDS-86712 | Improvement | Library Documentation: "Script your Documentation" reference to prerequisite installations needed | Fixed |   
CDS-86711 | Bug | switching simulation modes can lead do grayed out device name | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP19 Patch2 and SP20  
CDS-86710 | Bug | Missing crossreference for FB called from POOL | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-86708 | Bug | Compiler: Exception for the assignment of a property of type REFERENCE TO FB to a local reference variable | Won't Fix | [[GENERAL]]  
The reference variable which is assigned in this project is not initialized. Therefore the exception is correct.  
CDS-86700 | Improvement | Licensed Software Metrics: add compile button to screen | Fixed |   
CDS-86699 | Bug | Compiler: Error C0230 when accessing a enum with the __POOL operator | Fixed |   
CDS-86695 | Improvement | BACnet2: IEC-lib CmpBACnet2 - change company and author of CmpBACnet2.library | Fixed |   
CDS-86692 | Improvement | Licensed Software Metrics: don't show 0 Bytes code size | Fixed |   
CDS-86690 | Bug | EasyUnit: Mock generation with const pointer leads to non compilable code | Fixed |   
CDS-86687 | Bug | OnlineHelp: Outdated Offline Help is triggered by using "F1", the Online Help is not opened | Won't Fix | [[GENERAL]]  
The error could be narrowed down and a workaround could be found: It only occurs on the first call in connection with loading the CHM help. Once the help is opened from CODESYS, all subsequent help calls are jumped to correctly.  
  
Additionally, the CHM help will not be triggered by "F1" anymore when CDS-86696 got implemented for SP20. Therefore, this issue will cannot happen anymore.  
CDS-86683 | Bug | Two renamed subdevices under separate parent devices cannot be committed individually | Fixed |   
CDS-86671 | Bug | Compiler: Unnecessary compiler warning (C0447) if a persistent variable is initialized with a constant variable | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
Changed the text of the message: "Only replaced constants can be applied as initial value for a mapped persistent variable".  
This is because of: Persistent is even initialized before allocated constants, so the compile option "Replace constants" must be activated.  
CDS-86667 | Bug | RTE: SysEthernet-drivers: CmpEt1000Drv: The intel driver periodically scans for a link in case no cable plugged and blocks CPU too long. | Fixed |   
CDS-86661 | Bug | Device editor, Access Rights: Wrong Chinese translation in Access Rights tabs | Fixed |   
CDS-86660 | Improvement | DeviceRepository: Improve behavior for a broken device cache | Fixed |   
CDS-86659 | Bug | CmpOpenSSL: Update OpenSSL to version 3.0.10 | Fixed |   
CDS-86658 | Bug | CmpRetain: free retain area if it is reserved for invalid application | Fixed |   
CDS-86657 | Improvement | Online: Password should be cleared if LoginDialog is idle for some time | Fixed | [[GENERAL]]  
The Dialog to provide credentials for a authentication on a device will now reset the entered password after 2 minutes. The OK button will also be disabled in this case until the user reenters credentials.  
CDS-86646 | Bug | Compile: VAR GENERIC CONSTANT not working in METHOD | Fixed | [[GENERAL]]  
Works now with Compilerversion >= 3.5.20.0  
CDS-86645 | Improvement | [Essentials] Check and remove references to Compression GAC | Fixed | [[GENERAL]]  
Zip compression part has been removed from the essebtials code base. With the follow up issue CDS-87310 we move the CRC32 code from compiler into Utilities.dll to finally eliminate the Compression.dll  
CDS-86642 | Bug | DeviceEditor: prepared value does not check correct values for signed datatypes | Fixed |   
CDS-86640 | Improvement | Visu Utils: Extension that the header (reverse proxy setup, RFC7239, HTTP header "forwarded") is evaluated with the method GetIPv4Address | Fixed | [[GENERAL]]  
The webserver now interprets the HTTP Header fields "X-Forwarded-For" and "Forwarded" according to RFC7239. If there are multiple IP adresses the first is retrieved.  
The resulting IP address can be retrieved with the function VU.IVisualizationClient.GetIPv4Address() from the library VisuUtils.  
CDS-86638 | Bug | Libman: "Export Library Parameters" leads to unhandled exception if no value is defined | Fixed |   
CDS-86637 | Improvement | SVG-Renderer: Provide version information of submodules in OSS | Fixed |   
CDS-86636 | Bug | Compare: Unhandled exception after compare for different devices in tab "Backup and Restore" or "Log" | Fixed | [[KNOWN_LIMITATIONS]]  
DeviceEditors opened from a ProjectCompare will no longer cause unhandled exceptions in the described szenario.   
However if no online device for such an editor exists, it might have reduced functionality, show an error message or simply not show information for certain tab pages.  
CDS-86613 | Improvement | Online: User credentials have to be re-entered after automatic logout from PLC | Fixed | [[GENERAL]]  
When an automatic logout is performed due to inactivity the currently logged in device user will also be cleared.  
CDS-86612 | Bug | Compiler: Internal Error in x86 codegenerator with special declaration of initial value | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-86603 | Bug | Compile: C0072 generated in case of REF Property passed to VAR_IN_OUT of method | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-86602 | Improvement | [Technical Debt] Rework CompilerPhase5_Codegenerator of compiler | Fixed |   
CDS-86598 | Bug | PLCHandler Interface Gateway3: delete[] / delete mismatch | Fixed |   
CDS-86585 | Improvement | ProjectCompare: Adapt interface to allow finetuning of comparison of MetaObject properties | Fixed |   
CDS-86579 | Bug | Update CodeMeter runtime to version V7.60c | Fixed | [[GENERAL]]  
For more details see Advisory 2023-10, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17809&token=c3b4e3ec4956099de26f0c6caf194d1ba341040a&download=  
CDS-86573 | Bug | Templates CmpQtControl: cannot be loaded | Fixed |   
CDS-86572 | Improvement | Performance, Online Change: In case of compile errors the fast online change should not fall back to a full compile | Fixed |   
CDS-86571 | Improvement | SysTaskLinux: make use of pthread_sigqueue optional for old linux systems | Fixed |   
CDS-86570 | Bug | Const Generic type does not work with VAR_INST declaration | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-86566 | Bug | Targetvisu, Overlay: Possible crash during application restart | Fixed |   
CDS-86565 | Bug | SIL2: Delivery feature for AURIX PSP is incomplete | Fixed |   
CDS-86561 | Improvement | STM32: Improve TargetVisuLight Speed on STM32 board | Fixed |   
CDS-86548 | Epic | RTE Support AppBased Licenses | Fixed |   
CDS-86530 | Bug | FBD: Division by zero leads to an unhandled CDS exception | Fixed | [[GENERAL]]  
An OnlineExpressionException is no longer thrown in case of a division by 0.  
The value NaN is returned in this case  
CDS-86529 | Bug | DeviceObject: refactoring with customer plugin does not work as expected | Fixed |   
CDS-86528 | Bug | Compiler: Using a reference to an enum with attribute 'strict' in a selection operator leads to a compile error | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-86527 | Improvement | Remove the feature "implicit reference type" | Fixed | [[COMPATIBILITY_INFORMATION]]  
With Compilerversion >= 3.5.20.0, the feature implicit reference type will no longer be supported  
CDS-86514 | Bug | TS_Runtime: execute single cycle takes very long after reset application | Fixed | [[GENERAL]]  
Issue caused by CDS-73536  
CDS-86506 | Bug | IntelliSense: IntelliSense (list components) opens across two screens | Fixed | [[GENERAL]]  
The position of the IntelliSense window now depends on the screen, CODESYS is displayed on. This leads to better handling of multiscreen setups.  
CDS-86505 | Bug | Create application from xml code file: Problem with FOR loop using BY with operator expression | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-86503 | Improvement | Linux, Targetvisu: Possibility to log Qt-Messages only to console | Fixed |   
CDS-86495 | Improvement | Package Manager/CLI: Inject user relevant environment variables | Fixed | [[GENERAL]]  
Resolving environment variables now takes into account that the installation process can be an elevated process with different environment variables.  
CDS-86493 | Bug | FlowControl, IDE: activating the FlowControl leads to whiteout, the IDE does no longer react proper | Fixed |   
CDS-86491 | Improvement | Project defines dialog: improve feedback for error in project define list | Fixed |   
CDS-86490 | Bug | AppBased Licenses: Exception on Download after downloading an application with zero I/O data | Fixed |   
CDS-86486 | Bug | [RTS OnlineHelp]: Correct external library chapter | Fixed |   
CDS-86482 | Bug | Compiler: Wrong Compiler Message C0032 is created | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-86481 | Bug | Generate Code: Compiler error because of global_init_slot after project update | Duplicate | [[GENERAL]]  
Duplicates CDS-82727  
CDS-86480 | Improvement | LacUtil: Checks for admin and access rights prevent plugin installation | Fixed |   
CDS-86478 | Improvement | LicensedSoftwareMetrics: Define a page identifier in LicensedSoftwareMetricPage | Fixed | [[GENERAL]]  
PageIdentifiert is now "LicensedSoftwareMetrics"  
CDS-86476 | Improvement | DeviceScan: improve number of subdevice levels in device tree | Fixed |   
CDS-86472 | Improvement | Compiler: New method GetExpressionInfo, that supports implicit code | Fixed | [[GENERAL]]  
Starting with compilerversion 3.5.20.0 a new interface ILMPreCompileSmartCodingService5 providing a new method GetExpressionInfo(ILMPreCompileSet, Guid, string, bool) (similar to ILMPreCompileSmartCodingService.GetExpressionInfo(ILMPreCompileSet, Guid, string)) is available  
CDS-86445 | Improvement | LibMan, Performance: Don't trigger PutLanguageModel of all projects on install/uninstall of library | Fixed |   
CDS-86444 | Bug | Library Manager: graphic of safety function block in library is not yellow if only SAFE[L]REAL is used | Fixed |   
CDS-86442 | Bug | DeviceEditor: No recompilation done when resetting a modified address in IO Mapping | Fixed |   
CDS-86440 | Improvement | DeviceObject: improve saving Parametercache files | Fixed |   
CDS-86439 | Bug | License: Unable to use the OPCUA Server SL and CODESYS OPC UA Client SL on the UFC Container | Cannot Reproduce | [[GENERAL]]  
Bug was located within the licenses. No Sourcecode was affected => Cannot Reproduce  
CDS-86438 | Improvement | LibMan, Exception: Remove various pointless exceptions in the LibMan | Fixed |   
CDS-86437 | Improvement | Compiler, Exception: Use TryParse in LanguageModelManager.ConversionException | Fixed |   
CDS-86434 | Bug | Remove compiler warnings in CmpBlkDrvTcp | Fixed |   
CDS-86431 | Bug | CmpDynamicTextSym: Unnecessary large memory allocation in HashtableOpen | Fixed |   
CDS-86428 | Bug | Compiler: No error C0268 in case of nested structures | Fixed | [[GENERAL]]  
For compatability reasons a new warning C0572 was introduced for these new cases.  
CDS-86420 | Bug | LibMan: NullReferenceException in specific customer project when adding Visu Manager | Fixed |   
CDS-86419 | Bug | CmpUserMgr: Admin can not change password for user created with "Password can be changed by user" unselected (RTS-Part) | Fixed |   
CDS-86417 | Improvement | LibDev: Check Title in the project templates | Fixed |   
CDS-86414 | Bug | OnlineHelp: Outdated Offline Help is triggered by "F1" if PING is disabled by IT department | Fixed |   
CDS-86412 | Bug | DeviceScan: When Removing Device during 'Scan for Devices' the Configuration of Devices gets lost | Fixed |   
CDS-86405 | Bug | Control Raspi: PN-Controller and PN-Device on same application may create "Error Init RPC | Cannot Reproduce |   
CDS-86404 | Bug | Remove Duplicate Section from DevDesc of STM32 board. | Fixed |   
CDS-86401 | Improvement | Package Manager: Prohibit the installation of older packages | Fixed | [[GENERAL]]  
Prohibit the installation of older packages.  
The installation of older packages must be explicitly allowed.  
Either by means of the package tag "AllowOlderVersions" or an OEM customization.  
CDS-86396 | Bug | LibMan: Detail and documentation view windows do not work correctly after switching to another library | Fixed |   
CDS-86395 | Bug | STM32: Slow communication with higher execution | Cannot Reproduce |   
CDS-86391 | Bug | Package Manager: Libraries and devices should be installed to system repositories | Fixed | [[GENERAL]]  
Libraries will be installed into system repository during package installation.  
CDS-86390 | Bug | LibMan: Exception when deleting a repository location while Library Manager is open | Fixed |   
CDS-86388 | Improvement | Software license metrics: jump to Store and transmit metrics values | Fixed |   
CDS-86383 | Epic | Object Manager: Support alternative project formats | Fixed | [[GENERAL]]  
Object Manager has been reworked to support alternative project formats.  
CDS-86380 | Bug | SysProcessLinux: possible endless loop in SysProcessExecuteCommand | Fixed |   
CDS-86378 | Bug | AuthZipArchive uses vulnerable version of Bouncy Castle libraries | Fixed |   
CDS-86374 | Improvement | Online Change: Complete application is retypified although only one FB is changed | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-86372 | Bug | Online change: Fast online change not done after opening project | Fixed |   
CDS-86371 | Improvement | Add functionality to scan libraries for project defines | Won't Fix | [[GENERAL]]  
Too costly for too little result  
CDS-86369 | Bug | Rebuild before Login after online change | Fixed |   
CDS-86368 | Improvement | BACnet: BACstack2 - update to BACstack V25.1.33.1 | Fixed |   
CDS-86363 | Bug | PLCHandler: Access violation occurs in ResolveIpAddressCallback after PLCComBase3 destruction | Fixed |   
CDS-86351 | Bug | InputAssistantCallback: wrong data is given to the eventhandler | Fixed |   
CDS-86349 | Improvement | Device Communication Editor: Update Wibu Gateways | Fixed | [[GENERAL]]  
Device licensing has been ported to the new WIBU gateways.  
CDS-86347 | Bug | [RTS OnlineHelp]: Remove legacy CODESYS-Runtime-en.pdf | Fixed |   
CDS-86341 | Bug | PLCHandler VxWorks Source Delivery: Files are missing | Fixed |   
CDS-86340 | Bug | FastOnlineChange: no fast online change if call to instance is added | Fixed | Compilerversion >= 3.5.20.0  
CDS-86333 | Bug | Compile errors with online change in customer project | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-86325 | Bug | Package Manager: GUID reference cannot be resolved when ID2 is used | Fixed |   
CDS-86324 | Improvement | [Technical debt] LMM: Separate source file for each expression/statement class | Fixed |   
CDS-86313 | Improvement | StringUtil: Improve library documentation | Fixed |   
CDS-86311 | Bug | LibMan: Documentation not shown on double click on function block from LD / FBD / CFC | Fixed |   
CDS-86308 | Improvement | Subscription license, expired: it would be nice if the developer get a warning when starting CDS | Fixed | [[GENERAL]]  
A new status filed will be visible if the 30 days subscription licenses will expire. The tooltip shows a detailed list of the affected licenses. Currently, only workstation licenses are considered. Different background colors visualize the require time to expire:  
CDS-86304 | Bug | Compiler: no error message for reference to property | Fixed | [[GENERAL]]  
Compiler error "C0141 Reference assign needs variable with write access" is now reported also for structured types by compile.  
CDS-86295 | Bug | Library Repository: Failed to organize library repositories | Fixed |   
CDS-86292 | Bug | [Communication]: CODESYS still sporadically sends illegal service requests to the RTS before the IOnlineDevice is fully logged in | Cannot Reproduce |   
CDS-86276 | Bug | Linux: SysEthernetGetCapabilities returns wrong value for Auto-MDIX | Fixed | [[GENERAL]]  
SysEthernetLinux now supports 4 new events:  
EVT_EthGetInterfaceCounters, EVT_EthGetMediaCounters, EVT_EthGetCapabilities, EVT_EthGetPortConfigAndStatus to make it easier to overload the ethernet statistics. There is also a new template component: SysEthernetLinux_Events that shows these events and an example project.  
CDS-86270 | Bug | CmpOPCUAServer: Semaphore missmatch within alarm handling | Fixed |   
CDS-86269 | Bug | License terms for Evergreen Webview2 installation are not complete | Fixed | [[GENERAL]]  
Microsoft Edge WebView2 runtime is no longer installed with CODESYS. The user has to download it from https://developer.microsoft.com/en-us/microsoft-edge/webview2 and confirm the license terms.  
We have disabled Microsoft Defender SmartScreen as described by Microsoft.  
CDS-86267 | Bug | Error in IEC array addressing | Duplicate | [[GENERAL]]  
Allready fixed wih CDS-82162 for SP19  
CDS-86257 | Bug | CmpOPCUAProviderIecVarAccess: Writing ARRAY of ENUM does not work | Fixed |   
CDS-86254 | Bug | CmpIecVarTest does not load as dynamic component | Fixed |   
CDS-86251 | Improvement | PlcHandler, IecVarAccessBrowsing: Provide API functions to access Enum infos | Fixed |   
CDS-86212 | Bug | unbound placeholders are not set if an application is copied | Fixed |   
CDS-86210 | Bug | Compiler: Incorrect ambiguous warning messages | Won't Fix | [[GENERAL]]  
See release note of CDS-63576: The new warning C0508 is reported when a local variable shadows a local method or action in a POU.  
CDS-86209 | Bug | GUID Object error, when performing a 'clean all' operation with a open common library element element | Fixed |   
CDS-86208 | Bug | Compiler: Attribute 'monitoring_encoding' in a string alias has no effect on an array of that string alias | Fixed |   
CDS-86203 | Bug | Compiler, Precompile: Components of userdefined types check the global scope | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-86201 | Improvement | BACnet: IEC-lib CmpBACnet2 remove libdoc error related to EVTID_BACNET_OBJECT_ID_CHANGE | Fixed |   
CDS-86194 | Bug | Compiler: Check all application objects reports error about types not being online changeable | Cannot Reproduce |   
CDS-86193 | Bug | CmpIecVarAccess: Use IecVarAccGetAccessRights instead of IecVarAccessGetAccessRights2 to serialze type members | Fixed |   
CDS-86188 | Bug | Watchlist: Exception "too many items added" when opening library method in online mode | Fixed | [[GENERAL]]  
The error message is displayed in case of problems when getting the subordinate elements.  
The meaningless error message has been changed to a more general one.  
In this case: The error is no longer displayed  
CDS-86184 | Bug | Frame: Broken UIAutomation for ContextMenu | Fixed | [[GENERAL]]  
To solve problems with UIAutomation behaviour in new .net Framework, the following switches will be set within the CODESYS.exe.config  
  
<AppContextSwitchOverrides value="Switch.UseLegacyAccessibilityFeatures=true;Switch.UseLegacyAccessibilityFeatures.1=true;Switch.UseLegacyAccessibilityFeatures.2=true;Switch.UseLegacyAccessibilityFeatures.3=true;Switch.UseLegacyToolTipDisplay=true;Switch.System.Windows.Controls.ItemsControlDoesNotSupportAutomation=true" />  
CDS-86173 | Improvement | CmpUserDBEmbedded: Move to Template from Components and simplify it | Fixed |   
CDS-86165 | Bug | Compiler: Check all application objects command might runs on old code | Fixed |   
CDS-86164 | Bug | Compiler, Stack size calculation: Orphaned callstack messages in case of too many compiler warnings | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-86163 | Improvement | CmpLog: provide PLCShell command for enabling log debug filters | Fixed | [[GENERAL]]  
New PLCShell commands available:  
  
logsetfilter [<CmpName>...] <FilterValue>  
Configures log filter settings using hexadecimal values.  
  
loggetfilter [<CmpName>...]  
Retrieve the current log filter settings for a component.  
  
logdelfilter [<CmpName>...]  
Deletes the log filter settings for specified components.  
CDS-86161 | Improvement | LibDev: Company and Author Attribute must be adjusted in the project templates | Fixed |   
CDS-86160 | Bug | DeviceObject: No online change possible after loading project with EL6900 and ESM package | Fixed |   
CDS-86159 | Bug | CmpOpenSSL: Certificates not usable with Visu Webserver | Fixed | [[COMPATIBILITY_INFORMATION]] Due to the additional filter for the alternative names configured in the cert info, the encrypted communication certificate is no longer used as a web server certificate. Instead, it has to be created with a CSR or as a self-signed certificate. To achieve that a self-signed certificate is created automatically if no other certificate is available, the security setting "CreateSelfSignedCert" in "CmpWebserver" has to be set to TRUE. Otherwise, it can be created manually within the CODESYS Security Agent.  
CDS-86154 | Improvement | The update dialog should recommend rebranded libraries as compatible successors for an update | Fixed | [[GENERAL]]  
New interfaces IRebrandingProvider and IRebranding to allow OEMs to contribute rebrandings.  
CDS-86151 | Bug | Compile: VAR_GENERIC CONSTANT not working in compiled libraries | Fixed | [[GENERAL]]  
a type declaration using a generic type will be saved for Compiler Version >= 3.5.20.0  
CDS-86145 | Bug | Compiler, Precompile: Operator expression has no type in precompile in special constellation in pool | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-86144 | Bug | AppBasedLicenses: Validation failed at standard onlinechange | Fixed |   
CDS-86143 | Bug | Replace device returns error "Too few arguments..." for specific customer devices | Fixed |   
CDS-86136 | Bug | Device User Management: Admin can not change password for user created with “Password can be changed by user” unselected | Fixed | [[GENERAL]]  
This issue fixes a problem in the IDE so that it works again for older runtime systems (e.g. SP15). For a full fix for newer runtime systems, an additional fix on the runtime side is needed (CDS-86419).  
CDS-86135 | Improvement | WebBrowser: Update to Microsoft.Web.WebView2 V1.0.1823.32 | Fixed |   
CDS-86133 | Bug | Device User Management: Option “Password must be changed at first login” is not working | Fixed |   
CDS-86132 | Improvement | Add CODEYS Ladder to setup | Fixed | [[GENERAL]]  
Added CODESYS Ladder to setup  
CDS-86125 | Bug | Compiler, Cross references: Null reference exceptions possible when forcing early cross references | Fixed |   
CDS-86124 | Bug | License: when we activate a license on the Dongle, we get the following error message "ReturnCode:403046401" | Won't Fix | [[GENERAL]]  
The inital cause was an already installed license. With CDS-85292 the Wibu gateways will be updated to get more detailed error texts.  
CDS-86119 | Improvement | Delivery Manager: create new Linux Device workarounds based on Debian bookworm | Cannot Reproduce | [[GENERAL]]  
The following workarounds already exist:  
\- Linux_Default_arm64-bookworm-qt5  
\- Linux_Default_arm64-bookworm-qt6  
\- Linux_Default_armhf-bookworm-qt5  
\- Linux_Default_armhf-bookworm-qt6  
\- Linux_Default_x64-bookworm-qt5  
\- Linux_Default_x64-bookworm-qt6  
\- Linux_Default_x86-bookworm-qt5  
\- Linux_Default_x86-bookworm-qt6  
=> Cannot Reproduce  
CDS-86115 | Bug | TextDocument: Empty ST after opening an SP17 project and directly using "Save as..." without modification | Fixed |   
CDS-86114 | Improvement | Stack size calculation: Improve handling of recursions involving interfaces | Fixed | [[GENERAL]]  
With compiler version >= 3.5.20.0 the stack size calculation does only calculate with one call in case of a recursive call of an interface method.  
E.G. if a Call itf.Next occurs in an implementation of Next, a recursion is detected and no further stack size is calculated.  
CDS-86106 | Improvement | [TechnicalDebt] Integrate new unit tests for "LoginWithParameters" into trunk | Fixed |   
CDS-86105 | Bug | RemoteTargetVisu: Failed connection depending on startup timing | Fixed |   
CDS-86098 | Improvement | CmpSettings: Provide hook to update settings without runtime restart | Fixed |   
CDS-86096 | Bug | Package Manager: Missing menu items in standard menu option files after package installation | Fixed |   
CDS-86087 | Bug | Compiler, Precompile: No precompile id in special constellation with method using SUPER^ in pool | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-86081 | Bug | Precompile: Wrong errors C0004 and C0046 | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-86065 | Improvement | Package Manager: Blacklist old AddOn versions encrypted with AxProtector 10.60 | Fixed | [[GENERAL]]  
The following add-ons have been blacklisted due to upcoming compatibility issues.  
CODESYS UML < 4.3.0.0  
CODESYS SVN < 4.5.0.0  
CODESYS Static Analysis < 4.4.3.0  
CODESYS Test Manager < 5.1.0.0  
CODESYS Profiler < 2.2.0.0  
CODESYS GIT < 1.3.0.0  
CODESYS Application Composer Single License < 4.3.0.0  
CODESYS Visu Elem Toolkit < 4.3.0.0  
CDS-86064 | Bug | Precompile: Wrong Precompile error if interface is compared with a constant pointer | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-86054 | Bug | Open Project: Crash while opening NVL project | Fixed |   
CDS-86051 | Bug | Exception in Task Editor when updating device | Fixed |   
CDS-86049 | Bug | Compile error after updating a device twice | Fixed |   
CDS-86036 | Bug | Fast online change: Not working in certain circumstances | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-86029 | Improvement | Compiler, Breakpoint list: Breakpoint list is slow with a lot of entries | Fixed |   
CDS-86024 | Improvement | Performanceimprovment for projects with many function blocks | Won't Fix | [[GENERAL]]  
Won't Fix, the proposed change contains to many bugs and a correct variant does not improve the performance measurably  
CDS-86023 | Bug | CmpEventMgr: Exception in IEC Callback leads to timeout and inconsistent state | Fixed |   
CDS-86020 | Bug | Addressing with target setting byte-addressing is not working as expected | Fixed |   
CDS-86014 | Improvement | Runtime: CmpUserDBTemplate with static analysis issue | Cannot Reproduce |   
CDS-86013 | Improvement | DeviceEditor: Attribute "onlineHelpUrl" should work with https | Fixed |   
CDS-86011 | Bug | DeviceScan: If an EtherCAT coupler is replaced by another one, the instance name of the child devices change | Cannot Reproduce | [[GENERAL]]  
Does not happen with SP20 anymore. Changes in the device object now do not rename the fb instance anymore  
CDS-86008 | Bug | Visu, text variable: VISU_MIN_NUMBER_OF_CLIENTS and VISU_MAX_NUMBER_OF_CLIENTS lead to an exception | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85985 | Improvement | CmpRedundancy: services for additional settings required | Duplicate | [[GENERAL]]  
Duplicates CDS-84919 CmpRedundancy: Improve usability.  
CDS-85983 | Bug | Runtime templates: UserDBTemplate implementation of UserObjectsDB interface causes problems | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
\- Deprecated template CmpUserDBTemplate was deleted! Was a mixture with CmpUserDBEmbedded and empty implementations of the config interfaces  
\- New template implements only CmpUserDBItf and CmpUserGroupsDBItf  
CDS-85967 | Epic | If defined-pragma should be possible in interfaces | Fixed |   
CDS-85966 | Bug | RTE: DHCP only works on Start up | Fixed | -  
CDS-85965 | Bug | CmpOPCUAServer: Strange behavior for variables of type interface | Fixed |   
CDS-85961 | Bug | Compiler, Codesys Debug, context menu cannot be open to set a breakpoint, debug crashes | Duplicate | [[GENERAL]]  
The performance issue was introduced with CDS-76705 and fixed with CDS-85470  
CDS-85960 | Bug | Devices Repository: Install-Device-Description (Automatic detection) always uses default converter | Fixed |   
CDS-85959 | Bug | CmpOPCUAServer: Calculation for mempool extension is incorrect for PublishRequests and Subscriptions | Fixed |   
CDS-85958 | Bug | Targetvisu, Overlay: EventCapturing should not raise Assertions | Fixed |   
CDS-85955 | Bug | SVG-Renderer: Update OSS to latest versions (libcurl 8.1.2) | Fixed | [[GENERAL]]  
Updated libcurl to version 8.1.2  
CDS-85946 | Bug | STM32: CanDrv: Multiple definitions of hfdcan1 and hfdcan2 | Fixed | variable in can driver header set to extern so that the variable is no longer defined twice  
CDS-85945 | Bug | [Unittest] Compiler: _IExpression.Literal does not work for enum values without inital value | Fixed |   
CDS-85940 | Bug | [Tests] VS project file of PluginTests is broken | Fixed |   
CDS-85938 | Bug | Copy&Paste of an EtherCAT junction device to its own port may not work correct | Fixed | -  
CDS-85928 | Improvement | LibDevSummary: Update info about Company and Author | Fixed |   
CDS-85927 | Improvement | FlowControl: Task for FlowControl should be selectable | Fixed | [[GENERAL]]  
The used task can be selected in the message when switching to flow control mode and in the context menu of the tasks in the navigator. The "automatic mode" behaves as before the changes. The flow control task is always marked with <Flow Control> in the navigator control.  
CDS-85926 | Bug | Exception after several download same application | Fixed |   
CDS-85918 | Improvement | Inform User in case sync timeout is too small | Fixed | [[GENERAL]]  
New "EnableSyncTimeTrace" setting for component CmpRedundancy.  
CDS-85917 | Bug | Build error C0332 without explainable reason | Fixed | [[GENERAL]]  
With the target setting "codegenerator\\\check-multiple-task-output-write" a check is performed whether the same byte is updated in different tasks.  
This check was wrong and could produce wrong error messages without clear indication.  
The only workaround is not to use the target setting.  
With this bugfix and Compiler Version >= 3.5.20.0, the check should be working as intended.  
CDS-85908 | Bug | SDK Documentation: XML Tag spelling not consistent | Cannot Reproduce | [[GENERAL]]  
Has already been updated with CDS-83668 for SP19.  
CDS-85906 | Bug | Selection of the available devices in the Add Device dialog changes, if the Device Tree is set to AutoHide | Duplicate |   
CDS-85903 | Bug | Compiler: Wrong precompile id in special constellation with method having same name as functionblock | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85902 | Bug | FB_Parent, FB_Child: Inheritance error in combination with VAR_GENERIC CONSTANT | Cannot Reproduce | [[GENERAL]]  
The project does not match the error message. The error cannot be reproduced with a newly created project analogous to the attached screenshots.  
CDS-85901 | Bug | WebBrowserIntegration/Store: Without network CPU load goes to 100% | Fixed |   
CDS-85899 | Bug | WebBrowserIntegration: Library documentation not shown in LibMan with OEM customized homepage | Fixed |   
CDS-85896 | Bug | Persistent Vars: Uncommented variable is still available in compile context | Fixed |   
CDS-85895 | Bug | DeviceObject: after update device metaobject property IExplicitConProperty could have wrong value | Fixed |   
CDS-85891 | Bug | Library Manager: Summary execution is slow and leads to different results | Duplicate | [[GENERAL]]  
Duplicate of CDS-85878  
CDS-85889 | Bug | User Management: Import from disk fails for user containing comma in name | Fixed |   
CDS-85885 | Bug | CmpOpcUAProviderIecVarAccess_Informationmodel.c : ReadNumElements() : Bad parameter passing | Fixed |   
CDS-85881 | Improvement | CODESYS Control: Add a log message, if a file access is denied by ForceIecFilePath | Fixed |   
CDS-85879 | Bug | CmpOPCUAProviderIecVarAccess: Enum handling incorrect for INT based enums; Source Timestamp for EnumValues missing. | Fixed |   
CDS-85878 | Bug | Library Manager: Summary execution is slow and leads to different results | Fixed |   
CDS-85876 | Bug | DeviceObject: upgrade storage format window is shown by mistake | Fixed |   
CDS-85875 | Improvement | TaskConfig / FlowControl: Option needed to select FlowTask manually | Duplicate |   
CDS-85874 | Bug | RSM Utility Library: Wrong parameter usage of IecTaskDelete3 | Fixed |   
CDS-85872 | Bug | Compiler: Compile error in combination with VAR_GENERIC CONSTANT and an implemented interface | Won't Fix | [[GENERAL]]  
The correct syntax to declare a function block with VAR_GENERIC and with Interface implementation is:  
  
FUNCTION_BLOCK FB_Test  
VAR_GENERIC CONSTANT  
nBuffer : INT := 100;  
END_VAR IMPLEMENTS I_Test  
  
VAR_GENERIC are parameters to the function block and should not be seen as normal variables. The special declaration position emphasizes this special role. Furthermore, VAR_GENERIC can be used to derive from the base class, and thus the constant should be declared before the base class:  
  
FUNCTION_BLOCK FB_Test  
VAR_GENERIC CONSTANT  
nBuffer : INT := 100;  
END_VAR EXTENDS FB_Base<nBuffer>  
CDS-85871 | Bug | Compiler, Generics: Wrong pointer calculation with ADR and Generic FBs | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85867 | Bug | NetVars: (Big Endian) UdpSendTlg transfers wrong number of data to be sent to the runtime | Fixed |   
CDS-85866 | Bug | Project recovery is not working | Fixed |   
CDS-85861 | Bug | CmpApp: Log error needed for AppBasedLicenses if metrics in bootproject exceeds license | Fixed |   
CDS-85850 | Bug | App Based License: __ValidateLicenseMetrics is not called in onlinechange | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0 and runtime version >= 3.5.19.20  
CDS-85849 | Bug | RTS, Targetvisu: Memory leak in Overlay-Targetvisu | Fixed |   
CDS-85846 | Bug | Debugging: Problems to debug correctly in Visu libraries | Fixed |   
CDS-85820 | Bug | Debug: set breakpoint is not possible | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce with CODESYS 3.5.20.0  
CDS-85815 | Bug | DeviceObject: plc import of exported file does not work | Fixed |   
CDS-85811 | Improvement | Standalonecompiler: Replace APEnvironmentReferences in LanguageModelManagerUtilities | Fixed |   
CDS-85808 | Bug | Project Import: Command does not work, if InstallerIntegration plugin is missing | Fixed |   
CDS-85806 | Bug | Intellisense does not work properly with variables written after a bracket | Fixed |   
CDS-85801 | Improvement | Logout IDE from PLC after configurable time of inactivity | Fixed | [[GENERAL]]  
Added new option page "Online"  
* New Setting "Force disconnect from device after time of inactivity"  
  
Added new startup parameter "ForceDisconnectAfterInactivity", which overrides the new setting:  
* --ForceDisconnectAfterInactivity="2000" (Will perform a force logout after 2000 seconds of inactivity. The specified time will be clamped to the range of 10-10800)  
* --ForceDisconnectAfterInactivity="0" (Will disable the new setting)  
  
Note that the inactivity is tracked by mouse/keyboard events that are local to CODESYS. This means that CODESYS running on a second monitor will force a disconnect even if the user is busy typing inside another application on the primary monitor. However, simply moving the mouse across the CODESYS UI without any clicking will reset the inactivity.  
CDS-85795 | Improvement | CmpIecVarAccess: Add new API RTS_BOOL IecVarAccIsReference | Fixed |   
CDS-85794 | Improvement | EasyUnit: Add Default Mocks for CmpTraceMgr tests | Fixed |   
CDS-85792 | Bug | Dialogs above the XYChart cannot be operated with touch inputs if 'Open dialog modal' is not set (For TargetVisu) | Fixed |   
CDS-85789 | Improvement | STM32 Cube: implement demo IO driver | Fixed | Fully functional Joystick  
Led 2 and 4 writeable  
Module integrated in device devdesc  
CDS-85776 | Bug | Notification Center: Potential remote code execution | Fixed | [[GENERAL]]  
For more details see Advisory 2023-07, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17767&token=7ed2d9324eff98a0a319c455d0256dc7627c705e&download=  
CDS-85758 | Bug | former version from the lib profile is not handled in update dialog | Won't Fix | [[GENERAL]]  
Starting with V3.5 SP18 the library profile is no longer used and the affected libraries are treated like unbound placeholders where the newest available version is used.  
Therefore it makes no sense to display/handle this outdated information in the project environment dialog.  
Additionally the user has the possibility to adjust the placeholder resolution in the editor of the library manager  
CDS-85756 | Bug | DeviceObject: Exception in method LanguageModelMgr_CodeChanged when called within non primary project | Fixed |   
CDS-85754 | Bug | Generate Code: Internal error on project | Duplicate | [[GENERAL]]  
Duplicate of CDS-82582  
CDS-85753 | Bug | Generate Code: DINT variable initialization via constants multiplication leads to build error | Duplicate | [[GENERAL]]  
Duplicate of CDS-82582  
CDS-85748 | Bug | PLCHandler memory leak with parameter DontLoadSymbolsFromPlc set to 1 | Fixed |   
CDS-85740 | Bug | Edit Object (Offline) opens dialog for instance selection | Duplicate |   
CDS-85736 | Improvement | Do not throw ThreadAbortException in go! | Fixed |   
CDS-85729 | Bug | RTE CX Example Project has a Warning due to old EtherCAT Task | Fixed |   
CDS-85728 | Bug | Refactoring: rename a array variable which is used in IO-mapping is not renamed | Fixed |   
CDS-85726 | Bug | Linux x64: SIGILL terminates runtime | Fixed |   
CDS-85724 | Bug | SIGABRT on Reset Cold with MODBUS Slave | Fixed |   
CDS-85720 | Bug | "Create application from XML Code file" (CodeSpy Command) does not import FB init values | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85718 | Improvement | CmpIecTask: IEC call of IecTaskDeleteInternalAsync() with parameters from stack can lead to stack overwrite | Fixed |   
CDS-85703 | Bug | Edit Object (offline): Command does not work – modification not possible | Fixed |   
CDS-85699 | Improvement | ComponentManager: Event needed when license failed or demo | Fixed | [[GENERAL]]  
New event CMPID_CmpMgr :: EVT_CmpMgr_LicenseState informs over changes in the licensing of the runtime.  
Those can be: Demomode, license available, license lost and trigger shutdown.  
In case of demomode and license lost, this event is raised at certain timestamps before the shutdown of the runtime together with the time left.  
CDS-85686 | Bug | STM32: BaudRate can not be changed in SysComStm32 | Fixed |   
CDS-85683 | Bug | CmpApp: Reset on breakpoint w/o finish cycle leads to watchdog exception | Fixed | [[GENERAL]]  
Accident because of CDS-76248  
CDS-85680 | Bug | Linux SysOut / SysFile: wrong log class in LogAdd2 leads to unnecessary log messages | Cannot Reproduce |   
CDS-85672 | Improvement | LanguageModelUtilities: ConstantEvaluator should be able to calculate divisions | Fixed | [[GENERAL]]  
The ConstantEvaluator now is based on the built-in functionality of the compiler (starting with compilerversion 3.5.20.0) and supports now things like  
\- ConversionExpression  
\- MOD  
\- ABS  
\- ...  
CDS-85671 | Improvement | LibDevSummary: Update content of CBML library in the download area | Fixed |   
CDS-85669 | Improvement | NBS: ResolveHostname document the handling of VAR_IN_OUT itfIPAddress | Fixed |   
CDS-85668 | Bug | CmpIoMgr : IO driver parameter access fails in specific environment - step2 | Fixed |   
CDS-85664 | Improvement | NBS: Provide a PingRequest function block | Fixed |   
CDS-85660 | Bug | Implemented POUs are shown also if conditionalshow_all_locals is set | Won't Fix | [[GENERAL]]  
Won't fix because wrong usage of the attribute 'conditionalshow_all_locals'  
\- Attribute needs an attribute value which must passed to the command line (using --conditionalshowsymbols) to show the corresponding symbols  
\- Attribute has only an effect for compiled libraries (attached was a source library)  
\- Attribute has only an effect on local variables not on VAR_INPUT/VAR_OUTPUT/VAR_INOUT  
Although if a function block is decorated with this attribute the inheritance hierarchy will be shown with nodes "SUPER^" when being online.  
CDS-85637 | Bug | Exception while updating notifications | Fixed |   
CDS-85616 | Improvement | NBS: Provide Doc and Example for IOptionProvider usage | Fixed |   
CDS-85613 | Bug | Browse Commands: "Go to Definition" leads to wrong behavior of documentation window in the library manager | Cannot Reproduce |   
CDS-85602 | Improvement | SysPCIWin32: Remove irrelevant pragma pack of PCI_INFO_RESULT | Fixed |   
CDS-85601 | Improvement | DeviceObject: Increase speed for editor tab change | Fixed |   
CDS-85600 | Bug | CmpOpenSSL: Wrong index variable used in X509StoreBackEndFilterCertificate() | Fixed |   
CDS-85599 | Bug | CmpMonitor2: Value of Device Parameters > 768 Bytes is invalid | Fixed |   
CDS-85597 | Bug | Webserver: Generated TLS certificate not accepted by Chrome | Duplicate | [[GENERAL]]  
This issue is a duplicate of CDS-86159. The generated certificate of the visu webserver is now accepted by Chrome.  
Furthermore the usage of HTTPS for the webvisu is possible again without workarounds.  
CDS-85592 | Bug | CDS hangs if open too many editors then update "Library Manager" in the "Message" pane | Cannot Reproduce | [[GENERAL]]  
With V3.5 SP20 this problem is no longer reproducible  
CDS-85591 | Improvement | Remove untested CmpBACnet2 from Platforms/VxWorks | Fixed |   
CDS-85590 | Improvement | STM32: Implement Can Driver | Fixed |   
CDS-85587 | Bug | Precompile: Wrong errors C0004 and C0046 with VAR_GENERIC CONSTANT | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85585 | Improvement | Enable usage of memory reserve for POUs allocatable using __NEW | Fixed | [[GENERAL]]  
Is is now possible to change function blocks with the 'enable_dynamic_creation' attribute, as long as the size of the function block does not change, if the size changes C0264 is reported and the online change fails.  
As a warning new variables that are added to functions blocks will only be initialized for new dynamic instances and existing static instances, existing dynamic instances will not receive initialization.  
CDS-85584 | Improvement | Persistent Variables List, Scripting: Add Scripting API | Fixed |   
CDS-85557 | Improvement | CmpCodemeter: Little improvements (more log information) | Fixed |   
CDS-85555 | Bug | Task Deployment, specific project: IDE freeze when opening the 'Task Deployment' in the device Tab | Fixed |   
CDS-85549 | Bug | DeviceObject: Update device does not remove compile context | Fixed |   
CDS-85534 | Bug | LibManObject: Library parameters are not saved in project | Fixed |   
CDS-85526 | Improvement | 3SLicense.library: UFC firmcode must be recognized for feature licenses | Cannot Reproduce | UFC containers are already supported by 3SLicense.  
CDS-85525 | Bug | ST Text Editor: Messages with length < 3 are not indicated correctly in line | Fixed |   
CDS-85524 | Bug | CmpOPCUAProviderIecVarAccess: Browsing with MaxNodesToReturn=1 does not work | Fixed | [[GENERAL]]  
Tested as described - OK --> Close.  
CDS-85519 | Bug | It is no longer possible to set constant variables in the libraries via python script | Won't Fix | [[GENERAL]]  
This issue will be fixed with SCRIPT-45  
CDS-85517 | Bug | External File: In project embedded file without file extension causes error on download | Duplicate |   
CDS-85513 | Improvement | Static Analysis: Add opportunity to calculate + export the standard metrics via Automation Interface | Fixed | [[GENERAL]]  
New command "exportstandardmetrics" in category "staticanalysis" with following parameters  
\- File path of the export file  
\- "true" if the min/max values have to be exported, "false" otherwise  
CDS-85512 | Bug | LibMan: Exception in UnboundPlaceholderService.ResolveUnboundPlaceholder | Fixed |   
CDS-85510 | Bug | CODESYS backup/restore does not work (error message: Non-negative number required) | Fixed |   
CDS-85507 | Bug | CmpOPCUAStack: Strange Assignments in copy functions | Fixed | [[GENERAL]]  
Review - OK --> Close  
CDS-85506 | Bug | CmpOPCUAServer: Inconsistency if Events and Alarms are deactivated | Fixed | [[GENERAL]]  
Tested as described - OK --> Close.  
CDS-85498 | Bug | Flow Control does not work with instances called in different tasks | Won't Fix | [[GENERAL]]  
For flow control, it is necessary to know in which task the code to flow is running. The compiler calculates for each variable in which tasks it is accessed. An array however, is only one variable and if the individual elements in an array are accessed in different tasks, this will be considered to be a property of the array to be accessed in different tasks.  
Typically an array element is accessed within a loop with loop index variable i, and it is not possible to derive individual task accesses for each element in an array.  
If you have an array with elements that are only used explicitly with concrete indices 1, 2, 3, then you should consider using individual variables.  
However, CDS-85927 adresses this problem. With this issue, the user is prompted to select a task for flow control, and they can change the task to flow a POU.  
CDS-85497 | Bug | DeviceObject: type list from devdesc is not available after new types are added by plugin | Fixed |   
CDS-85490 | Bug | DeviceObject: If two physical devices are renamed, it can happen that a logical device is mapped twice | Fixed |   
CDS-85488 | Bug | Monitoring: Unable to monitor array index access with variable access | Fixed |   
CDS-85479 | Improvement | CODESYSControl: SVN: Update generated *.h and *.cpp files | Fixed |   
CDS-85477 | Improvement | CmpUsrMgr: Log Create Keypair in progress | Fixed |   
CDS-85476 | Improvement | CmpOpenSSL: Log generate entropie in progress | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
New console entries available to check the time to get enough entropy:  
CmpOpenSSL, "Wait for enough entropy..."  
CmpOpenSSL, "Enough entropy available after Xms!"  
CDS-85475 | Improvement | Runtime Configuration: Add examples to Toolkit Configuration for password strength | Fixed |   
CDS-85470 | Bug | Setting of instance specific breakpoint in base implementation not possible | Fixed |   
CDS-85465 | Bug | Compiler: NullReferenceException with VAR_GENERIC CONSTANT | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce with compiler version 3.5.20.0  
CDS-85458 | Bug | Autodeclare should consider instance path | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85457 | Bug | Installer Integration: Resolving path to installer executables considers working directory | Fixed | [[GENERAL]]  
For more details see Advisory 2023-06, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17766&token=667d36292e99e6f6b7eb8c0b4a86d27137c31f98&download=  
CDS-85456 | Improvement | Compile: reduce number of messages in message view | Fixed | [[GENERAL]]  
Starting with compilerversion 3.5.20.0 a new compile option "Report compiled POUs during incremental compile" is available.  
Default value of this new option is true (because of compatibility).  
The info messages "Generate code for <POU name> ..." are only reported in the build message category if this option is set.  
CDS-85447 | Bug | Compiler: Open project with later version CDS and get Error “C0140: Reference assign is only allowed to variables of reference type” | Won't Fix | [[GENERAL]]  
Starting with V3.5 SP18 opening an older project without updating everything is no longer a supported usecase.  
When updating everything the project can be compiled without any errors.  
This is both true for V3.5 SP18 Patch 3 and V3.5 SP20  
CDS-85446 | Improvement | Compiler: Some issues with callstack output for stack overflow calculation | Fixed | [[GENERAL]]  
The call stack should now be complete. Implicit code is displayed as <Hidden POUs>, the ordering of POUs should now be according to the call stack, calls of interface methods are replaced with the call of the implementation method with the deepest stack.  
CDS-85445 | Bug | IoDrvSafetySP: with some projects the logical exchange GVL do not exchange data | Fixed |   
CDS-85441 | Bug | TabularDeclarationEditor: "Not Implemented yet" error appears if you click on the bar under the tab of a GVL | Fixed |   
CDS-85439 | Bug | Intellisense suggestion are diplayed from wrong Lib | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce with compilerversion 3.5.19.0  
CDS-85437 | Bug | DeviceObject: logical device is renamed by mistake if physical device is in slot | Fixed |   
CDS-85435 | Bug | NBS: UDP_Receive output 'udiPortFrom' not working | Fixed |   
CDS-85432 | Bug | import_io_mappings_from_csv return error "Too few arguments..." | Duplicate |   
CDS-85428 | Bug | NetVar: Variables of extended types are not transmitted | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85424 | Bug | IO-mapping is not updated if a symbolic access is deleted | Fixed |   
CDS-85423 | Bug | Frame: No Trace values shown on Logout when Trace window undocked | Fixed |   
CDS-85421 | Bug | Compiler: No compile error if 0 is assigned to a REFERENCE TO DUT | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85419 | Improvement | IIoT Libraries SL: Investigate the posssibilities to import and use client certificates | Fixed |   
CDS-85418 | Bug | Logout doesn't finish with simulation device if a big GVL is open | Cannot Reproduce |   
CDS-85416 | Bug | CmpTraceMgr: Missing Trace entries | Won't Fix | [[GENERAL]]  
Investigation shows that there are no lost values in trace buffer but a delayed entry. But this is not a problem of the runtime system and there is no chance to check this.  
CDS-85400 | Bug | Linux: unnecessary Logger Warnings | Fixed |   
CDS-85399 | Bug | MessageView: "InvalidProjectHandle" exceptions are slowing down the loading of projects | Fixed |   
CDS-85397 | Bug | If 'Structured display of inheritance hierarchy' is activated, changing the display mode does not work for variable shown under SUPER^ | Fixed |   
CDS-85395 | Bug | Property call returns wrong value if Property contains CASE with empty ELSE branch | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85394 | Bug | File Commands: Nested folders for project templates may lead to duplicate entries | Fixed |   
CDS-85386 | Bug | ARM64 syscpudebughandler: possible overwrites of FPU parameterregister | Fixed |   
CDS-85372 | Improvement | Embedded: Check stack size in regression tests | Fixed |   
CDS-85366 | Bug | Compile: Array of Alias of a structure: initial value of alias is ignored | Fixed | [[GENERAL]]  
Compilerversion 3.5.20.0  
CDS-85363 | Bug | Project Inspection: missing addon(s) dialog suggest Code Generator ARM for a Control Win x64 project | Duplicate | [[GENERAL]]  
Duplicate of CDS-85014  
CDS-85362 | Improvement | Installer Integration: Consider LanguageModelVersion during project inspection | Fixed | [[GENERAL]]  
LanguageModelVersion is now considered during project inspection.  
CDS-85356 | Bug | OPCServer: Very rare semaphore deadlock possible | Fixed |   
CDS-85328 | Improvement | Combine Compiler.QualifiedTypeGenerator and LanguageModelUtiltities.QualifiedTypeTextCreator | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85315 | Improvement | Package Manager: Write tags and language model version into package db | Fixed | [[GENERAL]]  
Tags and LanguageModelVersion of Packages are now written to the PackageDB. Tags and LanguageModelVersion are now exposed in an Interface.  
CDS-85314 | Bug | Compile: Array of Alias of Array with initialisation reports unexpected errors | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-85310 | Bug | [Setup] Codemeter installation is required even if a newer version is already installed | Fixed |   
CDS-85305 | Bug | Internal compiler error when complex user-specific data types are used | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85301 | Bug | Redundancy: Writing redundancy settings overwrites configured BootupWaitTime with default value | Fixed |   
CDS-85296 | Improvement | Installer Integration: RequiredAddonService should be able to be switched off | Fixed | [[GENERAL]]  
Analysis can be skipped during XML import by OEM customization with the following hook  
Section: InstallerIntegration  
Key: DisableAddonService  
Value: true  
The events triggering the service have been switched to project structure changed event.  
CDS-85294 | Bug | SVG-Renderer: Update OSS to latest versions (libcurl 8.0.1, cairo 1.17.8, libpng 1.6.39, libjpeg-turbo 2.1.5.1, libxml2 2.10.4) | Fixed | [[GENERAL]]  
Updated libcurl.dll to version 8.0.1  
Updated libxml2.dll to version 2.10.4  
Updated libpng to 1.6.39  
Updated cairo to 1.17.8  
Updated libjpeg-turbo to 2.1.5.1  
  
[[COMPATIBILITY_INFORMATION]]  
The update of cairo might cause some texts that are part of an SVG to be moved by 1px. We consider this as not problematic as images hardly contain texts.  
CDS-85292 | Improvement | License Manager: Update Wibu Gateways | Fixed | [[GENERAL]]  
The essential parts of workstation licensing has been ported to the new WIBU gateways. The device part is covered by CDS-86349.  
CDS-85290 | Bug | Crash during compile of assignment with complex index access and data copy | Fixed |   
CDS-85289 | Improvement | LibManEditor: Add a TryParse variant of AbstractVersion.Parse(string) | Fixed |   
CDS-85281 | Bug | LibMan, Parameter Editor: Wrong link to online help | Fixed |   
CDS-85279 | Improvement | SysCpuHandlingLinux.c: ARM32/THUMB/??/ does not build with GCC11 | Fixed | [[GENERAL]]  
Thumb2 targets with GCC11 and higher are supported.  
CDS-85277 | Bug | SysCpuMulticore linux: Crash in case of restricted cores with cgroups/containers | Fixed |   
CDS-85276 | Bug | Compiler: Compile errors with special customer device settings | Fixed | [[GENERAL]]  
Compiler Version 3.5.20.0  
CDS-85274 | Improvement | CmpHilscherCIFX.c : Add missing variable attribute to function GetPacketInQueue() | Fixed |   
CDS-85267 | Bug | Visu, NativeControls: SysNativeControlDestroy is not always called | Fixed |   
CDS-85252 | Bug | DeviceEditor: Online values for bool are not updated if editor is already open and download | Fixed |   
CDS-85247 | Bug | DeviceObject: rename and refactor a device may undo previous delete | Fixed |   
CDS-85245 | Bug | Online go-to definition for an array element does not display the variable | Fixed |   
CDS-85242 | Bug | Nullreference Exception occurs,when changing array size and doing an Online Change | Fixed |   
CDS-85241 | Bug | WebBrowserIntegration: StartPage configured in Options shall be an allowed target | Fixed |   
CDS-85238 | Improvement | Licensed Software Metric: OEM Customization Hook to hide metrics in the presentation layer | Fixed | [[GENERAL]]  
There is a new OEMCustomization Hook that returns the product codes of the licenses to hide in the presentation layer  
Section: LicensedSoftwareMetrics  
Key: ProductCodesToHide  
Datatype: HashSet<uint>  
CDS-85234 | Bug | Package Manager CLI: Package installation fails if profile has errors | Won't Fix | [[GENERAL]]  
Due to the fix of INST-458 this issue is not required anymore.  
CDS-85233 | Improvement | IPM: Support Additional Folder | Fixed | [[GENERAL]]  
IPM now shows a list of additional folders (if available) to choose from on startup.  
CDS-85223 | Bug | DeviceObject and ScriptDriverDevices: import_io_mappings_from_csv broken with CODESYS V3.5.19.0 | Fixed | [[GENERAL]]  
Accident by CDS-82588.  
CDS-85214 | Bug | Project Inspection: unhandled exception on finish | Fixed |   
CDS-85213 | Bug | Monitoring: The monitoring_encoding attribute does not work for REFERENCE TO STRING | Fixed |   
CDS-85189 | Bug | CODESYS Control: Authenticated DoS vulnerabilities in CODESYS protocol servers | Fixed | [[GENERAL]]  
For more details see Advisory 2023-05, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17765&token=04e117e1408fdb8e02b4bc821aa3be819668aef4&download=  
CDS-85170 | Improvement | CmpIecVarAccess: Implement new interface IecVarAccFindChildByName | Fixed |   
CDS-85165 | Epic | VxWorks: Support ARM64 | Fixed | [[KNOWN_LIMITATIONS]]  
* Runtime exception handling is not working reliably. See CDS-85733  
* Redundancy feature is not yet tested and should not be used for production.  
CDS-85162 | Bug | SysTaskLinux: Fast Resume/Suspend might lead to inconsistent state | Fixed | [[KNOWN_LIMITATIONS]]  
Implementation not possible for QNX plattforms.  
CDS-85150 | Improvement | Make it possible to store V3 Libraries without signature | Fixed |   
CDS-85137 | Bug | Codesys dialogs on opening are not visible or blocking | Cannot Reproduce |   
CDS-85135 | Bug | [MessageView] Messages added during Engine initialization are not shown | Fixed | [[GENERAL]]  
Adding messages to the MessageStorage before UIReady is now working properly  
CDS-85129 | Bug | Util Library: PD’s Y output does not consider modified KP input while running | Won't Fix | [[GENERAL]]  
Won't Fix as the special case described in this issue is not specified at all and the risk of changing the behaviour is rated too high.  
CDS-85127 | Improvement | Extend AuthZipFile to support additional signatures and use these signatures for usercode detection | Fixed |   
CDS-85125 | Improvement | [Setup] Show Release Notes instead of ReadMe | Fixed |   
CDS-85122 | Bug | Exception in Codegenerator when profiling a special Project | Fixed |   
CDS-85121 | Bug | Exception if STRING_TO_DT is used to convert specific strings (incomplete) | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85117 | Bug | Using "INTERNAL" in declaration and using tabular view works not correct | Fixed |   
CDS-85116 | Bug | Cannot create context file for UFC-Container | Fixed |   
CDS-85114 | Bug | Online Change: change of initial value of a VAR_OUTPUT CONSTANT is not applied | Fixed | [[GENERAL]]  
A not replaced constant in a function block will now be initialized during online change for all instances of the function block.  
However, if not absolutely necessary, you should avoid these situations. We recommend to replace constants by default in code. If you need some constants to be located in memory, use the attribute 'const_replaced'. Constants are often used for initialisation of other variables and constants. If the initialisation order is not correct, then the old value of a constant could be used during online change before the constant is initialised with the new value.  
CDS-85113 | Bug | NBS: TCP_Client can not work over TLS without CertInfo | Fixed |   
CDS-85110 | Bug | Frame: CommandInfoCache causes GDI Leak | Fixed | [[GENERAL]]  
Icons have been removed from command info cache. Missing commands will only have a name and description.  
CDS-85109 | Bug | ARM Debughandler: "Step into" overwrites an used FPU parameterregister | Fixed |   
CDS-85103 | Improvement | Runtime documentation: Remove documentation of not implemented login types | Fixed |   
CDS-85095 | Bug | Targetvisu, Overlay: mouse click executed within the wrong image object | Fixed |   
CDS-85088 | Epic | Redundancy: RTS connection stabilization | Fixed |   
CDS-85087 | Bug | [Setup] OPC Server DA cannot be installed if newer Gateway V2.3 is already installed | Fixed |   
CDS-85074 | Bug | TargetVisu, Overlay: Arrows do not look good on scrollbars | Won't Fix | [[GENERAL]]  
Won't Fix. With Antialiasing option activated in the TV, the arrows look smooth.  
CDS-85067 | Bug | [Delivery] Setup Sources Zip does not contain MicrosoftEdgeWebview2Setup and Installer | Fixed |   
CDS-85065 | Bug | Wrong precompile error C0201 with enum in complex declaration | Fixed |   
CDS-85058 | Improvement | CmpRouter: Optional package logging | Fixed | [[GENERAL]]  
Package logging can be activated/configured by the following settings:   
[CmpLog]  
CmpRouter.Filter=0xFFFFFFFF  
CmpRouter.Mask=3  
  
Mask=1: Only Rx; Mask=2: Only Tx; Mask=3: Both  
CDS-85056 | Bug | Compile: Stack overflow detected although it should not | Won't Fix | [[GENERAL]]  
The stack check is a worst case analysis. The calculated stack size for the reported project seems to be correct. The reported call stack, however, is not complete. The calculated stack size for each function only considers the local stack size, and not the stack size that is allocated by the caller.  
But the functions reported in the call stack are potentially called in this order and allocate large objects on the stack.  
All the allocated stack amounts to a potential stack overflow. It is absolutely possible that some functions in the call stack are never actually executed and there won't be the same stack consumption at runtime. Nevertheless, you should try to avoid a large stack consumption, and large value objects on the stack.  
The reported project contains several large objects on the stack, that are used to copy information. Check these situations, whether it is possible to use references.   
A new issue has been created : CDS-85446 to fix some problems in the reported call stack to improve the call stack output to give complete information on the calculated stack.  
CDS-85055 | Bug | ST Editor: Smart Coding option "Highlight symbols" leads to delay on variable click in lengthy text editor | Fixed |   
CDS-85054 | Bug | Virusscanner, Codesys Addons: Installing can lead to "process cannot access the file 'CurrentInstall.log' " message | Fixed | [[GENERAL]]  
Log will be hold in memory instead of writing to disc.  
CDS-85053 | Bug | Device Tree: Generate code leads to errors for a project containing devices plugged in slots | Fixed |   
CDS-85052 | Bug | Linux Targetvisu Webbrowser Element: Stack Overflow causes Exception | Fixed |   
CDS-85048 | Bug | Visu, Overlay, password field: The password entry is visible in Targetvisu | Fixed |   
CDS-85037 | Epic | SysTimeRtc: Improve timezone handling and dailight saving time | Fixed | [[GENERAL]]  
The SysTimeRtcGetTimezone function has been marked **deprecated** as of release 3.5.20.0. Replacement is the SysTimeRtcGetTimezone2 function.  
CDS-85032 | Epic | File Transfer: GetFileInfo service should allow to check several files at once | Fixed |   
CDS-85030 | Improvement | LMM: Remove dead code in monitoring byte code | Fixed |   
CDS-85025 | Bug | OPC UA Server: BadAttributeInvalid if you browse through the CODESYS Node IDs | Fixed |   
CDS-85024 | Bug | NBS: Release Event and Callback handles | Fixed |   
CDS-85022 | Bug | Crash when updating parameters of a library | Cannot Reproduce |   
CDS-85021 | Improvement | NBS: Document the handling of VAR_IN_OUT itfIPAddressFrom | Fixed |   
CDS-85020 | Bug | Compiler: internal error in case of unexpected call on variable in GVL | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85019 | Improvement | LMM: Provide access method to the type table | Fixed | [[GENERAL]]  
Starting with compilerversion 3.5.20.0 the interface ILMPreCompileService5 provides access to an interface ILMTypeService, that offers commonly used functionality related to types.  
Additionally ILMPreCompileService5 allow access to an interface ILMStringEncodingService  
CDS-85014 | Bug | ProjectLanguageModelProvider: BackendGuid target setting is evaluated wrong | Fixed |   
CDS-85013 | Improvement | Compiler: remove confusing memory outputs | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-85003 | Improvement | DeviceObject: add flag for safety input and outputs to skip swapping of io channels | Fixed | [[GENERAL]]  
Compiler version >= 3.5.20.0 required  
CDS-84999 | Bug | Compiler: No breakpoint can be set in an implicit check function after exporting and importing it as PLCopenXML | Fixed |   
CDS-84996 | Bug | CmpIoMgr : IO driver parameter access fails in specific environment | Fixed |   
CDS-84994 | Improvement | Find Replace: Improve editor-based FindReplace | Fixed | [[GENERAL]]  
Block Selection is not supported.  
CDS-84979 | Improvement | CmpMemPool: Trace for MemPoolLock/MemPoolUnlock | Fixed |   
CDS-84977 | Bug | Memory Leak with activated Overlay-Visu | Fixed |   
CDS-84975 | Improvement | WebBrowserIntegration: Method IsKosherURL needs to be improved | Fixed |   
CDS-84968 | Bug | Usability: Performance is bad when switching from device editor in customer project | Won't Fix | [[GENERAL]]  
The compiler spends most time with the enormous(a total of 92.000 lines) device parameter lists provided by the device object. I think for this the performance is acceptable. It might be possible to reduce the size of these lists in the device description.  
CDS-84967 | Bug | [OLH] Help SerializeHexReal (FUN) | Fixed |   
CDS-84965 | Bug | SysTaskLinux.c: SysTaskSuspend does not save context if it is suspending the own task | Fixed |   
CDS-84964 | Bug | Compiler: Wrong error is shown, if two values are multiplied within an initialization | Duplicate | [[GENERAL]]  
duplicates CDS-82582  
CDS-84963 | Bug | Autotest TACO_IOBP_03 fails sporadically on Linux_ARM64 - Part 2 | Cannot Reproduce |   
CDS-84961 | Bug | FB instance can no tbe used as input of method | Won't Fix | [[GENERAL]]  
Not an error: a VAR_IN_OUT allows the change of the value of the assigned variable. The problem is, that an interface is a reference type and VAR_IN_OUT is also a reference. VAR_IN_OUT allows to change the value of the connected variable!   
FUNCTION POU1  
VAR_IN_OUT  
itf : ITF;  
END_VAR  
itf := global_inst;  
END_FUNCTION  
  
POU1(itf := myvar);  
  
After calling this function POU1, myvar will refer to global_inst. Therefore myvar has to have the exact type ITF and can't be an instance of a function block implementing the interface.  
Any interface variable is by itself a reference type. If you just want to pass a reference to POU instances to a function without writing to the variable, use VAR_INPUT.  
CDS-84957 | Bug | External file: File without file extension leads to an error message | Fixed |   
CDS-84952 | Improvement | BACnet: BACstack - update to BACstack V25.1.5.1 | Fixed |   
CDS-84951 | Bug | Refactoring: rename application is not recognized by IO mappings | Cannot Reproduce |   
CDS-84931 | Improvement | Reserve Component IDs for CmpDNP3 | Fixed |   
CDS-84923 | Bug | CmpRedundancy: Loss of synchronization with lots of data and DataSyncAlways activated | Cannot Reproduce |   
CDS-84919 | Improvement | CmpRedundancy: Improve usability | Fixed |   
CDS-84918 | Bug | CmpRedundancy: Race condition sporadically occurs when setting up the redundancy | Fixed |   
CDS-84917 | Bug | CmpRedundancyConnectionIP: Several Downloads lead to Sys Socket Error 0x207 | Fixed |   
CDS-84916 | Bug | CmpRedundancyConnectionIP: Changing IP-Adress leads to Socket error | Duplicate | [[GENERAL]]  
Duplicates bug [CDS-84918] "CmpRedundancyConnectionIP: Socket error 2 occurs on synchronous bootup".  
CDS-84915 | Bug | CmpRedundancy: Port Number from Config File is different from Logger | Cannot Reproduce |   
CDS-84914 | Bug | CmpRedundancyConnectionIP: Write Settings and Controller reboot lead to Socket Error 0x208 | Won't Fix | [[GENERAL]]  
The problem is that after rebooting the Linux system, the CODESYSControl runtime system starts automatically and tries to open the TCP sockets/communication too early because they are not available at that time. For the specific system, the default (5000 ms) for the BootupWaittime is too short.   
  
Increasing the value of the following setting solves this problem:  
[CmpRedundancy]   
BootupWaitTime  
CDS-84913 | Bug | CmpRedundancy: Wrong synchronization timeout lead to RT freeze | Fixed |   
CDS-84909 | Bug | Watch window: Watch window doesn't recognize copied variables | Fixed |   
CDS-84900 | Bug | LibraryManager: Libraries are not listed as intended when implementing ISecureServerProvider | Fixed |   
CDS-84897 | Bug | Ethernet/IP: Scan and some acyclic services no longer working on WinCE | Fixed | [[GENERAL]]  
Caused by CDS-81388.  
CDS-84894 | Bug | Comparison in GetLocalizedString-Method does not work in every case | Fixed |   
CDS-84890 | Bug | Compiler: Instancepath is not correctly set in Childapplications | Fixed |   
CDS-84888 | Bug | CODESYS doesn't react after activate the single cycle if application is on exception | Fixed |   
CDS-84886 | Improvement | Linux Runtime: Add flag O_DSYNC for open the char device, used for retain memory | Fixed |   
CDS-84876 | Bug | Compile: Stack overflow is not detected, if function block implements derived interface | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-84873 | Improvement | Spec./Protoype IecVarAccess: Type name of structs should be available by online services | Fixed | [[COMPATIBILITY_INFORMATION]]  
The response of the online service SRV_IECVARACC_BROWSE_GET_TYPE_DESCS of the service group SG_IEC_VAR_ACCESS has been extended by an TAG_IECVARACC_TYPE_NAME tag for STRUCT types.  
NOTE: The type name is only available if the setting "Support OPC UA features" is set in symbol configuration of the IEC application.  
CDS-84867 | Bug | Monitoring of access to a pointer via index does not work | Cannot Reproduce | [[GENERAL]]  
Problem is already fixed with CDS-82010 for SP 19  
CDS-84864 | Improvement | [Setup] OEM adaption for productPathComponent and repositoryRoot | Fixed | [[GENERAL]]  
For more information see the documentations "CODESYS Installation Extended OEM Adaptions".  
CDS-84861 | Bug | Audit Log Message after delete application | Fixed |   
CDS-84854 | Bug | Load project message dialog could not open ... open path for not loaded objects | Fixed |   
CDS-84852 | Bug | ProjectCompare: Taskgroups are not considered in diff view | Fixed | [[GENERAL]]  
Taskgroups and their properties are displayed in the project compare for the Taskconfiguration.  
The associated Taskgroup is displayed in the project compare to the Taskobject.  
The Taskgroups and their properties can be merged with SingleAccept.  
CDS-84850 | Bug | Compiler: CODESYS crashes when creating a recursive ALIAS | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.20.0  
CDS-84847 | Improvement | Unittests: Reactivate BinaryArchive Unittests | Fixed |   
CDS-84846 | Bug | Option Files: Files end up in the same folder in customized installation | Fixed |   
CDS-84843 | Bug | License Manager: License activation not possible on dongle connected to PLC | Fixed |   
CDS-84832 | Bug | CMUtils / Hash: OPC UA Server exception on reset cold with new symbol configuration (Linux Device) | Fixed |   
CDS-84829 | Bug | Compiler: Types from Visu-Interface are resolved incorrectly | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-84827 | Bug | [Compatibility]: login to an SP12 runtime fails with some projects | Duplicate |   
CDS-84822 | Bug | ProjectCompare: Identical projects are shown as different | Fixed |   
CDS-84813 | Bug | WatchList: FindAll and FindNext donot jump to correct target in GVL | Fixed |   
CDS-84810 | Improvement | DeviceObject/DeviceEditor: add support for non-IEC-compliant identifiers | Fixed |   
CDS-84809 | Improvement | BACnet: BACstack - update to BACstack V25.1.2.1 | Fixed |   
CDS-84801 | Bug | IECTextEditor: deadlock on generate code if some ST editors are open | Fixed |   
CDS-84793 | Bug | Go to Definition: Command 'Go to Definition' should open the method in an offline editor | Fixed |   
CDS-84792 | Bug | Refactoring: Renaming variables declared after an initialized ALIAS variable does not rename the variable declaration | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.20.0  
CDS-84791 | Bug | Monitoring: wrong monitoring of static function block instance in instance | Fixed |   
CDS-84782 | Bug | AP: Behaviour OEM Customization Hook broken (LoggerPage) | Fixed |   
CDS-84774 | Bug | Compiler: Compile error due to initialization order although attribute 'global_init_slot' is used | Fixed | [[GENERAL]]  
The non-breaking-space(unicode 0xA0) is now interpreted as a whitespace character starting from compiler version 3.5.20.0  
CDS-84770 | Improvement | RTS Online Help: Improve debugging chapter | Fixed |   
CDS-84769 | Bug | Compiler: Attributes are not working with non breaking spaces | Duplicate | [[GENERAL]]  
Duplicates CDS-84774  
CDS-84756 | Bug | CmpOPCUAProviderIecVarAccess: Return OpcUa_BadNodeIdInvalid instead of Misconfigured Node when the wrong plc name is used | Fixed |   
CDS-84748 | Bug | Compiler: String Online value representation wrong | Fixed |   
CDS-84747 | Bug | Persistent variables: wrong error message for persistent variable of library of complex type | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-84744 | Bug | SmartCoding: Library namespace not shown in case it has same name as enum values inside other library | Fixed |   
CDS-84742 | Bug | Setup: Check on path length fails | Fixed |   
CDS-84740 | Bug | Compiler: ARRAY initialization does not work anymore for Alias | Duplicate | [[GENERAL]]  
Duplicates CDS-85314: Compile: Array of Alias of Array with initialisation reports unexpected errors  
CDS-84734 | Bug | CmpOpenSSL: Update OpenSSL to most recent version 1.1.1t | Fixed |   
CDS-84730 | Bug | Linux: assertion in Targetvisu code generates runtime exception | Fixed |   
CDS-84727 | Improvement | Project inspection: Bad performance of "Download and setup a new installation" | Won't Fix | [[GENERAL]]  
The item is not fixed for the following reasons:  
\- The installation of all add-ons takes 9 min on current computers, which is quite acceptable.  
\- The upcoming CODESYS Sandbox allows to easily keep and manage sandboxes that fit the project. These can then be opened by simply unzipping. In this sandbox then everything is contained, which belongs to the project.  
\- Gradually, new add-ons are provided with compatibility information, to which a new version is compatible. This will make the project inspection more tolerant and less frequent.  
CDS-84726 | Improvement | PLCHandler: Interface Gateway: Improve login result and Gateway notification handling. | Fixed |   
CDS-84722 | Bug | DeviceObject: Read of IoConfig.par does not work anymore | Fixed |   
CDS-84719 | Bug | Login to SIL3 device leads to compile error "C0188: Device not installed" | Cannot Reproduce | [[GENERAL]]  
Not able to reproduce this issue with CODESYS V3.5.19.0.  
CDS-84712 | Bug | Breakpoint cannot be set/removed in method of nested libraries | Fixed |   
CDS-84710 | Bug | LibManEditor: Tab 'Inputs/Outputs' is missing 'Initial' values for variables of struct-types | Fixed |   
CDS-84707 | Bug | Compile: Internal error occurs during build | Fixed |   
CDS-84706 | Improvement | Scan Network/Communication Editor: Allow disabling Update non matching devices use case | Fixed | [[GENERAL]]  
Use the new boolean Hook to dis-/enable the feature:  
Section: "DeviceCommunicationEditor"  
Key: "IsUpdatingDevicesFromNetworkScanSupported"  
  
Return FALSE to disable the feature, return TRUE (=default) for activating the feature of updating devices in a project.  
CDS-84696 | Bug | Visu, Targetvisu: Warning: QApplication was not created in the main() thread | Won't Fix | [[GENERAL]]  
Won't Fix. This problem is related to a Qt-Bug, see https://bugreports.qt.io/browse/QTBUG-101288.  
CDS-84678 | Bug | Compiler, Generics: Generic type can only be used with source library | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-84672 | Bug | Exception with specific project: Invalid memory is accessed under Linux and simulation Mode | Cannot Reproduce | [[GENERAL]]  
The steps to repeat are not clear enough to reproduce the error  
CDS-84671 | Bug | Add to watch: Structure variable within another structure cannot be expanded | Fixed |   
CDS-84663 | Improvement | Package Manager: Batch installation should not break in cause of a blacklisted package | Fixed | [[GENERAL]]  
There has been a new pre installation check included. Blacklisted packages will be checked a priori. If found an error message will be prompted. PackageManagerCLI will return errorcode 4 in this case.  
CDS-84661 | Bug | SysSocketVxworks.c : Explicit cast required to avoid compile error (VxWorks 22.06) | Fixed |   
CDS-84660 | Bug | CmpX509CertItf.m4 : Missing dependency for SysTimeItf.m4 | Fixed |   
CDS-84659 | Bug | LanguageModelManager: task cross references are not updated as expected | Won't Fix | [[GENERAL]]  
The issue with broken IO-Data was fixed with a seperate profinet issue PN-502.  
The issue that the compiler might report to many crossreferences in some situations. Removing these crossreferences will severly reduce the performance of online changes. After some investigation we are sure that these additional crossreferences will never reference variables that don't exists or that any crossreferences will miss. The next normal onlinechange will fix the crossreferences again.  
CDS-84650 | Bug | Software license metrics: Child applications are not considered in the codesize metric | Fixed |   
CDS-84646 | Bug | ProjectCompare: readonly situation enables write by itself on closing view | Fixed |   
CDS-84643 | Bug | Compile: Memory corruption with special GVL | Fixed |   
CDS-84641 | Bug | CmpUserMgr: Change password with old one expects ERR_DUPLICATE | Fixed |   
CDS-84640 | Bug | DeviceObject: Mapping of Variable of Bittype to Bit-Channel does not produce an error | Won't Fix | [[GENERAL]]  
The created task mapping is correct. wSize is 1 and therefore the IO driver shall only copy one bit with the correct position given by wParameterBitOffset and wIecAddressBitOffset.  
Therefore won't fix  
CDS-84636 | Bug | Select Device dialog: minimizing the displayed devices under a gateway does not work properly | Fixed |   
CDS-84614 | Improvement | BACnet: BACstack (2) BACnetWritePropertyInstance(ByHandle) Argument pValueSrc comment misssing statement about optional semantics of pValueSrc | Cannot Reproduce |   
CDS-84613 | Improvement | BACnet: BACstack (2) BACNET_RAW_CB wrong return type int | Cannot Reproduce |   
CDS-84607 | Bug | Package Manager: Exception when canceling package installation | Duplicate | [[GENERAL]]  
Deplicates CDS-83413.  
CDS-84586 | Bug | Find&Replace: “Replace All” with regular expression containing dot leads to Freeze of CODESYS | Fixed |   
CDS-84575 | Bug | Compiler: Unexpected error messages when using an older project in a new CODESYS version | Cannot Reproduce | [[GENERAL]]  
Starting with V3.5 SP19 this problem is no longer reproducible  
CDS-84570 | Improvement | Move .NET 6 build files of StandaloneCompiler to AP NuGets - Cleanup Essentials | Fixed |   
CDS-84569 | Bug | Device Diagnosis: GetDeviceInfo() fails with Profinet Port-Submodules | Fixed |   
CDS-84565 | Bug | Targetvisu, Windows, Overlay and Legacy: Leak of temporary files | Fixed |   
CDS-84562 | Bug | Updating an package can lead to break of dependency (PackageReference) | Fixed | [[GENERAL]]  
Existing package reference constraints will now be checked before a new package will be installed. If the new one would break a reference an error will be shown.  
CDS-84558 | Bug | DeviceApplication: Removed Commands still show up in Customization | Fixed |   
CDS-84554 | Improvement | CmpCodeMeter: minimal required version of CodeMeter Runtime should be configurable | Fixed |   
CDS-84553 | Improvement | LibraryManager, Refactoring: Refactor LibraryRepository files | Fixed |   
CDS-84544 | Epic | Support App Based licenses - Release | Fixed |   
CDS-84537 | Improvement | SysSemLinux / SysMutexLinux use "robust" pthread_mutex to avoid SIGABRT | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
SysMemLinux and SysSemLinux are now using "robust" mutexes by default if possible (not for old libc < 2.12 or QNX).  
CDS-84533 | Bug | Unjustified storage format upgrade | Fixed |   
CDS-84531 | Improvement | DeviceCommunicationEditor: Extend the API of the device license activation to allow selecting the container for the activation | Fixed |   
CDS-84530 | Bug | Package Manager: Id2 check does not consider older packages not having such | Fixed | [[GENERAL]]  
Allow the installation of a package with a lower version and without ID2 although an already installed package with a higher version has an ID2  
CDS-84529 | Bug | Cross Reference: Context column in cross reference list does not sort correctly | Fixed |   
CDS-84527 | Improvement | DeviceEditor I/O Mapping: Not all information texts are painted grey. | Fixed |   
CDS-84520 | Bug | CmpOPCUAProviderAlarmConfiguration: Events are reported three times | Fixed |   
CDS-84504 | Improvement | [Unittest] Update and configure package signature unittest | Fixed |   
CDS-84478 | Bug | AutoDeclare: Exception in ST editor of execute box if autodeclare is activated in SmartCoding | Fixed | [[GENERAL]]  
Initially, this bug reported two individual problems. One was the critical crash that was also present in older versions (e.g. SP17) and the effect, that auto-declaring did not work for the very first try. As both problems are unrelated, the implementation for this bug fixes the critical crash that needs to be patched.   
The minor effect with the missing auto-declare for the first try will be handled by the separate issue CDS-84790.  
CDS-84458 | Bug | Compile: Internal error occurs during build | Cannot Reproduce | [[GENERAL]]  
Starting with compilerversion 3.5.19.0 this problem is no longer reproducible. The compile errors C0018 and C0046 are reported instead  
CDS-84446 | Improvement | CODESYS, if started by/in another process, can be stopped and unloaded completely | Fixed |   
CDS-84443 | Bug | unexpected compile error TIME literal 2 UDINT | Cannot Reproduce | [[GENERAL]]  
Starting with compilerversion 3.5.19.0 this problem is no longer reproducible.  
This problem was fixed with CDS-83281  
CDS-84436 | Bug | Export device from device tree with adapted channels is not possible | Fixed |   
CDS-84432 | Bug | Compile: Same name of GVL/POU as namsespace in libraries leads to no error | Fixed | [[GENERAL]]  
the binding preferences of names are according to specification: the GVL name has precedence over the library name. But the precompile error message was wrong, now the precedence for precompile check is the same as for compile. If a global variable list has the same name as a library, the gvl-Name hides the library.  
CDS-84419 | Bug | Compile: Build leads an error „‘C0358 eVal‘ is not a valid value for strict ENUM type ‚E_Test‘" | Fixed |   
CDS-84418 | Bug | Libraries released with an old version cannot be signed | Won't Fix | [[GENERAL]]  
A source library with (storage) version less than 3.3.0.0 cannot be opened without updating the storage format, because the minimal supported storage version of CODESYS is 3.3.0.0.  
Without updating the storage format a TypeNotSerializableException will be thrown when trying to store/serialize the library.  
  
The best approach to avoid this problem is the following:  
\- Open the library with a suitable non-modularized CODESYS (e.g. V3.5 SP12)  
\- Update the storage format  
\- Update the currently stored compilerversion (normally "Newest" in old libraries) to the oldest available compilerversion (normally 3.4.0.0)  
\- Save the library using the oldest available storage format "Library files (CoDeSys V3.3)"  
  
Such a modified library can be signed without any errors.  
Also source libraries with (storage) version 3.3.0.0 or newer can be signed without any errors (e.g. CmpApp 3.3.0.0).  
When signing such a modified library with a modularized CODESYS the "Compiler Versions Archive" addon must be part of the installation.  
  
[[COMPATIBILITY_INFORMATION]]  
When using the compiler version "Newest" or the oldest available compiler version it is not guaranteed that a login is possible without onlinechange when using the signed compiled library  
CDS-84415 | Bug | PackageManager: TestFiles Path is not used | Fixed |   
CDS-84413 | Bug | Software license metrics: Too simple check for not available licenses | Fixed |   
CDS-84406 | Improvement | NBS: TCP_Connection shows wrong configuration if no TLS Context is configured | Fixed |   
CDS-84398 | Bug | License Manager: error dialog only display error code instead of an information of the error | Fixed |   
CDS-84396 | Bug | ST: Type converting error occurs, if two different FB instances with the same input variable are dynamically defined via __NEW operator | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-83811 | Bug | DeviceObject: update environment shows unwanted device descriptions | Fixed |   
CDS-83805 | Improvement | [Technical Debt] Compiler: Fix critial issues | Fixed |   
CDS-83799 | Bug | Refactoring: Null Reference Exception is thrown | Fixed |   
CDS-83793 | Improvement | New compiler version for SP 20 | Fixed |   
CDS-83792 | Improvement | Webserver: Use TLS1.3 by default | Fixed | [[COMPATIBILITY_INFORMATION]]  
The Webserver in the runtime system uses now TLS in version 1.3 by default, instead of version 1.2  
CDS-83785 | Bug | LanguageModelManager: GetVarReference performance issue | Cannot Reproduce | [[GENERAL]]  
The issue is fixed with SP 19 with CDS-81751.  
CDS-83784 | Improvement | Keyboard shortcut: Create a default keyboard shortcut for Go To Definition | Fixed | [[GENERAL]]  
There are two new keyboard shortcuts:  
CtrlShiftD: Go to Definition  
CtrlShiftX: Display Cross References  
CDS-83777 | Bug | BACnet: BACstack - BACstack 24.1.33.1 - error creating BISTRING properties with length 0 | Cannot Reproduce | [[GENERAL]]  
Solved with CDS-84809 BACnet: BACstack - update to BACstack V25.1.2.1  
CDS-83776 | Bug | BACnet: BACstack - BACstack 24.1.33.1 - error reading number of elements in ARRAY property reading element 0 | Cannot Reproduce | [[GENERAL]]  
Solved with CDS-84809 BACnet: BACstack - update to BACstack V25.1.2.1  
CDS-83775 | Improvement | BACnet: BACstack - BACstackV24 - BACnetAuthorizationExemption missing | Cannot Reproduce | [[GENERAL]]  
Solved with CDS-84809 BACnet: BACstack - update to BACstack V25.1.2.1  
CDS-83774 | Bug | NBS: NBS.ResolveHostname cannot be executed again in the event of an error. | Fixed |   
CDS-83771 | Bug | Compiler: conditional compilation in interface not working when certain return types are used | Won't Fix | [[GENERAL]]  
We recommend to place define attributes only at locations where attributes are supported, in this case the define attribute must be placed before the signature itself.  
CDS-83768 | Bug | Compiler: Internal error in combination with a generic datatype and an action | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-83765 | Bug | Compile: Compile error when using __POOL for a function with VAR_INPUT | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-83758 | Improvement | UnitTests: Update 'Engine' and 'OnlineCommands' tests to run on SP20 trunk | Fixed |   
CDS-83757 | Bug | IOMapping: Implicit conversion error when mapping an enum | Fixed |   
CDS-83756 | Improvement | Online Change: Improve message output regarding actually compiled POUs | Fixed | [[GENERAL]]  
Compilerversion 3.5.20.0  
CDS-83753 | Improvement | Online Change: First online change after opening project is considerably slower | Cannot Reproduce | [[GENERAL]]  
The issue is fixed with SP 19 with CDS-81751.  
CDS-83752 | Improvement | Online Change: Only retypify complete application if unqualified GVL changes | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.20.0  
CDS-83740 | Bug | QNX 7.1 / Cortex : Communication Channel timeouts | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
QNX Runtimes running on multicore systems now pin to first cpu by default. This behavior might be changed by command line parameter "-c" and providing a cpu mask.  
CDS-83725 | Bug | RTS_I64_MAX is defined with a wrong value ("-1") | Fixed |   
CDS-83717 | Epic | Help portal: generate offline help | Fixed |   
CDS-83716 | Improvement | CmpBACnet, CmpBACnet2: Replace IEC API calls with C API calls within components | Fixed |   
CDS-83715 | Improvement | CmpBACnet, CmpBACnet2: Improve type casts on 64 bit systems | Fixed |   
CDS-83711 | Improvement | CODESYS Control Win Setup: Remove copy step of bacstac.ini | Fixed |   
CDS-83704 | Bug | Flow Control: Wrong behavior of MemCmp together with SIZEOF | Won't Fix | [[GENERAL]]  
The problem is not per se a problem of Flow Control, but a problem of the string assignment. The code that is reported essentially looks like this:  
  
string1 := CONCAT("X", "Y");  
btest := MemCmp(string1, string2, SIZEOF(string1));  
MemCpy(string2, string1, SIZEOF(string1));  
  
string1 and string2 are STRING(80), SIZEOF(string1) are 81 bytes.  
CONCAT returns STRING(255).  
the assignment to string1 copies 80 bytes from the callstack to string1, only the first 3 of these bytes have a guaranteed value: 'X', 'Y', 0. You should not make any assumption on the content of a string beyond the terminating zero.  
  
In most cases, the used stack will be the same from one cycle to the next, so the call of CONCAT returns the same bytes in each cycle. So btest will be true most of the time. But this is not guaranteed! If you add a function call before the CONCAT, with a function call without constant values, btest will probably be false, because the content of the STRING-variable after the terminating zero changes with each call.  
  
Flow control interrupts the program execution several times with calls to runtime system functions. This has an effect on the values on the stack, and so the result of the MemCmp is different in this case.  
CDS-83690 | Epic | Support LoongArch64 Platform | Fixed | [[GENERAL]]  
Is already supported since CODESYS 3.5.19.0  
CDS-83686 | Bug | FlowControl: Cycle time expansion occurred with several IEC tasks | Fixed | [[KNOWN_LIMITATIONS]]  
1\. Sometimes monitoring artifacts for flowcontrol positions occurred (green execution box will be displayed sporadically white, although code was definitely executed)  
CDS-83681 | Bug | Find: Searching in online mode with “Find Next” doesn’t jump to right GVL location; “Find All” leads to Freeze of IDE | Fixed | [[General]]  
Little fix to stop the freezing of CODESYS. To fix the less dramatic "not-finding" in the Watchlist there is the new bug CDS-84813.  
CDS-83680 | Bug | Exception if CheckPointer is used for Reference to Pointer | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-83667 | Bug | Rts, Targetvisu: Non cyclic leak in SysNativeCommonControlsQt | Fixed |   
CDS-83651 | Bug | IecCoreSetOverwrite event doesn't work anymore | Fixed |   
CDS-83644 | Bug | IntelliSense: auto-complete within actions does not work with 'protected' methods | Fixed |   
CDS-83643 | Bug | Project Archive: Data has been skipped while storing | Fixed | [[GENERAL]]  
The warning about skipped data for the line IDs in the ST based code parts is no longer shown. The data itself was never skipped. Depending on the profile it is only stored at a different location.  
CDS-83642 | Bug | LibMan: MessageView is not cleaned up properly | Fixed |   
CDS-83636 | Improvement | CmpCodeMeter: Iteration interface needed over all containers and licenses in every container | Fixed |   
CDS-83633 | Improvement | BACnet: BACstack (2) - read Property_List[0] element access returns BACNET_STATUS_VAL_OUT_OF_SPACE, forcing inefficient workaround in BACnet.library | Cannot Reproduce | [[GENERAL]]  
Fixed as with BACstack2 24.1.35.1 objdbacces.c FetchObjectPropertyValue  
Next version after 24.1.35.1 delivered to CODESYS was V25.1.2.1.  
CDS-83624 | Bug | Compiler: unexpected compile error for use of enumerations in generic function blocks | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-83618 | Improvement | OPC UA Server: Adopt endpoints and behavior dynmaically on changed security settings | Fixed | [[GENERAL]]  
All security settings (except Activation) of the OPC UA server can now be modified without restarting the PLC.  
CDS-83601 | Bug | Compiler: Different TAN - calculation detected | Won't Fix | [[GENERAL]]  
The calculation of TAN is done by the runtime system (by the C compiler). CODESYS codegenerator only generates a call to an external C function.  
CDS-83569 | Improvement | BACnet: BACstack (2) - cleanup initialization of BitString with bitCount = 0 | Cannot Reproduce | [[GENERAL]]  
Solved with CDS-84809 BACnet: BACstack - update to BACstack V25.1.2.1  
CDS-83556 | Improvement | [Technical Debt] Refactor PrecompileCrossRefCollector | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-83535 | Improvement | Fast online change: compile errors might prevent consequent fast online changes | Fixed |   
CDS-83534 | Improvement | Libman: Don't use libraries with external objects if not resolved by device | Fixed | [[GENERAL]]  
Libraries that contain externally implemented objects are not resolved as unbound placeholders, if a unbound placeholder can only be resolved by externally implemented libraries it is redirected to Not Implemented By Device instead.  
This behaviour can be overwriten by the library developer by setting the parameter IsExternallyImplemented of type BOOL to FALSE  
This behaviour only applies to normal projects, in library-projects it is disabled since no device is used/avaiable  
CDS-83531 | Improvement | Retains: Support Shm custom device file | Fixed | [[GENERAL]]  
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
CDS-83509 | Bug | Compiler does not generate error for wrong pointer initialisiation | Won't Fix | [[GENERAL]]  
Compiling the attached project already reports more than 100 Warnings "C0441:Access to unitialized VAR_IN_OUT Variable". This warning is intented to catch exactly the described problem. For compatibility reasons it cannot be turned into an error  
CDS-83495 | Improvement | Webserver, CmpOpenSSL: adjust TLS support for Version TLS1.3 | Fixed | [[GENERAL]]  
With the following security setting, the TLS version can be set to TLS 1.3. Then only TLS1.3 is allowed.  
  
[CmpWebServer]  
SECURITY.TLSVersion=1.3  
CDS-83492 | Improvement | CmpIecTask: IecTasksWaitForStop( ): Adjust tSleepMs timeout | Fixed |   
CDS-83490 | Bug | Compile exception with pointer to global constant | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-83481 | Bug | Codesys completely freezes if you define a Constant recursively | Fixed |   
CDS-83425 | Bug | FlowControl: Occurrence of further deadlocks detected | Fixed | [[KNOWN_LIMITATIONS]]  
1\. Sometimes with a very sharp watchdog timeout and many open instance windows with flow control we still had an deadlock issue. We will further investigate this.  
CDS-83418 | Bug | Compile: Warnings missing in "Compiler warnings" list in the Project Settings | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.20.0  
New warnings at the end of the list with the correct warning texts:  
* C0565 with same text as error C0120  
* C0566 with same text as error C0524  
* C0567 with same text as error C0319  
* C0568 with same text as error C0094  
* C0569 with same text as error C0244  
see documentation of the respective errors for the expected error messages.  
CDS-83417 | Bug | OPC UA Server: Sometimes publish less monitored items than expected | Fixed |   
CDS-83413 | Bug | PackageManager : Unhandled Exception when clicking "Cancel" | Fixed |   
CDS-83411 | Bug | Runtime Crash with Flow Control on Specific PLC | Fixed |   
CDS-83407 | Improvement | 3s.dat: Implement switching in CmpCodeMeter for new license model | Fixed |   
CDS-83395 | Bug | Access Violation in EtherCAT_Task if network is set down | Fixed |   
CDS-83390 | Bug | License Manager: Object reference not set to an instance of an object | Fixed |   
CDS-83389 | Bug | Intellisense: Inherited FB IOs are not displayed in Pool | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
Using Intellisense in pool objects now also returns suggestions from the active application  
CDS-83388 | Bug | [LongPath] The Bootstrap/DelayedOperations mechanism does not support LongPath | Won't Fix | [[GENERAL]]  
We reverted all the changes done because the changed executables had sometimes deadlocks in the process shutdown.  
CDS-83386 | Improvement | Installer: RepositoryLocations.ini should support relative paths | Fixed | [[GENERAL]]  
Relative path support for RepositoryLocations.ini  
CDS-83364 | Bug | BACnet: BACstack - BACstackV23/24 - fix Audit-Reporter recursive call | Cannot Reproduce | [[GENERAL]]  
Solved with CDS-84809 BACnet: BACstack - update to BACstack V25.1.2.1  
CDS-83333 | Bug | RTE: No Link with 4-Wire Ethernet Cable | Fixed |   
CDS-83295 | Bug | Wrong Compile Error in library project using _IMPLICIT_APPLICATION_INFO constructor | Fixed |   
CDS-83201 | Bug | OPC UA Server: ServerCapabilities: SoftwareCertificates and MaxInactiveLockTime return NULL values | Fixed |   
CDS-83192 | Improvement | CmpOPCUAServer: Allow to use Full qualified Domain Name (FQDN) in Endpoints and Certificates | Fixed | [[GENERAL]]  
There is a new setting which allows the use of the FQDN instead of the hostname used by the OPC UA Server. This will not be enabled by default as this would break existing applications. If needed this can be configured:  
[CmpOPCUAServer]  
UseFQDN=1  
  
The FQDN is retrieved by SysSockGetFQDN. If required and the system does not have proper DNS suffixes, the following setting can be used to set up the correct FQDN:  
[SysSocket]  
PrimaryDnsSuffix=<any valid suffix>  
CDS-83178 | Bug | Compiler: C0111 error message does not specify that output area limit is in “bytes” | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-83174 | Improvement | CODESYS.exe needs --noConsole to hide the console window with --noUI | Fixed | [[GENERAL]]  
Added commandline switch --noConsole to hide the console  
CDS-83136 | Bug | Persistent Variables: change size may result in compile error C0163 | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-83126 | Bug | Windows: sysdefines.h: #ifdef WIN32_LEAN_AND_MEAN is missing | Fixed |   
CDS-83113 | Bug | Project Compare: Differences shown in CFC, although it should not | Duplicate | Duplicate issue of CDS-69817 that has been fixed in CODESYS CFC 4.0.0.0  
CDS-83098 | Bug | SysDrv3S can not be installed on clean systems | Fixed |   
CDS-83095 | Bug | Boot Application: Switching application from unencrypted to encrypted does not provoke Boot App update | Fixed |   
CDS-83083 | Bug | CANL2: Documentation contains wrong store link | Fixed |   
CDS-83067 | Bug | Linux ARM: conversion for DATE > 2038 is not working correct | Won't Fix | [[GENERAL]]  
Linux 32-bit systems, that have datatype "time_t" as signed 32 bit, are prone to the "year 2038" problem. This cannot currently be solved in a good way on these systems. Linux glibc developers are working on a way to resize the time_t to signed 64 bit type. This might come in the future. Until this solution is there, we cannot fix this issue in on 32 bit systems.  
CDS-83023 | Bug | ObjectManager: Property types are not deserialized if the property implementation is missing | Won't Fix | [[GENERAL]]  
With the introduction of the ProjectInspectionData all necessary information is stored there  
CDS-83007 | Bug | LibraryManager (POU): irrelevant message that libraries could not be resolved | Fixed |   
CDS-82966 | Bug | [LibraryManager]: on a fresh CDS installation it is not possible to open the editor of an object from LibMan | Duplicate | [[GENERAL]]  
duplicates CDS-83807  
CDS-82922 | Improvement | SJA1000 driver: CmpSJACanDrv: Add new PCI IDs for Advantech's PCM-26D2CA-BE. | Fixed |   
CDS-82913 | Bug | CmpOpenSSL: Basic constraint should be set to false by default for self-signed certificates | Fixed | [[COMPATIBILITY_INFORMATION]] By default, new self-signed certificates of our runtime will no longer have an authority key identifier and a subject key identifier.  
CDS-82900 | Bug | Two different version restrictions for the same package | Cannot Reproduce | [[GENERAL]]  
With the reworked project inspection the issue does not occur any more.  
CDS-82882 | Bug | Interactive login with ID enable disable ID-save | Fixed |   
CDS-82870 | Bug | Visu, IV: Toggle alarm color doesn't work with expression | Cannot Reproduce | [[GENERAL]]  
Starting with V3.5 SP19 this problem is no longer reproducible  
CDS-82863 | Bug | Package Manager: Memory leak while installing hundreds of packages | Fixed |   
CDS-82853 | Improvement | [ComponentMgr]: check needed to prevent call into dependency injection from the constructor of a system instance | Fixed | [[GENERAL]]  
There is a new exception "EarlySystemInstanceAccessException" that will be thrown if a system instance will be accessed before all have been loaded. The exception will be written into debug output as well. The system starts as usual.  
CDS-82822 | Bug | Online Help: Click 'F1' opens wrong online help contents at first try | Fixed |   
CDS-82819 | Bug | APUnitTestFramework should resolve interface dependencies of loaded plugins in their respective target | Fixed | [[GENERAL]]  
ApUnittestFramework uses the plugin cache file of the target for test execution.  
CDS-82792 | Bug | SharedQueue from the “SharedDataUtilities for MultiCore” does not appear to be thread safe | Fixed |   
CDS-82789 | Improvement | help: F1 on lib-FB instance/declaration opens lib man and jumps to FB showing its inline (lib) documentation | Fixed |   
CDS-82788 | Bug | VxWorks / SysCryptoVxWorks : Undeclared identifier with VxWorks 7 / CPP | Fixed |   
CDS-82775 | Bug | File, Download Source: using max_source_download_size causes different behavior | Fixed |   
CDS-82753 | Bug | VxWorks: SysSockGetHostbyName() returns wrong values | Fixed |   
CDS-82733 | Bug | WatchList: Monitoring of dereferenced pointer does not work under certain circumstances | Fixed |   
CDS-82727 | Bug | Compile error unitialized variable after update to 3.5.18.0 | Fixed | [[GENERAL]]  
The use of a reference or a pointer or an interface to an uninitialized variable to initialize a variable will produce a warning with Compilerversion >= 3.5.20.0.  
So in some cases (interfaces) existing projects may produce now a warning instead of an error. In other cases (pointer, references) existing projects may now produce new warnings.  
CDS-82680 | Bug | ST: For each new line, which is entered within a region, an increased number of tabs is added | Fixed |   
CDS-82662 | Bug | IecVarAccess: Consistent read blocks sporadically the IEC tasks for 1s | Fixed |   
CDS-82651 | Bug | The attribute {implicit on}/{implicit off} is not handled properly by PreCompile | Duplicate | [[GENERAL]]  
Duplicate of CDS-71115  
CDS-82618 | Bug | Flow control does not work in areas with conditional compilation | Cannot Reproduce |   
CDS-82591 | Improvement | RTE: Support of App Based licenses | Fixed |   
CDS-82582 | Bug | Compiler: "C0032: Cannot convert type 'DINT' to type 'INT'" message appears with customer project | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-82566 | Improvement | Project Compare: Add interface so that plugins can better decide to hide/show objects in a diff view | Fixed |   
CDS-82535 | Improvement | LicenseManager: The Select Device dialog should show all available PLCs | Cannot Reproduce | [[GENERAL]]  
Scan dialog lists a various kinds of devices either with an opened project or without.  
CDS-82471 | Bug | Compile: Wrong messages regarding Retain memory | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.20.0  
CDS-82437 | Improvement | Compiler: Scanner option to count line numbers. | Fixed |   
CDS-82427 | Bug | NullReferenceException if AlarmConfiguration is deleted | Duplicate | [[GENERAL]]  
Duplicate of CDS-81285  
CDS-82423 | Bug | LWIP: Update to latest version 2.1.3 | Fixed |   
CDS-82422 | Improvement | CmpCodeMeter: Update CodeMeter Embedded SDK to latest version 2.61 | Fixed |   
CDS-82403 | Bug | LibMan: Resolve unbound placeholder is not possible with a command | Won't Fix | [[GENERAL]]  
There is no need to implement a command "Set all unresolved unbound placeholder...", because the problem reported by the customer is no longer reproducible.  
When running the attached script the Standard.library is added to the library manager and the resolution of the unbound placeholder is the newest available version.  
CDS-82382 | Bug | Compiler: Flow Control does not show values in green in processed code in a project with two tasks and OOP | Duplicate | [[GENERAL]]  
Flow Control needs to be done in one specific task in order to get consistent values. A suitable task is calculated automatically, whenever the editor changes. This is not always possible, especially when POUs are called via interface or pointer, a wrong task may be used.  
This issue will be resolved with CDS-85927. With this issue, the user is prompted to select a task for flow control, and they can change the task to flow a POU.  
CDS-82324 | Improvement | Package Manager: Create API to get signature of installed packages | Fixed | [[GENERAL]]  
PackageEngine15 provides access to the signature information for installed packages  
CDS-82323 | Improvement | About Dialog: Version Info should contain PackageInfo and Signature | Fixed |   
CDS-82294 | Improvement | SyncOnlineFiles: Creating a boot project offline should also trigger “PrepareTransferOffline” | Fixed |   
CDS-82256 | Improvement | Refactoring: Add user option so that refactoring is executed automatically without the dialog | Fixed | [[GENERAL]]  
Added a new Refactoring option "Preview Refactoring Changes".  
If disabled, Refactoring is executed automatically without the preview changes dialog.  
  
Note: Regardless of this option, the prompt to check if a "Rename" operation in the navigator should be executed, will always be displayed. This renaming is not an explicit operation and the user should get the chance to prevent it.  
CDS-82245 | Improvement | PLCHandler: Interface Simulation and Monitoring2 services: Provide type information for ENUMs and simple types | Fixed | [[GENERAL]]  
New API functions GetAllTypes() and GetTypeByName() added. See PLCHandler Programming Guide.  
CDS-82228 | Bug | Actual storage format is not shown after "save project as" including Addon objects | Fixed |   
CDS-82214 | Bug | User handling: import of user and groups does not work | Fixed |   
CDS-82210 | Bug | SysTaskLinux: Race condition between SysTaskCreate and SysTaskSetPriority | Fixed | [[COMPATIBILITY_INFORMATION]]  
SysTaskSetPriority might now return ERR_NOTINITIALIZED as long as the systask is not yet initialized completely, causing that the prio cannot be set.  
CDS-82204 | Bug | CmpIoMgr.c : Issues causing crash after few Run->Halt->Reset cycles | Fixed |   
CDS-82171 | Bug | Find: object reference not set to an instance of an object | Cannot Reproduce |   
CDS-82149 | Bug | Package uninstallation fails if you update the installer from version 1.1.0.0 to 1.3.0.0 | Cannot Reproduce |   
CDS-82148 | Improvement | CODESYS / DeviceUserManagement: GB40050: Support configuration of password expiration update cycle | Fixed |   
CDS-82071 | Improvement | Upgrade Storage Format: Name the future profile | Fixed |   
CDS-82070 | Improvement | Upgrade Storage Format: Provide API to confirm prompt automatically | Duplicate | [[GENERAL]]  
Duplicate of CDS-79946  
The interfacee IProjectUpdateConfigurator should already provide the required API.  
CDS-82062 | Bug | Project inspection: Download missing addons not possible | Cannot Reproduce | [[GENERAL]]  
With the reworked Project Inspection it is possible to install the missing add-on by choosing "project is in development phase".  
CDS-82060 | Bug | Search and replace: Replacing one by one of a selection does not work | Fixed |   
CDS-82052 | Bug | SysEthernetLinux: Log message prints garbage socket file descriptor | Fixed |   
CDS-81932 | Bug | Compiler: No error when using %MXn.m where m is greater than the used type range | Won't Fix | [[GENERAL]]  
An error message for a direct address %MX0.8 would produce error messages in many existing projects. It is not a problematic address at all since it either denotes the same bit as %MX1.0 or the 8th bit in the first WORD in memory if bit_word_addressing is set as target setting. In either case, there is nothing wrong with this address.  
However, mapping a bit-Variable with "Map on existing" to a bit channel in the IO-Mapping is not possible at all.   
The compiler produces a warning "C0355: A single bit cannot be referenced.", but this warning is not simply connected to the mapping and it is hard to understand the cause of the warning.  
To improve the warning for this mapping a new issue is created: CDS-84640  
CDS-81905 | Bug | Edit object (Offline): Opens object online | Duplicate |   
CDS-81901 | Improvement | RTE / CmpET1000Drv: Extend driver to support new generation eth chips like i225/i226 | Fixed |   
CDS-81880 | Bug | SysDrv3S: Wrong datatype used for PCI_INFO.ulBusNr | Fixed | [[GENERAL]]  
This fix was made to also support CODESYS V2 with the same driver version. We aren't aware of any use case where this fix is relevant for CODESYS V3.  
  
If you nevertheless want to use the new driver version, you must manually update the SysDrv3S.sys driver to the latest version V3.5.19.10:  
\- In the Microsoft Windows Device Manager right-click on the Hilscher device to open the context menu.  
\- Select Update driver within this.  
\- Install the driver from the subdirectory "./Driver" of your CODESYS Development System or CODESYS Control installation directory.  
\- Check the driver version after the update. The driver must have version number 3.5.19.10.  
CDS-81802 | Improvement | TaskConfig: Limit the type selection of a Task | Won't Fix | [[GENERAL]]  
Use cases are not clear  
CDS-81801 | Bug | SysEthernetLinux: GetLinkSettings2: dont crash in case of unsupported ioctl(SIOCETHTOOL) | Fixed |   
CDS-81772 | Bug | License Manager: Request offline file fails | Cannot Reproduce |   
CDS-81769 | Improvement | CmpMemGC: SystemTrace needed to check memory consumption on runtime per component | Fixed | [[COMPATIBILITY_INFORMATION-EndUser]]  
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
CDS-81757 | Bug | OPC DA Server: Setup displays empty firewall dialog | Fixed |   
CDS-81754 | Bug | CmpSessionInformation: Integration into FW based on C++ RunTime does not work | Fixed |   
CDS-81670 | Improvement | Project Compare: Changes in Communication Setting are not recognized | Fixed |   
CDS-81640 | Bug | Library Manager, PLCopenXML import: Placeholder resolution gets lost | Fixed |   
CDS-81571 | Bug | CmpOpenSSL: Update OpenSSL to version 3.0.5 (LTS) | Fixed |   
CDS-81552 | Bug | Linux Templates don't compile with gcc version >= 10 | Fixed |   
CDS-81543 | Bug | Device, POU: "Index outside the bounds error" if "Auto Hiding" is active | Duplicate |   
CDS-81542 | Bug | LibMan: Device update of container libs with "NotImplementedByDevice" dependent libs not working correctly | Won't Fix | [[GENERAL]]  
The device description for SP12 does not define a placeholder resolution for CmpUserMgr_Implementation. After updating the device to SP12, the placeholder redirect will therefore keep the same resolution it had before the update i.e. CmpUserMgr Implementation 3.5.19.0. Before SP17 the Libraryprofile contained a redirection to NotImplementedByDevice, that would have be used in this case, but since SP17 the libraryprofile does not exist anymore.   
The new logic is: if there is no new resolution of the placeholder, the old resolution is preserved. Workaround is manually resolve to NotImplementedByDevice-Library.  
CDS-81539 | Improvement | CmpBlkDrvTcp: Improve ethernet configuration options | Fixed | [[COMPATIBILITY_INFORMATION]]  
[[COMPATIBILITY_INFORMATION-OEM]]  
The setting BLKDRVTCPKEY_STRING_LOCALADDRESS is now deprecated and only kept for compatibility reasons. It is replaced by the new setting BLKDRVTCPKEY_STRING_NETWORK_ADAPTER.  
See CmpBlkDrvItf.h for details.  
CDS-81537 | Improvement | OPC UA Server: Improve ethernet configuration options | Fixed |   
CDS-81536 | Improvement | CmpWebServer: Improve ethernet configuration options | Fixed | [[COMPATIBILITY_INFORMATION]]  
[[COMPATIBILITY_INFORMATION-OEM]]  
The settings "LocalAddress", "LocalAdapterName" and "LocalAdapterNameUnicode" are now deprecated and only kept for compatibility reasons. It is replaced by the new setting "NetworkAdapter".  
See CmpWebServerItf.h for details  
CDS-81513 | Improvement | VxWorks: Definition of max/min in sysspecific.h collides with C++17 build | Duplicate |   
CDS-81442 | Bug | CmpTecTask, function __sys__rts__cycle__2 without SIL2 check | Fixed |   
CDS-81435 | Bug | VxWorks / C++ : Definition of max/min in sysspecific.h collides with C++ 17 build | Fixed | [[GENERAL]]  
Fixed clash with min/max macro under VxWorks with c++17  
CDS-81347 | Bug | IEC-Texteditor: Auto complete inserts text at wrong position in Word Wrap mode | Fixed |   
CDS-81313 | Bug | Python API - Move will delete nodes in case of incorrect index | Fixed |   
CDS-81152 | Bug | GVL: Wrong addresses shown for located variable of DUT2 type, which contains an ARRAY of DUT1 | Fixed |   
CDS-81135 | Improvement | Device Repository: Option for detailed installation information | Fixed |   
CDS-81123 | Bug | OPC UA Server: session cleanup improper, always ends in timeout | Fixed |   
CDS-81090 | Bug | On DPI != 100% (or on High-Res screens), scaling of CODESYS MainForm scaling changed when clicking on element in lib man editor | Cannot Reproduce |   
CDS-80905 | Improvement | Modify sysdefines.h to allow defining NUM_OF_STATIC_IEC_EVENTS outside of the header | Fixed |   
CDS-80769 | Improvement | PLCHandler: Windows: Support VS2022 and remove support for VS2010 | Fixed |   
CDS-80754 | Improvement | Projectarchive: check if extracted file is identical with existing before prompting dialog | Cannot Reproduce | [[GENERAL]]  
Equality check has already been implemented by CDS-21407.  
CDS-80218 | Improvement | [Technical Debt] Refactor ProjectArchive | Fixed |   
CDS-80055 | Improvement | Login: Adapt message about Controller vs. Firmware version mismatch | Fixed |   
CDS-80035 | Bug | IPMCLI: Deferred installations will be cleared within a regular installation | Fixed | [[GENERAL]]  
When running IPMCLI with -i or -idrc previously deferred installations will also get installed  
CDS-79879 | Bug | Linux SysSockGetNextAdapterInfo shows no MAC Address for alias interfaces | Fixed |   
CDS-79436 | Bug | RTE: SysEthernet: CmpEt1000Drv: i219 LM does not work correctly . | Fixed |   
CDS-79391 | Epic | Qt6-Linux | Fixed |   
CDS-79379 | Improvement | Remove CODESYS Softmotion V3 from CODESYS and CODESYS Control setup (32 and 64 bit) | Fixed | [[GENERAL]]  
The CODESYS SoftMotion Win* and CODESYS SoftMotion RTE* device descriptions are no longer installed, nor are the *SoftMotion*.cfg configuration files. They are deprecated since V3.5 P17 (CDS-73957).  
CDS-79106 | Bug | Runtime: Exceptions in (asynchronous) GlobalInit handled incompletely | Fixed |   
CDS-78688 | Improvement | [Technical Debt] WatchList: Refactor WatchListNodeUtils | Fixed |   
CDS-78218 | Bug | CmpUserMgr: Authentication fails with insufficient memory w/o meaningful message or is terminated with an OutOfMemory exception | Fixed |   
CDS-77710 | Bug | Windows: Gateway/Runtime may crash, if more than 15 active IP addresses are available | Fixed |   
CDS-77578 | Bug | CmpBlkDrvCanServer: task prio is not set correctly in all cases | Fixed |   
CDS-76860 | Bug | OnlineManager: Sometimes users have to login twice on Clean Machines | Fixed |   
CDS-76605 | Bug | CmpApp: Bootproject must never be renamed or deleted in case of an exception | Fixed | [[COMPATIBILITY_INFORMATION-EndUser]]  
This is the existing setting adressed by this bugfix :  
[CmpApp]  
Bootproject.InvalidateNever=1  
=>[Default=1]: The bootproject should never be invalidated or deleted after an exception!  
  
This setting was ignored in the following cases:  
\- The bootproject was deactivated after an exception in non IEC tasks!  
\- The bootproject was deleted after an exception in an IO-driver during configuration phase!  
  
Bootproject is now never deleted or renamed in any case of an exception!  
CDS-76352 | Improvement | TaskMapList: Allow adding of new ITaskMapping to ITaskMappingInfo List | Fixed |   
CDS-76333 | Bug | Importing Project User Rights is vulnerable to brute force attack | Fixed | [[GENERAL]]  
For more details see Advisory 2023-08, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17768&token=9d206ea9e0449cd9d3ee60d5179d2761dad2d2dd&download=  
CDS-75569 | Bug | Add Object: Error index was outside the bounds | Fixed |   
CDS-75542 | Improvement | Fast Online Change doesn't work when type of local variable was modified | Won't Fix | [[GENERAL]]  
Changing the type of existing variables is an ambigious operation for the online change. For the compiler it is unclear whether it should try to preserve and cast the existing value or whether the variable should be reinitialized. Additionally casting is not always possible without data loss if the new type is smaller than the old type. In such cases it is always the better solution for the user to also rename the variable.  
CDS-74806 | Bug | CmpOPCUAClient: Pass return value of VerifyServerCertificate to ConnectionStateCallback | Fixed | [[COMPATIBILITY_INFORMATION]]  
The verification result returned by VerifyServerCertificate is now passed to the ConnectionCallback if the verification was not good.  
CDS-74271 | Bug | LacUtil: Option copyrefs does not work without administrative rights | Fixed | [[GENERAL]]  
Message of missing administrative rights has been reworked. Furthermore without admin rights the update of the Windows GAC will no longer be done. Instead there is a new console message.  
CDS-74219 | Improvement | CodeMeter: improve debugability of CmpCodeMeter | Fixed |   
CDS-73853 | Improvement | Project Recovery: allow recovery for integrity-protected projects | Fixed | [[GENERAL]]  
Project recovery will now be possible for projects that have the integrity check option enabled.  
CDS-73154 | Improvement | STM32 Cube: implement CANmini driver | Duplicate |   
CDS-73151 | Improvement | STM32 Cube: add VisuLight feature to configuration and implement frame buffer | Fixed | Enabled usage of external SDRAM bank 2 via FMC. Created Framebuffers in said SDRAM. Enabled the 640x480 display. Implemented TargetVisuLight.  
CDS-72769 | Improvement | CODESYS Linux: replace DEBUGP with proper CmpLog calls | Fixed | [[GENERAL]]  
Replaced startup parameter "-d" with logfilter-settings in .cfg file.  
CDS-71411 | Improvement | Compile: Fast Online for large projects slows down due to stack check | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
With the compiler define "suppress_stack_check" set in the build options of the application the check for the stack usage can be disabled.  
CDS-71190 | Bug | OPC UA Server: iTcpTransport_MaxChunkCount is ignored on PI or Win7 | Cannot Reproduce |   
CDS-71115 | Improvement | Precompile: be aware of __vfinit | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.0  
CDS-70807 | Bug | Properties dialog, Tab Encryption, table not completely visible | Fixed |   
CDS-70485 | Improvement | OPCUA Server: React to changes of the certificate store and renew endpoints with updated certificates | Fixed |   
CDS-70354 | Bug | [OpcUa Client]: some negative tests do not show expected behaviour | Fixed |   
CDS-70231 | Bug | CANbus: Type will be renamed although not selected in the refactoring dialogue | Won't Fix | [[GENERAL]]  
In the device description the FB instance name is defined with the macro $(DeviceName). Therefore the name is always replaced by the name of the object in the tree.  
Renaming the device in the tree changes the fb instance automatically as the FB instance name is not fixed.  
CDS-69882 | Improvement | CmpCodeMeter: Update to CodeMeter Embedded SDK 2.53 | Won't Fix | [[GENERAL]]  
SDK version is obsolete  
CDS-69281 | Improvement | Plugin Cache: The cache should be moved to the plugins folder of the installation | Fixed | [[COMPATIBILITY_INFORMATION]]  
The plugin cache will now be written into the plugins folder of the installation if possible. If the installation directory is not accessible ProgramData\AP\PlugInCaches will be used as fallback.  
An existing cache will not be moved unless it is rebuilded.  
DeletePluginCache.exe deletes caches from both locations if available.  
CDS-69138 | Improvement | Compare: allow to edit (freely) in compare mode | Duplicate | [[GENERAL]]  
This issue has already been fixed with CDS-78094.  
CDS-68844 | Improvement | Runtime: File Transfer: If there are many files to transfer, each download takes several seconds although the files are already present in the runtime | Fixed | [[COMPATIBILITY_INFORMATION]]  
[[COMPATIBILITY_INFORMATION-OEM]]  
[[GENERAL]]  
  
The error handling of the SRVFT_GET_FILEINFO online service has been changed.  
The following is the complete description of the service response:  
  
The service response does not contain a TAG_REPLY_FILEINFO tag only if the alignment and size check of the tag contents failed.  
In this case, it contains only a TAG_REPLY_ERROR tag.  
In all other cases, the service response always consists of a TAG_REPLY_FILEINFO tag.  
\- The TAG_REPLY_FILEINFO tag does only include a TAG_FILENAME tag if the service request did contain a TAG_FILENAME tag and no error occurred during the online operation.  
\- In addition to the TAG_FILENAME tag, the TAG_REPLY_FILEINFO tag contains the following additional tags, depending on the error situation:  
a) In case of missing access rights to the file: The two complex tags TAG_ONLINE_ACCESS_RESULT and TAG_ONLINE_ACCESS_OBJECT.  
b) For all other errors: The TAG_REPLY_ERROR tag.  
c) If executed without errors, the complex tag TAG_FILEINFO.  
  
The new online service SRVFT_GET_MULTI_FILEINFO does the same as SRVFT_GET_FILEINFO for multiple files at once, except for the following differences:  
  
\- The TAG_REPLY_FILEINFO tag does not include a TAG_FILENAME tag only if the service request did not contain a TAG_FILENAME tag.  
In all other cases, the TAG_REPLY_FILEINFO tag always includes a TAG_FILENAME tag.  
\- Maybe not all FileInfos can be transmitted in one single online service.  
In this case the service returns ERR_ENTRIES_REMAINING to indicate that more FileInfos are available.  
\- The TAG_REPLY_ERROR tag is always included at the beginning of the service response.  
CDS-68044 | Improvement | Device status page: Opimize layout | Fixed |   
CDS-67739 | Bug | Project Information, Last Saved with: the entry "Last Saved with" is only updated at Save As, but not at Save | Fixed | [[GENERAL]]  
This fix just replaces the string "Last saved with" with "Storage format" in the UI. The value will not be changed because the value displays the storage format and has no direct relationship to the exact version of CODESYS that was used for saving the file for the last time. There will be an additional documentation for this in the online help to clarify the situation for the end user (CDS-86082).  
CDS-67283 | Improvement | Dynamic licensing for OPC UA: check license more often | Fixed |   
CDS-67142 | Improvement | Smart Tags, Autodeclare: Offer direct declaration of VAR_INPUT | Duplicate | [[GENERAL]]  
Duplicate of CDS-85458  
CDS-67091 | Improvement | Package Manager: Use packed package for archiving | Fixed | [[GENERAL]]  
Use original package for archiving  
CDS-66508 | Bug | Signature: Invalid signature by extracting projectarchive | Fixed |   
CDS-65211 | Bug | TaskConfig: Object reference not set to an instance of an object | Cannot Reproduce | [[GENERAL]]  
This problem has been fixed with CDS-81285  
CDS-64847 | Improvement | SysTimeRtc: Offset in timezone should be UTC_Offset instead of Bias | Duplicate | [[GENERAL]]  
Duplicates CDS-64846.  
CDS-64846 | Bug | SysTimeRtc: Provide current timezone name, use UTC_Offset instead of Bias | Fixed | [[GENERAL]]  
The SysTimeRtcGetTimezone function has been marked **deprecated** as of release 3.5.20.0. Replacement is the SysTimeRtcGetTimezone2 function. Windows runtimes only return an IANA time zone if the operating system version is greater than or equal to Windows 10 version 1903.  
CDS-63970 | Bug | Compiler: Write access to VAR_INPUT does not lead to warning/error | Won't Fix | [[GENERAL]]  
We already provide a SAN rule SA0037 to check for this potential bug.  
CDS-63004 | Bug | Initialization: Namespace resolution does not work with nested libraries | Won't Fix | [[GENERAL]]  
This behaviour is intended, a namespace is not required at this location.  
CDS-62453 | Bug | Compile:The keyword INTERNAL is not working properly in libraries | Won't Fix | [[GENERAL]]  
See: https://ericlippert.com/2012/11/13/why-is-deriving-a-public-class-from-an-internal-class-illegal/  
CDS-60966 | Bug | License Manager: Expired items are not displayed as expired in the license manager | Cannot Reproduce |   
CDS-60424 | Bug | CmpCodeMeter: expired licenses are not detected correctly on Linux runtime | Fixed | [[COMPATIBILITY_INFORMATION]]  
Returned error code of CodeMGetContentByFirmcode* funktions was enhanced: for example if the license is expired they now return the new error code ERR_LICENSE_EXPIRED.  
CDS-59523 | Bug | FBD: Overlapping boxes | Cannot Reproduce | StR: Ok  
CDS-59416 | Bug | FBD: Change in ST box not automatically committed on login via keyboard shortcut | Cannot Reproduce | StR: Onile Change box is shown.  
CDS-59373 | Bug | FBD Editor: Drag and Drop of Inputs does not work any more. | Cannot Reproduce | StR: Ok  
CDS-59315 | Bug | Task Management: An watchdog exception occurs only in simulation mode | Cannot Reproduce | StR: Runs half an hour without watchdog.  
CDS-59262 | Bug | Package Designer: Exception installing a package due to missing access rights | Won't Fix | [[GENERAL]] package designer was redesigned.  
CDS-59180 | Bug | Package Designer: Changing id number of Sub Component from "1" to "99" gives an assertion error | Won't Fix |   
CDS-59176 | Bug | Breakpoint: Menu commands in breakpoint view not activ on first start. | Won't Fix |   
CDS-59169 | Bug | Web-based Online Help, SoftMotion: Wrong links for all SMC_TRAFO FBs | Cannot Reproduce | [[GENERAL]] works fine with new online help.  
CDS-59128 | Bug | Refactoring: Wrong method name is displayed in ST editor when renaming overridden method | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-58777 | Bug | LibMan : the library is currently loaded in background - message stay on some libraries | Cannot Reproduce | [[GENERAL]]  
StR: Ok  
CDS-58747 | Bug | Refactoring, Add variable: Does not work with persisteant vars | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-58629 | Bug | OnlineHelp: The result of the search will display the old library version. | Cannot Reproduce | StR: Ok  
CDS-58601 | Bug | The "View\Security" permission is not assigned to the "Security Screen" icon. | Cannot Reproduce | [[GENERAL]] Could by no means open the security screen.  
CDS-58563 | Bug | Logger: Double component entries | Cannot Reproduce | not reproducable.  
CDS-58497 | Bug | LibDoc: Using japanese characters leads to the message "Malformed Table" | Cannot Reproduce | StR: Ok  
CDS-58477 | Bug | Lib Development: Message "C0077: Unknown type..." occur if second level lib have the version 0.0.0.0 | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-58121 | Bug | Package Designer: Un/installation of package can fail ( restricted access right ) | Won't Fix | [[GENERAL]] package designer was redesigned.  
CDS-58100 | Bug | Signed Devdescs: OEM plugin cannot cancel the installation of devdescs with an invalid signature | Won't Fix | [[GENERAL]] No longer required.  
CDS-58046 | Improvement | Implicit Reference Type: Support Reference Type in Reference Type | Won't Fix | [[GENERAL]]  
The feature for implicit reference types is discontinued, new improvements or bug fixes will not be implemented.  
CDS-57934 | Bug | Library Manager: Hidden methods are visible in some scenario | Won't Fix | [[GENERAL]]  
This minor bug will not be fixed because no customer is waiting for it.  
CDS-57849 | Bug | Force List: Duplicate entry for camel case pous and NullReferenceException on unforce | Cannot Reproduce | StR: no double entry, no object reference error message.  
CDS-57848 | Bug | Several CODESYS versions on one computer influence each other | Cannot Reproduce | [[GENERAL]] Modularisation changed everything. Sandbox will solve the rest.  
CDS-57845 | Bug | Menus missing | Cannot Reproduce | [[General]] Everything changed with modularisation.  
CDS-57821 | Bug | OnlineCommands: Simulation Mode can be activated for non PLCs which leads to corrupt projects. | Cannot Reproduce | StR: Simulation is not offered.  
CDS-57819 | Bug | PLCopenXML, LD: ENO pin removed | Cannot Reproduce | StR: Ok  
CDS-57811 | Bug | Conversion of an array of derived interface differ to the conversion of an variable | Won't Fix | [[GENERAL]] as designed.  
CDS-57744 | Bug | DeviceCommunication: Use detailed description of PLC shell commands | Won't Fix | [[GENERAL]]  
This trivial bug will not be fixed as the description is already present in the web help.  
CDS-57742 | Bug | Documentation: Search in Online Help does not work with "-" | Cannot Reproduce | StR: tried to search add-on. Works fine.  
CDS-57619 | Bug | CompareProject: Compare project with it's self show changes in Library Manager | Cannot Reproduce | StR: project saved with latest version and compared with itself: no differences.  
CDS-57610 | Bug | Call Tree View: endless call recursion for function block callers | Cannot Reproduce | StR: Ok  
CDS-57602 | Bug | CompareProject: Comparison dialog closes even then the commit failes | Cannot Reproduce | StR: Ok  
CDS-57503 | Bug | User Management: Group view doesn't refresh user state | Cannot Reproduce | [[GENERAL]] Handling is different now. Problem cannot be reproduced.  
CDS-57416 | Bug | Warning "C0373: Channel XYZ is already used in another task..." should only occur on direct access of the mapped variable | Cannot Reproduce | [[GENERAL]] No Warning any more. Static Analysis generates warning.  
CDS-57334 | Bug | Library Manager - 1st item (Cut) of contextual menu of a library is immediately selected | Cannot Reproduce | StR: Ok  
CDS-57333 | Bug | Going online with 2 samed GVLs (one in app and one in POUs pool) only the one from the app will be monitored | Cannot Reproduce | [[GENERAL]]  
Issue cannot be reproduced anymore with V3.5 SP20  
CDS-57089 | Bug | Monitoring: enumeration drop down for "Prepared Value" not qualified | Cannot Reproduce | StR: Ok  
CDS-56560 | Bug | OnlineUserManagement: no login possible after "reset origin device" | Cannot Reproduce | [[GENERAL]] StR : Ok  
CDS-55390 | Bug | OPC UA Server: Improve Performance of TranslateBrowsePathToNodeId service | Fixed |   
CDS-54772 | Bug | Refactoring: Renaming functions or methods via "Refactoring" in declaration editor does not update Project Tree and calls | Duplicate | [[GENERAL]]  
Duplicates CDS-64691  
Tested with latest version: Works fine  
CDS-54283 | Bug | Pragma does not work in declaration part | Won't Fix | [[GENERAL]]  
We will not just extend the existing feature to interfaces but provide a new feature with CDS-86170  
CDS-54226 | Bug | Error "C0032: Cannot convert type Unknown type..." occur on using visualization from chained library | Duplicate | [[GENERAL]]  
Duplicate of CDS-86482  
CDS-54111 | Bug | IecVarAccess: If ROOT__NODE is available leaf nodes cannot resolved below __MIO | Cannot Reproduce |   
CDS-54014 | Bug | Generate Code: NullReferenceException with __CAST operator | Fixed | [[GENERAL]]  
Compile error "Identifier not defined" with compilerversion >= 3.5.20.0  
CDS-53835 | Bug | External file object: Timestamp of last modification is changed when a file is just opened for viewing | Cannot Reproduce |   
CDS-52334 | Bug | CmpIecTask: IecTaskCheckWatchdog has unnecessary INT cast | Won't Fix | [[GENERAL]] Build fails if mentioned cast is removed  
CDS-50928 | Improvement | Compiler: it should be possible to declare Array of Reference | Won't Fix | [[GENERAL]]  
This feature will not be implemented. Adding support for ARRAY OF REFERENCE would lead to ambigious syntax when accessing elements of that array. This is due to the fact that references are always implicitly dereferenced in contrast to a pointer and also because the index access operator is already overloaded for POINTER TO as it represent both an pointer to one element or an array of elements.  
CDS-50706 | Improvement | Runtime: File Transfer: Make bulk checks for files to speed up file consistency check during project download | Duplicate |   
CDS-50705 | Improvement | CODESYS: File Transfer: Make bulk checks for files to speed up file consistency check during project download | Duplicate |   
CDS-50084 | Bug | LMM: Resolving implicit check function shadowing may require clean/rebuild | Fixed | [[GENERAL]]  
The warning message is quite a special case. Detecting the relevant change would be very difficult, so we just changed the warning with the additional hint that a clean is necessary to use the hidden check function.  
CDS-49283 | Bug | Target Settings Linux: SysEthernet Filter's default value is set to EtherCAT-Frames only | Fixed | [[GENERAL]]  
Changed default of setting Linux.ProtocolFilter to 3 (ETH_P_ALL)  
CDS-49167 | Improvement | LibMan: Publish unbound placeholder resolution for AP customers | Won't Fix | [[GENERAL]]  
The method void IUnboundPlaceholderService.ResolveUnboundPlaceholdersRecursively(int projectHandle, Guid objectGuid, ILibManItem lmi, IList<string> filter) already exists as part of the public interface.  
CDS-48222 | Bug | Conditional breakpoints: no break on condition [some LREAL] <> [some LREAL] | Won't Fix | [[GENERAL]]  
1\. Cannot reproduce with compilerversion 3.5.20: "If a is an LREAL, then the condition a <> 0 won't trigger a breakpoint, even if a <> 0\. '=' does not seem to work well, either."  
  
2\. Won't fix: "ABS cannot be used within conditional breakpoint statement as it is an unsupported operator"  
CDS-47928 | Improvement | OPC UA Server / Split up startup of the OPC UA server in different init hooks | Fixed |   
CDS-46348 | Improvement | IecVarAccess: Type name of structs should be available by online services | Fixed |   
CDS-46346 | Improvement | PLCHandler: All V3 Interfaces: PlcSymbolDesc should provide struct name | Fixed |   
CDS-45888 | Bug | Symbolconfig/IecVarAccess: 3 dimensional ARRAY OF ARRAY OF ARRAY is not resolved correctly by browse feature | Cannot Reproduce |   
CDS-42991 | Epic | Visu, WebVisu: The language in the visualization should be clientspecific | Fixed |   
CDS-40906 | Bug | Monitoring: LREAL with many digits is shown wrong at 17nd digt | Won't Fix | [[GENERAL]]  
The precision of double values is limited. It is difficult to tell which values can be actually represented. .Net produces the same value for the same double literal, therefore we think the precision is good enough.  
CDS-40905 | Improvement | Logical devices: selection dialog for safeIO auto-mapping with multiple safe cpu (EL6900,SIL3) as slave (PN,ETC) | Fixed |   
CDS-36846 | Improvement | Logical devices: hierarchical safeIO auto-mapping with multiple safe cpu (EL6900,SIL3) as slave (PN,ETC) | Fixed | ,  
CDS-36290 | Improvement | ProjectCompare: Handling of MetaObject properties | Fixed |   
CDS-36146 | Improvement | Project: "Project Archive" dialog should display device versions | Fixed |   
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2024 CODESYS GmbH  | A member of the CODESYS Group 
