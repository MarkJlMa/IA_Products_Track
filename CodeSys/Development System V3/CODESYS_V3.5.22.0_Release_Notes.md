[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS V3.5 SP22

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
CDS-97564 | Bug | CLONE - Redundancy: Memleak if the configured ip address is not available | Won't Fix | [[GENERAL]] Implementing the fix at this late stage of the release carries too much risk.  
CDS-97508 | Improvement | LibDevSummary: Adjust the version information to SP22 | Fixed |   
CDS-97384 | Improvement | CLONE - CmpRedundancy: Make BootupWaitTime configurable | Fixed |   
CDS-97383 | Improvement | CLONE - Redundancy, Controller: add logmessages if the redundancy configuration does not match the PLC/project | Fixed | [[GENERAL]] The log messages that indicate that the configuration of application or task name do not match with the actual loaded bootproject, are now clearer.  
CDS-97382 | Improvement | CLONE - CmpRedundancy: Protocol should be resilient to tcp retransmissions | Fixed |   
CDS-97381 | Bug | CLONE - CmpRedundancyConnectionIP: No sync possible if one link is death at startup | Fixed |   
CDS-97380 | Bug | CLONE - Redundancy, Controller: After download active/passive can't be achieved | Fixed |   
CDS-97379 | Bug | CLONE - CmpRedundancy: Sync of PLC_ID1 not possible after reboot | Fixed |   
CDS-97378 | Bug | CLONE - CmpRedundancy: Collision of two mechanism to sync at bootup | Fixed | [[GENERAL]] When both PLCs are started simultaneously, PLC1 now typically becomes active first. In this scenario, PLC2’s startup may be slightly delayed, and a corresponding log message is generated on at least one of the PLCs.  
CDS-97377 | Bug | CLONE - CmpRedundancy: Invalid/Old sockets are not closed when switching to simulation | Fixed |   
CDS-97270 | Bug | CLONE - CmpOPCUAServer: Crash if CloseSession (or another service) is called before ActivateSession has finished | Fixed |   
CDS-97267 | Bug | Windows V3 delivery builds do not generate valid targetdefines.h | Fixed |   
CDS-97153 | Bug | CmpOpenSSL: Security issues in OpenSSL versions before 3.5.5 | Fixed |   
CDS-97149 | Improvement | DeviceObject:: update device should change settings for online configuration change | Fixed |   
CDS-97133 | Bug | CLONE - CompileErrors with lib in Pool | Fixed |   
CDS-97129 | Bug | CmpOpenSSL: Improve and update compatibility check for OS integrated OpenSSL versions | Fixed | [[COMPATIBILITY_INFORMATION]]  
Support for OS integrated OpenSSL versions below 3.0 has been discontinued.  
In other words we now accept all OpenSSL Versions >= 3.0.  
CDS-97007 | Bug | CLONE - CmpOPCUAServer: Racecondition in session timout calculation | Fixed |   
CDS-96933 | Bug | TargetVisu: Security issues in Qt versions before 6.10.2 | Won't Fix | [[GENERAL]]  
This issue will not be fixed because the CVE-2025-12385 was assessed to not affecting the CODESYS Targetvisualization and therefore the update to Qt 6.10.2 is not necessary at the moment.  
CDS-96902 | Bug | Runtime Settings: It is no longer possible to delete a configuration entry | Fixed |   
CDS-96886 | Bug | SysEthernetLinux XDP: two test cases with EtherCAT autotest do not work | Fixed |   
CDS-96842 | Bug | Japanese Localization: Menu item "Export" is wrong | Fixed |   
CDS-96803 | Bug | False positiv SA0034 | Duplicate | [[GENERAL]]  
Duplicate of CDS-94075  
CDS-96796 | Improvement | Device: add new license metrics to distinguish controller and device instances | Fixed |   
CDS-96791 | Bug | Refactoring: Remove variable doesn't work in Transitions in some cases | Fixed |   
CDS-96786 | Improvement | Linux QS-Targets: Update Defaults for recently added security settings | Fixed |   
CDS-96785 | Improvement | StringUtils: Provide method FromConstantString in CharBufferString that does not copy the string | Fixed |   
CDS-96783 | Improvement | RTE: Update Defaults for recently added security settings | Fixed |   
CDS-96782 | Improvement | Device Log UI: Finetune UI implementation | Fixed |   
CDS-96165 | Bug | Project Creation: Project starting with # can not be created | Fixed |   
CDS-96132 | Bug | Compiler: RawST parser does not report errors in case of POUs at unexpected position | Fixed |   
CDS-96131 | Improvement | Fix QNX builds | Fixed |   
CDS-96114 | Improvement | Reset s_tLastWdTick in CH_Init | Fixed |   
CDS-96113 | Improvement | CmpLinuxRTDiag: adapt CAL_CMHOOK(SETTINGS_CHANGED,...) | Fixed |   
CDS-96104 | Bug | CmpLog: if BUFFER_OVERFLOW occurs, all available entries should be provided to CODESYS | Fixed |   
CDS-96103 | Bug | DeviceEditor: additional empty IO-Mapping page is shown | Duplicate |   
CDS-96097 | Bug | Various commands from Addons are still part of essentials configuration | Fixed |   
CDS-96093 | Bug | Update Device: fails if devdescs have specific differences in connector params | Fixed |   
CDS-96092 | Bug | Libman, Parametervalues: Use the displayname without version for saving parameterlist | Fixed | [[GENERAL]]  
The library parameters were stored with a wrong key (containing a fixed version) if the library uses the newest version ("*")  
This caused problems when installing a newer version of the library.  
Now the library parameters will be stored using "*" instead of a fixed version.  
  
[[KNOWN_LIMITATIONS]]  
For existing projects, the values have to be changed again, then the values will be stored correctly.  
Only after a modification of the library parameters the correct key will be used.  
CDS-96083 | Epic | XDP Bursts | Fixed |   
CDS-96082 | Bug | Restart after setting dpiunaware drops commandline arguments | Fixed |   
CDS-96079 | Bug | Visu Device User Management is not possible with encrypted communication | Duplicate | [[GENERAL]] The CODESYS Webvisualization is now able to communicate also if encrypted runtime communication is enforced.   
Please remark: If you also want to encrypt the communication of the CODESYS Webvisualization, the following security setting of the webserver should be active:  
[CmpWebServer]  
SECURITY.CommunicationMode=HTTPS  
; Alternatively  
; SECURITY.CommunicationMode=REDIRECT_HTTP_TO_HTTPS  
CDS-96075 | Bug | CmpRedundancy: Possible Loggerspam due to acyclic redundancy feature | Fixed |   
CDS-96068 | Bug | Compiler: LibraryTable ignores 'Publish Symbols' of underlying libraries | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-96067 | Bug | CmpOPCUAServer, CmpOPCUAStack: Harden AuditLogs against specifiers placed in user defined text | Fixed | [[GENERAL]]  
For more details see CODESYS Security Advisory 2026-03, which is available on the CODESYS website:  
https://api-www.codesys.com/fileadmin/user_upload/CODESYS_Group/Ecosystem/Up-to-Date/Security/Security-Advisories/Advisory2026-03_CDS-95911.pdf  
CDS-96053 | Bug | DeviceObject: Update device removes manual change | Fixed |   
CDS-96048 | Bug | Login not possible "An item with the same key has already been added" | Fixed |   
CDS-96044 | Improvement | CmpRtDiag - new command to enable performance event kernel trace marker | Duplicate |   
CDS-96038 | Improvement | [Project Inspection] Possibility to modify add-ons for creating a new installation | Fixed | [[GENERAL]] Two new OEMCustomization Hooks  
Section: InstallerIntegration; Key: FilterRequiredAddOns; Data Type: Func<IEnumerable<IAddOnInformation>, IEnumerable<IAddOnInformation>>  
Section: InstallerIntegration; Key: FilterOptionalAddOns; Data Type: Func<IEnumerable<IAddOnInformation>, IEnumerable<IAddOnInformation>>  
CDS-96035 | Bug | SVG-Renderer: Security issues in OSS versions before (libcurl 8.18.0, libpng 1.6.54) | Fixed | [[GENERAL]]  
Updated libcurl.dll to version 8.18.0  
Updated libpng to 1.6.54  
CDS-96029 | Bug | DeviceObject: Fastonlinechange needs more time if OEMCustomization is set | Fixed |   
CDS-96023 | Bug | Windows Overlay Targetvisu: Crash during TargetVisu shutdown | Cannot Reproduce | [[GENERAL]]  
The issue could not be reproduced with the provided information on a ControlWin SoftSPS.  
CDS-95999 | Bug | Logical IO: InvalidObjectGuidException on compile when linked device missing | Fixed |   
CDS-95994 | Bug | [FBS] Save as dialogs point into temporary folder | Fixed |   
CDS-95993 | Bug | SysTarget with CmpSettingEmbedded -> no device name, no vendor available from targetdefines.h | Fixed |   
CDS-95984 | Improvement | Library Manager: SourceLibraryProviders should be used for selected libraries | Fixed |   
CDS-95981 | Bug | runtime system documenation: article designation inconsistent for 'ThisisanextensioninthehighwordofTypeClass3 ' | Fixed |   
CDS-95978 | Improvement | CmpUserMgr: Enable loading of saved rights databases via API | Fixed |   
CDS-95976 | Bug | Project folder can not be deleted | Fixed |   
CDS-95965 | Bug | Library Manager: Documentation shows BLACK background and text when Windows color set to Dark | Fixed |   
CDS-95960 | Bug | Check All PoolObjects: Empty Library results in Exception | Fixed |   
CDS-95957 | Improvement | CmpLinuxPrivilegeProxy should provide a PLCShell command to show which linux user and group the process is running | Fixed | [[GENERAL]]  
New PLCShell command "getlinuxids" available to show user and group under which the runtime process is executed.  
CDS-95953 | Improvement | Extend profile serializer to serialize optional profile name | Fixed |   
CDS-95944 | Improvement | CmpApp: Time needed by onlinechange should be logged optional | Fixed | [[GENERAL]]  
OnlineChangeCode execution time calculation can be instrumented by the following logfilter:  
  
[CmpLog]  
;--Component specific logger filters:--  
CmpApp.Filter=0xFFFFFFFF  
CDS-95937 | Improvement | Improve diagnostic message in case of exception in CommCycle hook | Fixed |   
CDS-95932 | Bug | Download required after reloading specific customer project | Won't Fix | [[GENERAL]]  
The download is caused by the customer project.  
When the project is opened the customer plugin sets a parameter to value 0.  
Also the dirty flag is set.  
In the event OnBeforeCompile the value is set 4.  
A plugin must not change any parameter values when a project is opened.  
Therefore won' t fix!  
CDS-95931 | Bug | No error is returned if raw st could not be parsed | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
New Interface IRawSTParser2 with method ParsePOUs(out IEnumerable<IMessage>)  
CDS-95916 | Bug | CmpCodeMeter: missing USEEXTERN_STMT in CmpCodeMeterUtils.c: cannot compile with gcc14 | Fixed |   
CDS-95915 | Bug | Project Compare: New slot device cannot be applied in project compare | Fixed | [[GENERAL]]  
When merging changes for a slot device, both of its associated lines must be accepted.  
  
[[KNOWN_LIMITATIONS]]  
At the moment, changes to the parent EtherCAT device cannot be merged. This limitation is tracked in issue ECAT-879.  
CDS-95906 | Bug | Exception on Open FBS project due to merge conflict markers | Fixed | [[GENERAL]]  
Update the ObjectType property on the meta object after the object has been fetched.  
CDS-95900 | Improvement | Compiler: More general description of compile warning C0351 | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-95891 | Bug | ComponentManager: Returning error code in CH_POST_INIT and CH_PRE_INIT2 of a component does not lead to safemode | Fixed |   
CDS-95887 | Bug | Compiler: Internal Error when assigning constant or property rvalue to "REFERENCE TO" input | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.22.0  
  
Note that input assignments in call expressions to parameters of type "REFERENCE TO ..." are always implicitly reference assignments (REF=).  
Therefore the right-hand side of the assignment must be an expression whose address can be taken (e.g. a variable), or the literal 0.  
  
The compiler now generates proper error messages during compile in those cases. This includes error messages for assigning literals other than 0 or e.g. when trying to assign a property.  
CDS-95885 | Bug | [Logical Exchange GVL] Incomplete Editor if WIN language is Chinese(traditional) | Fixed |   
CDS-95878 | Improvement | Update to CodeMeter version 8.40b | Fixed |   
CDS-95872 | Bug | Setting BP results in "Object reference not set..." | Duplicate | [[GENERAL]]  
CompilerVersion >= 3.5.22.0  
  
Duplicates CDS-94120  
CDS-95864 | Improvement | Remove internal libraries for CODESYS Safety Support from the setup | Fixed | [[GENERAL]]  
Following libraries have been removed from setup:  
SNCM ECAT Slave/3.5.17.0  
SNCM ECATSlave Interfaces/3.5.17.0  
IoDrvEtherCATSafeCPU/3.5.17.0  
IoDrvEtherCAT/3.5.17.0  
IODrvEtherCATDriver/3.5.17.0  
EtherCATStack/3.5.17.0  
CDS-95860 | Improvement | Support xdp for multiple adapters | Fixed |   
CDS-95858 | Improvement | Improve runtime features to support online change for IO devices | Fixed | [[GENERAL]]  
There are 2 runtime features to enable online configuration changes:  
\- OnlineConfigurationChange.xml:  
=>Enables fix online changes for IO-configuation, alarms, datasources  
\- OnlineConfigurationChange_licensable.xml:  
=>Enables the check box under "PLC settings" in the device to activate online configuration changes  
=>If activated: For SP22 this is only enabled for IO-configuration changes. Later for alarms and datasources  
  
For both features: You need a valid single license "CODESYS Online Configuration Change" on the runtime system!  
CDS-95857 | Improvement | CmpPlcShellLinuxBackend: move component from RTSL to CDS | Fixed |   
CDS-95854 | Bug | Login with compile may fail if compile takes more time as sessiontimeout | Fixed |   
CDS-95851 | Improvement | CmpOpenSSLX509Cert: "Import CRL" should return ERR_DUPLICATE if this CRL (update time equal or newer) has already been imported before | Fixed |   
CDS-95848 | Bug | DeviceScan: With Profinet the submodule could not be added after scan | Fixed |   
CDS-95846 | Improvement | AP SDK: The App.config for the CODESYS.exe in the SDK should be the same as the one for the CODESYS.exe in the Setup | Fixed |   
CDS-95843 | Improvement | Extend IUnknownObject to support custom editor message | Fixed | [[GENERAL]]  
Introduce IUnknownObject2  
CDS-95838 | Bug | Japanese Localization: 'Automatically generate Project Information POUs' is missing | Fixed |   
CDS-95837 | Bug | Control Win / Windows 11: Suppress supervisor messages starting as console application | Fixed |   
CDS-95835 | Improvement | RTE: Integrate new EC1000 driver into build pipeline and setup | Fixed |   
CDS-95831 | Bug | Device Scan: Exception in Device Import Blocks UI-Commands | Fixed |   
CDS-95829 | Bug | RTE: EC1000 has incorrect version in SysEthernetDep.h and wrong platform toolset | Fixed |   
CDS-95818 | Improvement | CmpOpenSSL: Update OpenSSL to latest version 3.5.4 | Fixed |   
CDS-95817 | Bug | Compiler: Unhandled null-reference exception on generate code with optional input using STRING_TO_BYTE conversion. | Cannot Reproduce | [[GENERAL]]  
CompilerVersion >= 3.5.22.0  
CDS-95807 | Improvement | [Setup] Update InstallShield to latest version 2025 R1 | Fixed |   
CDS-95804 | Bug | Data breakpoint cannot be set in visu program | Fixed |   
CDS-95801 | Bug | Debugging: Current line not highlighted during debugging | Duplicate |   
CDS-95794 | Bug | Implement interface should copy attributes of parameters | Fixed |   
CDS-95776 | Bug | OfflineHelpClient does not support OEMCustomized folders properly | Fixed |   
CDS-95773 | Bug | DeviceRepository: project archive does not contain some files with long paths | Fixed |   
CDS-95750 | Improvement | STM32: Support SysTimeRTC | Fixed |   
CDS-95680 | Bug | DeviceObject: Compile error C0136 with dynamically created nested parameter structures with arrays | Fixed |   
CDS-95679 | Bug | SymbolConfig: OnlineChange fails due to changes in the SymbolConfig | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.22.0  
CDS-95674 | Bug | Debugging: Current position is no longer displayed correctly when debugging in libraries | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.22.0  
CDS-95659 | Bug | NullRefException in Phase 5 of CodeGeneration on x64 | Duplicate | [[GENERAL]]  
No longer reproducible with CompilerVersion >= 3.5.22.0.  
Issue has been fixed as a side effect of the rework done in CDS-94630.  
CDS-95656 | Bug | CODESYS runtime crashes when communicating with HMI's and ARTI driver (plc handler) | Cannot Reproduce | [[GENERAL]]  
Issue was already fixed by CDS-94691 in version 3.5.21.20.  
  
For more details see CODESYS Security Advisory 2025-08, which is available on the CODESYS website:  
https://www.codesys.com/fileadmin/user_upload/CODESYS_Group/Ecosystem/Up-to-Date/Security/Security-Advisories/Advisory2025-08_CDS-94690.pdf  
CDS-95655 | Bug | M4 Export: Generate Runtime System File exports functions/POUs that are not marked as External Implementation (EXT) but have the flag "enable system call" | Won't Fix | [[GENERAL]]  
Behaves as intended see CDS-86006.  
CDS-95646 | Bug | Refactoring: Variable of GVL not renamed if blanks are added (Essentials part) | Fixed |   
CDS-95644 | Bug | IPMCLI: dumpprelim does not support additional file references | Fixed |   
CDS-95641 | Bug | Setup: Cancel button not working | Fixed |   
CDS-95635 | Bug | DeviceRepository: Project archive does not contain device description if version is empty | Fixed |   
CDS-95634 | Bug | Compiler: Object reference not set to an instance of an object in a specific project | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-95621 | Improvement | CodeMeter: Extend container info with container CmActID | Fixed |   
CDS-95606 | Bug | precompile has C0062 with SysTime | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce with compilerversion 3.5.22.0  
CDS-95595 | Bug | Add-ons marked as 'optional' after creating new project | Fixed |   
CDS-95594 | Bug | CmpUserMgr: Administrator group has potentially no rights to modify security settings | Fixed |   
CDS-95593 | Bug | Save as compiled library: User object leak in specific customer library | Duplicate | [[GENERAL]]  
Duplicates CDS-94596  
CDS-95591 | Bug | Compiler: Internal error if LOWER_BOUND or UPPER_BOUND is used for arrays with calculated borders | Cannot Reproduce | [[GENERAL]]  
Compiler Version >= 3.5.22.0  
The issue is no longer present after rework of the constant folding service (see CDS-94630)  
CDS-95586 | Bug | Command, Add Device: adding additional winV3 PLC to a project does not include the needed "Standard" Library | Won't Fix | [[GENERAL]]  
The compiler only add required libraries to the library manager automatically. While the standard library might be useful, it isn't required for a new project, so it isn't added.  
CDS-95585 | Improvement | CmpWebserver: Implement option to use a tls context with an own certificate chain | Fixed | [[GENERAL]] Entire certificate chains will be sent by the webserver without an option.  
CDS-95582 | Improvement | STM32: Merge SysTimeRTC branch to trunk | Duplicate |   
CDS-95577 | Improvement | Template "CODESYS library": remove library references | Fixed |   
CDS-95573 | Bug | CDS: Codesys IDE Exception when using multi-column edit and auto-completion | Fixed |   
CDS-95570 | Bug | Handling of Library Parameters for Libraries that are resolved by Library Mapping Provider | Fixed | [[GENERAL]]  
Only relevant if an implementation of ILibraryMappingProvider is active in the current installation.  
The library parameters were stored for a wrong library resolution.   
The values shown in the editor of the LibraryManager have been stored with a fixed version.  
This caused problems when updating the library to a different version.  
Now the library parameter will be stored without a version (only library name and company are part of the key)  
  
[[KNOWN_LIMITATIONS]]  
For existing projects, the values have to be changed again, then the values will be stored correctly.   
Only after a modification of the library parameters the correct key will be used.  
CDS-95567 | Bug | Exception when clicking on plugin "AudiTools" in menu "help > about > Version Info" | Duplicate | [[GENERAL]]   
The problem was fixed in CDS-93838  
CDS-95558 | Bug | Debugging: Code line is no longer highlighted in color (yellow) | Duplicate | [[GENERAL]]  
Duplicate of CDS-95674  
CDS-95557 | Improvement | Project Open: Implement trust and open dialog | Fixed | [[GENERAL]]  
Add ITrustProjectService to optional opt in for a "trust project" dialog when opening a project.  
CDS-95545 | Bug | CmpUserObjectsDBFile: Loading the object DB, incorrectly checks and truncates the object name to USERMGR_MAX_GROUPNAME_LEN | Fixed | [[GENERAL]] Accident caused by CDS-94899 in V3.5.21.30.  
CDS-95528 | Bug | CODESYS: Application crash when delete variable and then select scope | Fixed |   
CDS-95526 | Bug | DM CmpBACnet2 is missing in source delivery | Fixed |   
CDS-95522 | Bug | Onlinechange: “Internal error (x86-64): Unsupported conversion!” is generated after removing TON declaration and implementation in project | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.22.0  
CDS-95511 | Bug | CANopen: Truncated IdPath in ARRAY parameters during device export | Fixed |   
CDS-95510 | Bug | Incomplete Display of Logic ExchangeGVL Editor/Mapping under Chinese/Korean WIN OS language | Duplicate |   
CDS-95496 | Bug | Login to a CAN application created with SP21 is no longer possible without onlinechange. | Won't Fix | [[GENERAL]]  
As the code generation was wrong with SP21 the wrong crc calculation was fixed with CDS-94861. It is not possible to detect the wrong crc. Therefore a new download or online change must be done if the project was downloaded with SP21, SP21 Patch 1 or SP21 Patch 2.  
Therefore won't fix.  
CDS-95489 | Bug | ProjectCompare: Takes too long after committing changes | Fixed |   
CDS-95484 | Bug | RTE installation shows .cfg file path not correct | Fixed |   
CDS-95483 | Improvement | [Setup] Use argument "cancelOnException" when installing packages | Fixed |   
CDS-95466 | Bug | Device: IO Addresses get modified on Open project | Cannot Reproduce | [[GENERAL]]  
Already fixed with CDS-94955   
Therefore cannot reproduce anymore.  
CDS-95448 | Bug | Compiler: Build error after Build + Generate Code | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.22.0  
  
Workaround: Do not use conversions without explicit FROM-Type (e.g. TO_BYTE/ANY_TO_BYTE) in initial variable assignments. Instead use explicit casts (e.g. STRING_TO_BYTE) or just assign a literal that is already in the correct target-type.  
  
Please note that STRING_TO_BYTE conversions do NOT trigger an ASCII-Conversion but instead tries to parse a number from the string (similar to STRING_TO_INT).  
CDS-95442 | Bug | WinCPP: Runtime crashes while removing all applications | Fixed |   
CDS-95441 | Improvement | Move CmpUnixDomainSocket from RTSL to CDS and change implementation of CmpLinuxPrivilegeProxy to this | Fixed |   
CDS-95427 | Bug | CmpOPCUAProviderIecVarAccess: Implementation blocks Write and several method calls in case of enabled redundancy | Fixed |   
CDS-95423 | Improvement | CmpLinuxRTDiag - unify PLCShell commands: throttling / napi / hyperthreading | Fixed |   
CDS-95421 | Bug | Unexpected compilation error when attempting an online change. | Cannot Reproduce | [[GENERAL]]  
The problem can no longer be reproduce in CODESYS 3.5.22.0 (even with the older compilerversion).  
CDS-95410 | Bug | CODESYSControl: Security issues in Expat versions before 2.7.3 | Fixed |   
CDS-95409 | Bug | CmpOpenSSL: Security issues in OpenSSL versions before 3.2.6 | Fixed |   
CDS-95408 | Improvement | CmItf.m4/h: Increase/make overloadable static defines for MAX_COMPONENT_NAME and MAX_API_NAME | Fixed |   
CDS-95407 | Improvement | Use extended license finder request | Fixed | [[GENERAL]]  
Extend license finder request to the format of licensefinder 1.2.0  
CDS-95406 | Bug | SVG-Renderer: Security issues in OSS versions before (libxml2 2.15.1, libcurl 8.16.0) | Fixed |   
CDS-95405 | Bug | Compiler: STCodeGenerator does not consider the __LOCALOFFSET operator | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-95403 | Improvement | Improve format of cubicle file for Contrib dependencies | Fixed |   
CDS-95401 | Bug | PLCOpenXML Export: Empty <data> elements when exporting FB with Property excluded from Build | Fixed |   
CDS-95397 | Improvement | Provide thousand separators in format string like "%'.2f" | Fixed | [[GENERAL]]  
A new format specifier ' after the % causes thousands separators to be displayed. The new specifier ' can be used in combination with f,d, i and u.  
Examples:  
%'d and UDINT UPPER_LIMIT --> 4,294,967,295  
%'.2f and REAL --> 12,345,235.00  
CDS-95395 | Bug | Linux SysCpuHandling: remove warning about executable stack | Fixed |   
CDS-95392 | Improvement | Update System.Data.SQLite at version 2.0.2 containing SourceGear.sqlite3 3.50.4.2 | Fixed | [[GENERAL]] Update System.Data.SQLite to version 2.0.2  
CDS-95391 | Improvement | Add API for setting the --noUI behaviour to not exit | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
After raising the event IEngine7.ConsoleReady the application is usually exited in the noUI mode. With the property IEngine12.ExitAfterConsoleReady you can switch off the automatic exit. See interface documentation for more details.  
CDS-95390 | Improvement | Support multi project files in file open | Fixed | [[GENERAL]]  
Add IAdditionalFileOpenDialog2 to support multi project selection  
CDS-95385 | Improvement | Add new 3slicense library version 3.5.22.0 to library resolution | Fixed |   
CDS-95371 | Improvement | Compile: Create attribute to pass callee-name, position and instance-path automatically into POUs | Fixed |   
CDS-95370 | Bug | LDFBD, Monitoring: Unhandled exception when result of SUB on ULINT is invalid (negative) | Fixed | [[GENERAL]]  
Requires LDFBD-423  
CDS-95367 | Improvement | Frame: Provide an Interface to let other plugins check the availability of SystemHandles | Fixed |   
CDS-95363 | Bug | Dialog for Login Device has a typo (Logon) | Fixed |   
CDS-95341 | Bug | Targetvisu, Overlay: No inputs raised on touchscreen without option "Multitouch Handling" | Fixed |   
CDS-95339 | Improvement | TraceMgrPacketStore: Finalize call with CAL_SysFileFlush() | Fixed |   
CDS-95330 | Bug | Performance Onlinechange: Targetsetting "report-retain-persistent-update-in-cycle" is making problems | Fixed | [[GENERAL]]  
With Compiler version >= 3.5.22.0  
the performance of online change may improve a lot and the performance of generate code may improve significantly for targets with"codegenerator\\\report-retain-persistent-update-in-cycle".  
CDS-95329 | Bug | Compare View exception if arbitrary compare is selected for different editors | Fixed |   
CDS-95328 | Bug | Project Inspection: Suppress unwanted AddOn installation prompts when opening existing projects | Fixed | [[GENERAL]]  
Add customization to remove addOn in project inspection.  
The function is called with the package guid and should return false if the package should not be listed as a required addOn.  
  
Section: InstallerIntegration  
Key: FilterAddOnGuid  
Type: Func<Guid, bool>  
CDS-95323 | Improvement | Compiler: Store UTF-8 Encoding as ApplicationFlag | Fixed |   
CDS-95321 | Improvement | Control Win / RTE: Support of Windows API functions as UTF-8 | Fixed |   
CDS-95320 | Improvement | BrowseCommands: Provide API for automated tests of command 'Goto Definition' | Fixed |   
CDS-95318 | Improvement | Improve Docu for Util.BASE64 | Fixed |   
CDS-95316 | Bug | CmpOpcUaClient: Wrong behaviour for multiple calls to OpcUaClient_GetEndpoints | Fixed |   
CDS-95311 | Bug | Visu - Webbrowser element, Linux, Target Visu: absolute file path is shown (plcLogic/Visu folder) with the index of the elements | Fixed |   
CDS-95310 | Bug | Download-Meldung einer Applikation mit "Encryption with license management" ist auf Deutsch statt auf Englisch | Won't Fix | [[GENERAL]] Won't fix because feature is not state of the art any longer and localization is not important  
CDS-95306 | Bug | AuditLog: Wrong "Add User" and "Remove User" log entry in Audit.log during new user creation | Fixed |   
CDS-95303 | Bug | Exception on CPU during Online Change in Simulation Mode | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-95296 | Improvement | Hide option editor | Fixed | [[GENERAL]]  
Add ICustomizedOptionEditorSelector in Views to select which option editor will be shown.  
CDS-95294 | Bug | OPCUAServer: Crash if several clients are connected and connection is interrupted multipe times | Fixed |   
CDS-95292 | Bug | CmpLog: MaxInfoLength not working for longer strings | Fixed |   
CDS-95288 | Improvement | Device Log UI: Usability, Make it possible to parametrize the new optimized services | Fixed |   
CDS-95285 | Bug | BACnet: BACstack Loongson segfault within send_request_to_tsm | Fixed |   
CDS-95281 | Improvement | Linux runtimes: allow for 16 CAN interfaces instead of 12 | Fixed |   
CDS-95280 | Improvement | License Manager Status Field: Load subscription licenses without await | Fixed |   
CDS-95274 | Improvement | Online: Only set visible Editors to online mode when logging in | Fixed |   
CDS-95268 | Bug | CmpOPCUAServer: Browsenames containing a : within the nodesetfile are not corret | Fixed |   
CDS-95267 | Bug | CODESYS restart needed to update retain area size | Cannot Reproduce | [[GENERAL]]  
There is a customized AddOn involved, that overwrites the settings from the device description. The memory settings do not change, so we do not expect different compile result.  
CDS-95264 | Bug | LibManObject: Removing a library implicitly added by an object fails after importing data source objects | Duplicate | [[GENERAL]]  
Duplicate of CDS-95222  
CDS-95258 | Improvement | CmpLog: Possibility to reduce transferred numbers of log entries | Fixed |   
CDS-95252 | Bug | Using DUT declaration in POU leads to crash in tabular view | Fixed |   
CDS-95250 | Bug | Frame: POU floating panels are closed after executing logout | Cannot Reproduce | [[GENERAL]]  
This Issue is no longer reproducable with the current version because of the improvement CDS-93135.  
CDS-95249 | Bug | Frame: IDE hangs after clicking disabled toolbar icon if all panes are floating | Fixed |   
CDS-95248 | Bug | Runtime logger files do not work on pathlength >31 | Fixed | [[GENERAL]]  
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
CDS-95244 | Improvement | Remove libraries required by AC from Setup | Fixed | [[GENERAL]]  
Following libraries have been removed from setup:  
\- Storage 3.5.7.0  
\- SysTypes_Itfs 3.5.2.0  
CDS-95239 | Improvement | CmpOpenSSL: Possibility that the TLS context can send a certificate chain | Fixed |   
CDS-95231 | Epic | Runtime: Online change for IO devices | Fixed |   
CDS-95230 | Bug | Device Tree: Green task icons in OEM device tree after Logout | Fixed |   
CDS-95229 | Improvement | Support for License-Metrics for KNX | Fixed |   
CDS-95222 | Bug | LibManObject: Error when removing objects referenced by RequiredLibraries | Fixed | [[GENERAL]]  
CODESYS Communication 4.7.0.0 is also required  
CDS-95220 | Bug | Compiler: Type of lazy variable cannot be inferred inside of pragma statement | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
The first use of the variable in the IF statement now determines the type. If the variable is used in ELSE with a different type, there will be compilation errors.  
CDS-95219 | Bug | LREAL compare behaves unexpected on VxWorks | Won't Fix | [[GENERAL]]  
In the reported issue here, the compiler generates exactly the same code for the VxWorks-Target as for 32-Bit ControlWin. If both targets behave differently, there is nothing we can do on the compiler side.  
Anyway: you should never compare floating point values for equality (or inequality), floating point values are not exact.   
In the reported issue, the result of an operation is once stored in variable and then the variable is compared with the operation again, like in the following simplified example:  
  
x := fun()  
IF x <> fun() THEN  
notexpected := TRUE;  
END_IF  
  
It is not guaranteed that the IF- condition resolves to FALSE on any FPU.  
The x86-FPU for example is working internally with a 80 bit precision, the variable x has a 64 bit memory word. It is never guaranteed that storing the value from the FPU Stack to a variable and reloading it will result in the same value on the Stack.  
CDS-95215 | Bug | pwszDNSSuffix is always empty on Linux | Fixed |   
CDS-95214 | Bug | CmpOPCUAClient: Certificate registration is not removed if client is deleted. | Fixed |   
CDS-95211 | Bug | exception in SysWindowSingleTaskingTask on button click | Fixed |   
CDS-95198 | Bug | vxworks SysSockPing: ulTimeout to be handled and documented | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
SysSockPing behavior was not changed, only the description. In general: value 0 for timeout leads to immediate return of function. For VxWorks: the timeout parameter is ignored (unless it is 0), as VxWorks OS cannot deal with this value, as there is no function to use this value. Instead the VxWorks kernel uses an internal configuration value for timeout (and this cannot be changed via this function SysSockPing).  
CDS-95195 | Bug | CmpOPCUAServer: setting ItemMinSamplingRate=0 causes exception on subcribe | Fixed |   
CDS-95194 | Bug | Redundancy, AutoSync: AutoSync enabled means that active/passive is no longer achieved | Cannot Reproduce | [[GENERAL]]  
The issue described here has been fixed by the already released fixed bug CDS-95515.  
CDS-95192 | Bug | Redundancy: After download active / passive state isn't possible without reboot | Cannot Reproduce | [[GENERAL]]  
The issue described here has been fixed by the already released fixed bug CDS-95515.  
CDS-95186 | Improvement | Don't use dev dependencies for xdp | Fixed | [[GENERAL]]  
SysEthernetLinux now dynamically loads libxdp.so.1 and libbpf.so.1 instead of the symbolic links libxdp.so and libbpf.so.  
CDS-95185 | Bug | List components and Go To Definition not working when declaring subrange variables | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-95184 | Bug | List components and Go To Definition not working when declaring subrange variables | Duplicate | [[GENERAL]]  
Duplicates CDS-95185  
CDS-95183 | Bug | CmpOPCUAServer: OPCUA_Provider_ServerBasics does not allow creating monitored Items with subcodes of Good status codes | Fixed |   
CDS-95182 | Bug | Redundancy, Controller: After reboot the synchronisation ends in standalone/standalone | Duplicate |   
CDS-95177 | Improvement | Support for License-Metrics for IO-Link gateways | Duplicate |   
CDS-95176 | Improvement | Support for License-Metrics for IO-Link gateways | Fixed |   
CDS-95174 | Bug | Missmatch between versions of a function | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-95173 | Improvement | Support for License-Metrics (special devices) | Fixed |   
CDS-95158 | Bug | Empty CODESYS.opt file causes an exception when starting the IDE | Fixed | [[GENERAL]]  
Do not crash if option files are empty.  
CDS-95150 | Improvement | Support creation of a parser/scanner without using the project compilerversion | Fixed | [[GENERAL]]  
New interface ILMCreatorService3 having the following methods  
\- CreateRawSTParser(string, bool, Version, ILMCompileOptions3)   
\- CreateRawSTParser(char[], bool, Version, ILMCompileOptions3)  
  
[[KNOWN_LIMITATIONS]]  
Currently only the version 3.5.22.0 is supported.  
CDS-95145 | Bug | DeviceEditor: Configurator Offline / Online Mode | Fixed |   
CDS-95083 | Bug | Compiler: Compiler error when using TRY-CATCH with __XWORD_TO_UDINT | Duplicate | [[GENERAL]]  
The issues duplicate CDS-94409  
CDS-95081 | Improvement | VxWorks: SysTaskDestroy- Increase priority of helper task | Fixed |   
CDS-95077 | Bug | [Project Metrics] Task Group Assignment doesn't detekts Task Groups | Fixed |   
CDS-95065 | Improvement | DeviceScan: implement new factory for selecting the device in the multiselect box | Fixed |   
CDS-95063 | Bug | Project Inspection: not open because of misleading check | Won't Fix | [[GENERAL]]  
The project inspection only checks add-ons, that are required for the project. Since the project does not require any add-ons the project inspection does not appear. The project inspection only opens if any version of a package does not match with the version required inthe project and the LanguageModelVersion definition of the packages does not match.  
CDS-95061 | Improvement | Move MonitoringByteCodeCreator usable for go | Fixed |   
CDS-95060 | Bug | [Refactoring] Rename a variable in a function renames also the caller | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.22.0  
CDS-95059 | Improvement | DeviceObject: Speed improvments for language model | Fixed |   
CDS-95053 | Bug | OnlineApplication: Signing boot applications does not work for all X.509 certificates | Fixed |   
CDS-95052 | Bug | CmpOPCUAStack - component init doesnt handle OpcUa_P_Crypto_Init() error properly | Fixed |   
CDS-95048 | Bug | Library Manager: Reload libraries in background does not work reliably | Fixed |   
CDS-95047 | Bug | Compile: Internal Compiler Error when initializing 2D array | Duplicate | [[GENERAL]]  
Duplicate of CDS-93226.  
CDS-95045 | Bug | Exchange GVL: Variables are not updated, if no variable is used in the source code and qualified only is set | Fixed |   
CDS-95044 | Bug | IEC watchdogs, outside the IEC program, can generate a PLC logger overflow | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
SysMemIsValidPointer for linux platforms is now using a pipe to detect invalid memory addresses. This increases performance massively, so timing might be different (for heavy usage). There are no more "SysExcept" messages for invalid pointers that are checked via SysMem.  
CDS-95039 | Improvement | BACnet: BACstack(2) fix gcc14 errors | Fixed |   
CDS-95038 | Improvement | BACnet: CmpBACnet(2) fix gcc14 errors | Fixed |   
CDS-95034 | Bug | Scan-Dialog: Copy Before issue in Scan Devices dialog | Fixed |   
CDS-95033 | Bug | ST-Editor: Possible line info inconsistencies with SVN | Fixed |   
CDS-95032 | Bug | LicenseManager: No licenses are displayed from server | Fixed |   
CDS-95031 | Improvement | Linux SysCpuHandling Thumb2/ARM: remove warning about executable stack | Fixed |   
CDS-95026 | Improvement | [License Manager] License sever option page reject urls | Fixed | [[GENERAL]]  
Add error indicator for ip addresses of license servers in the options  
CDS-95020 | Improvement | CmpMemGC: enhanced debugging feature: enable exception on double free and bounds check | Fixed |   
CDS-95015 | Bug | [LibMan] Strange lib resolution after Update SP20 -> SP21 | Cannot Reproduce | [[GENERAL]]  
The attached project does not reference CmpCodeMeter with SP21.  
CDS-95012 | Bug | TargetVisu: Security issues in Qt versions before 6.9.3 | Fixed |   
CDS-95011 | Improvement | SysEthernetLinux XDP: dont force zerocopy | Fixed | [[GENERAL]]  
New config setting available to set the bind flags for an XDP socket:  
  
/**  
* <category>Settings</category>  
* <type>String</type>  
* <description>XDP: bind flags for socket create</description>  
* Interface name must be appended to setting, e.g.:  
* Linux.xdp.bindflags.eth0=4 (4 means XDP_ZEROCOPY)</description>  
*/  
#define SYSETHERNETKEY_STRING_LINUX_XDP_BINDFLAGS "Linux.xdp.bindflags"  
#define SYSETHERNETKEY_STRING_LINUX_XDP_BINDFLAGS_DEFAULT 0  
CDS-95006 | Bug | CmpApp: Wrong session handling in multi application projects | Fixed |   
CDS-95005 | Bug | RTS: Security issues in sqlite versions before 3.50.4 | Fixed |   
CDS-94995 | Bug | Incorrect array initialization not reported in precompile | Duplicate | [[GENERAL]]  
The problem with the internal error has been fixed with CDS-93226.  
No precompile error will be reported for such an erroneous array initialization.  
CDS-94992 | Bug | False positive for precompile C0227 | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with compilerversion 3.5.22.0  
CDS-94982 | Bug | Linux sysspecific.h: atomic macros are missing memory barrier for ARM and PPC | Fixed |   
CDS-94981 | Bug | Compile Internal error with CheckBounds in a Library | Fixed | [[GENERAL]]  
Starting with compilerversion 3.5.22.0 check functions declared in libraries will also be considered within other libraries even if there is no explicit reference to the library declaring the check function.  
If both the application and a library declare the same check function the check function of the application takes precedence over the check function of the library.  
If a check function is declared in more than one library the new warning C0456 will be reported and the check function will not be used.  
If the application declares the check function no warning is reported in case of the existence of this check function in several libraries.  
CDS-94976 | Improvement | CmpApp: Log reset commands | Fixed |   
CDS-94974 | Bug | Compiler: Fix trivial bug in GetInterfaceOffset of Signature | Fixed |   
CDS-94971 | Improvement | DeliveryManager: runtime source delivery feature is missing more components | Fixed |   
CDS-94966 | Bug | CmpCodeMeter: CodeMGetContentByFirmcode3() returns unexpected errorcode | Fixed |   
CDS-94956 | Bug | Project user management: When editing a user and reusing the current password, an unhandled error occurs | Duplicate | [[GENERAL]]  
Duplicates CDS-94189  
CDS-94955 | Bug | DeviceObject: Overlapping memory areas are not avoided | Fixed |   
CDS-94953 | Epic | Linux products should run as dedicated users | Fixed |   
CDS-94949 | Bug | WhiteParseTree, ParseTreeFormatter: Var length arrays have broken syntax after formatting | Fixed |   
CDS-94941 | Improvement | Dockerize Loongson toolchain | Fixed |   
CDS-94939 | Bug | CmpVisuServer: Possible handled exception with vast amount of client registrations | Fixed | [[GENERAL]]   
A bug that could lead to an inaccessible web visualization has been fixed.   
  
For more details see CODESYS Security Advisory 2025-10, which is available on the CODESYS website:  
https://api-www.codesys.com/fileadmin/user_upload/CODESYS_Group/Ecosystem/Up-to-Date/Security/Security-Advisories/Advisory2025-10_CDS-94939.pdf  
CDS-94934 | Bug | Crash of WebServer-Task during TCP scan robustness test | Fixed | [[GENERAL]]  
For more details see CODESYS Security Advisory 2025-09, which is available on the CODESYS website:  
https://api-www.codesys.com/fileadmin/user_upload/CODESYS_Group/Ecosystem/Up-to-Date/Security/Security-Advisories/Advisory2025-09_CDS-94934.pdf  
CDS-94928 | Bug | CmpOPCUAClient: RaceCondition in varions state machines | Fixed |   
CDS-94924 | Bug | REFERENCE TO is not recognized as an error in persistent variable list | Duplicate | [[GENERAL]]   
Duplicates CDS-94923  
CDS-94923 | Bug | Persistent variables have incorrect values after library changes and online changes | Fixed |   
CDS-94919 | Bug | Compiler: FbExit is not called on onlinechange if marked with no_copy | Fixed |   
CDS-94914 | Bug | Trace from VAR_INST no longer works with SP21 compiler | Fixed |   
CDS-94913 | Bug | Compiler: No compile errors for usage of property assignment within other expressions | Fixed | [[GENERAL]]  
Starting with compiler version 3.5.22.0 the error C0032 will be reported in these cases.  
This error will be also reported for the following cases  
\- Call to action instead of assignment to property  
\- Call to function without return value instead of assignment to property  
CDS-94912 | Bug | Library Parameters: ILibManItem3.GetParameterValue does not work anymore. | Fixed | [[GENERAL]]  
Restored the SP18 behaviour of the GetParameterValues API.  
Added new interfaces to use the new behaviour  
CDS-94911 | Bug | Simulation is shut down without waiting for init | Fixed |   
CDS-94909 | Bug | Compiler: __LocalOffset does not consider index accesses. | Fixed | [[GENERAL]]  
CV >= 3.5.22.0  
CDS-94908 | Bug | Compiler: Wrong compiler error if uninitialized variable is used with __LocalOffset | Fixed | CV >= 3.5.22.0  
CDS-94898 | Bug | Scripting: create_external_file_object adds file as link instead of embedded | Fixed | [[GENERAL]]  
Modifications of a non-primary project are generally not supported and may lead to unexpected behaviour.  
Generally trying to do so for embedding file references will now lead to a warning, but OEMs may overwrite this behaviour in special cases.  
With the following OEM customization hook, a file reference of an external file object can be set to embedded, even if it isn't part of the primary project.  
Section: Engine  
Key: FileReferenceSkipPrimaryProjectCheck  
Type: Bool  
CDS-94891 | Bug | Compiler, AP: IConverterFromIEC.GetInteger not thread safe | Fixed |   
CDS-94890 | Improvement | Toolbox: Support for delayed rendering of toolbox preview images | Fixed |   
CDS-94885 | Improvement | SmartCoding: namespace and symbols from sub-libraries are shown | Fixed | [[GENERAL]]  
Compiler version >= 3.5.22.0  
New Smart Coding option 'List components of subordinate libraries' to suppress items from subordinate libraries in Intellisense.  
Option is active by default (i.e. items from subordinate libraries are displayed)  
CDS-94872 | Bug | Refactoring, Cross Reference: VAR_GENERIC CONSTANT: Refactoring and Cross Reference List do not work correctly in the extending FB | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.22.0  
CDS-94871 | Improvement | ObjectManager: Add option to fully load a project without background tasks | Fixed |   
CDS-94866 | Bug | CrossReferenceView: Sporadic hang in crossreferenceview | Fixed |   
CDS-94863 | Improvement | RESET cold/warm/origin: Deny if RUN/STOP transition is already in progress | Fixed |   
CDS-94862 | Improvement | RTS build: AppBased licenses and legacy 3s.dat licensing shall work with one runtime build | Cannot Reproduce | [[COMPATIBILITY_INFORMATION-OEM]]  
\- "3S.dat" and feature "AppBasedLicenses" must be integrated in the runtime system  
\- If at least one AppBasedLicense is available, the 3S.dat license will be disabled automatically!  
CDS-94861 | Bug | Onlinechange is possible for parameter changes but it should force a full download | Fixed | [[GENERAL]]  
Caused by CDS-87310  
Project loaded with SP21 and also SP21 Patch 1 and Patch 2 will show an online change as the wrong CRC was used for the code generation. With the fix the old CRC generation was restored but is is not possible to find out if the wrong crc code was used.  
CDS-94859 | Bug | Performance, OnlineChange: Unexpected pou are typified | Won't Fix | [[GENERAL]]  
Changes to this behavior have been deemed to risky at the current time, while the speed up where not significant.  
CDS-94858 | Bug | PrintEngine: Vulnerability caused by deserialization of untrusted option data | Fixed | [[COMPATIBILITY_INFORMATION]]  
The two option keys "PageSettings" and "PrinterSettings" are now obsolete and will be reset. Printer and page settings will be lost and have to be reconfigured.  
Please note that only these specific parts of "Project Options -> Page Setup" are affected by this. The configured Header, Footer, TitlePage and Document options will be kept.  
  
[[GENERAL]]   
For more details see CODESYS Security Advisory 2025-11, which is available on the CODESYS website:  
https://api-www.codesys.com/fileadmin/user_upload/CODESYS_Group/Ecosystem/Up-to-Date/Security/Security-Advisories/Advisory2025-11_CDS-94858.pdf  
CDS-94854 | Bug | Typo in C0415 error message | Fixed |   
CDS-94846 | Bug | Task Configuration: NullRefException on reopen editor after changing compiler version | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-94844 | Bug | Add generated_intellisense_item to list of known attributes | Fixed |   
CDS-94843 | Bug | Compiler: ILMPreCompileSmartCodingService3.WriteExprement does not consider assignments in comparison operations correctly | Fixed | [[GENERAL]]  
Compiler version >= 3.5.22.0  
CDS-94842 | Bug | Compiler: Internal error if UPPER_BOUND is used with an array defined with a VAR_GENERIC CONSTANT | Cannot Reproduce | [[GENERAL]]  
problem does no longer occur with SP 22. The problem ist not exactly a duplicate of any other issue, but was fixed in combination with some other issues.  
CDS-94841 | Bug | Compiler: __TRY/__CATCH: FB_exit of a function block is not called if a try/catch-statement is executed | Won't Fix | [[GENERAL]]  
This is a known limitation of exception handling in CODESYS and will not be changed.  
CDS-94838 | Bug | OnlineManager: Obsolete Target Settings are still listed in the documentation | Fixed |   
CDS-94834 | Bug | CmpGwClientImpl: Investigate PLCHandler deadlock in gateway v3 communication | Cannot Reproduce |   
CDS-94833 | Bug | Scripting: Creating a secondary library project and adding code to it fails | Fixed |   
CDS-94832 | Bug | CmpWebSocketClient: CAS connect from Redhat system is not possible | Fixed |   
CDS-94824 | Improvement | DeliveryManager: spdx creation should use variable as EULA location | Fixed |   
CDS-94810 | Bug | Compiler: URL in generated function global__init | Won't Fix | [[GENERAL]]  
Url is part of project source code, so it becomes included in the code. Behaves as intended.  
CDS-94765 | Bug | POUSyntaxParser: Attributes of type declarations get lost | Fixed |   
CDS-94763 | Improvement | NVL: Activating NVL leads to Exception on PLC. Enable concurrent online change again | Fixed | [[GENERAL]]  
There is currently no good way to perform online changes, while very large Netvar-Objects are part of the application. We improved the speed of the online change with this issue and prepared the code for further changes, but a real solution needs are more fundamental change in how netvars handle online changes.  
CDS-94762 | Bug | Targetvisu, Overlay: Random rotation of elements after reopen of dialog | Fixed | [[GENERAL]]  
This problem can occur in Multitouch projects containing elements with configured animations. Possible workaround is to disable the caching with configuration option:  
[SysWindow]  
MaxCachedClientObjects=0  
CDS-94760 | Bug | Signed-only application: CODESYSControl runtime generates invalid implicitly created boot application without reporting an error | Fixed |   
CDS-94755 | Bug | Compile: wrong error message for complex expression for size in __NEW-operator | Fixed | CompilerVersion >= 3.5.22.0  
CDS-94751 | Bug | Compiler: VAR_GENERIC wrong number of instances offered in online mode | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.22.0  
CDS-94749 | Bug | DeviceObject: logical device is removed after drag and drop by mistake | Fixed |   
CDS-94745 | Bug | Compiler: "Object reference not set" error message for cross reference search of interface properties | Fixed |   
CDS-94743 | Bug | Massive CPU usage after device is added | Fixed |   
CDS-94738 | Improvement | Project Inspection: Define fixed order of dialogs during project opening | Fixed | [[GENERAL]]  
New customization hook to enable this feature  
Section: ProjectInspection  
Key: ProjectInspectionSuspendDialogs  
Data type: bool  
Return Value: true  
CDS-94736 | Bug | NVL: Activating NVL leads to Exception on PLC | Fixed | [[GENERAL]]  
Disabled the concurrent online change feature for NVLs again. They can be reactived at a later time again.  
CDS-94734 | Improvement | CmpAuditLog: Use fix define for maximal string length | Fixed | [[GENERAL]]   
New maximal length of 512 bytes for audit log strengh is defined.   
It is used independent on the standard value of CmpLog:  
/**  
* Fix length for audit log messages. It shall not be overloaded to ensure that IEC   
* applications can rely on this value, too.  
*/  
#define AUDITLOG_MAX_INFO_LEN 0x200  
CDS-94721 | Bug | SysTaskLinux exception on reset cold when in Exception state | Fixed |   
CDS-94719 | Improvement | DeviceRepository: internal speed improvements | Fixed |   
CDS-94716 | Bug | DeviceObject: Online config mode does not woirk with groups in task configuration | Fixed |   
CDS-94713 | Bug | Compiler, M4 : IEC interface type defined after usage | Fixed |   
CDS-94708 | Improvement | Add --noExit parameter to the noUI mode | Fixed |   
CDS-94690 | Bug | CODESYS Control Runtime: Crash at login with CODESYS protocol clients before 3.5.16.0 | Fixed | [[GENERAL]]  
Accident caused by CDS-93240, patched with CDS-93618 to version 3.5.21.10.  
  
For more details see CODESYS Security Advisory 2025-08, which is available on the CODESYS website:  
https://www.codesys.com/fileadmin/user_upload/CODESYS_Group/Ecosystem/Up-to-Date/Security/Security-Advisories/Advisory2025-08_CDS-94690.pdf  
CDS-94688 | Improvement | Integration of the CppCheck branch | Fixed |   
CDS-94684 | Bug | Compiler: Wrong behaviour with call of external function | Won't Fix | [[GENERAL]]  
The attached project contains a user error: The parameter piLen of SettgGetStringValue is a POINTER TO DINT but in the project a POINTER TO INT is passed, this leads to memory overwrites.  
CDS-94682 | Bug | Compiler: RawST Parser should start counting lines with 1 instead of 0 | Fixed |   
CDS-94679 | Bug | Untranslated texts in Codesys during application download when create boot application is disabled | Fixed |   
CDS-94678 | Improvement | Device Repository: Filter-Options for IDeviceCatalogFilter | Fixed |   
CDS-94677 | Improvement | DeviceObject: Device Dialog Shall Show More Information | Fixed |   
CDS-94675 | Bug | Targetvisu, Linux: Browser might block Visu with D&D operations | Fixed | [[GENERAL]]  
Using a newly introduced mechanism for injecting scripts into websites loaded within the Qt Webbrowser, it is possible to circumvent these problems by disabling drag&drop entirely.  
For details see the runtime documentation of the setting "BrowserScriptExtensionFile". If activating this setting, please especially respect the hints regarding file access from that documentation.  
CDS-94674 | Bug | Compiler, M4: Wrong casing for enum types in some cases | Fixed |   
CDS-94673 | Bug | Compiler, M4: Duplicate definition for RTS_IEC-types | Fixed | [[GENERAL]]  
Types starting with RTS_IEC_ from libraries will not be seperatly exports when exporting to runtime system files, since they normally are defined in standard headers of the runtime.  
CDS-94664 | Epic | DeviceUserManagement: Remove implicit rights for admin users | Fixed |   
CDS-94658 | Epic | CmpOpenSSL: Update OpenSSL to version 3.5 (LTS) | Fixed |   
CDS-94654 | Bug | Visualization doesn't cover full screen when using Qt.LoadSysNativeCommonControlsQtFromQtTask=1 | Fixed | [[GENERAL]] The Problem seems to be Wayland related. We have added some new config switches to bypass this behavior.  
[SysGraphicWindowQt]  
Qt.Linux.ForceX11=1 # xcb has to be installed  
Qt.Linux.OverlayFullscreenBypassWindowMgr=1  
CDS-94653 | Bug | Compiler: Internal error when using property with additional VAR_IN_OUT section | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
The same error message as for inputs is reported:  
C0411: It is not allowed to define input variables in property accessors: <name>  
CDS-94645 | Bug | The group permissions granted by default are not passed on correctly to the corresponding users | Won't Fix | [[GENERAL]]  
The behaviour of the project user management rights will not be altered, as this may lead to problem for already configured projects. Instead, the documentation will be improved.  
CDS-94642 | Bug | CmpIecTask: IecTaskGetCurrent() failed under special environment | Fixed |   
CDS-94641 | Bug | Import PLCopen xml format generates Object reference not set message | Fixed |   
CDS-94625 | Bug | CmpAppBP: Signal overflow can occur on SingleCore CPU under Linux | Fixed |   
CDS-94624 | Improvement | New runtime feature: Deactivate modifications and new classes with dedicated feature | Fixed |   
CDS-94623 | Bug | Missing source position for pou statements with raw st | Fixed |   
CDS-94611 | Improvement | Linux: Make Signal SIG_EXIT configurable | Fixed |   
CDS-94605 | Bug | Unhandled exception when double clicking on a method declaration in the Cross Reference List | Fixed |   
CDS-94604 | Bug | Frame: Status bar flickers when opening ST-Editors | Fixed |   
CDS-94598 | Epic | SysTimeRtc: Support of SysTimeRtcSetTimezone2() | Fixed |   
CDS-94596 | Bug | UI Performance: Memory, GDI and User objects are leaked when logging in/out of an application | Fixed | [[KNOWN_LIMITATIONS]]  
Some possible GDI leaks in Editors and controls were identified and fixed with this issue, however there may be more in the environment of the DeviceEditors, which will be adressed with CDS-95224  
CDS-94594 | Improvement | Remove Utilities-References from LMM-Test | Fixed |   
CDS-94589 | Bug | Linux: incorrect error message in SysModuleLoad2 | Fixed |   
CDS-94586 | Bug | OPCUAClient: Short connection lost is not recognized | Cannot Reproduce | [[GENERAL]]  
Was fixed with COMM-1127  
CDS-94584 | Bug | Compiler: Change of a subrange expression is not recognized during online change | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-94500 | Bug | CmpCodeMeter: SRV_CODEMETER_READ_LICENSE_CACHE needs modify right instead of only view right | Fixed |   
CDS-94495 | Improvement | CmpIoMgr: Support online change for IO devices | Fixed |   
CDS-94488 | Bug | Compile: Internal error if a comparison is used in combination with __NEW | Fixed | [[GENERAL]]  
New compile error C0454 if an assigment expression (using the __NEW operator) is used within another expression.  
CDS-94485 | Improvement | Compiler, ConstantFolding: Support for LDATE[_AND_TIME] + Refactoring | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-94480 | Bug | IntelliSense: IntelliSense may not be shown/drawn properly | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce with CODESYS 3.5.22.0  
CDS-94473 | Improvement | Update AxProtector to 11.60a | Fixed | [[GENERAL]]  
On systems with older CPU generations, a timeout may occur when starting the CODESYS Control service. An indicator of the problem is high CPU usage when starting for more than 30 seconds and an event 7000 or 7011 logged in the windows event viewer.  
  
To work around this problem, the ServicesPipeTimeout can be increased in the registry:  
HKLM:\SYSTEM\CurrentControlSet\Control\ServicesPipeTimeout  
DWORD : 60000  
CDS-94471 | Bug | Security issues in WibuCmNet versions before 8.30a | Fixed | [[GENERAL]]  
WibuCmNet is now on version 8.30  
CDS-94470 | Bug | Security issues in CodeMeter versions before 8.30a | Fixed |   
CDS-94467 | Bug | TextDocument: Exception when displaying SVN changes | Fixed |   
CDS-94465 | Bug | Deadlock on runtime startup | Fixed |   
CDS-94460 | Improvement | Storage Abstraction: Possibility to set modification date | Fixed | [[GENERAL]]  
Extend IStorage interface to provide a API to set creation time, last write time and last access time of file sytem entries.  
CDS-94459 | Bug | Online Change: Internal error prohibiting online change | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.22.0  
CDS-94458 | Bug | Compiler: MissingCrossreferences after FastOnlineChange | Fixed |   
CDS-94456 | Improvement | Remove SysExcept from IntegrationTestGTest | Fixed |   
CDS-94445 | Bug | Compile: Wrong code with REF= with Scope operators | Fixed |   
CDS-94441 | Improvement | CmpOPCUAClient: Add a log message, if the client is out of resources | Fixed |   
CDS-94439 | Improvement | Cleanup APEnvironment and Compilerintefaces for go | Fixed |   
CDS-94431 | Bug | DeviceObject: Adding a device leads to compiler error which disappears after Clean All | Duplicate |   
CDS-94422 | Bug | TS_Runtime Linux x64: TACO_OMITTED_CYCLES fails sporadically | Cannot Reproduce | [[GENERAL]]  
Reason of the problem is the Linux scheduler configuration on some linux QS targets:  
"RT throttling" must be deactivated echo -1 > /proc/sys/kernel/sched_rt_runtime_us) to overcome large task delays during execution on a CPU core with a high load.  
CDS-94421 | Bug | Update device is adding slots, not replacing them | Fixed |   
CDS-94418 | Bug | CmpUserGroupsPAM: filter user ids when iterating over group members | Fixed |   
CDS-94414 | Bug | TargetVisu Qt: rare race condition at shutdown | Fixed |   
CDS-94410 | Bug | Access Violation at Online Change with FB with reference | Fixed |   
CDS-94409 | Bug | Overloaded conversion "TO_WORD": Internal error if used inside of a try-catch statement | Fixed |   
CDS-94407 | Bug | CmpApp.AppGenerateException: Exeption when using "__SYSTEM.ExceptionCode.RTSEXCPT_USER_EXCEPTION_BASE" on input "ulException" | Won't Fix | [[GENERAL]]  
This is an implmentation bug in the IEC application:  
A vendor specific exception must be specified with RTSEXCPT_VENDOR_EXCEPTION_BASE!  
  
If this is not specified, we do not return to the __CATCH statement!  
CDS-94406 | Improvement | Use of BIT passed into ANY | Won't Fix | [[GENERAL]]  
While bits are allowed, it is not possible to retrieve the address to a single bit. We don't see this usecase as necessary since it can be trivially worked around by using a pointer to a full byte and passing a seperate bitoffset.  
CDS-94401 | Bug | Package Manager: Finishing OEM migration fails | Fixed | [[GENERAL]]  
Reinstallation of OEM retain packages will now be installed within a single PackageManagerCLI.exe --installAll call.  
  
[[COMPATIBILITY_INFORMATION-OEM]]  
The new implementation forces exactly all retain packages delivered via OEMCustomization hook being present for installation.  
CDS-94400 | Bug | License Manager: An unhandled exception occurs during license activation | Fixed |   
CDS-94385 | Bug | CmpUserGroupsPAM: dont unregister in case of any error | Fixed |   
CDS-94380 | Improvement | DeviceCommunication, PLC Settings page: Checkboxes enabled in online mode | Cannot Reproduce | [[GENERAL]]  
Was already fixed with CDS-93949.  
Therefore not reproducible anymore.  
CDS-94378 | Bug | DeviceCommunication, PLC Settings page: Box flashing when generating code | Fixed |   
CDS-94374 | Bug | Compiler: Private method of a derived function block can be called via reference | Fixed | [[GENERAL]]  
New warning message #591 "Method <name> changes access modifier <modifier> when overriding method <name>" with compilerversion >= 3.5.22.0 if a public method is overloaded with a private method.  
CDS-94366 | Bug | IECTextEditor: SingleLineIECTextEditor: auto complete of variables should use the right namespace | Fixed |   
CDS-94360 | Bug | Codesys freeze after import xml project without softmotion package | Fixed | [[GENERAL]]   
To avoid this error, the use of IRequiredTypeGuidProvider2 is required  
CDS-94357 | Bug | OPC UA: OPCUA_Session_Delete causes an exception (page fault), if deleting of the OPCUAClientTask fails | Won't Fix | [[GENERAL]]  
There is no cure (in code using SysTaskExit) for a SysTaskExit call which did not exit the task properly. No conceivable code can solve this problem.  
The only solution is to ensure under all circumstances that the task exit properly, before SysTaskExit does return.  
See CDS-95081 which resolved this problem.  
CDS-94354 | Bug | Localization: Buttons in Help -> About -> Version Info misplaced in Japanese language | Fixed |   
CDS-94345 | Bug | CmpOpenSSL: "cert-createcsr" plcshell command does not work a second time after calling with invalid paramater | Fixed |   
CDS-94343 | Bug | SysFileCopy on VxWorks: A non existing destination folder is not created any more | Fixed |   
CDS-94340 | Bug | Command “Online Config Mode": "prohibit-duplicate-priorities" setting leads to compiler errors | Fixed | [[GENERAL]]  
In case of Online Config Mode only the hidden online config mode application is checked for duplicate priorities all other applications are ignored.  
CDS-94338 | Improvement | SysTimeRtc / VxWorks: Support of SysTimeRtcSetTimezone2() interface needed | Fixed | [[GENERAL]]  
SysTimeRTCVxWorks now provides a new interface SysTimeRtcSetTimezone2. This is enabled by default for VxWorks >= 7 but can be enabled/disabled at buildtime via preprocessor define.  
If enabled a call to SysTimeRtcSetTimezone2 sets the environment variable "TZ" with the given string and persists the string in the runtime configuration file as new setting "VxWorks.Timezone". When the runtime starts and this setting is set, the configured value will be set via SysTimeRtcSetTimezone2 automatically.  
CDS-94337 | Improvement | SysTimeRtc: Support of SysTimeRtcSetTimezone2() interface needed | Fixed | [[GENERAL]]  
Added new C and IEC interface function SysTimeRtcSetTimezone2(RTS_CSTRING* pszTimezone). With which the timezone of the PLC can be set via the POSIX environent variable TZ. See POSIX 1.2024 for details on how this variable is formatted.  
Added function to IEC library SysTimeRtc  
CDS-94336 | Improvement | CmpOPCUAServer: Extend audit log messages with detailed UA compliant parameters | Fixed |   
CDS-94335 | Improvement | OPC UA Server: Make audit logs available via OPC UA audit events | Fixed | [[GENERAL]]  
The CODESYS OPC UA Server now has the ability to transmit the audit log messages of CmpAuditLog as OPC UA AuditEvents to OPC UA clients. According to the UA specification this has to be done via an encrypted channel. Therefor the following things has to be configured to enable AuditLogs via CODESYS OPC UA Server  
  
1\. The component CmpOPCUAProviderAuditLog has to be added to the runtime configuration.  
2\. The Securits Setting [CmpOPCUAServer] SECURITY.SendAuditLogViaOpcUaServer nees to be configured to YES  
3\. Encrypted communication must be configured and used by the client which should receive audit events.  
4\. The user logged into a session needs access rights to Device.Logger.AuditLogger  
  
[[KNOWN_LIMITATIONS]]  
Auditlogs for written values and method calles are not supported right now. These will be added, as soon as the needed infrastructure has been added.  
CDS-94332 | Bug | RTS: Security issues in sqlite versions before 3.50.1 | Fixed |   
CDS-94331 | Bug | SVG-Renderer: Security issues in OSS versions before (libxml2 2.14.4, libcurl 8.14.1) | Fixed |   
CDS-94330 | Improvement | CmpUserGroupsPAM: Make pam errors visible and remove dev-dependency | Fixed |   
CDS-94327 | Improvement | Support RemoveLanguageModelofObject for libraries | Fixed | [[GENERAL]]  
New interface ILMProviderService2 with method RemoveLanguageModelOfObject(string, Guid)  
CDS-94324 | Bug | CmpUserMgrItf: Password policy description error | Fixed |   
CDS-94316 | Improvement | CmpAuditLog: Add object for access rights | Fixed | [[COMPATIBILITY_INFORMATION]]  
In the context of the new access rights for "AuditLog" the log files were renamed from ".Audit.log" to ".AuditLog.csv".  
CDS-94313 | Bug | Compiler: Missing compile errors if an abstract function block has a property with access modifier | Cannot Reproduce | [[GENERAL]]  
With compilerversion 3.5.22.0 this problem is no longer reproducible  
CDS-94302 | Bug | CmpOpenSSL: Small violations to RFC 5280 with basic constraints and serial number for self signed certificates | Fixed |   
CDS-94301 | Improvement | MBM: Incorporate TaskLock and TaskUnlock from CAATypes | Fixed |   
CDS-94299 | Improvement | Visu, Targetvisu: simple way to set up a own "loading" page or just a colored screen, that is displayed, when the targetvisu is started | Fixed | [[KNOWN_LIMITATIONS]]  
This functionality is only available for Linux runtimes using the setting "Linux.KeepMainWindowOpen=1". On such devices a file named rts_background.bmp can be stored in the PlcLogic folder of the runtime system. This image will then be displayed as background image.  
All other configurations of the Targetvisualization could e.g. use functionaliy of the window manager to display a backgroud image while there is no open Targetvisualization.  
CDS-94296 | Improvement | Project environment: dialog cannot be enlarged in height | Fixed |   
CDS-94295 | Bug | project enviroment: "set all to newest" summary does not show all applied changes | Won't Fix | [[GENERAL]]  
Issue needs to be fixed within add-on implementations.  
CDS-94293 | Improvement | SysEthernetLinux XDP: improve default behaviour for opening adapter | Fixed | [[GENERAL]]  
New PlcShell commands available to enable/disable XDP usage for specified ethernet interface:  
ethernet-xdp-set <interface> on|off  
Set state of XDP for specified interface.  
ethernet-xdp-get  
Get state of XDP for all available ethernet interfaces.  
  
[[COMPATIBILITY_INFORMATION]]  
If XDP usage is configured for an ethernet interface (by runtime cfg-setting "Linux.xdp.bpfsec"), openethernet() will no longer try to open the interface in legacy mode in case of an error.  
CDS-94292 | Bug | SysDirAsync: Restriction of diMaxDirLen/diMaxDirEntry to 80bytes is no longer needed | Fixed |   
CDS-94291 | Improvement | Usage Analysis: Remove plugins from essentials | Fixed |   
CDS-94289 | Bug | Sporadic exceptions in PutLanguageModel | Fixed |   
CDS-94272 | Epic | CODESYS: FBS Integration | Fixed |   
CDS-94271 | Bug | Compiler: Internal error in customer project | Fixed | [[GENERAL]]  
Similar to compilerversion 3.5.16.0 the error C0227 is reported again instead of the internal error.  
CDS-94267 | Improvement | About dialog: "License Info" should show generated License Info | Fixed | [[GENERAL]]  
License info button in about dialog opens now the license folder paths(%rootfolder%/Licenses, %rootfolder%/../Licenses).   
  
[[COMPATIBILITY_INFORMATION-OEM]]  
The interfaces IAdditionalLicenseAgreementSupplier and IAdditionalLicenseAgreementInformation are no longer support.  
CDS-94265 | Bug | VxWorks / C++ : Cast error in CmpAuditLog | Fixed |   
CDS-94262 | Bug | Compiler: "Internal error 2 prohibiting online change" after adding a new member to a structure in a specific project | Fixed |   
CDS-94258 | Bug | Exception when calling Engine.InvokeInPrimaryThread in noUI mode | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
The noUI mode of the CODESYS.exe was changed to fix the exception during the Engine.InvokeInPrimaryThread() call. OEMs with custom CODESYS.exe are required to update their source code.  
  
The fixed noUI mode uses the Application.Run() to run the message queue and the Engine.InvokeInPrimaryThread() is done with Dispatcher.Invoke()/BeginInvoke().  
Additionally a timer raises the Application.Idle event every 10ms. This is necessary for the execution of test scripts in the Test Manager.  
CDS-94257 | Bug | CmpOPCUAServerItf: Correct interface and security setting “Stack.MaxArrayLenth” in documentation | Fixed | [[COMPATIBILITY_INFORMATION]]  
Some settings within the CmpOPCUAStackItf.m4 have been renamed because of types. The old incorrect name is used as fallback for compatibility reasons.  
Stack.MaxArrayLenth -> Stack.MaxArrayLen  
Stack.MaxMaxMessageSize -> Stack.MaxMessageSize  
CDS-94256 | Bug | Code Review on an Assertion Error Message | Fixed |   
CDS-94251 | Bug | Compiler, warning attribute "old_input_assignments" appears and can not be resolved | Fixed |   
CDS-94249 | Bug | CAA FILE: Execute more than 3 fopen in one cycle, leads to an INVALID_HANDLE on fread | Fixed |   
CDS-94248 | Bug | TS_Runtime PPC: TACO_WD_S_XX fails | Fixed |   
CDS-94246 | Improvement | Scripting: Context object for Python calls needed | Fixed |   
CDS-94245 | Improvement | CmpIoMgr: PlcShell command needed to list all registered IO-drivers | Fixed | [[GENERAL]]  
New plcshell command "iomgr-listiodrivers" to list all registered IO-drivers  
CDS-94241 | Improvement | Device Repository: Customize Device Categories | Fixed |   
CDS-94240 | Bug | DeviceEditor: CODESYS Crashes if Modules are Updated | Fixed |   
CDS-94239 | Improvement | Runtime Password Policy: Change default of maximum values in Runtime code | Fixed |   
CDS-94238 | Bug | Compiler: Output of Function block called in Method leads to assigned variable being TRUE | Fixed |   
CDS-94237 | Improvement | SysFile: In case a placeholder is added to the black list also add the file path to it | Fixed |   
CDS-94236 | Bug | Installation of packages leads to inactive message from CODESYS with longer waiting times | Fixed |   
CDS-94228 | Bug | ProjectCompare: Compare might crash if only one SafetyDiffViewerNotImplementedFactory is present | Fixed |   
CDS-94227 | Bug | Update device: Data in IO mapping is mixed up | Fixed |   
CDS-94224 | Bug | Compile error out of implicit code with warning as error | Fixed | [[GENERAL]]  
Starting with compilerversion 3.5.22.0 suppressed warnings reported as errors will not be reported (i.e. the errors keep suppressed)  
CDS-94216 | Improvement | Gateway: Interface needed for GatewayClient methods "Initialize" and "Shutdown" | Fixed | [[GENERAL]]  
The new interface grants direct access to some internals of the the GatewayClient instance. Please note that when the ShutdownInstance() was performed, acessing the instance will throw a InvalidOperationException until InitializeInstance() was called again. Therefore it is not recommanded to try to call other GatewayClient services until this was done again.  
CDS-94201 | Improvement | Test License: The runtime should generate a log message, when a test and development license is detected | Fixed | [[GENERAL]]  
An ABL testlicense can be marked with an own license productcode = 20007.  
If such a sublicense is added to an ABL package license, we detect this as a testliecense and the runtime system add a warning as a logmessage with user notification to the standard logger.  
  
#define RTS_CODEMETER_APPBASEDLICENSES_PRODUCTCODE_TESTLICENSE 20007  
CDS-94190 | Bug | Project Open: Sporadic "Project already in use" exceptions | Fixed |   
CDS-94189 | Bug | Project settings, Users and Groups: Unhandled exception after three failed attempts to change usergroup password | Fixed |   
CDS-94188 | Bug | Compilererror C0032: Cannot convert type on same data types in Precompile phase | Cannot Reproduce | [[GENERAL]]  
Starting with compilerversion 3.5.22.0 this problem is no longer reproducible  
CDS-94176 | Bug | Compiler: Wrong value for property without monitoring attribute | Fixed | [[GENERAL]]  
The source of this error was a mismatch of the attribute 'monitoring' := 'call' between the implementation and the interface. For most cases a error was already reported with older compiler versions for this. The case in this issue now also correctly reports an error.  
CDS-94172 | Improvement | Linux SysCpuHandling X64/X86: remove warning about executable stack | Fixed | ,  
CDS-94170 | Bug | Wrong code generated for output assignment in call-by-reference | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-94168 | Improvement | Compiler: Support attribute 'external' | Fixed | Compilerversion >= 3.5.22.0  
CDS-94157 | Improvement | CmpOpenSSL: X509CertStoreImportP12 allow import of p12 container without private key | Won't Fix | [[GENERAL]]  
When a PKCS#12 container is packed without private key, OpenSSL will use all certificates als CA certs, and no certificate a client cert. Therefor it is not easiely possible to distinguish between the PKCS#12s intendend certificate and the included chain certificates.  
CDS-94153 | Improvement | Windows VS Solutions: Remove all projects from "All Components" that are already in "All Windows Products" | Fixed |   
CDS-94150 | Bug | Project Documentation: Export device IO mapping | Fixed |   
CDS-94149 | Improvement | PLCHandler: Check device name of the PLC during connect/login | Fixed |   
CDS-94125 | Improvement | Add Interface between SimulationRts and Simulation Plugin in CODESYS to retrieve the OPC UA Server endpoint URL | Fixed |   
CDS-94124 | Improvement | SimulationRts: Extend with OPC UA Server | Fixed | [[GENERAL]]  
The CODESYS Simulation now has an integrated OPC UA server. This OPC UA is restricted as readonly server without subscriptions and monitored items  
CDS-94106 | Bug | CmpOpenSSLX509Cert: Basic constraints ca flag not compliant with the specification | Fixed |   
CDS-94105 | Bug | Internal Error (Code386): Type size illegal at this position | Fixed | [[GENERAL]]  
Compilerversion >0 3.5.22.0  
CDS-94103 | Bug | Engine: Opening a non existing project ends in nullRef Exception | Fixed |   
CDS-94101 | Improvement | VisuStructPoint, VisuStructEvent and VisuTypes should be documented. | Fixed |   
CDS-94092 | Bug | NetVars, Acknowledgement: Transmitter does not recieve the acknowledge, even though it is transmitted | Cannot Reproduce |   
CDS-94091 | Bug | Installer Integration: Exception during project save if package plugin has been removed manually | Fixed |   
CDS-94090 | Improvement | Investigate if the compiler could produce compiled_libraries for old versions | Fixed |   
CDS-94088 | Improvement | Runtime Password Policy: Change default of maximum values | Fixed |   
CDS-94085 | Bug | CmpOPCUAClient: Exception in OPCUAClient task | Cannot Reproduce | [[GENERAL]]  
Affacted code path does not exist anymore. Was changed with implementation of CDS-83196  
CDS-94083 | Improvement | CmpOpenSSL: Update/Upgrade OpenSSL to version 3.5.1 (LTS) | Fixed |   
CDS-94081 | Bug | Event EVT_EthPacketArrived not always triggered under load | Fixed |   
CDS-94078 | Improvement | Util: Improve library documentation of the PID function block | Fixed |   
CDS-94076 | Bug | Compiler: Compile error for the instantiation of a function block with VAR_GENERIC CONSTANT that extends a function block with FB_init | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.22.0  
CDS-94075 | Bug | Static Analys reports false positives if CASE variable has an enum type from a library | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-94073 | Improvement | CmpOPCUAProviderIecVarAccess: Add EVTPARAMID_CmpOPCUAProviderHideIecVariable to InformationModelProvider | Fixed |   
CDS-94071 | Improvement | Implementing WIBU EWF container in our Runtimes (Preparation) | Fixed |   
CDS-94067 | Improvement | Standard.library: Improve comments for RS and SR | Fixed |   
CDS-94053 | Bug | PLCHandler: Array variable communication failure by wrong data size from PLCHandler | Fixed |   
CDS-94052 | Improvement | License Manager: Invalid containers are not recognized as broken | Fixed | [[GENERAL]]  
Check license containers for being invalid or broken.  
CDS-94042 | Improvement | Linux QS Target PPC: fix multicore settings in Runtime and devdesc | Fixed |   
CDS-94030 | Improvement | CmpOPCUAStack: Add audit logs to OpenSecureChannel and CloseSecureChannel as well as to ValidateCertificate | Fixed |   
CDS-94014 | Bug | FileBasedStorage: Application properties are marked as modified even though nothing has been changed | Fixed |   
CDS-94013 | Improvement | CAA Device Diagnosis: API for Reseting Diag-Cleared Flag | Fixed |   
CDS-94012 | Bug | Replace all sometimes changes or replaces code section incorrectly | Fixed |   
CDS-94011 | Bug | LibManEditor: The existence of a corrupted compiled-library in the library repository makes the search functionality unusable | Fixed |   
CDS-94008 | Bug | Compile: Internal error for static variable in Functionblock initialized with local constant | Fixed | [[GENERAL]]  
Fixed for Compilerversion >= 3.5.22.0  
CDS-94003 | Bug | False Positive: VAR_GENERIC is not considered when evaluating constants | Fixed |   
CDS-94000 | Bug | System.NullReferenceException in Cross Reference List: after "update the array variable in the configuration of the table" a unhandled exception is thrown | Fixed |   
CDS-93990 | Improvement | Support refactoring with Explicit Connectors | Fixed |   
CDS-93989 | Bug | Manual address change not working with Explicit Connectors | Fixed |   
CDS-93984 | Improvement | Renewed licenses cannot be distinguished from expired licenses | Won't Fix | [[GENERAL]]  
To get the expiration date, a customization of wibu gateway interface needs to be done before.  
CDS-93981 | Bug | TS_Runtime: Control_WinV3(x86): Missing Multicore licence in TACO Test | Duplicate |   
CDS-93971 | Bug | Device Log: Long loading time if a lot of messages are displayed | Cannot Reproduce | [[GENERAL]]  
Starting from SP22, the default for reading the logs is the last hour. So even if the PLC ran for several months, only the log entries will be loaded for the last hour (CDS-95288). Even, if there are more than 10000 entries in the last hour, only the first 10000 will be loaded. Therefore, there is no long delay anymore.   
  
To make it easy to find past events in the log, there are numerous UI controls for moving forward and backward in the timeline.  
  
Please note, that the new functionality is only available if both the IDE and the Runtime use SP22 or newer! The related Runtime ticket is CDS-95258.  
CDS-93967 | Improvement | CmpOPCUA*: Remove C++ and WinCE support from OPC UA Components | Fixed | [[GENERAL]]  
Compatibility code for C++ and non C99 has been removed from the following components:  
\- CmpOPCUAStack  
\- CmpOPCUAClient  
\- CmpOPCUAServer  
\- CmpOPCUAProviderIecVarAccess  
CDS-93958 | Bug | Runtime doesn't compile with openwrt-sdk-21.2.7 | Fixed |   
CDS-93953 | Bug | Update Device: after update device the datatype (declared as rangetype) is not updated | Fixed |   
CDS-93952 | Bug | Cortex Codegen: Internal error during generate code for LD/FBD | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
Now there are internal error messages to use temporary results because the expression is to complex.  
CDS-93950 | Bug | VxWorks: SP21 binariy deliveries use wrong paths in makefile | Fixed |   
CDS-93948 | Bug | SysSocketOS.c Template syntax error | Fixed |   
CDS-93946 | Improvement | Performance: Internationalisation-Tab in Options takes very long to load | Fixed |   
CDS-93945 | Improvement | Reduce flickering on ProjectClosing | Fixed |   
CDS-93939 | Bug | CmpWebServer accesses request memory after it was free'd | Fixed |   
CDS-93937 | Bug | Compile errors after updating version of source library | Fixed |   
CDS-93935 | Bug | Project Compare: Accept Single on a device value leads to wrong display value | Fixed |   
CDS-93934 | Bug | Auto Declare: Checkbox "CONSTANT" not set for existing VAR_INPUT CONSTANT | Fixed |   
CDS-93931 | Improvement | SysEthernetLinux XDP / BPF / ARP: use pin maps to have a second channel from bpf to userspace for ProfiNet | Fixed |   
CDS-93929 | Improvement | CmpOpenSSL: No consistency between security setting RSAMinKeyLen and MinAsymmetricKeySize guranteed | Duplicate | [[GENERAL]]  
Duplicates CDS-73671  
CDS-93924 | Improvement | License metrics dialog: Compiling of project can be very slow if dialog is open | Fixed |   
CDS-93922 | Bug | IDE hangs on downloading | Duplicate | [[KNOWN_LIMITATIONS]]  
[[GENERAL]]  
Duplicates CDS-93319  
CDS-93914 | Bug | AsyncServices: Sporadic communciation error, if a client (e. g. PLCHandler) closes and reopens channels very fast | Fixed |   
CDS-93913 | Bug | Device security settings, access rights: Visible even though no rights are given | Fixed |   
CDS-93912 | Bug | SysTimeRtcVxWorks.c : Bad parameter conversion for used localtime_r function | Fixed |   
CDS-93856 | Bug | VxWorks Multicore : IEC FreeFloating tasks require setting of global variable before runtime start and CFG file setting | Fixed |   
CDS-93853 | Bug | Performance problems during refactoring | Won't Fix | [[GENERAL]]  
After large changes to the project like renaming device, the project has to be reanalyzed by the compiler. This normally happens in a background-thread but some operations like refactoring need this to be completed. This is the reason for this delay of some seconds, which cannot be easily reduced.  
CDS-93851 | Bug | Device: IO Addresses get modified on Open project in SP20P31 | Fixed |   
CDS-93848 | Improvement | Import of KBUS devices is not possible | Won't Fix | [[GENERAL]]  
The device description of the plc contains a fixed module (KBUS) and this module limited to 1. Therefore the KBUS could not be deleted and also no additional module could be added.   
This is the reason why the import window shows no modules to insert.   
The customer could either export the complete plc with all subdevices or only the sub devices below the fixed module. Then the import of the files is possible.  
CDS-93845 | Improvement | Tests, IecTextEditor: Enhance test interface to test intellisense in testmanager | Fixed |   
CDS-93843 | Bug | Linux SysEventWait returns after arbitrary time | Fixed | [[GENERAL]]  
If runtime is build with toolchain glibc >= 2.30, SysEventWait uses static call of sem_clockwait  
CDS-93842 | Bug | "EXCEPTION [License invalid]" after modifying symbol configuration and download of application in logged in state | Cannot Reproduce |   
CDS-93841 | Bug | Breakpoints menu has 2 Step out but no Step over | Fixed |   
CDS-93839 | Bug | Compiler: Initial values of existing FB instance lost if FB_init is changed and a new instance is added | Fixed | [[GENERAL]]  
Changing the implementation of FB_Init now performs a standard online change instead of a fast one.  
CDS-93838 | Bug | About Dialog: Unhandled exception when displaying details of plugin of unsigned package | Fixed |   
CDS-93836 | Improvement | SysTaskLinux: improve usage of new jitter event | Fixed |   
CDS-93830 | Bug | Bus cycle task in fieldbus devices is not updated if PLC device configuration has changed. | Fixed |   
CDS-93829 | Bug | Compiler: "Go to definition" and "Find all references" does not work in combination with VAR_GENERIC CONSTANT | Cannot Reproduce | [[GENERAL]]  
Issue cannot be reproduced starting with V3.5.21.0  
CDS-93827 | Bug | Internal error: System.AggregateException shown, when specific configuration of function inputs are used | Fixed |   
CDS-93825 | Bug | IoDrvSafetySP: crash with attached project | Fixed |   
CDS-93806 | Bug | LMM: NullRef Exception in SideCarEntryHelper in case of no primary project | Fixed |   
CDS-93802 | Bug | Refactoring: Renaming an FB instance leads to rename of call (FBD, LD & CFC) | Won't Fix | [[GENERAL]]  
Investigation showed that the described problems are located within the LDFBD and CFC Addons and cannot be fixed in CODESYS itself.  
CFC-248 and LDFBD-408 will be used for individual fixes within the Addons.  
CDS-93799 | Bug | EtherCAT, Scan Dialog: SubDevices are not inserted if no entry is selected in the list of slaves found | Fixed |   
CDS-93794 | Bug | DeviceObject: Compile errors after adding Ethernet device | Fixed |   
CDS-93793 | Bug | Error in internal Code for network variables with CmpSchedule-Library | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.22.0  
CDS-93789 | Bug | Intellisense: __SYSTEM.TYPE_CLASS proposal missing | Fixed |   
CDS-93785 | Improvement | DeviceCommunicationEditor: Add a shortcut to Import/Export Gateway configurations | Fixed |   
CDS-93783 | Improvement | CAN FD support for Socket CAN minidriver | Fixed | [[GENERAL]]  
CmpSocketCanDrv now supports CAN FD (if corresponding headers are available in the toolchain).   
  
[[COMPATIBILITY_INFORMATION-OEM]]  
If scripts like rts_set_baud.sh is used, an additional argument for the databaudrate is provided. So the script must be aware of 2 baudrates (depending on if CAN fd is used or not)  
CDS-93778 | Bug | CmpOPCUAServer, CmpOPCUAStack, CmpOPCUAClient: Missing USEEXTERN_STMT in some files | Fixed |   
CDS-93768 | Improvement | Placeholder Device: Add command "Add placeholder" to menu | Won't Fix | [[GENERAL]]  
The command must be added manually as it is only for one customer.  
Therefore won't fix  
CDS-93767 | Bug | Inline Monitoring: Local variables of library functionblock are not monitored | Fixed |   
CDS-93766 | Bug | Cannot Enter Unicode Signs in the Texteditor anymore | Fixed |   
CDS-93754 | Bug | Gateway.cfg contains a non-printable NBSP character | Fixed |   
CDS-93726 | Bug | Online Change vPLC: connection loss, not possible to send application | Won't Fix | [[GENERAL]]  
The fix for keeping the online connection established needs to be done in the safety extension (SAFETY-295). Therefore, this issue here will not be fixed in essentials.  
CDS-93723 | Bug | LMM, Library Compatibility Check: False positive when installing newer version of interface library | Won't Fix | [[GENERAL]]  
The issues described here already have been fixed with CDS-91872 and CDS-65714. Since it is not possible to changed the already released Redundancy, 3.5.21.0 Library, the following steps to repeat solved the problem. Open Redudancy,3.5.22.0. Save the library as a compiled-library-v3. The created compiled-library-v3 is compatible with Redundancy, 3.5.21.0.  
The command SaveAsCompiledLibraryAndInstall must not be used for this case.  
CDS-93717 | Bug | RTE delivery fails with SP21 | Fixed |   
CDS-93713 | Bug | Issues with language model provision if project is loaded with command line switch | Fixed |   
CDS-93712 | Bug | Compiler: number of precompile error changes without explanation | Cannot Reproduce | [[GENERAL]]  
Issue canno be reproduced anymore with V3.5 SP21  
CDS-93711 | Bug | Autocomplete functionality does not always work in ST Editor | Fixed |   
CDS-93709 | Bug | CmpIecTask: Sporadic watchdog error could occur | Fixed |   
CDS-93707 | Improvement | Tools/ExtractLoggerIDs: Python script should support auditlog messages and components with subfolders | Fixed | [[GENERAL]]  
All log messages are exported from the runtime system code:  
\- Standard Log: =>$/Tools/ExtractLoggerIDs/GenericLogStrings_en.xml  
NEW: CmpRedundancy is included now in the export file  
\- NEW: Audit Log: =>$/Tools/ExtractLoggerIDs/GenericAuditLogStrings_en.xml  
CDS-93706 | Bug | Intellisense: List Components Not Working for Pointers | Fixed |   
CDS-93704 | Improvement | SysEthernetLinux: if ethtool ioctl fails with "operation not supported" make a nicer error message and log only once | Fixed |   
CDS-93703 | Bug | Mapping property of FB from ARRAY to I/O channel leads to compile error C0131 | Fixed | [[GENERAL]]  
New compiler error message will be shown if properties are mapped to an IO channel. This is not possible as ADR(property) is not allowed.  
CDS-93697 | Improvement | Linux QS Targets: move component list to _User.cfg | Fixed |   
CDS-93691 | Improvement | ARM FPU Neon support as DeliveryManager feature (and preset) | Fixed |   
CDS-93687 | Improvement | Monitoring, Provide support for automated testing (e.g. inline monitoring, watchlist in declaration part, ...) | Fixed |   
CDS-93686 | Improvement | Add new AddOn CODESYS Math Libraries to Setup | Fixed | [[GENERAL]]  
The AddOn "CODESYS Math Libraries" is included with version 4.0.0.0 in the setup.  
CDS-93685 | Improvement | CmpRetainDoubleBufferedInFile: Support of loading legacy RETAIN files and bootprojects | Fixed |   
CDS-93680 | Epic | CodeMeter CmRuntime: Usage of enhanced write filter (EWF) | Fixed |   
CDS-93679 | Bug | CreateProject does not succeed if relative path is used for stProjectLocation | Won't Fix | [[GENERAL]]  
Relative paths can not be supported as the object manager has no information to which directory the provided path is relative to.  
CDS-93671 | Improvement | OPC UA Server, Certificate: Add different DNS names to the certificate | Fixed | [[GENERAL]]  
There is a new security setting for the OPC UA Server which allows defining additional DNS names for the X.509 certificate or CSR used by the OPC UA Server.  
  
[CmpOPCUAServer]  
SECURITY.CertificateDnsNames=<comma seperated list>  
  
This can be setup either via CODESYS Security Agent or via the CODESYSControl.cfg file  
CDS-93670 | Improvement | Packagemanagercli: Improve message if minimum installer version is not reached | Fixed | [[GENERAL]]  
Clarify error message if a not sufficient package manager is used.  
CDS-93665 | Epic | PLCHandler for Loongson | Fixed | [[GENERAL]]  
PLCHandler now also supports loongson64 architecture for linux.  
CDS-93654 | Bug | PLCOpenXML, Export, Import: CDS returns inapplicable error messages | Cannot Reproduce |   
CDS-93651 | Improvement | Customization of license finder | Won't Fix | [[GENERAL]]  
The CODESYS Store button can already be hidden by returning null for the OEM Customization  
Section: LicenseManager  
Key: LicenseFinderUri  
CDS-93648 | Bug | Precompile: wrong cross references for transitions in SFC | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-93647 | Bug | LMM: Library compatibility check fails if attribute 'obsolete' is used | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
  
[[KNOWN_LIMITATIONS]]  
It is necessary for both compiled libraries, that at least compiler version 3.5.22.0 is used for creating the compiled library  
CDS-93646 | Improvement | WatchList: Provide support for automated testing | Fixed |   
CDS-93643 | Bug | sysmemxxx external operators + CMUtlMemCpy: Parameter check for NULL pointer missing | Fixed |   
CDS-93641 | Bug | Combination of targetsettings "retain-in-cycle" and "report-retain-persistent-update-in-cycle" leads to invalid retain__updated() calls | Fixed |   
CDS-93635 | Bug | RTE: Update LWIP to latest version 2.2.1 | Fixed |   
CDS-93633 | Bug | SVG-Renderer: Security issues in OSS versions before (libxml2 2.14.2, libcurl 8.13.0) | Fixed |   
CDS-93631 | Bug | CheckPrecompileSize: Invalid cast for Reference To XType | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-93629 | Bug | Report compiled POUs during incremental compile should be off by default | Fixed |   
CDS-93623 | Bug | TargetVisu: Security issues in Qt versions before 6.9.1 | Fixed |   
CDS-93614 | Bug | Build - Internal error: Sytem.AggregateException | Fixed | [[GENERAL]]  
A compile error C0231 is reported if the condition of a JMP or RET instruction is not BOOL.  
CDS-93608 | Epic | Auditlog events for certificate and password expiration and successful/failed login | Fixed |   
CDS-93564 | Improvement | CmpAuditLog: Support of SessionID and ExtraEventInfo in event parameter and log | Fixed |   
CDS-93563 | Bug | CAA Device Diagnosis: GetDeviceNameString does not return value if EtherCAT modules are added | Fixed | [[GENERAL]]  
Compiler version >= 3.5.22.0 and CAA Device diagnosis library 3.5.22.0 required.  
CDS-93560 | Bug | CODESYSControl: Security issues in Expat versions before 2.7.1 | Fixed |   
CDS-93557 | Bug | LibMan: Inserting a lib without a placeholder produces an error message | Fixed | [[GENERAL]]  
A library without placeholder will be inserted with fixed version.  
When storing a library without placeholder as compiled-library a warning will be displayed.  
CDS-93556 | Bug | LMM: Internal errors with older compilerversion | Fixed | [[GENERAL]]  
There was a break in binary compatability of interface libraries with 3.5.21.0 this breaking change was reverted with this fix.  
CDS-93554 | Bug | OnlineManager: Missing content in subtag can lead to error at download | Fixed |   
CDS-93546 | Bug | Auto Declare: IDE crashes if you want to pre-initialize an object from a compiled lib | Fixed |   
CDS-93543 | Bug | Next button active, although "Download and set up a new installation" is deactivated | Fixed | [[GENERAL]]  
Prevent next button in project inspection if no suitable installation was found and no new installation can be created.  
CDS-93542 | Bug | Update Enviroment update device different to Update Device | Fixed |   
CDS-93535 | Bug | project inspection selection dialog: frame does conceale dialog elements when resizing dialog | Fixed |   
CDS-93534 | Bug | WhiteParser: TIME() and LTIME() are not recognized as PrefixOperators | Duplicate |   
CDS-93533 | Bug | Library parameter are not correct on first modify | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.22.0  
CDS-93528 | Improvement | DeliveryManager: remove SVN module from DeliveryManager | Fixed |   
CDS-93525 | Improvement | CODESYS Control: enhance debug mechanism: SysSemEnter diag | Fixed |   
CDS-93522 | Improvement | CmpApp: Save retains immediately after AppStopApplications during shutdown process | Fixed |   
CDS-93520 | Bug | Online Download is not possible with old runtimes | Fixed |   
CDS-93517 | Improvement | CmpAppBP: Improve FlowControl+Debug logging via component specific log mask | Fixed | [[GENERAL]]  
\- Extended logfilter via logmask for CmpAppBP:  
[CmpLog]  
CmpAppBP.Filter=0xFFFFFFFF  
CmpAppBP.Mask=0x00000xxx  
  
\- Filter masks:  
/**  
* <category>LogFilter masks</category>  
* <description>Mask to filter debug outputs module or scope specific</description>  
* <element name="LFM_APPBP_MASK">Global mask for all filters</element>   
* <element name="LFM_APPBP_DEBUG_HANDLER">Enable logging in debug handler</element>   
* <element name="LFM_APPBP_PATCH_BP">Enable logging in patch/repatch breakpoints/flowpoints</element>   
* <element name="LFM_APPBP_FLOW_CONTROL">Enable logging for flowcontrol</element>   
* <element name="LFM_APPBP_SERVICES">Enable logging of online services on request (e.g. set/reset breakpoints/flowpoints)</element>   
* <element name="LFM_APPBP_SERVICES_CYCLIC">Enable logging for cyclic online services (e.g. monitoring)</element>   
* <element name="LFM_APPBP_SUSPEND_RESUME">Enable logging for suspend/resume the IEC tasks</element>   
*/  
#define LFM_APPBP_MASK 0x00000FFF  
  
#define LFM_APPBP_DEBUG_HANDLER 0x00000001  
#define LFM_APPBP_PATCH_BP 0x00000002  
#define LFM_APPBP_FLOW_CONTROL 0x00000010  
#define LFM_APPBP_SERVICES 0x00000100  
#define LFM_APPBP_SERVICES_CYCLIC 0x00000200  
#define LFM_APPBP_SUSPEND_RESUME 0x00000400  
CDS-93516 | Improvement | [TechDebt] DeviceCommunicationEditor Improve CodeBase | Fixed |   
CDS-93506 | Bug | opening template-project in sandbox exits with: Project handle -1 is invalid | Fixed |   
CDS-93494 | Bug | Project size does not decrease when deleting POUs | Fixed | [[GENERAL]]  
Add command "Compact project" to automate the workflow to compact the shared data storage within a project.  
CDS-93490 | Bug | Auto Declare Dialog: Initialized FB_Init Parameters with 0 leads to an Environment crash | Cannot Reproduce | [[GENERAL]]  
Starting with V3.5 SP21 this problem is no longer reproducible  
CDS-93489 | Improvement | Add log message in case of no memory | Fixed | [[GENERAL]]  
In case SysMemAllocData or SysMemReallocData on Linux, Windows or VxWorks are unable to allocate memory an error message will be logged.  
CDS-93486 | Improvement | CmpAuditLog: New API to also protocol sessionId and server login and logout | Fixed |   
CDS-93485 | Improvement | CmpOPCUAServer: Add AuditLog message for session services | Fixed |   
CDS-93484 | Bug | Engine: Options could no be saved with reduced user rights | Fixed | [[GENERAL]]  
If a "RepositoryRoot" is configured in "RepositoryLocations.ini" options are now saved there instead of the default %programdata%\CODESYS\ path.  
CDS-93477 | Bug | Online Change is triggered if precompilecache is not available | Fixed | [[GENERAL]]  
Fixed for compiler version >= 3.5.22.0  
CDS-93471 | Bug | Tool Pretty Printer for Structured Text, Subrange types sometimes causes error | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce with SP22 anymore.  
CDS-93469 | Bug | Remote TargetVisu: it should be possible to set the screen resolution | Cannot Reproduce | [[GENERAL]]  
This issue could not be reproduced because the settings VisuClient.BestFit and the Screen Resolution settings work as expected on a Raspberry Pi.  
CDS-93467 | Bug | Compile errors when library is in pool lib man only | Fixed |   
CDS-93465 | Bug | Compile: wrong offset for __LOCALOFFSET(a.b.c) | Fixed | [[GENERAL]]  
__LOCALOFFSET of a component-expression returns the relative offset of the right-most-expression to the left-most-expression.  
__LOCALOFFSET of a single variable just returns the offset of the variable which might be local or global.  
CDS-93463 | Bug | Automatic adressing from Array of Array with "AT %MWX" not working | Fixed |   
CDS-93461 | Improvement | Deactivate add-on update notifications for sandboxes | Fixed |   
CDS-93448 | Bug | FBD, SIL2: After loading the project, a Safe network becomes an Unsafe network | Duplicate | [[GENERAL]]  
Duplicate of CDS-90105  
CDS-93445 | Improvement | Tasks: Macros TASKPREFIX and TASKPLACEHOLDER are not exported in reference documentation | Fixed | [[GENERAL]]  
Tasks specified by TASKPREFIX() and TASKPLACEHOLDER() macros in <Component>Dep.m4 are exported now in "Tasks" overview page in RTS-OnlineHelp reference documentation:  
$/Reference/tasks.html  
  
NOTE:  
Existing <Component>Dep.m4 files must be generated newly to <Component>Dep.h files with m4-compiler!  
CDS-93444 | Improvement | Compiler: Display Lengthy-Operation for BeforeCompile | Fixed |   
CDS-93441 | Improvement | Package Manager: Improve handling of Visu content | Fixed | [[GENERAL]]  
Reference CODESYS Visualization implicitly if visualization items are used in the package manifest but no reference to CODESYS Visualization exists.  
CDS-93439 | Bug | CmpAppBP: Improve Suspend/Resume behaviour for breakpoint handling | Fixed |   
CDS-93429 | Bug | SysIntLinux doesn't compile | Fixed |   
CDS-93425 | Bug | Precompile: wrong error message for alias of type REFERENCE TO | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-93424 | Improvement | Library Repository: Hook or OEM customization needed to select libraries to be installed into local-repository | Fixed | [[GENERAL]]  
Created new interface to select dialog used to install libraries. Used instance can be selected by GLOBAL.dependencies.  
CDS-93423 | Bug | Compiler: Compileerrors disappear if warning as error is active | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-93422 | Improvement | CmpX509Cert: Enable searching the certificate store for certificates valid at a specific time | Fixed |   
CDS-93421 | Bug | ObjectDisposedException might occure for special AutoCompleteComboBox control | Fixed |   
CDS-93419 | Bug | DeviceObject: fb instance for devices diagnosis is removed if symbolc access is enabled | Fixed |   
CDS-93407 | Bug | WhiteParser: Bundled parsing errors | Fixed |   
CDS-93403 | Improvement | Online Usability: Automatic device update after scan should support more use cases | Fixed |   
CDS-93402 | Bug | Compiled, Libraries: Cannot create compiled-library-v3 with implicit enum | Cannot Reproduce |   
CDS-93401 | Bug | Precompile error has no effect to the build | Won't Fix | [[GENERAL]]  
The compiler only translates objects that are used in the application, while the precompile checks everything. This can lead to the situation that precompile errors are reported, while the build works without issues, this is as designed. Using the GVL in the project or marking it at link always, reports the same error at compile time.  
CDS-93399 | Bug | WhiteParser: Parsing errors for Cast Operator with Variable Access | Fixed |   
CDS-93396 | Bug | WhiteParser: Support keyword IMPLEMENTS for INTERFACES | Fixed |   
CDS-93395 | Bug | WhiteParser: Parsing error for strings with expression in STRING length | Fixed |   
CDS-93394 | Improvement | CmpAuditLog: New generic AuditLog Event with unique ID | Fixed | [[GENERAL]]  
\- New event is specified in CmpAuditLogItf (similar to EVTL_LogAdd event):  
/**  
* <category>Event parameter</category>  
* <element name="pApp" type="IN">Pointer to application description</element>  
*/  
typedef struct  
{  
RTS_HANDLE hAuditLog;  
RTS_CSTRING *pszUser;  
CMPID CmpId;  
RTS_I32 iClassID;  
RTS_RESULT iErrorID;  
RTS_I32 iInfoID;  
char *pszInfo;  
va_list *pargList;  
} EVTPARAM_CmpAuditLogAdd;  
#define EVTPARAMID_CmpAuditLogAdd 0x0001  
#define EVTVERSION_CmpAuditLogAdd 0x0001  
  
/**  
* <category>Events</category>  
* <description>Event is sent, after a new audit log entry was added to the logger.  
* NOTE: Is posted only, if the corresponding audit log entry has a unique iInfoID != 0!  
* </description>  
* <param name="pEventParam" type="IN">EVTPARAM_CmpAuditLogAdd</param>  
*/  
#define EVT_AuditLogAdd MAKE_EVENTID(EVTCLASS_INFO, 1)  
  
\- Event is fired in AuditLogUserAddArg() only, if iInfoID != 0  
\- Event is specified in new CmpAuditLog.library too (optional component and so it must be an optional library too!)  
CDS-93393 | Bug | WhiteParser: Parsing error for mixed brace use for sized strings | Fixed |   
CDS-93390 | Improvement | QS Target Linux/x64 for consistent Retain (double buffer in file) | Fixed |   
CDS-93389 | Improvement | OpenSSL: Avoid semaphores in atomic functions | Fixed |   
CDS-93387 | Bug | Licensed Software Metrics: Missing column headers | Fixed |   
CDS-93385 | Bug | Ladder + LAZY type: missing type errors hidden behind lazy errors | Fixed | [[GENERAL]]  
Lazy errors for implicit variables are grouped into a single error  
Related Positions information messages are not reported if more than 500 errors have been reported.  
CDS-93381 | Improvement | Task Config, interval: tooltip is not meaningful when false inputs are performed | Fixed |   
CDS-93377 | Bug | Compiler: Crash of the development system when renaming a method of an interface that extends itself | Duplicate | [[GENERAL]]  
Duplicate of CDS-93017  
CDS-93376 | Bug | WhiteParser: Parsing errors for empty intialization type | Fixed |   
CDS-93375 | Bug | WhiteParser: Parsing errors for SubrangeDeclarationStatements with initializations | Fixed | [[GENERAL]]  
The White Parser now produces IWhiteVariableDeclarationStatements instead of IWhiteSubrangeDeclarationStatements for subrange type declarations.  
CDS-93372 | Bug | PackageManagerCLI does not print all help | Fixed |   
CDS-93371 | Bug | LicensedSoftwaremetrics, Performance: An open device editor while opening a project prevents lazy loading | Fixed |   
CDS-93367 | Bug | WhiteParser: Parsing errors for variable declarations with access specifiers | Fixed |   
CDS-93351 | Bug | WhiteParser: Error for DUTs with access modifiers | Fixed |   
CDS-93348 | Bug | CODESYS crashes when device tab was open | Cannot Reproduce |   
CDS-93347 | Improvement | CmpOpenSSL :: X.509: It should be possible to change "VerifyUseCRL" in the IDE | Fixed |   
CDS-93334 | Bug | Syntax for global defines (project_defined) does not work in gvl | Won't Fix | [[GENERAL]]  
project_define cannot be used in GVLs by design, since they could affect the public interface of the GVL which must stay fixed.  
CDS-93333 | Bug | Performance Regression in Update_all | Fixed |   
CDS-93329 | Bug | Compiler: Internal Error in _IStatement by doing an online change | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.22.0  
CDS-93323 | Bug | PackageManagerCLI: Signing package with pkcs12 certificate fails | Fixed |   
CDS-93319 | Bug | ControlWin: Login takes much longer in special environments and could lead to network license blockings | Fixed | [[COMPATIBILITY_INFORMATION-EndUser]]  
The use of the CmRuntime server-search list (default is broadcast) is now deactivated. If this feature is needed, it can be activated with [CmpCodeMeter] UseCodeMeterServerSearchList=1  
  
[[KNOWN_LIMITATIONS]]  
The CmRuntime server-search list does not work with application based licenses.  
Use the setting [CmpCodeMeter] LicenseServer.[1-9]=<IP> instead.  
CDS-93311 | Epic | Support Ethernet EC1000 interfaces | Fixed | [[KNOWN_LIMITATIONS]]  
The EC1000 driver currently is working only for EtherCAT.   
Ethernet/IP is working too, but only for Point-to-Point connections. Multicast connections will fail.  
Profinet is not working.  
See CDS-97625  
CDS-93309 | Improvement | Targetvisu, Webbrowser: Support client certificates | Fixed | [[KNOWN_LIMITATIONS]] Usage of client certificates is available in all Linux based Targetvisualizations and in Windows with active Overlay functionality.  
  
Currently the activation and configuration can be done using the settings ClientCert.* in the section SysNativeCommonControlsQt.  
CDS-93306 | Bug | Code generator X86/64bit, monitoring, writing: wrong values are written | Cannot Reproduce | [[GENERAL]]  
Steps To Repeat cannot be reproduced.  
CDS-93300 | Improvement | License Metrics Dialog: create possibility to add links to help pages for a metric | Fixed | [[GENERAL]]  
New interface ILicensedSoftwareMetricProviderWithAdditionalHelp, that can be optionally implemented by the implementor of ILicensedSoftwareMetricProvider  
CDS-93299 | Improvement | Compiler: Improve codegeneration for init code of arrays with one element | Won't Fix | [[GENERAL]]  
Only minimal performance improvements can be achieved.  
An array with one element should not be used.   
Therefore the Static Analysis rule SA0010 (Arrays with only one component) exists.  
CDS-93298 | Bug | Compiler, OnlineChange: Lazy Variables are always displayed as changed in Source Code Changes | Fixed | [[GENERAL]]  
New checkbox "Show implicit objects" (inactive by default) to show/hide implicit objects in the OnlineChange dialog  
CDS-93295 | Bug | Visu, Targetvisu: Image from ImagePool in library not shown | Fixed |   
CDS-93292 | Improvement | Display Progressbar after changing BuildProperties | Fixed |   
CDS-93290 | Bug | Application Info: Garbled characters in Application Info | Fixed |   
CDS-93288 | Bug | CmpDevice.c: Fix spelling typos | Fixed |   
CDS-93285 | Bug | [TS_Runtime]: Win32 + Linux: Sporadic wrong application state after watchdog exception (TACO) | Cannot Reproduce |   
CDS-93271 | Bug | RTE: Scheduler: Possible Jitter in highest priority IEC Task in case of dynamic task creation. | Fixed |   
CDS-93266 | Bug | Task deployment: is not updated after modification in I/O mapping followed by Generate Code | Cannot Reproduce | [[GENERAL]]  
Already fixed in SP21 -> cannot reproduce!  
CDS-93265 | Bug | precompile errors are shown for constant, generic variable used in libraries | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with compilerversion 3.5.22.0  
CDS-93251 | Bug | Improve Codegeneration for trailing comments | Fixed | [[GENERAL]]  
The problem must be fixed in the codegenerators: Fixed for x86 and x64 codegeneration.  
CDS-93244 | Bug | Runtime: Improper protection of pki folder | Fixed | [[GENERAL]]  
For more details see CODESYS Security Advisory 2025-07, which is available on the CODESYS website: https://www.codesys.com/fileadmin/user_upload/CODESYS_Group/Ecosystem/Up-to-Date/Security/Security-Advisories/Advisory2025-07_CDS-93244.pdf  
  
[[COMPATIBILITY_INFORMATION]]  
The placeholder $.pki$ and its relative path, is now no longer accessible by IEC code or file transfer online services. To restore the old insecure behavior following setting needs to be added to the configuration file:  
[CmpOpenSSL]  
EnforceBlacklistOnPKIDir=0   
  
However, we strongly advise against this, because it is exposing the runtime to this vulnerability.  
CDS-93243 | Bug | Runtime: Other OS users may read private keys and password hashes because of improper file protection | Fixed | [[GENERAL]]  
For more details see CODESYS Security Advisory 2025-06, which is available on the CODESYS website:  
https://www.codesys.com/fileadmin/user_upload/CODESYS_Group/Ecosystem/Up-to-Date/Security/Security-Advisories/Advisory2025-06_CDS-93243.pdf  
  
Also the CODESYS Control V3 Runtime System Documentation now provides detailed guidance for device manufacturers how to configure operating system file permissions in a secure way. See Chapter 5 (Architecture Manual), Section 5.4 (Portings), Subsection 5.4.1 (Security Considerations), Subsection 5.4.1.1 (Operating System Folder Permissions).  
CDS-93241 | Bug | CmpOpenSSL: Security issues in OpenSSL versions before 3.2.4 | Fixed |   
CDS-93240 | Improvement | CmpDevice: In case of an authentication failure on runtime/webserver audit log message with event is fired | Fixed | [[GENERAL]] The authentication on the web server with runtime user management corresponds to the authentication on the CODESYS runtime server. By interpreting the provided audit log string, it is possible to distinguish which server was affected.  
CDS-93239 | Improvement | CmpUserMgr: New event to inform that the password has expired | Fixed | [[GENERAL]]  
A new event is fired in case a device user password is expired: EVT_UserMgrPasswordExpired.  
For more information see help pages or library documentation.  
CDS-93238 | Improvement | CmpUserMgr: New event to inform that the password will expire soon | Fixed | [[GENERAL]]  
A new event is fired once a day to inform about the validity of the device user passwords: EVT_UserMgrPasswordValidity.  
For more information see help pages or library documentation.  
CDS-93237 | Improvement | CmpUserMgr: New AuditLog Message to inform that a user was locked | Fixed |   
CDS-93232 | Improvement | Fix ObjectManagerTests | Fixed |   
CDS-93227 | Improvement | Add web browser feature to qt6 rtv qs targets | Fixed |   
CDS-93226 | Bug | Compiler: Internal error for wrong initialization of a multi-dimensional array | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-93224 | Bug | Compiler: Initialization of union members depends on order | Won't Fix | [[GENERAL]]  
For compatibility reasons we choose not to change the current behaviour.  
CDS-93223 | Bug | Misleading error messsage if migration fails due to invalid profile | Fixed | [[GENERAL]]  
Print plug-in information to console if migration fails due to unsatisfied profile  
CDS-93217 | Bug | Compiler: Change the progress text "Retrieving working set" to "Typifiying" | Fixed |   
CDS-93212 | Improvement | I/O mapping Dialog: "Description" field is not filled with variable comment | Won't Fix | [[GENERAL]]  
This is as designed. The comment column in the I/O mapping editor is a descriptive comment for the I/O channel itself. It has nothing in common with the comment of an IEC variable.  
==> Won't Fix  
CDS-93211 | Improvement | Logical(Safety) Devices: Quick access for counterpart to fast jump | Fixed |   
CDS-93199 | Bug | Compiler, M4-Export: Wrong codegeneration with Interface-Inheritance | Fixed | [[GENERAL]]  
The interface pointers are now exported to the m4 file using generated names for the exported members  
CDS-93196 | Improvement | Update Device Dialog: Redirect Pre-Selection (Usability) | Fixed |   
CDS-93195 | Improvement | Device Repository: Provide Display String for "Version" | Fixed |   
CDS-93193 | Bug | CmpOPCUAClient: Exception on VxWorks, if client fails to connect to an OPCUA server | Fixed |   
CDS-93190 | Bug | Export Mapping as CSV: Duplicate entries | Fixed |   
CDS-93184 | Bug | SysDirVxWorks.c : Update error codes for Reliance FS | Fixed |   
CDS-93183 | Bug | SysSocket AdapterInfo 2 IP addresses for one ethernet interface should be supported | Fixed |   
CDS-93181 | Bug | Access to WebVisu not possible with only encrypted communication for runtime-based user management | Fixed | [[GENERAL]] The CODESYS Webvisualization is now able to communicate also if encrypted runtime communication is enforced. Pleas remark: If you also want to encrypt the communication of the CODESYS Webvisualization, the following security setting of the webserver should be active:  
[CmpWebServer]  
SECURITY.CommunicationMode=HTTPS  
; Alternatively  
; SECURITY.CommunicationMode=REDIRECT_HTTP_TO_HTTPS  
CDS-93177 | Improvement | OnlineDevice: Transport AppSessionId in SRV_REINITAPP service with additional tag | Fixed |   
CDS-93174 | Bug | Compiler: Repeated method calls lead to very long build | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-93173 | Bug | Task deployment: is not updated after modification in I/O mapping followed by Generate Code | Cannot Reproduce | [[GENERAL]]  
Already fixed in SP21 -> cannot reproduce!  
CDS-93172 | Bug | Task deployment: is not updated after modification in I/O mapping followed by Generate Code | Cannot Reproduce | [[GENERAL]]  
Already fixed in SP21 -> cannot reproduce!  
CDS-93171 | Bug | UpdateEnvironment: Placeholder is resolved to an old version, despite All To Newest | Fixed |   
CDS-93161 | Improvement | Integrate googletest | Fixed |   
CDS-93159 | Bug | Unhandled exception on clicking on IO channel mapping value in case it is FORCED | Cannot Reproduce | [[GENERAL]]  
Already fixed with CDS-91125  
Therefore not reproducible anymore in SP21  
CDS-93157 | Improvement | CmpSocketCanDrv: eliminate dead code in case of embedded configuration -> direct pthread_* calls | Fixed |   
CDS-93155 | Improvement | SysCpuMultiCore: Provide SysMCGetCurrentCoreID for IEC code | Fixed |   
CDS-93151 | Improvement | CmpOpenSSL: New feature needed to use OS integrated openssl | Fixed |   
CDS-93146 | Bug | TS_Runtime: Linux: TACO_WD_S_10 fails on Linux_ARM | Cannot Reproduce |   
CDS-93145 | Bug | CMUtils.c: CMStringCreate3 missing NULL ptr check after SysMemAllocData | Fixed |   
CDS-93135 | Improvement | Online/Offline editors: If editors are opened while online they are closed as soon as you go offline | Fixed | [[GENERAL]]  
The behavior of editor tabs when switching between online and offline modes has been updated as follows:  
\- Editors opened online will remain open when going offline, if possible.  
\- Additional FB instances are automatically restored when going online and closed again when going offline.  
\- The docking state of editors (floating or split view) is preserved during online/offline transitions whenever possible.  
  
[[KNOWN LIMITATIONS]]  
\- Additional FB instances may still lose their docking state when going offline.  
CDS-93129 | Improvement | Compile: Increase STRING(39) of "Symbol" in __VARINFO to STRING (255) | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
The string length of the "symbol" component of __VARINFO has changed from 39 to 255 => Symbol : STRING(255);  
Incompatibility to existing code and perfomance issues are not expected.  
CDS-93123 | Bug | M4 Export: "Enable System Call" exports DEF_API, which is not needed and leads to runtime build errors | Fixed |   
CDS-93117 | Bug | Views: Opening a project with many open tabs from last session takes a very long time | Fixed | [[GENERAL]]  
Overall performance when restoring a lot of editors (more than 5) from the last session should now be improved by delaying some layouting operations until a doccontrol is visible.   
However is still takes time to open many editors as also the factories do a lot of stuff to prepare the editors.  
CDS-93115 | Bug | Sporadic internal Error at compile | Fixed | [[GENERAL]]  
Compiler version >= 3.5.22.0  
CDS-93114 | Improvement | Allow other plugins to provide the source code for step-in into compiled-libraries | Fixed | [[GENERAL]]  
New interface ISourceLibraryProvider.  
A default implementation is available, that evaluates the environment variable CDS_SOURCE_LIBRARY_FILEPATH, where the file path to a single source library file to be loaded can be specified. This default implementation can be used for automatic tests.  
User plugins can implement more complex solutions to automatically find and load source libraries.  
CDS-93113 | Bug | Pool, Input Assistent: When inserting a derived FB, the inputs and outputs of the basic FB are missing | Fixed |   
CDS-93110 | Bug | Frame: Annoying prompts for user/pwd when opening a project with password protection | Fixed | [[KNOWN_LIMITATIONS]]  
The number of login dialogs was reduced significantly. Depending on the project to be openend and the plugins installed, there might still be a very small number of additional login dialogs.  
CDS-93073 | Improvement | Improve Linux Lint | Fixed |   
CDS-93069 | Improvement | DM / VxWorks : implement exclude external for Contrib/OpenSSL in VxWorks7 buildsystem | Fixed |   
CDS-93067 | Bug | Build - Internal error: Sytem.AggregateException... | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.22.0  
CDS-93062 | Epic | Method overloading | Fixed |   
CDS-93044 | Bug | TS_Runtime TEST_CAA_Storage_Stresstest. Application start is not detected by CODESYS | Fixed |   
CDS-93042 | Bug | CODESYS close unexpected on rename device | Cannot Reproduce | [[GENERAL]]  
Fixed with CDS-91996  
CDS-93030 | Bug | LMM: Subsequent OnlineChange leads to an exception on second PLC | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.22.0  
CDS-93029 | Bug | CmpApp/CmpRetain in SRAM: Retain mismatch exception is not persistent after a reboot | Fixed |   
CDS-93019 | Bug | RTE: Memory double free | Fixed |   
CDS-93017 | Bug | Cross reference: Crash with property of FB which extends itself | Fixed |   
CDS-93015 | Bug | X64 codegenerator: Data areas with start adress are not correctly relocated | Fixed | [[KNOWN_LIMITATIONS]]  
The start addresses for areas in the device description are limited to 32 Bit also for the 64 Bit Codegenerator. Therefore only direct start addresses < 0x7fffffff are possible.  
  
This fix revealed a defect in the CODESYS Memory Tools Addon.  
Memory Tools versions 4.1.0.0 and earlier may report false positives (e.g., “Code for compiled POU changed for entry …”) on 64‑bit targets such as ControlWin64. A fix will be included in the next release of the CODESYS Memory Tools Addon.  
CDS-93006 | Bug | CmpSchedule : Incorrect processor load calculation for external triggered + freewheeling tasks | Fixed |   
CDS-93003 | Bug | Compile: Unclear message/situation with CompileInformation after opening project | Cannot Reproduce | [[GENERAL]]  
The issue is a duplicate of CDS-87684, and can no longer be reproduced with Compilerversion >= 3.5.20.0  
CDS-93000 | Bug | wrong value for pool gvls after reloading of a project | Fixed |   
CDS-92995 | Bug | Device Communication: Users and Groups: No check for valid characters | Fixed |   
CDS-92990 | Improvement | Visualize the current setup configuration in each CODESYS instance | Fixed | [[GENERAL]]  
The title of the main window now contains the profile name and, if available, the name of the additional folder used.  
CDS-92989 | Bug | RTE driver has wrong provider name | Fixed |   
CDS-92984 | Bug | Compiler: Interface reference is not set to zero if the assigned function block instance is deleted via onlinechange | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.22.0  
CDS-92974 | Bug | DeviceObject: Monitoring of IO-Data not updating for certain blocks | Duplicate |   
CDS-92973 | Bug | Spacific Project: Duplicated libraries within the project archive | Duplicate | [[GENERAL]]  
Duplicates CDS-89110  
CDS-92972 | Bug | Device Object: Monitoring of IO-Data may not work | Fixed |   
CDS-92971 | Bug | Specific Project: Duplicated objects (same name, same object) in the POUs part | Fixed | [[GENERAL]]  
The RepairProject tool repairs the wrong relationships between objects and its parent in a project. It does not fix the duplicate objects and maybe other problems caused by the bug. The bug was fixed with CDS-93013.  
CDS-92969 | Improvement | CmpOpenSSL: New API X509CertStoreBuildChain needed | Fixed | [[GENERAL]]  
There is a new trustlevel OwnChain where certificates for chain building are stored. If chain certificates are part of a PKCS#12/PFX/P12 container, they will be added to this truste level. X509CertStoreBuildChain will use this store for intermediate and root certificates for chain building.  
CDS-92968 | Bug | C0139: Inconsistent used languages after switching languages | Won't Fix | [[GENERAL]]  
This issue only occurs if the project was compiled with one language and is then edited with another one. In this case warnings in POUs that are not changed will still be reported in the old language. Since this is a very minor bug that only occurs in quite special circumstances, we decided to not fix it.  
CDS-92965 | Improvement | PLCopen Import Export: Add functionality to export and import the FB mappings | Fixed |   
CDS-92963 | Bug | IntelliSense: Auto complete with Ctrl + Space does no longer work | Duplicate |   
CDS-92960 | Improvement | PLCHandler: Deletion of internal UpdateThread tasks needs to be more robust | Fixed |   
CDS-92959 | Improvement | CODESYSControl: SysTask: Improve interface specification | Fixed |   
CDS-92950 | Bug | IECTextEditor: Missing inline monitoring and breakpoint positions when stepping into compiled library with reloaded source library | Fixed |   
CDS-92933 | Bug | Variable range is not updated for a variable of an underlying FB instance during an online change | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.22.0  
CDS-92931 | Improvement | CmpOPCUAServer: Small Code cleanups | Fixed |   
CDS-92918 | Bug | Attribute call_before_online_change_concurrent_slot is not working | Won't Fix | [[GENERAL]]  
We recommend avoiding the use of call_before_??? and call_after_??? attributes on methods. These attributes generate code for an unpredictable number of instances, which makes it challenging to assess their performance impact accurately. Given that online changes are performance-critical, it's crucial to minimize the amount of code executed during these changes. To ensure optimal performance, users should focus on keeping the executed code during online changes small, efficient, and easy to understand.  
CDS-92916 | Improvement | PLCHandler: Create pdb files for static linked plchandler | Fixed |   
CDS-92895 | Improvement | CmpWebserver: Support for allowing file transfer access by IEC application | Fixed |   
CDS-92893 | Bug | PackageManager.exe: can't copy ComponentModel, because it is used by another process | Fixed |   
CDS-92879 | Improvement | LibDevSummary: Link to Write the Docs broken | Fixed |   
CDS-92868 | Improvement | DeviceObject: Implement IObjectNameConflictChecker2 to return a conflicting object GUID | Fixed |   
CDS-92867 | Improvement | Object Manager: Extend IObjectNameConflictChecker to allow implementations to defineconflicting objects | Fixed |   
CDS-92862 | Epic | CODESYSControl: Application based licenses - support modifications and new classes | Fixed |   
CDS-92859 | Bug | CmpRedundancy: Memleak in automatic synchronization under certain conditions | Cannot Reproduce |   
CDS-92854 | Epic | Application Metrics differentiated by market or device class | Fixed |   
CDS-92851 | Bug | First and Last Slave change position during insert into project | Fixed |   
CDS-92849 | Improvement | Improve StackMarker for x86 devices | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
The marker is pushed (prerequisite: the attribute or the compiler define) after the parameter of the function. Followed by a optional alignment and the pointer to the parameter for the external function call.  
CDS-92845 | Bug | Autodeclare opens when it shoudn´t | Cannot Reproduce |   
CDS-92841 | Bug | LibMan: deleting a repository and NOT reloading the project can lead to exception | Fixed |   
CDS-92836 | Bug | IO mapping overlap when using manual address | Fixed |   
CDS-92823 | Bug | Unhandled exception appears, when opening the Library Parameters dialog in the Library Manager | Fixed |   
CDS-92821 | Improvement | PLC Log: Display of Time/Date format in regional format | Fixed |   
CDS-92819 | Bug | Precompile error for two variables with the same name in two different libraries although one variable is internal | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-92815 | Improvement | CmpIoMgr: Data Consistent call of non-IoDrv | Fixed | [[GENERAL]]  
\- New event available for CmpIoMgr to register a callback to get informed if an IoMgrStartBusCycle resp. IoDrvStartBusCycle is executed. This can be used to hook on the StartBusCycle without writing a full IO-driver.  
  
\- New event defined in CmpIoMgrItf.m4/.h:  
/**   
* <category>Event parameter</category>   
* <element name="pConnector" type="IN">Pointer to the connector on which the StartBusCycle is executed</element>   
* <element name="dwType" type="IN">Type of the bus cycle</element>   
*/   
typedef struct   
{   
IoConfigConnector *pConnector;   
RTS_UI32 dwType;   
} EVTPARAM_CmpIoMgrStartBusCycle;   
#define EVTPARAMID_CmpIoMgrStartBusCycle 0x0004   
#define EVTVERSION_CmpIoMgrStartBusCycle 0x0001   
  
/**   
* <category>Events</category>   
* <description>Event is sent at the end of StartBusCycle for each connector. BusCycle task can be specified in target configuration under "PLC Settings".</description>   
* <param name="pEventParam" type="IN">EVTPARAM_CmpIoMgrStartBusCycle</param>   
*/   
#define EVT_StartBusCycle MAKE_EVENTID(EVTCLASS_INFO, 9)  
  
\- Event is defined in CmpIoMgr_Itfs.library. So you can use the event in IEC code too.  
CDS-92808 | Bug | Generate Code: ELSIF without condition in pragma leads to Internal Error | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-92805 | Bug | error msgs are shown after the first fatal error | Fixed |   
CDS-92798 | Improvement | LicenseManager: Get license container serialnumber out of online tags | Fixed |   
CDS-92795 | Improvement | CmpCodeMeter: Transport BoxMask as additional online tag in SRV_CODEMETER_READ_CONTAINER_LIST service | Fixed |   
CDS-92791 | Bug | FindReplace: Unhandled exception in device editor | Fixed |   
CDS-92789 | Improvement | Support dividerless syntax for properties | Fixed | [[GENERAL]]  
You can now define properties in RawST according to the 4th edition of the IEC standard.  
CDS-92768 | Improvement | ControlEmbedded: Create QS Device - First steps | Fixed |   
CDS-92730 | Improvement | New compiler version for SP 22 | Fixed |   
CDS-92728 | Bug | CODESYS crashes when generating code | Fixed | [[GENERAL]]   
CompilerVersion >= 3.5.22.0  
CDS-92727 | Bug | CODESYS hangs several seconds when a PowerPoint page is in the clipboard | Won't Fix | [[GENERAL]]  
The cause of this issue was determined to be a call into the windows system to access the clipboard not returning as expected. This issue cannot be fixed within the CODESYS environment, because neither managed nor unmanaged access to the clipboard can be used to resolve the problem.  
CDS-92720 | Bug | Only code of compiled library is shown, when compiled lib would be opened with locally stored library. | Fixed |   
CDS-92719 | Bug | Breakpoints set in FB-Instances of Libraries, will not be shown correctly | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-92707 | Bug | Performance worsened form 3.5.17.2 to 3.5.20.40 | Duplicate | [[GENERAL]]  
Duplicates CDS-89850  
CDS-92699 | Bug | Crossreferences: Usages as FB_Init parameter are not found if used in array initialization | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-92697 | Bug | [3SLicense.library] Resync license before demo mode expires for feature licenses | Fixed |   
CDS-92682 | Improvement | Disable alphabetical sorting in the POU/device tree | Fixed | [[GENERAL]]  
With the following OEM customization hook, the comparer for navigators can be replaced. This can be used to control the displayed order of objects.  
Section: Navigator  
Key: ProjectModelNodeComparer  
Type: IProjectModelNodeComparer   
  
Please note that introducing a custom comparer is a complex task and will lead to negative side effects if not done correctly. To help you get started, we have created a demo implementation, which is available on request.  
CDS-92681 | Bug | CmpOPCUAServer: Empty User Credentials are not handled as Anonymous token | Cannot Reproduce | [[GENERAL]]  
Already implemented with SP21  
CDS-92078 | Bug | TextDocument: Exception when deleting a POU | Fixed |   
CDS-92071 | Bug | LibRepo/LibMan: "Object reference not set to an instance of an object." when installing a spacific, simple library | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce this issue neither with SP21 od SP20 Patch 4.  
CDS-92068 | Improvement | Security Screen: Hide project file encryption controls for project created with File-Based Storage | Fixed |   
CDS-92060 | Improvement | Linux SysCpuHandling X86: always use STACKMARKER for callstack | Won't Fix | [[GENERAL]]  
Wont fix note: No implementation change in Exceptionhandling for linux x86 (32 bit) for SP22 regarding stackmarker, as there is no backward compatible and isolated solution for SP22 (on X86 linux).  
CDS-92057 | Bug | Compiler, Precompile: _IMPLICIT_APPLICATION_INFO reports precompile error in libraries | Fixed |   
CDS-92053 | Bug | Setup: Entries in Gateway.cfg and CODESYSControl.cfg missing after modifying installation | Fixed |   
CDS-92049 | Improvement | Inverting variables in I/O mapping | Won't Fix | [[GENERAL]]  
Can be solved by using I/O channel function blocks.  
See button "Add FB for IO channel"  
CDS-92041 | Bug | Drag and Drop: If an object in the device tree is not dropped exactly on the right spot, object gets moved to POU-pool | Cannot Reproduce | [[GENERAL]]  
Was fixed with CDS-93013 and is not reproducable with current SP22  
CDS-92040 | Bug | Online change causes compile error if a new variable is added to a function block with an interface instance as additional input in FB_init | Fixed | [[GENERAL]]  
Compilerversion 3.5.22.0  
CDS-91999 | Improvement | a more Convenient access to underlying data types for BYTE, WORD, DWORD | Duplicate | [[GENERAL]]  
CODESYS already supports the partial access to bitfield types according to the IEC 61131-3 defines this feature in "6.6.1.3 Partial access to ANY_BIT variables"  
CDS-91996 | Bug | Refactoring: IDE closes/crashes when Refeactoring is executed on ethernet-device | Fixed |   
CDS-91985 | Bug | Compiler: Precompile errors in the extending FB for the use of variables defined in the base FB | Fixed |   
CDS-91982 | Improvement | Generate Code: IDE is shown as "inactive" in TaskManager, no response | Won't Fix | [[GENERAL]]  
Inactivity display depends mostly on performance of the computer and cannot be generally solved for all cases.  
CDS-91981 | Bug | Precompilecache: Precompilecache file is not deleted | Fixed |   
CDS-91980 | Improvement | Clean All: IDE is shown as "inactive" in TaskManager, no response | Duplicate | [[GENERAL]]  
Duplicates CDS-93292  
CDS-91978 | Bug | GoToDefinition: Command does not work for Pointer To Partial Variables | Fixed | [[GENERAL]]   
CompilerVersion >= 3.5.22.0  
CDS-91977 | Improvement | Device, Editor: remember the shown (online) status of the opened / unfolded SM IEC Objects when the Tab is changed | Fixed |   
CDS-91975 | Improvement | Project Inspection: optional add-ons should be available with a “select all” function | Fixed | [[GENERAL]]  
All optional Add-Ons can be (de)selected at once  
CDS-91974 | Bug | Signing application only works for implicitly created boot application | Fixed |   
CDS-91973 | Bug | Compiler: Pre-compile error when using a pre-initialized constant structure to initialize another constant | Fixed |   
CDS-91968 | Improvement | F1 : Context-sensitive help should display the related location in the LibMan | Duplicate |   
CDS-91965 | Bug | CODESYS loads slow if messages window is in attached and a project containing Git is used | Fixed |   
CDS-91958 | Bug | Persistent Variables: Mapped persistent variable is not retained | Cannot Reproduce | [[GENERAL]]  
The described problem can't be reproduced on a simulation target or another target. There seems to be a special handling of Memory areas %M on the specific target.  
CDS-91947 | Improvement | RTE Configuration: Button that opens the Explorer with the folder of the stored logger data | Fixed |   
CDS-91946 | Bug | PackageManager.exe: Admin rights are still needed to complete a deferred installation | Fixed |   
CDS-91936 | Improvement | License Manager usability for the selected device | Fixed | [[GENERAL]]  
Devices included the project can be selected via a combobox in the license manager dialog  
CDS-91926 | Improvement | AuditLog: Log synchronously with LT_DUMP_ALWAYS in all log backends to avoid log entry gaps | Fixed |   
CDS-91897 | Bug | Persistent variables, C0415, not enough free memory, no download possible: Monitoring fails | Fixed | [[GENERAL]]  
Even if there are compile errors, login should be possible and monitoring should be possible. Thus, it should be possible to save the content of an existing persistent variable list to a recipe even if the controller is out of memory for the new list.  
CDS-91891 | Bug | Compiler: Unnecessary compiler warning (C0447) if a persistent variable is initialized with a constant variable | Won't Fix | [[GENERAL]]  
The warning is correct in this case, since structured variables are never replaced.  
CDS-91886 | Bug | Project Compare: External file object loses embedded content when merged | Fixed |   
CDS-91884 | Bug | GACs are not correctly installed | Fixed | [[GENERAL]]  
Install .NET Framework assemblies in LAC if they are newer than the assembly provided by the framework  
CDS-91875 | Bug | LibMan: Representation of Signed Libraries with Visualization | Fixed |   
CDS-91873 | Bug | M4 Export : Referenced IEC constructs from external libraries not included in export | Fixed |   
CDS-91872 | Bug | Compiler: Online Change when compiled library is installed instead of source library | Fixed | [[GENERAL]]  
If a compiled_library is stored with compiler version 3.5.22.0 it can be installed instead of a source library, and a login of a project using the library should be possible without online change.  
CDS-91864 | Improvement | Online: Add logging functionality for exceptions | Fixed | [[GENERAL]]  
The log files that are created as part of this issue contain debug information that is provided as such without further documentation or support. They may prove useful if, for example, support explicitly asks for this information to create a bug report. Please only send these files if explicitly requested by support staff.  
  
Option-SUB_KEY = "{6F610974-74C6-4BEE-A636-1BED605DE8E5}"  
Option-Names:  
"LoggingActive"  
"NumberOfFiles"  
"NumberOfLogsPerFile"  
"AnyCategory"  
"SelectedCategories"  
"FolderPath"  
"FilePrefix"  
CDS-91830 | Bug | Linux QS Target: qs_raspberry: remove obsolete settings for CmpRaspi | Fixed |   
CDS-91826 | Improvement | [Technical Debt] TaskConfigEditor: Replace SandBar stuff by standard means | Fixed |   
CDS-91821 | Improvement | [Project Usermanagment] Dialog for information to change "Owner" password | Won't Fix | [[GENERAL]]  
There is no need to implement anything because the Automation Platform already has all of the functionality for customers to implement their own solution. An extensive example is attached to this issue.  
CDS-91818 | Bug | Library Manager: Download Link for library CAA CanOpen Stack is wrong | Fixed |   
CDS-91816 | Improvement | Native Import: Add conflict resolution | Fixed | [[GENERAL]]  
For the native import, it's now possible to select a conflict resolution for objects with a name conflict.  
CDS-91802 | Bug | Properties changing exclude from Build takes too much time | Fixed |   
CDS-91780 | Bug | ImagePool: Loading embedded images is slow | Fixed | [[Known Limitations]]  
This fix addresses one of two possible causes for the behaviour. The other will be addressed with VSPRT-234.  
CDS-91752 | Improvement | Manage Gateways: Option to editing the Idendifier and Description settings | Duplicate |   
CDS-91751 | Bug | Intellisense: Auto-Completion: Ctrl+Space doesn't work if the auto declaration icon (smart tag) appears | Fixed |   
CDS-91744 | Bug | FlowControl: output of conversion not shown anymore in certain cases | Fixed |   
CDS-91727 | Bug | LibMan: Library Parameters of sub-libraries are not saved and loaded when redirected by customization hook | Fixed | [[KNOWN_LIMITATIONS]]  
The library parameters were stored for a wrong library resolution. The values shown in the libman-Editor were not the same as the values used in the compiler. Now the editor shows the values used in the compiler. For existing projects, the values have to be changed again, then the values will be stored correctly. Only after a modification of the library parameters the correct key will be used.  
CDS-91715 | Improvement | Add Option for Connection Timeout Gateway <-> PLC | Cannot Reproduce | [[GENERAL]]  
Session timeout was already introduced in version 3.5.18.0 by CDS-31565 for the CODESYS Control runtime system.  
CDS-91698 | Bug | Extended POU (Safety): Variables that are exchanged with logical devices are not updating in standard application | Cannot Reproduce | [[GENERAL]]  
Ist not reproducible anymore.  
CDS-91692 | Bug | Visu: Investigate placeholder redirection when visu is added later | Fixed |   
CDS-91686 | Bug | Flow Control: Code is sporadically shown as not being reached, even though it is passed | Duplicate |   
CDS-91685 | Bug | Flow Control: Code is sporadically shown as not being reached, even though it is passed | Fixed |   
CDS-91676 | Bug | Inline Monitoring: 64-bit Pointers overflow in display in simulation mode. | Fixed |   
CDS-91674 | Improvement | CmpRedundancy: Redundancy State changed event | Fixed |   
CDS-91641 | Bug | Compiler, LanguageModel: SignatureInserted event is missing for pool signature | Fixed |   
CDS-91566 | Bug | Precompile error if a subordinate library is installed in the Lib Repository while project is opened | Fixed |   
CDS-91563 | Improvement | Parse BuildProperty pragmas for dividerless go! format | Cannot Reproduce |   
CDS-91555 | Epic | Logger with implicit context information | Fixed |   
CDS-91543 | Bug | [Any-Array with FB_Init implementation]: Array not initializing properly (No UPPER_BOUND and LOWER_BOUND, no values) | Fixed |   
CDS-91527 | Improvement | VxWorks CmpMemGC: Use SysMemAllocData() instead of calloc() or malloc() | Fixed |   
CDS-91511 | Bug | Project name containing “%25” leads to corrupt project | Fixed |   
CDS-91510 | Improvement | Linux CmpMemGC: Use SysMemAllocData() instead of calloc() or malloc() | Fixed |   
CDS-91483 | Bug | CmpRedundancy: Standalone/Standalone after reboot of active linux machine | Fixed |   
CDS-91432 | Bug | Adding application object as redo step clears redo stack | Fixed | [[GENERAL]]  
Add the "Library Manager" object of an application object within the application object factory.  
CDS-91429 | Improvement | LibDevSummary: Little corrections on help page | Fixed |   
CDS-91408 | Bug | Intellisense: The variable types listed in the declaration section are not consistent. | Fixed |   
CDS-91403 | Bug | LibManObject: Library with invalid characters in company or title produces wrong cache if cache is rebuilt | Fixed |   
CDS-91399 | Improvement | Visu, Toolbox: Command to open visualization toolbox | Cannot Reproduce |   
CDS-91337 | Bug | Compiler: Warning C0441 appears in declaration editor for initialized VAR_IN_OUT variables | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-91305 | Bug | CmpCodeMeter: Activated logfilter must not block startup of the runtime system | Fixed | [[GENERAL]]  
CmpCodeMeter now has an extra log mask when filter is opened:  
  
0x01 generates the list of licenses found (now asynchronously).  
0x02 fetches extra license info like name, company etc.  
To do none of the above, the mask has to be set to 0 explicitly.  
  
Example:  
  
[CmpLog]  
CmpCodeMeter.Filter=0xFFFFFFFF  
CmpCodeMeter.Mask=0x03 ; generates list of licenses with extra license info  
CDS-91301 | Bug | CmpCodeMeter: networklicense do not work reliable if the codemeter service will be stopped and restarted | Duplicate | [[GENERAL]]  
Duplicates CDS-91554  
CDS-91267 | Bug | Compiler: Precompile false positives with customer project | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-91260 | Bug | Compiler: Warning C0041 missing in "Compiler warnings" list in the Project Settings | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
Warning C0389 is reported instead of warning C0041.  
CDS-91239 | Bug | CODESYSControl Runtime: Enrypted Communication: No login possible after 10x ResetOriginDevice | Fixed |   
CDS-91216 | Improvement | CmpBlkDrvShm use case communication with embedded devices | Fixed | [[GENERAL]]  
To configure pyhsical addresses for the shared memories used to communicate with a PLC on another CPU core, the following settings need to be set.   
The example shows the values for the default sizes and default shared memory base names. Addresses need to be adapted to the real ones, sizes may be adapted (increased) to match complete memory pages.  
  
[CmpBlkDrvShm]   
BCSHMBlkDrvShm__0.PhysicalAddress=0xA2345678  
BCSHMBlkDrvShm__0.Size=2640  
SHMBlkDrvShm_0_0.PhysicalAddress=0xB2345678  
SHMBlkDrvShm_0_0.Size=2596  
SHMBlkDrvShm_1_0.PhysicalAddress=0xC2345678  
SHMBlkDrvShm_1_0.Size=2596  
  
Alternativly on Linux based systems it is also possible to write a kernel driver and some user space code which maps the addresses to /dev/shm/BCSHMBlkDrvShm__0 etc. to run the CmpBlkDrvShm without the configuration above.  
CDS-91087 | Bug | Intellisense: Library Namespaces are missing in IntelliSense. | Won't Fix | [[GENERAL]]  
Won't fix because user error  
* IoDrvEtherNetIP, IoDrvGPIO, IoStandard and SM3_Transformation are "System libraries" and will be only considered in Intellisense if the smart coding option "Show symbols from system libraries in input assistant" ist set (Library IoDrvEthernet has the flag "ShowSmartCodingInfo" and therefore this library will be always considered in Intellisense)  
* The namespace of library SM3_Robotics_Visu will be not offered because this library does not contain any POUs, that the end user case use (only visualizations and textlists providing only implicit language model)  
* Namespace "SMBC" will be not offered, because it does not exist (Namespace "SMCB" will be offered if the smart coding option "Show symbols from system libraries in input assistant" ist set)  
* Namespace "SM3_Math" will be offered, because library SM3_Basic uses this library and has the flag "Publish all IEC symbols to that project as if this reference would have been included there directly" set  
CDS-91086 | Bug | Autodeclare will not work with "_System." Types | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-91077 | Bug | Compiler: wrong alignment in m4 file for derived iec types with 64-bit runtime | Fixed | [[GENERAL]]  
No members of the base functionblock/structure are exported in a derived functionblock/structure.  
A member __BASE representing the base functionblock/structure will be exported instead.  
No fill bytes for padding are exported any more.  
CDS-91076 | Improvement | PLCHandler: New interface needed to check an offline boot application against loaded application on the PLC | Fixed | [[GENERAL]]  
There is a new PLCHandler API method:  
virtual long CheckHostApplicationFileConsistency(/*[In]*/ const char* pcszHostApplicationFile, /*[Out]*/ long* plComparisonResult, /*[Out]*/ ApplicationInfo2** ppAppInfo2);  
  
Note: Additional, withCheckApplicationFileConsistency() can be checked, if the PLC has matchng boot applications.  
CDS-90940 | Improvement | Remove/Replace Redistributable Packages | Fixed | [[GENERAL]]  
Microsoft Visual C++ 2013 Redistributable Package is no longer installed.  
Microsoft Visual C++ 2015-2019 Redistributable Packages (x86/x64) are replaced by Microsoft Visual C++ 2015-2022 Redistributable Packages (x86/x64).  
CDS-90914 | Improvement | Update IDE: all configured gateways should be adopted during an update | Fixed |   
CDS-90897 | Bug | [ESM]: login to standard runtime not possible when a project is created via test script | Cannot Reproduce |   
CDS-90825 | Bug | Gateway SysTray: Config mode cannot be activated | Fixed |   
CDS-90745 | Bug | Usage Analysis: Not registered properly in Installer, making it impossible to uninstall addon | Won't Fix | [[GENERAL]]  
The existing usage analysis is implemted as essentials plugins from the beginning and is not handled as an add-on. In the future, this feature will be replaced by a new implementation, which is part of the existing add-on.  
CDS-90706 | Bug | Intellisense, AutoDeclare: AD is called/required although Intellisense has listed and found the method before | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-90629 | Improvement | PLC Shell: Always displayed command-line at the bottom of the available editor border | Fixed |   
CDS-90623 | Bug | Log take a long time to load / Usabilty Logger | Duplicate | [[GENERAL]]  
Starting from SP22, the default for reading the logs is the last hour. So even if the PLC ran for several months, only the log entries will be loaded for the last hour (CDS-95288). Even, if there are more than 10000 entries in the last hour, only the first 10000 will be loaded. Therefore, there is no long delay anymore.   
  
To make it easy to find past events in the log, there are numerous UI controls for moving forward and backward in the timeline.  
  
Please note, that the new functionality is only available if both the IDE and the Runtime use SP22 or newer!  
  
This issue requires runtime changes from CDS-95258 and duplicates CDS-93971.  
CDS-90602 | Epic | TargetVisu: Provide QML VideoPlayer Element for SL runtimes | Fixed | [[KNOWN_LIMITATIONS]]   
* Mirroring the video is so far only possible using the overlay Targetvisualization. For further details see the issue CDS-96073  
* Usage of the Mediayplayer in Windows based Targetvisualizations requires using the overlay functionality.  
CDS-90585 | Improvement | CmpX509Cert: New event to inform about the validity period of certificates per CODESYSControl RTS use case | Fixed |   
CDS-90533 | Epic | Redundancy: File synchronization interface | Fixed |   
CDS-90497 | Improvement | Diff view for textual objects: add results view (ex. 3-way-merger ST) missed in Action, Method, Property, Transition | Fixed |   
CDS-90316 | Bug | RTE: CmpIecTask: IecTaskExceptionHandler crashes in seldom cases at shutdown | Cannot Reproduce | [[GENERAL]]  
Could not be reproduced.  
  
Additionally per code review we cannot see any unprotected code during shtdown.  
The suspicion is, that the holding time of the UPS is too short, if a handled exception occurred during shutdown and so the RETAIN file was not stored.  
  
There are two possible solutions to solve the potential problem of a too short UPS holding time:  
  
1\. A solution was implemented already with CDS-93522. Here we store the RETAIN data in files earlier in the shutdown phase of the runtime system. This could help in some situations, where the holding time of the UPS is too short.  
  
2\. The following EPIC can solve the problem in the future (for the RTE too), if something goes wrong during shutdown, the RETAINs are stored during runtime on data change:  
CDS-90565  
CDS-90211 | Improvement | Cross Reference: slow cross-reference search | Fixed | [[GENERAL]]  
The results of the crossreference searchs are limited to 1000 elements  
CDS-89930 | Improvement | Logic Exchange GVL: Possibility to set the attribute 'linkalways' | Duplicate | [[GENERAL]]  
Already fixed with CDS-95045  
CDS-89839 | Bug | Help: OfflineHelp does not support jumping into libraries when pressing F1 | Fixed |   
CDS-89800 | Bug | CmpRetain: Error in the management of retain segments | Fixed |   
CDS-89692 | Bug | Installshield: Security issues in zlib versions before 1.3.1 | Fixed | [[GENERAL]]  
CODESYS has been upgraded to use Installshield 2024 R2. According to revenera, this version uses zlib 1.3.1 (see https://community.revenera.com/s/question/0D7PL000009H6Jx0AK/detail ).  
CDS-89529 | Improvement | Add Option for Connection Timeout Gateway <-> PLC | Won't Fix | [[GENERAL]]  
This Issue was already implemented in SP20 with CDS-85801  
CDS-89457 | Bug | CmpApp / encrypted bootpoject: Improve log entries if certificate has expired and bootproject is denied | Fixed |   
CDS-89379 | Improvement | Browse Commands: add new command “Go to definition of <Type>” while a variable instance is selected | Fixed | [[GENERAL]]  
New command "Go to Definition of Type", that is available on variables of userdefined types (also array of userdefined type, pointer to userdefined type, reference to userdefined type)  
CDS-89100 | Improvement | LicensedSoftwareMetric: Possibility to open a detail view | Fixed | [[GENERAL]]  
new interface _3S.CoDeSys.LicenseManagement.ILicensedSoftwareMetricWithDetailInformation  
CDS-89074 | Improvement | CmpIecTask.c: Logfilter should be enabled for VxWorks, QNX and RTE | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
\- Existing compiler switch IECTASK_DEBUG_RUNSTOP is renamed now to RTS_IECTASK_LOG_RUNSTOP  
\- RTS_IECTASK_LOG_RUNSTOP is now an official compiler switch  
\- IECTASK_DEBUG_RUNSTOP is mapped to new define RTS_IECTASK_LOG_RUNSTOP  
\- RTS_IECTASK_LOG_RUNSTOP is activated now for alle full runtimes:  
\-- Win  
\-- RTE  
\-- Linux  
\-- VxWorks  
\-- QNX  
CDS-88872 | Bug | Endless loop if open project with password protection but password is not available | Fixed |   
CDS-88566 | Improvement | [Technical Debt] Compiler: Fix critial issues in SP22 compiler | Fixed |   
CDS-88547 | Improvement | AuditLog / UserActions: Log of further security related online services / operations | Fixed |   
CDS-87693 | Improvement | EtherCAT support for Embedded: adapt base configuration for Win Embedded | Fixed |   
CDS-87643 | Improvement | STM32: SysTimeRtc Implementation | Duplicate |   
CDS-87388 | Epic | Fieldbus: Online change for IO devices | Fixed |   
CDS-86995 | Bug | NVL Sender throws warning C0564 | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP21 anymore  
CDS-86919 | Bug | Select online state: Function block instance names are not visible if names start with a unicode character | Fixed |   
CDS-86884 | Bug | Device Communication Settings: Adding a DNS entry to the gateway does not work | Fixed |   
CDS-86702 | Bug | CmpOpenSSL: X509CertStoreRegister allows only a single registration of one component | Fixed |   
CDS-86577 | Bug | Installation process is stuck on install package in special circumstances | Fixed |   
CDS-86499 | Bug | [Setup] Package installation cannot be canceled | Duplicate | [[GENERAL]]  
Duplicates CDS-95641.  
CDS-86302 | Bug | Compiler: Logical operators (AND, OR, XOR) with mixed types (BOOL, BYTE...) are not possible in every composition | Cannot Reproduce | [[GENERAL]]  
The issue cannot be reproduced anymore with V3.5 SP21  
CDS-86301 | Bug | Compiler: Boundaries of DATE literals is not checked | Cannot Reproduce | [[GENERAL]]  
The issue cannot be reproduced anymore with V3.5 SP21  
CDS-86110 | Bug | CodeMeter GAC: Error message "The file name or the extension is too long" | Fixed |   
CDS-85915 | Bug | Visu, ARM: Exception with webbrowser on Targetvisu | Cannot Reproduce | [[GENERAL]]  
In a newer version of Ubuntu (arm64) for Raspberry Pi this problem could not be reproduced. The described issue did not appear with Ubuntu 25 (64bit) and Codesys Runtime 3.5.21.0.  
There was a issue with Ubuntu 22 (32bit) and a previous versions of CODESYS Control  
CDS-85877 | Improvement | Var Generic Constant: Assignment via name | Fixed | [[GENERAL]]  
It is now possible to explicitly name the generic variable in the declaration of a generic type. The assignment to the generic variable needs to be in Parenthesis  
inst<(const:= value)>  
It is not possible to mix assignments to generic constants with simple constant values:  
inst<(const:= value), 5> // leads to error message  
The order of parameter assignments in the declaration is arbitrary.  
CDS-85821 | Epic | CAN FD | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
Following macros were deleted:  
CL2I_GetBlockDataPointer, CL2I_GetBlockTSP, CL2I_GetBlockNet, CL2I_SetBlockTSP, CL2I_SetBlockNet, CL2I_GetBlockSync, CL2I_SetBlockSync.  
Use the corresponding structure members of CL2I_BLOCK and CL2_FD_BLOCK instead.  
  
[[GENERAL]]  
To enable general CAN FD support set following define in CAADefines.h:  
#ifndef CL2_CAN_FD  
#define CL2_CAN_FD 1 /* enable CAN FD support */  
#endif  
Furthermore, a CANMinidriver has to implement CMD_CMDRV_FD additionally to CMD_CMDRV and register via CMD_Register2.  
CDS-85700 | Improvement | Generics: Specify values using 'named arguments' | Duplicate | [[GENERAL]]  
Duplicates CDS-85877  
CDS-85696 | Improvement | CmpCodeMeter: Startup timeout CM_WAIT_FOR_CODEMETER_RUNTIME_TIMEOUT_MS must be a setting | Duplicate | [[GENERAL]]  
Duplicate of CDS-82917  
CDS-85682 | Improvement | Debugging: Step-Into in a compiled library when the source library does not exist | Fixed |   
CDS-85527 | Bug | CmpOpenSSL: SIGSEGV:Segmentation fault in SSL_CTX_free() | Fixed |   
CDS-85427 | Bug | Compiler, Propertyinfo: System call not generated with hierarchical interfaces | Fixed |   
CDS-85210 | Improvement | FOSS: Changes in document format needed | Duplicate | [[GENERAL]]  
This issue duplicates CDS-89099  
CDS-84905 | Bug | RTE: PLC configuration dialog shows wrong applications if applications are removed | Fixed |   
CDS-84582 | Bug | CmpRetain/CmpApp: RTE: Setting Retain "On Powerfail" needs a UPS but no info is shown | Fixed |   
CDS-83767 | Bug | Installer icon in customize menu too large | Fixed |   
CDS-83589 | Improvement | LibDevSummary: Recommendation and information on library development under SP17/SP18 | Fixed |   
CDS-83431 | Bug | RTE: SysEthernet receives wrong packet after close and open | Fixed |   
CDS-83303 | Bug | Library is kept in projects collection if installation fails | Cannot Reproduce | [[GENERAL]]  
Issue cannot be reproduced anymore with V3.5 SP21  
CDS-83243 | Bug | CmpOPCUAClient: Session is not closed, if the certificate validation fails | Fixed |   
CDS-83222 | Bug | Project import, gives an unintelligible message when a necessary addon is missing | Won't Fix | [[GENERAL]]  
The described problem is already fixed with newer versions (>=SP19) where the missing Addon is reported and  
proposed for installation by project inspection as expected. Therefore there is nothing more to do here.  
CDS-83196 | Epic | OPC UA: Support certificate chains in client and server | Fixed | [[GENERAL]]  
The OPC UA Server and OPC UA Client now support proper splitting and validation of certificat chains. Either sent by the peer, or if intermediate certificates have been added by hand to the corresponding folders.  
  
Additionally, the server and client have security setting which allows both parts to send the certificate with a valid chain during OPC UA handshake and session services.  
  
See the following new security settings. Both settings default to YES.  
  
[CmpOPCUAServer]  
SECURITY.SendCertificateChains=<YES|NO>  
  
[CmpOPCUAClient]  
SECURITY.SendCertificateChains=<YES|NO>  
CDS-83120 | Bug | signature for some CAN-Drivers is missing | Fixed |   
CDS-82917 | Improvement | CmpCodeMeter: Configurable CM_WAIT_FOR_CODEMETER_RUNTIME_TIMEOUT_MS as setting | Fixed | [[GENERAL]]  
\- New setting to specify the timeout to wait for CmRuntime ready:  
/**  
* <category>Settings</category>  
* <type>Int</type>  
* <description>Setting for the timeout in [ms] to wait for CmRuntime ready!  
* </description>  
*/  
#define CODEMKEY_INT_TIMEOUT_WAITFOR_CMRUNTIME "TimeoutWaitForCmRuntime"  
#ifndef CODEMVALUE_INT_TIMEOUT_WAITFOR_CMRUNTIME_DEFAULT  
#define CODEMVALUE_INT_TIMEOUT_WAITFOR_CMRUNTIME_DEFAULT 60000  
#endif  
  
\- Default timeout was increased from 15s to 60s! This is no problem, because we only wait, until CmRuntime reacted correctly!  
CDS-82386 | Bug | Device User Management: Password of a new user cannot be changed | Fixed |   
CDS-82211 | Bug | CmpUserMgr: the hash buffer used for CMUtil is not aligned which leads to alignment exceptions | Fixed |   
CDS-81940 | Improvement | CODESYS Control Linux: Determine IEC Callstack of SIGABRT | Duplicate | [[GENERAL]]  
In general: Duplicate of CDS-91716.  
Particularly: Exception in FB_EXIT still does not show sourceposition: will be solved with CDS-95479.  
CDS-81883 | Bug | CmpUserMgr: Add access rights to call UserMgrUserGetProperty for the own user | Fixed |   
CDS-81645 | Bug | CmpOpenSSL / X509: Infinite loop leading to Security Agent Freeze in case of specific certificates | Fixed |   
CDS-81525 | Improvement | Create possibility to add additional navigators to the mechanism implemented by the TaskConfigEditor plugin. | Duplicate | [[GENERAL]]  
Duplicates CDS-95230. After this issue is fixed all navigators are always updated so no new interfaces is needed anymore.  
CDS-81353 | Bug | VxWorks: X86: Async Services (CmpSrv) may lead to crash in case of reconfigure / reset cold / download | Cannot Reproduce |   
CDS-80909 | Improvement | SysMsgQ: Improve performance | Fixed |   
CDS-79613 | Bug | Task Config: Wrong export of Bus cycle task after deletion of task | Fixed |   
CDS-79337 | Bug | Trace Packet Configuration, UpdatesAfterTrigger: it is not possible to use a PostTrigger > 255 with the Traceconfig file. | Fixed |   
CDS-79310 | Improvement | CmpX509Cert: New event to inform about expired certificates of CODESYSControl RTS use cases | Fixed |   
CDS-78848 | Improvement | CmpPlcShell: Integrate improvements from SL extension api | Fixed |   
CDS-78476 | Improvement | RTE, lwIP: Increase limit on multicast group registration | Fixed |   
CDS-78183 | Improvement | Compiler: Codesys should support "overloading" methods/functions | Duplicate | [[GENERAL]]  
Duplicates CDS-93062  
CDS-78166 | Bug | Linux SysEthernet: no result check when setting promiscuous mode via ioctl | Fixed |   
CDS-77496 | Bug | "Online Config Mode" fails with device setting "max_number_of_apps" equals 1. | Cannot Reproduce | [[GENERAL]]  
Already fixed with CDS-90224  
CDS-77031 | Improvement | CmpStd.h: Add support for new data type RTS_IEC_LDATE, RTS_IEC_LDATE_AND_TIME/RTS_IEC_LDT and RTS_IEC_LTIME_OF_DAY/RTS_IEC_LTOD | Fixed |   
CDS-76790 | Improvement | EdgeGateway: Activate PLCHandler logger | Fixed | [[COMPATIBILITY_INFORMATION-EndUser]]  
\- All PLCHandler log outputs in EdgeGateway are moved now to gateway logfile (typically gateway.csv)  
\- PLCHandler log filter can be configured in future in CODESYS Automation Server  
CDS-76274 | Bug | Compiler: Compiler errors occurred in a project because a comment accidentally put a "}" in place of a "]". | Cannot Reproduce | [[GENERAL]]  
Issue cannot be reproduced with V3.5 SP22  
CDS-75505 | Bug | Compiler: Warning C0140 cannot be deactivated via pragma | Cannot Reproduce | [[GENERAL]]  
Issue cannot be reproduced anymore with V3.5 SP22.  
CDS-75475 | Improvement | Device Repository: Import ZIP-Files Directly | Fixed |   
CDS-75300 | Bug | CmpRetain: Define of CMPPLCSHELL_NOTIMPLEMENTED is not used for calling RetainAddSRAMPlcShellCommands() | Fixed |   
CDS-75095 | Improvement | POU for implicit checks: include the __POUNAME() and __POSITION() where the check was performed | Fixed |   
CDS-73710 | Improvement | LibMan: show qualified-access-only lib attribute being set in properties dialog | Fixed | [[GENERAL]]  
There are two ways to set qualified access: in the dialog box of the library manager item and in an attribute of the library itself. If the library already defines qualified access that takes precedence over the setting in the dialog box, a note ("Qualified access is already defined by a library project itself") to this effect is now displayed next to the setting in the dialog box. The setting in the dialog of the library manager item is not changed if the library setting itself changes.  
CDS-73672 | Improvement | SecurityScreen: MinAsymmetricKeySize from RTS should be used in Addon Security Agent | Fixed | [[GENERAL]]  
\- When creating new certificates from the SecurityScreen, the configured SecuritySetting "RSAMinKeyLen" of the PLC will be now queried to prevent creating invalid certificates for the PLC.  
\- requires the Addon "CODESYS Security Agent" in Version >= 1.4.0.0  
CDS-73671 | Improvement | CmpOpenSSL: MinAsymmetricKeySize from RTS should be used in Addon Security Manager | Fixed | [[GENERAL]]  
1\. Setting X509CERTVALUE_INT_MIN_ASYMMETRIC_KEY_SIZE was deleted from CmplX509CertIft.h  
  
2\. New define was added:  
/**  
* <category>Static defines</category>  
* <description>This define is used for the default key len of certificates (CSRs and self-signed), if nothing else is specified </description>  
*/  
#ifndef X509CERT_STANDARD_KEY_LEN  
#define X509CERT_STANDARD_KEY_LEN 2048  
#endif   
  
3\. When ever a key len is needed, but not provided by the caller (e. g. omitted PLCShell parameter or 0 as function paramter) use the following value:  
MAX( X509CERT_STANDARD_KEY_LEN, "Value of SECURITY.RSAMinKeyLen")   
  
4\. The following PLC Shell commands are extended by keylength of csr:  
\-- "cert-genselfsigned": "cert-genselfsigned [<number retrieved by \"cert-getapplist\">] [expdays=<days>] [keylen=<length in bits>]"  
\-- "cert-createcsr": "cert-createcsr [<number retrieved by \"cert-getapplist\">] [encoding=Base64 | ASN.1] [keylen=<length in bits>]"  
CDS-73001 | Improvement | Create a bootstrap exe enabling the Visual Studio GUI designer to use our Controls GAC | Won't Fix | [[GENERAL]]  
Concept does not work because it causes plugin installations to fail  
CDS-72128 | Bug | CmpUserObjectDBFile: Rights database file is written at shutdown even if no UserManagement is configured | Fixed |   
CDS-71301 | Bug | Compile: __LOCALOFFSET Operator does not consider Bit offsets | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.22.0  
CDS-71231 | Improvement | CmpOpenSSL: Protect .pki folder | Duplicate | [[GENERAL]]  
Duplicate of CDS-93244.  
CDS-71229 | Improvement | FileTransfer/SysDir: Deny directory access via blacklist | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
The blacklist functionality of SysFile now works for directories too, i.e. a check is now added to directory services of filetransfer and directory functions from IEC.  
CDS-70569 | Improvement | CmpUserObjectDBFile: Improve file format | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
The access rights data base of the CODESYS Control runtime system is now stored in the file ObjectDatabase.csv with an optimized format.   
For compatibility, at startup of the CODESYSControl RTS, the old date base is converted:  
If there is no "ObjectDatabase.csv" file (the new CSV object database) but there is a "UserMgmtRightsDB.csv" file (the pre-V3.5.22.0 XML object database), then the RTS will convert the "UserMgmtRightsDB.csv" file to the "ObjectDatabase.csv" file. The "UserMgmtRightsDB.csv" file will not be deleted by the RTS, until a ResetOriginDevice is executed.  
CDS-68775 | Improvement | CmpLog / SysOut: Use colored console output for different log classes | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
\- New interface functions in SysOutItf to set/reset console window text colors:  
RTS_RESULT CDECL SysOutPrintfSetColor(const int textcolor, const int backgroundcolor);  
RTS_RESULT CDECL SysOutPrintfSetColorReset(void);  
  
\- OS implementations:  
o Win: Implemementation is done for CODESYS Control Win  
o Linux: https://jira-intern.codesys.com/browse/CDS-94212  
o For all other OS-SysOut implementations we provide functional stubs  
  
NOTES:  
\- You have to enable the feature with the following compiler switch for SysOut to activate both interface functions above:  
#define SYSOUTPRINTFSETCOLOR_ENABLED  
\- You can test all text colors by defining SYSOUT_TEST_TEXTCOLORS and start runtime  
CDS-68497 | Improvement | Device Editor, IEC Objects: Unicode characters should be support | Cannot Reproduce | [[GENERAL]]  
Already implemented with CDS-84810.  
CDS-68471 | Improvement | Linux CmpCharDevice: add setting to restrict access for paths | Fixed | [[GENERAL]]  
Paths that should be accessible by CmpCharDevice now have to be added to the configuration file to ensure only explicetly allowed paths can be accessed.  
  
[CmpCharDevice]  
PermittedPath.0=/dev/gpiochip4  
PermittedPath.1=/dev/i2c-*  
CDS-67554 | Bug | CAA Device Diagnosis - Library is missing key "LanguageModelAttribute = qualified-access-only" | Won't Fix | [[GENERAL]]  
Too many compile errors in different situations. Will not be done yet!  
CDS-65964 | Improvement | SmartCoding: The window should open on the monitor where the IDE is running | Duplicate | [[GENERAL]]  
Duplicates CDS-86506  
CDS-65827 | Bug | MessageView: Column without a title | Fixed |   
CDS-65588 | Epic | Toolbox: Possibility to customize POUs for IEC languages | Fixed | [[GENERAL]]  
A new toolbox was made available that is able to store and deliver custom elements for ST Language.   
The user may create, reorder or delete items in the toolbox to configure it individually and has different options where to store the toolbox configuration or where to load it from.  
The toolbox offers a search filter to let the user find specific items more easily as well as the possibility to define shortcuts for doing a quick insertion of specific items.  
  
Initially the new toolbox only supports snippets implemented in Structured Text, but also offers the infrastructure to be able to implement snippets in other implementation languages within their individual Addons later.  
CDS-64730 | Bug | Package Manager: Error during installation if plugin references a Microsoft binary that is not part of the Framework | Cannot Reproduce | [[GENERAL]]  
Can not be reprduced any more.  
CDS-60548 | Bug | SIL2: Add comments to undocumented LINT statements | Won't Fix | [[GENERAL]]  
Fix is not longer needed since with SIL2 SP21 MISRA C standard was introduced and LINT is not longer relevant for the assessment.  
CDS-59388 | Improvement | The compiler should check if an name of an method is double | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce starting with compiler version SP22, the compile error C0583 will be generated for this case.  
CDS-57761 | Improvement | Usability: Indication that lazy load has not finished yet | Fixed |   
CDS-57479 | Epic | X.509: Support of Certificate Signing Request (CSR) and Certificate Revocation Lists (CRL) | Fixed |   
CDS-57290 | Improvement | LibMan: The window "Details" should be available for all levels of libraries | Fixed |   
CDS-56099 | Improvement | CmpAppBP: SetNextStatement: adapt RTE adaptation to new AppDebugHandler2 interface | Cannot Reproduce |   
CDS-53652 | Bug | POU Editors: Incorrect I/O address format in online mode. | Fixed |   
CDS-51702 | Improvement | Implement Interfaces: Implement interfaces command creates methods already defined in base classes | Fixed |   
CDS-46048 | Improvement | Visu, Webvisu: Use websockets to reduce amount of transferred data | Fixed | [[GENERAL]]  
Websocket functionality is provided by CODESYS Control starting with 3.5.22.0. Websockets are used for communication of the CODESYS Webvisualization with versions of CODESYS Visualization >= 4.10.0.0.  
CDS-45547 | Improvement | LMM: Create a compile error when two subsignatures have the same name. | Cannot Reproduce | [[GENERAL]]  
This issue cannot be reproduced with SP22, a compile error C0582 is reported for the declaration and C0136 if the duplicated method is used.  
CDS-41891 | Improvement | Compile: Caller Input attribute | Duplicate | [[GENERAL]]  
Duplicate CDS-95371  
CDS-39506 | Improvement | RTE: RTL8169 add new PCIe ID to driver inf file | Fixed |   
CDS-39435 | Bug | LMM: Warnings created for initial values in variable declarations are output twice | Cannot Reproduce |   
  
 

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
