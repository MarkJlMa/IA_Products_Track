[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Product: CODESYS V3.5 SP19

Key  |  Issue Type  |  Summary  |  Resolution  |  Release Note   
---|---|---|---|---  
CDS-84842 | Improvement | [Setup] Update CODESYS Code Generator TriCore to 4.0.1.0 | Fixed |   
CDS-84841 | Improvement | [Setup] Update CODESYS EtherNetIP to 4.4.1.0 | Fixed |   
CDS-84820 | Bug | CmpDevice: Possible DOS vulnerability | Fixed | [[GENERAL]]  
For more details see Advisory 2023-03, which is available on the CODESYS website:  
https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17555&token=212fc7e39bdd260cab6d6ca84333d42f50bcb3da&download=  
CDS-84723 | Improvement | Wrong copyright year in CODESYS About dialog | Fixed |   
CDS-84689 | Improvement | [Setup] Update CODESYS Installer to 2.0.0 | Fixed |   
CDS-84475 | Improvement | BinTagUtil: Move alignment and size checks of BTagReaderGetContent2() to an extra function | Fixed |   
CDS-84466 | Improvement | [Setup] Update CODESYS Automation Server Connector to 1.28.0.0 | Fixed |   
CDS-84462 | Bug | BinTagUtil: Alignment check missing | Fixed |   
CDS-84461 | Bug | CmpSettings::SettgGetWStringValue: Duplicate call of MemPoolUnlock and incompatibility in usage | Fixed |   
CDS-83807 | Bug | LibMan: SFC POU and GVLs from source library cannot be opened in library manager | Fixed |   
CDS-83787 | Bug | Libman: Changed library parameters are only applied after clean all | Cannot Reproduce | [[GENERAL]]  
With V3.5 SP19 this problem is not reproducible because of the new serialization/deserialization of the library parameters (see CDS-81934)  
CDS-83712 | Improvement | Compile: Enable possibility to use non-IEC-compliant identifiers by default | Fixed | [[GENERAL]]  
Support non-IEC-compliant identifiers by default  
CDS-83707 | Bug | Online Device: Online connection with safety controller is not possible | Won't Fix | [[GENERAL]]  
As agreed on by our Support and Runtime Team, this issue cannot be fixed in our code, instead it has to be investigated and solved by the hardware supplier Kendrion. See associated COS-11368 for more information.  
CDS-83697 | Bug | Linux SL: file descriptor leak | Fixed |   
CDS-83676 | Improvement | [Setup] Update CODESYS Softmotion to 4.13.0.0 | Fixed |   
CDS-83674 | Improvement | Update SoftMotion to 4.13.0.0 (SP19) | Duplicate | [[GENERAL]]  
Duplicates CDS-83676  
CDS-83672 | Improvement | [Setup] Update CODESYS CANopen to 4.1.1.0 | Fixed |   
CDS-83670 | Improvement | [Setup] Update CODESYS Profinet to 4.3.0.0 | Fixed |   
CDS-83665 | Improvement | [Setup] Update CODESYS EtherNetIP to 4.4.0.0 | Fixed |   
CDS-83663 | Bug | VarPersistentObject: Crash IDE by Specific Procedure | Fixed |   
CDS-83654 | Improvement | DeviceObject: correct metrics number of instances of CANopen safety devices | Fixed |   
CDS-83649 | Bug | Setup: CodeMeter Container/license contain wrong company name "3S" | Fixed |   
CDS-83638 | Improvement | [Setup] Update CODESYS Ethernet Adapter to 4.1.0.0 | Fixed |   
CDS-83637 | Improvement | CmpBACnet, CmpBACnet2: Change default of bacstac.ini to a path within the PlcLogic directory | Fixed |   
CDS-83630 | Improvement | BACnet: BACstack2 and CmpBACnet2 - update to BACstack V24.1.33.1 | Fixed |   
CDS-83629 | Bug | SVG-Renderer: Update OSS to latest versions (pixman 0.42.2) | Fixed |   
CDS-83623 | Bug | CmpXMLParser / expat: Update to most recent version 2.5.0 | Fixed |   
CDS-83621 | Bug | POU, Editor: the OK button and text overlap in the "Edit Declaration Header" popup | Fixed |   
CDS-83619 | Improvement | DeviceObject: rename metrics description and add category fieldbus | Fixed |   
CDS-83615 | Bug | Embedded /SIL2: Retains are never initialized Companion | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
To make full use of retain handling, SysMemAllocArea() should be able to return two areas for retains. One for the data, and a small 32Bit one, for the data layout CRC.  
When this is provided, the retains are initialized even when the bootproject is exchanged.  
When the second area is not returned, the retains behave the same as before.  
CDS-83612 | Improvement | License Manager: Confirm license activation on UFC container | Fixed |   
CDS-83600 | Improvement | CmpIecVarAccess: Update content feature flags to latest changes of IecVarAccess3 Interfaces 4.3.0.0 | Fixed |   
CDS-83565 | Bug | RSMUtility: Proper handling of OnlineChange | Fixed |   
CDS-83564 | Bug | NBS: Proper handling of OnlineChange | Fixed |   
CDS-83557 | Bug | Licensed Software Metrics: Dialog shows unlimited metrics after "Read from device". | Fixed |   
CDS-83555 | Improvement | Licensed Software Metrics: Provide interface for "Generate Code required". | Fixed |   
CDS-83553 | Improvement | DeviceObject: do not count hidden channels for software metrics | Fixed |   
CDS-83548 | Bug | Compiler: Show compile warning if one alias type is assigned to another alias type with the same base type | Won't Fix | [[GENERAL]]  
An alias is defined as an alias of its base type. I.e. it behaves in the same way as the base type. If we have an assignment  
alias1 := alias2;   
Then on both sides of the assignment, the base type would be allowed with no warning. So the alias must be allowed as well.  
We cannot change this behaviour and produce a new warning for such a situation.  
Enumerations on the other hand are not the same type as its base.  
CDS-83544 | Improvement | SIL2: Improve state based test output (Companion) | Fixed |   
CDS-83522 | Improvement | QS target VxWorks/ARM64 - Test/Implement exception handling | Fixed |   
CDS-83521 | Improvement | QS target VxWorks/ARM64 - Implement IEC debugging | Duplicate |   
CDS-83519 | Improvement | LibDevSummary: How to handle blocking BackgroundTasks. | Fixed |   
CDS-83508 | Improvement | CmpCodeMeter: PatchProtection container must be filtered out from read service | Fixed |   
CDS-83493 | Bug | CMBasicChecks: Console output needs improvement | Fixed |   
CDS-83485 | Bug | Reference packages cannot be installed | Fixed |   
CDS-83483 | Bug | DeviceEditorCANOpen: SDO parameter modification takes long time (~30s) | Duplicate |   
CDS-83478 | Bug | App Based License: Wrong product code and conversion factor for code size | Fixed |   
CDS-83476 | Bug | CDS crash: when click Toolbar button Tools -> Options -> Libraries if the language is Simple Chinese | Fixed | [GENERAL] Missing placeholder sign in chinese localization  
CDS-83471 | Improvement | [Setup] Update CODESYS Automation Server Connector to 1.27.0.0 | Fixed |   
CDS-83467 | Improvement | License Manager: Hide internal licenses | Fixed | [[GENERAL]]  
License Manager does not display ".Internal" Licenses.  
CDS-83466 | Bug | Deviceobject: If you select another Bus Cycle Task and switch back again, you cannot log in without downloading | Fixed | [[GENERAL]]  
Compiler version >= 3.5.19.0 required.  
CDS-83464 | Bug | Wrong code relocation for direct calls with Thumb-codegenerator | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
CDS-83460 | Improvement | BACnet: CmpBACnet - build with dm instead VS | Fixed |   
CDS-83459 | Bug | WatchList: Missing check for null pointer | Fixed |   
CDS-83458 | Bug | DeviceCommunicationEditor: Setting active path fails if encrypted communication is enforced by device | Fixed |   
CDS-83457 | Bug | Sporadically, a new download is necessary after project load | Fixed | [[GENERAL]]  
Compiler version >= 3.5.19.0  
-> The performance of some operations in combination with the loading and storing of compile information (project load, download, update environment etc.) may decrease by some percent.  
CDS-83456 | Bug | CmpOPCUAClient: If the server disconnects without sending a FIN packet, then on reconnection the client receives a SIGABRT | Fixed |   
CDS-83455 | Bug | [TechDebt] Fix a subset of SonarLint issues in Essential Plugins | Fixed |   
CDS-83453 | Improvement | CmpBACnet2: Add CmpBACnet2 to all PLC's running CmpBACnet(1) | Fixed | [[GENERAL]]  
Components CmpBACnet and CmpBACnet2 are linked dynamically to the runtime.  
CDS-83452 | Bug | Licensed Software Metrics: Bad performance with objects providing large language model | Fixed |   
CDS-83450 | Bug | LibraryManager: Signed and timestamped library is displayed as "expired" in LibMan Editor | Fixed |   
CDS-83446 | Improvement | Store: Remove Sonarqube issues related to CDS-78757 | Fixed |   
CDS-83444 | Improvement | [Setup] File type extensions should be parameterized | Fixed | [[GENERAL]]  
If the property CDS_PROJECT_TYPEEXTENSION is set to 1, the setup adds the file type extension for .project, .projectarchive and .library.  
The default value for the property is 0, so the file type extensions are not registered.  
If you double-click a project, projectarchive or library file and CODESYS Installer 1.6.0 (or later) is installed, CODESYS Installer is launched.  
For more information see the documentation "CODESYS Installation Extended OEM Adaptions" and CODESYS Installation OEM Adaptions"  
CDS-83440 | Bug | UFC PatchProtection Container is displayed in LicenseManager | Fixed | [[GENERAL]]  
UFC Patch Protection Container has been remove from UI.  
CDS-83435 | Improvement | CmpApp: External interface needed to check LicenseMetrics table from download in a secure way | Fixed |   
CDS-83434 | Bug | OnlineChange at Application took a long time = 10003 [ms] | Duplicate | [[GENERAL]]  
With CDS-83564 the cause of the problems has been fixed.  
As soon as the customer uses the current version of the library, the reported behavior can no longer be reproduced.  
CDS-83430 | Bug | Watchlist: Structure variable within another structure cannot be expanded | Won't Fix | [[GENERAL]]  
Won't fix because wrong usage of the user.  
It is not possible to monitor an unqualified variable (declaring pou is missing) in the watchlist because possibly ambiguous  
CDS-83429 | Bug | Refactoring: Default value of an enumeration is not changed if the corresponding enumeration member is renamed | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-83416 | Improvement | Update InstallShield to latest version 2022 R2 | Fixed | [[GENERAL]]  
InstallShield 2022 R2 is used to build the setups.  
CDS-83415 | Improvement | SIL2: Add Errata and Release Notes to SIL2 deliveries | Fixed |   
CDS-83409 | Improvement | Package Manager: Blacklist Visu < 4.3.0.0 | Fixed | [[GENERAL]]  
Package Visualization < 4.3.0.0 is now blacklisted for 3.5.19.0 or newer.  
CDS-83406 | Bug | NBS: TCP_Client handle udiTimeOut Parameter not properly | Fixed |   
CDS-83405 | Improvement | [Setup] Update CODESYS Visualization to 4.3.0.0 | Fixed |   
CDS-83404 | Bug | WinCE: Deliveries referencing wrong header files | Fixed |   
CDS-83403 | Bug | CmpCodeMeter: UFC PatchProtection Container must be ignored at startup of runtime | Fixed |   
CDS-83400 | Bug | OPC UA Server: ctrlConfigurationName is not set correctly | Fixed |   
CDS-83387 | Bug | SysTargetLinux / virtual Control: CAS does not reconnect after restart of PLC | Fixed |   
CDS-83382 | Improvement | Setup shall install UFC Container by default | Fixed |   
CDS-83376 | Improvement | BACnet2: CmpBACnet2 - modify property API to use subrange types where needed | Fixed |   
CDS-83373 | Bug | DeviceRepository: Installing a device description does not support long paths | Fixed |   
CDS-83372 | Bug | CmpCharDev.library freeze when cdmmap is used | Fixed |   
CDS-83368 | Bug | Device, PLC Open Import: Importing a module is possible, even the parent source and target device IDs are different | Fixed |   
CDS-83331 | Improvement | SysSocket documentation: Rename category "TCP flags" to "Message flags" | Fixed |   
CDS-83330 | Improvement | Libman, Parameter: Usability improvements | Fixed |   
CDS-83327 | Improvement | CmpOpenSSL: CRLs should be deleted on reset origin device | Fixed |   
CDS-83321 | Bug | Linux SysEthernet: possible heap corruption on startup | Fixed |   
CDS-83313 | Bug | Device Repository: folder of different vendors are not shown | Fixed |   
CDS-83311 | Improvement | Visu, Targetvisu: Support custom tooltips | Fixed |   
CDS-83302 | Improvement | BACnet23: BACstack23 - modifications required for initial bringup of CmpBACnet23 / BACstack23 | Fixed |   
CDS-83301 | Improvement | BACnet23: CmpBACnet23 - modifications required for initial bringup of CmpBACnet23 / BACstack23 | Fixed |   
CDS-83297 | Bug | [TechDebt] Fix a subset of SonarLint issues in Essential Plugins | Fixed |   
CDS-83296 | Improvement | CODESYS: Improve usability for check of passwords against RuntimePasswordPolicy | Fixed |   
CDS-83293 | Improvement | DeviceObject: option for outputs channels required to move to input task mapping list | Fixed |   
CDS-83292 | Improvement | Runtime Toolkit Dokumentation: Add examples to configuration files to extend the error logging | Fixed | [[GENERAL]]  
Added examples in .cfg to enable verbose logging for specific components  
CDS-83291 | Bug | Unhandled Exception: Scan Application in 'Online Change Memory Reserve Settings' View with specific project | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-83288 | Bug | [Setup] Packages cannot be installed if 8dot3 is disabled | Fixed |   
CDS-83287 | Improvement | Depictor: Remove Depictor-Prototype from runtime product | Fixed |   
CDS-83285 | Improvement | DM: DM should deliver UFC Container for device vendors automatically | Cannot Reproduce |   
CDS-83281 | Bug | Compile error C0032 if use TO_LREAL with a Input type Time | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
CDS-83276 | Improvement | DeviceRepository: add interface function for HideVersion attribute | Fixed |   
CDS-83268 | Bug | CmpIxxatCANDrv: Redefinition of HANDLE64 with latest Windows toolchains breaks windows build | Duplicate |   
CDS-83265 | Improvement | App Based License: Generate implicit code to check license metrics | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-83264 | Improvement | App based License: Display each metric only per application | Fixed | [[GENERAL]]  
With this CDS only the display was changed. Everything else: TBD  
CDS-83262 | Improvement | CodesysSpV3: Add contributions needed by Windows and 3SRTE to .cubicle | Fixed |   
CDS-83256 | Improvement | [Setup] Update CODESYS Installer to 1.5.0 | Fixed |   
CDS-83253 | Improvement | Change error / warning messages to lower severity | Fixed |   
CDS-83240 | Bug | Compiler: Interface method with attribute 'call_after_global_init_slot' causes fatal compile error | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-83238 | Bug | Function UPPER_BOUND: Internal error, if a one-dimensional array from a struct located within a library is used. | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-83236 | Bug | LibMan: Changed library parameters are ignored if same library is also present a subordinate library | Cannot Reproduce | [[GENERAL]]  
According to the description this is a SP18 Patch 3 specific problem and cannot be reproduced with compiler version SP19  
CDS-83233 | Improvement | [Project Inspection] Use project embedded type information | Fixed | [[GENERAL]]  
Project Inspections now considers the opt-in data file without server communication. If a project does not provide a data file, the analysis will be done the old way via deployment server.  
CDS-83232 | Improvement | [Project Inspection] Embed required type/add-ons into the project | Fixed | [[GENERAL]]  
Project insepction data will be stored as auxiliary within the project.  
CDS-83227 | Improvement | SysTaskLinux: TASKPRIO_IDLE priority should be mapped to SCHED_IDLE to support long running tasks | Fixed |   
CDS-83223 | Bug | Compiler: Wrong precompile error C0412 | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-83191 | Bug | It is not possbile to install CODESYS in a folder with chinese characters | Fixed | [[GENERAL]]  
Installation paths can now also contain Chinese characters  
CDS-83187 | Bug | CmpCodeMeter: CodeMGetContentByFirmcode3() must check for RTS_INVALID_HANDLE | Fixed |   
CDS-83183 | Improvement | CmpCodeMeter: Improve log messages for debugging | Fixed |   
CDS-83177 | Bug | Translation, German: Strings in Find dialog and Project Compare are cut | Cannot Reproduce |   
CDS-83175 | Improvement | CmpEventMgr: Log area/offset location of an IEC-callback at exception | Fixed |   
CDS-83173 | Bug | Refactoring: Commands may throw NullRefException in an OEM environment | Fixed |   
CDS-83168 | Bug | CmpFileTransfer: char* and const char* for RTS_COMPACT configuration not implemented | Fixed |   
CDS-83167 | Improvement | Update System.Data.SQLite to most recent version 1.0.117.0 containing sqlite 3.40.0 | Fixed |   
CDS-83166 | Improvement | Essentials: Update WibuCmNet to latest version 7.51 | Fixed | [[GENERAL]]  
CODESYS uses now the version 7.51 of the WibuCmNet assembly.  
CDS-83165 | Improvement | CEF: Update CEFSharp to latest version 107.1.50 | Fixed |   
CDS-83163 | Bug | Visu, Overlay, OnValueChanged: The ValueChanged test fails in Targetvisu Overlay test | Duplicate | [[GENERAL]]  
This issue was already fixed with CDS-82781 in SP19.  
CDS-83162 | Improvement | Update CodeMeter runtime to latest version V7.51 | Fixed |   
CDS-83161 | Bug | VxWorks: SysSockOSSetIpAddressAndNetMask() does not set the UP-flag of the IP stack | Cannot Reproduce |   
CDS-83157 | Bug | Libman: CDS crash when operating "Add library" in an "Input Assistant" dialog | Duplicate | [[GENERAL]]  
Duplicate of CDS-81358  
CDS-83156 | Bug | SIL2 PSP: SafetyComponents list is not extendable/modifiably by extension (companion) | Fixed |   
CDS-83154 | Bug | Gateway or PLCHandler Interface ARTI: Possible very very rare crash in CmpChannelClient | Fixed |   
CDS-83151 | Bug | Compile: Real values are displayed incorrectly | Fixed | [[GENERAL]]  
The values are now converted to the correct representation after they are entered.  
CDS-83150 | Bug | Compile: Internal error for access to an array with variable length if the index contains a variable of type REAL | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-83149 | Improvement | BACnet2: adapt CmpBACnet2 to final naming and package structure | Fixed |   
CDS-83146 | Bug | Visu: HMI shows Qt errors | Fixed |   
CDS-83140 | Improvement | CODESYS Control linux: SysCryptoLinux should adapt min_entropy define to kernel version | Fixed |   
CDS-83135 | Bug | [TechDebt] Fix a subset of SonarLint issues in Online Manager, Part II | Fixed |   
CDS-83134 | Improvement | BACnet23: CmpBACnet2 - modify CmpBACnet2 BACstack base type typedefs to avoid ALIAS chains. | Won't Fix | [[GENERAL]]  
Done with other JIRA's - won't fix.  
CDS-83133 | Improvement | [Setup] Update CODESYS CANopen to 4.1.0.0 | Fixed |   
CDS-83132 | Bug | Localization: "Auto Declare" Dialog, "Scope (範囲 in JP)", Shortcut character and closing blacket is hidden | Fixed |   
CDS-83129 | Bug | Project Inspection: In CODESYS < SP17 the Addon Versions are not detected correctly | Won't Fix | [[GENERAL]]  
Project's profile lists UML plugin being present in version 4.2.2.0.  
CDS-83128 | Bug | Project Inspection: Only optional addons cannot be selected | Fixed | [[GENERAL]]  
Add-ons that are required for the project but not listed within the project's profile have been added to the inspection result. Listing Control SL add-ons as required add-ons require changes to these products and must be fixed there.  
CDS-83121 | Bug | [PackageManager] Uninstall of the packages with the same plug-in failed | Fixed |   
CDS-83119 | Bug | Taskmonitor: Exception if a new task is created | Duplicate | [[GENERAL]]  
Duplicate of CDS-81285  
CDS-83117 | Bug | DeviceRepository: Icons not displayed correctly in some views. | Fixed |   
CDS-83115 | Bug | Password/Communication Policy: Issues with access rights on Runtime objects “Settings” and “SecuritySettings” | Won't Fix | [[GENERAL]]  
User rights configuration error  
CDS-83112 | Bug | Compiler: Internal error instead of identifier not defined. | Cannot Reproduce | [[GENERAL]]  
Cannot reproduct with compilerversion 3.5.19.0  
CDS-83105 | Bug | SysExceptLinux: suspicious log messages when debugging on 64bit system | Fixed |   
CDS-83104 | Bug | Possible DoS vulnerability in FileTransferStartUpload | Fixed | [[GENERAL]]  
For more details see Advisory 2023-02, which is available on the CODESYS website:  
https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17554&token=5444f53b4c90fe37043671a100dffa75305d1825&download=  
CDS-83103 | Improvement | RTS OnlineHelp: Improve CmpMemPool documentation | Fixed |   
CDS-83101 | Bug | RTSDoc coding_guide_documentation: Missing parameter type "INOUT" | Fixed |   
CDS-83100 | Bug | Setup: CODESYS Installer merge module sometimes fails to install | Fixed |   
CDS-83099 | Improvement | NBS: TCP_CONNECTION should provide the posibility to query current client data (IP + Port) | Fixed |   
CDS-83097 | Improvement | CmpBinTagUtil: Add new variant of BTagReaderGetContent() with alignment and size checks | Fixed |   
CDS-83089 | Bug | Refactoring: Renaming an interface property might lead to wrong but compilable code | Fixed |   
CDS-83086 | Improvement | SysSockRecvMsg: Implementations for VxWorks | Fixed | [[KNOWN_LIMITATIONS]]  
On VxWorks systems, the message flag SOCKET_MSG_BCAST is not supported. The socket option SOCKET_IP_PKTINFO will not be checked in that case.  
CDS-83082 | Bug | [TechDebt] Fix a subset of SonarLint issues in Online Manager | Fixed |   
CDS-83080 | Bug | LibMan: Wrong display for ANY Types in LibMan Dokuview | Fixed |   
CDS-83078 | Bug | Incorrect code with VAR_IN_OUT and a property call of a program | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-83073 | Bug | VxWorks: SysEthernetGetPortConfigAndStatus() does not return Advertised / Supported Capabilities | Fixed | [[GENERAL]]  
New settings for VxWorks targets, to specify the supported and advertised link capabilities.  
CDS-83071 | Improvement | WebBrowserIntegration: Wrap all necessary interfaces so that a "Visu" prototype can use WebView2 | Fixed |   
CDS-83070 | Improvement | WebBrowserIntegration: Wrap all necessary interfaces so that the "Store" plugin can use WebView2 | Fixed |   
CDS-83062 | Bug | RTS: Update sqlite to most recent version 3.39.4 | Fixed |   
CDS-83059 | Improvement | Fix command documentation of cert-importcrl | Fixed |   
CDS-83032 | Bug | Package Manager: Migration to additional folder fails if no package is installed | Fixed | [[GENERAL]]  
Corruption of the installation has been fixed. Further more the Installer menu item will be visible again for SP17 installations.  
CDS-83025 | Bug | Simulation: "License file invalid" in simulatiom mode | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced starting with compiler version 3.5.18.0  
CDS-83018 | Bug | DeviceTree: Modified address is kept during Copy/Paste of device, even if address modification is disabled for target PLC | Fixed |   
CDS-83015 | Bug | Control RTE: SysEthernetGetPortConfigAndStatus() does not return Advertised / Supported Capabilities | Fixed |   
CDS-83011 | Bug | Compiler: Method with ARRAY[*] parameter causes duplicate PrecompileId of variables when saved as compiled library | Fixed |   
CDS-83010 | Bug | RTE: SysEthernet Drivers: SysEthernetPortConfigAndStatus: MAUType member sometimes invalid. | Fixed |   
CDS-82977 | Improvement | Setup: Windows 11 should be listed as valid OS | Fixed |   
CDS-82976 | Bug | Compiler: Crossreference without source position in the hasconstanttype pragma statement | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82974 | Bug | Compiler: Strange crossreference for DUT used in hastype pragma | Fixed | [[GENERAL]]  
There should be a cross reference to the variable a when searching for the type.  
[[KNOWN_LIMITATIONS]]  
Due to technical limitations, a pragma statement must always be on a single line. Line breaks within a pragma are not allowed.  
CDS-82973 | Bug | New Project: Typing error in the "New project" dialog | Fixed | [[GENERAL]] Typing error in UI source  
CDS-82972 | Bug | SVG-Renderer: Update OSS to latest versions (curl 7.86.0, libxml2 2.10.3, libpng 1.6.38, zlib 1.2.13) | Fixed | [[GENERAL]]  
Updated libcurl.dll to version 7.86.0.0  
Updated libxml2.dll to version 2.10.3  
Updated libpng to 1.6.38  
Updated zlib to 1.2.13  
CDS-82971 | Bug | Visu: Error "Function 'FB_Init' requires exactly '6' inputs" in visualization objects after online change in CODESYS SP17 Patch 4 | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82970 | Bug | [Motorola RX63N]: DevDesc requires some adaptations | Fixed |   
CDS-82968 | Bug | PlugInCache: Initialization of PlugIn cache fails | Fixed | [[GENERAL]]  
Added a fallback for loading unmanaged additional file references during plugin cache creation.  
CDS-82950 | Improvement | DeviceObject: go to definition should be possible with symbolic access | Fixed | [[GENERAL]]  
Compiler version >= 3.5.19.0 required.  
CDS-82935 | Bug | LMM: "internal error" during loading of a project | Cannot Reproduce | [[GENERAL]]  
With V3.5 SP19 no longer reproducible  
CDS-82932 | Bug | Control RTE: Double ARP Response | Fixed |   
CDS-82920 | Improvement | SysSockRecvMsg: Implementations for RTE/LWIP | Fixed |   
CDS-82919 | Improvement | SysSockRecvMsg: Implementations for Linux, QNX | Fixed | [[KNOWN_LIMITATIONS]]  
On QNX systems, the message flag SOCKET_MSG_BCAST is not supported. The socket option SOCKET_IP_PKTINFO will not be checked in that case.  
CDS-82906 | Bug | Project Inspection: Not all addons are detected | Won't Fix | [[GENERAL]]  
Since SP18 the project inspection only project relevent types to mandatory ones. The mentioned addons are currently not required/used in the project and will not be prompted.  
CDS-82904 | Bug | Visu, Targetvisu: Crash during shutdown according to logfile | Fixed |   
CDS-82902 | Bug | RTE: CmpXMLParser: Mismatch in calling convention of xml-parser-callbacks and callback. | Fixed |   
CDS-82901 | Bug | Unhandled Exception for changing FB instance name | Duplicate | [[GENERAL]]  
Cannot reproduce with version 3.5.19.0 CurDev 185  
CDS-82899 | Bug | Libman: Unbound Placeholder | Won't Fix | [[GENERAL]]  
Works as designed, updating the visualisation profile and the libraries is necessesary in this case.  
CDS-82877 | Bug | Compile: Online change after changing a constant value leads to compile error | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82872 | Bug | PLCHandler: Flaws in PLCHandler::SetConfig method and PLCHandler documentation | Fixed |   
CDS-82869 | Improvement | [Setup] Update CODESYS EtherCAT to 4.4.0.0 | Fixed |   
CDS-82868 | Bug | Project Compare: Cursor position lost in comparison tree while committing changes | Cannot Reproduce | [[GENERAL]]  
Already fixed by CDS-81221.  
CDS-82861 | Bug | Monitoring: Implicit NVL variables cannot be monitored | Duplicate | [[GENERAL]]  
Already fixed with CDS-81443: NetVars: Monitoring of the implicit variables does not work anymore  
CDS-82858 | Bug | Compile: Build leads an internal error | Cannot Reproduce | [[GENERAL]]  
1\. Cannot reproduce with compilerversion 3.5.18.0 and 3.5.19.0  
There is another error message (see CDS-82582: Compiler: "C0032: Cannot convert type 'DINT' to type 'INT'" message appears with customer project)  
2\. Project Enviroment > Cancel" is no more a supported use case.  
CDS-82857 | Bug | TargetVisu / SysGraphicWindowQt: target visu causes a long startup | Fixed |   
CDS-82849 | Bug | Visu, FileTransfer: Streaming file transfer not working with 2-process Targetvisu | Fixed | [[GENERAL]]  
The streaming file transfer never worked correctly for the targetvisu. It is also a very rare used feature and therefore a follow-up issue for big files has been created: CDS-82856. This issue fixes the exception.  
CDS-82848 | Bug | LibMan: Performance problems in ResolveUnboundPlaceholdersRecursively | Fixed |   
CDS-82842 | Bug | False compatible message for compiled interface library | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82841 | Bug | Unexpected error from runtime during online change | Duplicate | [[GENERAL]]  
With CDS-83565 the cause of the problems has been fixed.  
As soon as the customer uses the current version of the library, the reported behavior can no longer be reproduced.  
CDS-82840 | Bug | WinCE 6,7: runtimes with Redundancy cannot be build | Fixed |   
CDS-82837 | Improvement | Update SoftMotion to 4.12.0.0 | Fixed |   
CDS-82836 | Bug | Second I/O Mapping Editors page appears | Cannot Reproduce | [[GENERAL]]  
Already fixed with CDS-78138 and Clone CDS-79091 in version 3.5.18.0 and 3.5.17.30 and therefore cannot reproduced anymore  
CDS-82833 | Epic | Support App Based licenses | Fixed |   
CDS-82831 | Improvement | WebBrowserIntegration: Remove any CEF-related files and implementations from Essentials | Fixed | [[GENERAL]]  
All functionality based on CEF (=Google Chrome browser) has been removed from the Automation Platform and the associated interface 'IWebBrowserIntegration' has been obsoleted.   
  
All users of the AP are advised to migrate their current implementation to the new interface 'IWebView2Wrapper' that is based on WebView2 (=Microsoft Edge browser).  
  
The motivation for this breaking change was the constant security risks contained in CEF, which could not be fixed by automatic updates of the operating system. The new implementation based on WebView2 is automatically updated to the most current secure state via the operating system.  
CDS-82829 | Bug | Libman: Online values are no longer displayed after setting a breakpoint in a library | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82828 | Bug | Device: Some device nodes missed after undo a delete controller | Fixed |   
CDS-82820 | Improvement | CODESYS Control: Create QS target for VxWorks/ARM64 | Fixed |   
CDS-82805 | Improvement | CODESYS Control: Create QS target for DragonCore | Fixed |   
CDS-82802 | Bug | Refactoring does not seem to work in compiler statements | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
Similar problems with other pragma statements will be fixed with CDS-82974 (hastype pragma) and CDS-82976 (hasconstanttype pragma)  
CDS-82795 | Improvement | RTS Unittest: Example for communication layer 7 | Fixed |   
CDS-82793 | Bug | Compiler, Reflection: Internal errors if two unqualified global variables with the same name same of a FB with 'instance-path' attribute exist | Duplicate | [[GENERAL]]  
Duplicate of CDS-82584  
CDS-82784 | Improvement | CODESYSControl: create x64 QS target for vControl | Fixed |   
CDS-82781 | Bug | Visu, Overlay, DateTimePicker: Cannot enter numbers with test script | Fixed |   
CDS-82777 | Improvement | BACnet23: CmpBACnet23 - extend BACstack logging to BACstack23 log level configuration | Fixed |   
CDS-82774 | Bug | LibMan: Possibility to reset the placeholder redirection of the pool libman to default although with no effect | Fixed |   
CDS-82773 | Bug | CmpSchedule: More than one external event task must be supported | Fixed |   
CDS-82771 | Improvement | Remove "First Steps" PDFs from CODESYS installation | Fixed |   
CDS-82768 | Bug | Compiler: Invalid precompile error when accessing member of type declared in a library | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce with compilerversion 3.5.19.0  
CDS-82765 | Bug | Project Inspection: Continue with installation provides unsuitable versions | Fixed |   
CDS-82764 | Bug | ImagePool, Textlist: Typo in Menu | Cannot Reproduce | [[GENERAL]]  
Cannot Reproduce, the menu texts are already fixed with SP19 and Visu CurDev.  
CDS-82763 | Bug | Project Inspection: Wrong Visualization Version detected | Duplicate |   
CDS-82760 | Bug | [OnlineCommands] Set the dependency SafetyOnlineControllerProvider as optional | Fixed |   
CDS-82759 | Bug | Project Inspection: ESM version not correct detected | Fixed |   
CDS-82754 | Improvement | BACnet23: BACstack23 - patch malloc/free etc. | Fixed |   
CDS-82749 | Bug | Output Default values are applied even after a reboot in "start in run" | Won't Fix | [[GENERAL]]  
The problem is caused by the io driver from the customer.   
The outputs are already set in IoDrvMapping and therefore before the tasks are started. This shall be done only in IoDrvWriteOutputs.   
In this case the system boots and loads the application.  
In GlobalInit the outputs variable is set to the initialization value (output true) and then IoMgrUpdateConfiguration and IoMgrUpdateMapping is called.   
In the customer driver here the outputs are already copied from the IEC address to the real output.  
Now the tasks are started and at the end of first task cycle IoMgrWriteOutput is called which clears the output.  
Therefore this issue is won't fix as a wrong implementation of the io driver and there is no possibility to change this in the programming system.  
CDS-82748 | Bug | Install package failes if devdesc has too long filepath | Fixed | [[GENERAL]]  
Fixed only the Long Path problem in the package manager. The error in the device repository will be fixed with CDS-83373.  
CDS-82735 | Bug | Localization: Typo "Implementierungsssprache" in German Add POU dialog | Fixed | [[GENERAL]] Typing error in UI source  
CDS-82729 | Bug | Auto declare dialog: CODESYS crashes when trying to use an undeclared variable at FbIterateClients | Cannot Reproduce | [[GENERAL]]  
Starting with V3.5 SP18 this problem is no longer reproducible  
CDS-82683 | Bug | Several RCE and DOS vulnerabilities | Fixed | [[GENERAL]]  
For more details see Advisory 2023-02, which is available on the CODESYS website:  
https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17554&token=5444f53b4c90fe37043671a100dffa75305d1825&download=  
CDS-82682 | Bug | Internal files or directories accessible to external parties | Cannot Reproduce | [[GENERAL]]  
Was already fixed by CDS-59017 in version V3.5.12.30.   
  
We highly recommend to keep the secure default values for the following settings:  
[SysFile]  
ForceOnlineFilePath=1  
DenyOnlineAccessCfgFile=1  
  
For more details see Advisory 2018-04, which is available on the CODESYS website:  
https://customers.codesys.com/fileadmin/data/customers/security/2018/Advisory2018-04_CDS-59017.pdf  
CDS-82672 | Bug | Remove compile warnings in SysExcept for SIL2 | Fixed |   
CDS-82663 | Bug | CmpMonitor2: Use TYPE3_NONE in ReadReadExp() to avoid warning for SIL2 | Fixed |   
CDS-82658 | Bug | Simulation: Stack Size exceeded in simulation mode (on 64Bit IDE) | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
If Simulation is enabled, the targetsettings memory-layout\max-stack-size and memory-layout\max-stack-size-external-call are read from the simulation device description.  
CDS-82657 | Bug | [CoreInstallerSupport] Wrong GAC DLL selected for the list of references | Fixed | [[GENERAL]]  
Probing für GACs has been adapted to prob for the exact matching assembly first.  
CDS-82653 | Bug | Compiler: Project update fails depending on update order | Cannot Reproduce | [[GENERAL]]  
Not reproducible vith V3.5 SP19  
CDS-82650 | Improvement | Display string constants with replaced escape sequence in a tooltip | Fixed | [[GENERAL]]  
If a string contains escape sequences a tooltip with the decoded string is displayed.  
CDS-82649 | Bug | An interface known by an alias is not handled correctly by the precompile | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82646 | Bug | CmpOpenSSL: In RtsX509CertExKeyUsageCopy() data is copied incorrectly | Fixed |   
CDS-82638 | Improvement | App Based Licenses: Remove limitation and display of task count | Fixed |   
CDS-82629 | Bug | Device Object: Multiple Device Diagnosis instances are created. | Fixed | [[GENERAL]]  
Compiler version >= 3.5.19.0 required to change the behaviour  
CDS-82623 | Bug | DeviceEditor: numerical controls can be changed while online with mouse wheel | Fixed |   
CDS-82621 | Bug | Redo is not available after Undo moving devices | Fixed |   
CDS-82620 | Bug | Visu, File Transfer: it does not work with overlay TV | Fixed |   
CDS-82617 | Bug | Internal Error when using property in visu under specific project SP18 | Duplicate | [[GENERAL]]  
duplicates CDS-82585  
CDS-82612 | Improvement | [Specification] SysMem: Set memory write protected | Fixed |   
CDS-82609 | Bug | Compile Errors after update from 3.5.18.0 to 3.5.18.10 | Fixed | [[GENERAL]]  
CompilerVersion>= 3.5.19.0  
CDS-82603 | Bug | Precompile Checks: No precompile checks in some POUs | Duplicate | [[GENERAL]]  
Duplicate of CDS-81249  
CDS-82600 | Bug | Compile: Crash after online change if FB_Init contains a virtual method call | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82590 | Improvement | [Setup] Update CODESYS IO-Link to 4.1.0.0 | Fixed |   
CDS-82589 | Improvement | Support UFC feature for all controls platforms | Fixed |   
CDS-82588 | Bug | DeviceObject: Import mapping from csv doesn't respect the selected node | Fixed |   
CDS-82585 | Bug | Compile Error: Internal error on specific project | Fixed |   
CDS-82584 | Bug | Internal Error in InstancePath generation for ambiguous paths | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
CDS-82583 | Improvement | User Management: Popup for unsuccesfull user creation should inform about non-compliance to password policy | Won't Fix | [[GENERAL]]  
This issue is not needed because it is not possible to add passwords that do not match the password policy anymore. See CDS-83296  
CDS-82580 | Bug | CmpRTL8169Mpd: RTE: Realtek driver does not update liTimestampHR in getethframeex. | Fixed |   
CDS-82578 | Improvement | DeviceCategories: Spelling of PROFINET is often wrong in device repository | Fixed |   
CDS-82574 | Improvement | [Setup] Update CODESYS Code Generator ARM to 4.0.2.0 | Fixed |   
CDS-82573 | Bug | LMM: internal error "DINT cannot be converted to INT | Duplicate | [[GENERAL]]  
Duplicate of CDS-82584  
CDS-82559 | Bug | Cross Reference: Using the Cross Reference List in a specific project leads to >90% CPU usage | Fixed |   
CDS-82557 | Bug | VisuClientX: Shutdown no longer working | Fixed |   
CDS-82555 | Bug | Installer: Versions prior 3.5.17.0 get installed without neccessary Addons | Fixed | [[GENERAL]]  
Requires CODESYS Installer 1.6.0.0 or later.  
CDS-82549 | Improvement | Improve Project Inspection Wizard | Fixed | [[GENERAL]]  
Wizard has been improved to follow an use case approach instead of the current error approach. Additionally there is a new "Details" button on the first page which shows the current differences to the installation. This button is only visible if the project has been saved with SP19 oder later.  
CDS-82539 | Bug | Compiler: Identifier 'i' is reported as undefined when accessing project variable from library | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
Accessing pool objects out of libraries is not an intentional feature. It might produce an error message in future versions. However, the code now compiles without error messages.  
CDS-82537 | Bug | InputAssistant: Wrong instance path inserted in the watch list | Fixed |   
CDS-82532 | Bug | Compiler: Division by zero exception in area-usage logging code | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82531 | Bug | IO Data is not updated if usage is only by Union | Won't Fix | [[GENERAL]]  
In this case, outputs are mapped to bits in a structure. This structure is also part of a union which contains a BYTE and this Byte is accessed in a task. The customers expectation now is that all the bits in the structure are updated in the task.  
The IO-Configuration only knows about the bits that are mapped to the output channel. The compiler does not provide information of all possible paths to the same memory location of the bit and doing so would be an incompatible change and it also would be quite time consuming.  
Therefore, if you map an instance path on a channel, make sure that this instance path is used in the code.  
CDS-82530 | Improvement | [Setup] Update CODESYS Code Generator ARM to 4.0.1.0 | Fixed |   
CDS-82513 | Bug | RTE: SysEthernetPortConfigAndStatus returns Invalid Values | Fixed |   
CDS-82499 | Improvement | [Setup] Update CODESYS Modbus to 4.2.0.0 | Fixed |   
CDS-82496 | Bug | [Docu] Online help for CAA File: Library does not support FTP/HTTPS | Fixed |   
CDS-82490 | Bug | DeviceScan: Scan without dialog does not use scan factories and inserts devices twice. | Fixed |   
CDS-82489 | Bug | CmpCodeMeter / CmEmbedded: Sporadically CmAct licenses after update lost / new empty container is created | Won't Fix | [[GENERAL]]  
This problem only affects PLCs without an installed CodeMeter runtime, i.e. with CODESYSControl with CodeMeter Embedded.  
  
Steps to repeat:  
1\. Install a CODESYSControl Linux SL Version 4.5.0.0 or newer.  
2\. Activate a license A.  
3\. Downgrade to CODESYSControl Linux SL Version 4.4.x.x or older.  
=> The CODESYSControl runtime does not recognize the previously created license container with license A and creates a new empty license container.  
4\. Activate a license B (different from license A).  
5\. Upgrade to CODESYSControl Linux SL Version 4.5.0.0 or newer again.  
=> The CODESYSControl runtime does not recognize the license container with license B that was created last, but now again the license container created at the beginning with license A.  
  
Workaround after step 5 (see above):  
1\. Remove (or comment out) the following setting from /etc/CODESYSControl_User.cfg:  
[CmpCodeMeter]  
FCBoundWithHashedSerNo.0=xxx  
2\. Restart the CODESYSControl runtime.  
=> Now the CODESYSControl Linux SL Version 4.5.0.0 or newer does recognize the license container with license A instead of the license container with license B.  
Unfortunately, the CODESYSControl runtime cannot recognize both license containers.  
With a CODESYSControl Linux SL Version 4.5.0.0 or newer, you can decide which license container should be recognized, using the workaround above.  
A CODESYSControl Linux SL Version 4.4.x.x or older is not able to recognize license containers created with CODESYSControl Linux SL Version 4.5.0.0 or newer.  
CDS-82481 | Bug | Compiler: "Assertion Failed" message appears with customer project | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce with the following version:  
\- CODESYS x64 3.5.19.0 CurDev 152  
\- ApaddonToolkit 1.0.2.0 CurDev 2  
\- CODESYS Application Composer 4.1.0.0 Release  
\- CODESYS Automation Server Connector 1.25.0.0 Release  
\- CODESYS C Code Integration 4.0.0.0 Release  
\- CODESYS CANopen 4.0.0.0 Release  
\- CODESYS CFC 4.1.0.0 Release  
\- CODESYS Code Generator ARM 4.0.0.0 Release  
\- CODESYS Code Generator ARM64 4.0.0.0 Release  
\- CODESYS Code Generator Blackfin 4.0.0.0 Release  
\- CODESYS Code Generator ColdFire 4.0.0.0 Release  
\- CODESYS Code Generator Cortex M3 4.0.0.0 Release  
\- CODESYS Code Generator PowerPC 4.0.1.0 Release  
\- CODESYS Code Generator RX 4.0.0.0 Release  
\- CODESYS Code Generator SH 4.0.0.0 Release  
\- CODESYS Code Generator TIC28x 4.0.0.0 Release  
\- CODESYS Code Generator TriCore 4.0.0.0 Release  
\- CODESYS CodeSpy 4.1.0.0 CurDev 151  
\- CODESYS Communication 4.2.0.0 Release  
\- CODESYS Compatibility Package 3.5.17.20 Release  
\- CODESYS Compiler Versions Archive 4.0.0.0 Release  
\- CODESYS Core Dump 4.0.0.0 Release  
\- CODESYS Device Reader 4.0.0.0 Release  
\- CODESYS EDS Import 4.1.0.0 Release  
\- CODESYS Embedded Runtime Extension 4.1.0.0 Release  
\- CODESYS EtherCAT 4.3.0.0 Release  
\- CODESYS Ethernet Adapter 4.0.0.0 Release  
\- CODESYS EtherNetIP 4.3.0.0 Release  
\- CODESYS IO-Link 4.0.0.0 Release  
\- CODESYS LD FBD 4.1.0.0 Release  
\- CODESYS Memory Tools 4.0.0.0 Release  
\- CODESYS Modbus 4.1.0.0 Release  
\- CODESYS NetX 4.0.0.0 Release  
\- CODESYS PROFIBUS 4.0.0.0 Release  
\- CODESYS PROFINET 4.2.2.0 Release  
\- CODESYS Recipes 4.1.0.0 Release  
\- CODESYS Redundancy 4.0.0.0 Release  
\- CODESYS RISC Front End 4.0.0.0 Release  
\- CODESYS SAE J1939 4.0.0.0 Release  
\- CODESYS Safety Support 4.0.0.0 Release  
\- CODESYS Scripting 4.0.0.0 Release  
\- CODESYS Security Agent 1.2.1.0 Release  
\- CODESYS Sercos III 4.0.0.0 Release  
\- CODESYS SFC 4.1.0.0 Release  
\- CODESYS SoftMotion 4.11.0.0 Release  
\- CODESYS Static Analysis 5.0.0.0 CurDev 193  
\- CODESYS Target Settings Export 4.0.0.0 Release  
\- CODESYS Test Manager for Automation Platform 4.3.1.0 Release  
\- CODESYS Trace 4.0.0.0 Release  
\- CODESYS Visualization 4.2.0.0 Release  
\- CODESYS Visualization Support 4.1.1.0 Release  
Test Environment:  
\- Windows 10 Professional x64  
CDS-82480 | Bug | DeviceScan: Junction Device: Copy all does not work as expected | Fixed |   
CDS-82475 | Bug | IEC Text Editor: Defines are not evaluated correctly | Fixed |   
CDS-82472 | Bug | CmpUserDBEmbedded: Impossible to change password | Fixed |   
CDS-82470 | Bug | BrowserCommand: "Go To Implementation" does not work for methods that are called via interface inside of a function block | Fixed | [[GENERAL]]  
The bugfix also fixes the problem, that the command "Go to instance" did not work in this case.  
CDS-82466 | Bug | Redundancy configurator does not work, shows up empty editor | Fixed |   
CDS-82463 | Bug | ComPages: Invalid UTF-16 node names from the RTS are handled incorrectly | Fixed | [[GENERAL]]  
While investigating this issue, it became clear that the node name in Step 1 of the Steps-to-Repeat is not a valid UTF-16 identifier. There is no way to fix this other than to prevent the user from setting the active path to a device with an invalid name.   
Please note that the differing display of the invalid node name as mentioned in Step 3 will not be fixed as we found no affordable solution for this and connecting to an invalid UTF-16 device is not a real-world scenario anymore.  
CDS-82454 | Bug | Setup: Update MicrosoftEdgeWebview2Setup.exe to latest version (1.3.165.21) | Fixed |   
CDS-82438 | Bug | LicenseManager: LicenseRepositoryDialog "Container serial number" textfield too long | Fixed |   
CDS-82436 | Bug | Linux x64: support set next statement | Duplicate |   
CDS-82430 | Bug | TargetVisu: Update to latest Qt version 6.3.2 | Fixed |   
CDS-82429 | Bug | Linux: runtime startup takes up to 1min on small devices | Duplicate | [[GENERAL]]  
Duplicate of CDS-83227  
CDS-82428 | Bug | Netvars UDP: sending blocks for 2-3 seconds | Fixed | [[GENERAL]]  
NetVarUdp.library 3.5.19.0: Nonblocking mode is set via  
diNonblocking: DINT := 1;  
SysSockIoctl(hSocket, SOCKET_FIONBIO, ADR(diNonblocking));  
CDS-82426 | Bug | Library Placeholder resolution missing after update all | Won't Fix | [[GENERAL]]  
The problem occurs due to some erroneous entries in the device description like this:  
<RequiredLib libname="Standard" placeholderlib="Standard" vendor="System" version="3.5.7.0" />  
After an update device the device object forces this library version which is not installed to the system. You should avoid to require libraries that are part of the installation and should be resolved to the newest available version.  
CDS-82415 | Bug | Compiler: Incorrect handling of FB instance with retain persistent variable | Won't Fix | [[GENERAL]]  
This behaviour is documented in the online help in several places:  
https://help.codesys.com/webapp/_cds_var_persistent;product=codesys;version=3.5.17.0  
"Whenever possible, avoid marking variables, which are declared in a function block, with PERSISTENT. This is because the function block instance is stored entirely in remanent memory and not just the marked variable."  
https://help.codesys.com/webapp/_cds_preserve_data_with_persistent_variables;product=codesys;version=3.5.17.0#double-allocation-of-memory-in-the-case-of-instance-paths  
"If only one variable in a function block is marked with PERSISTENT, then the function block instance is stored completely with all variables in remanent memory, although only the one variable is treated as persistent. "  
  
As a consequence if a device description contains an area for RETAIN PERSISTENT it also needs an area for RETAIN. We recommend to define a combined static area for both types of remanent variables.  
CDS-82398 | Bug | Runtime: Remove Compiler warnings | Fixed |   
CDS-82390 | Bug | SVG-Renderer: Update libxml2, zlib to latest versions (libxml2 2.9.14, zlib 1.2.12, libjpeg 9e und libjpeg-turbo 2.1.3) | Fixed |   
CDS-82387 | Improvement | SIL2: Compound Safety documentation must be extended | Fixed |   
CDS-82383 | Bug | Visu: Project with select and enter over selection api does not work in overlay mode | Fixed |   
CDS-82381 | Improvement | Output bugreport should be supplemented with LoadException | Fixed |   
CDS-82379 | Bug | NavigatorControl: Check if Primary Project != null is necessary in RenderingCallback | Fixed |   
CDS-82367 | Bug | Compiler, Incremental Compile: Newly added error-pragma does not report error | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82362 | Improvement | NetBaseServices: Add method to get IPV4Address as ARRAY OF BYTE | Fixed |   
CDS-82359 | Improvement | OnlineManager: Download of encrypted boot application with customized folder structure | Fixed |   
CDS-82352 | Bug | No Fast Online Change for FB with additional memory in some cases | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
CDS-82349 | Bug | ProjectCompare: Doesn´t work in Chinese language | Fixed |   
CDS-82341 | Bug | CmpIecTask.m4Itf: Clean up defines IECTASK_USE_(NO_)ATOMIC_BITACCESS | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
CmpIecTaskItf.h:  
\- IECTASK_USE_ATOMIC_BITACCESS no longer used. Is the default now!  
\- IECTASK_USE_NO_ATOMIC_BITACCESS used instead to deactivate atomic bit access for state and flag IEC-task variables  
CDS-82335 | Bug | CODESYS: Inadequate boot application encryption using Wibu dongle | Fixed | [[GENERAL]]  
For more details see Advisory 2022-15, which is available on the CODESYS website:  
https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17350&token=2cee62285d3ec76d6a78dfa9b9e81e66f6136a2a&download=  
CDS-82334 | Improvement | CmpSIL2: non-safe interface function to check for available external interface functions (compation) | Fixed |   
CDS-82333 | Bug | SysFileGetSize: Interface Description and SysTemplates are not correct | Fixed |   
CDS-82332 | Bug | Compiler: Warning C0417 is missing on "Compiler warnings" overview page of project settings | Fixed | [[GENERAL]]  
Starting with compiler version 3.5.19.0 the warning C0389 is reported for those situations where the message id C0417 was reported as warning in previous compiler versions. There still exist situations where the error C0417 is reported.  
CDS-82330 | Bug | Crash: CDS freeze if assigning an element of a constant as initial value of that constant (illegal operation) | Fixed |   
CDS-82313 | Improvement | DeviceObject: PLCopenxml Import: open device description with shared access | Fixed |   
CDS-82310 | Improvement | [Setup] Update CODESYS Installer to 1.4.0 | Fixed |   
CDS-82309 | Bug | DeviceEditor: Changing the Bus Cycle Task has no effect unless F11 or a clean all is made | Fixed |   
CDS-82306 | Bug | Crash: CODESYS crashes with special project during typing a variable | Cannot Reproduce |   
CDS-82305 | Bug | Scan Information: If a device enforces encrypted communication, the displayed info is wrong | Fixed |   
CDS-82302 | Bug | EasyUnitFramework: Fix generation of statics | Fixed |   
CDS-82296 | Bug | Compiler: Missing source position for error messages out of a library | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82293 | Bug | Linux & Templates : IoDrvSimple not useable with SP18 | Fixed |   
CDS-82292 | Bug | [Notification] Reg flag but no notifications are shown | Fixed |   
CDS-82289 | Bug | LicencedSoftwareMetrics, Memory-Leak: Remove CompileContext member from ApplicatoinUserCodeSizeDetailedForUI | Fixed |   
CDS-82286 | Bug | Compiler: Allow dynamic creation of interface instances with the operator __NEW | Fixed | [[GENERAL]]  
New compile error C560 "__NEW is not possible on interfaces"  
Compiler version >= 3.5.19.0  
CDS-82285 | Bug | DeviceEditor: Device name in Status tab overlaps with the value display bar | Fixed |   
CDS-82278 | Bug | Gateway: OpenChannelResponse contains unintialized dummy elements | Fixed |   
CDS-82258 | Bug | OPC UA Server: sporadic exception while calling operation 'Browse' | Fixed |   
CDS-82255 | Bug | Unhandled exception if used autodeclare with SMC_MoveContinuousAbsolute | Cannot Reproduce | [[GENERAL]]  
Starting with V3.5 SP18 this problem is no longer reproducible.  
Additionally with CDS-81244 a problem was fixed related to the problem of this issue.  
CDS-82248 | Bug | Persistent Variables: Bug with mapped variables and event task | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82244 | Bug | LMM: Internal error in OnlineChange | Fixed | [[GENERAL]]  
Compiler version >= 3.5.19.0  
CDS-82243 | Bug | Libman: Crash after changing placeholder and closing library | Duplicate | [[GENERAL]]  
After a general refactoring of the library manager editor (CDS-79420) this problem is no longer reproducible  
CDS-82241 | Bug | CmpOPCUAClient: Cleanup of OpcUa_CallRequest and OpcUa_CallResponse missing. Memory leak as a result | Fixed |   
CDS-82237 | Bug | DeviceObject: compiler error after disabling device diagnosis and start of online config mode | Fixed |   
CDS-82233 | Bug | Generate Code: Internal error in FUNCTION when initializing a VAR_INPUT of a subrange type | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82232 | Improvement | Fast Online Change: prevent progress update | Fixed | [[GENERAL]]  
CompilerVersion >3.5.19.0  
Section = LanguageModelManager  
Key = SuppressProgressUpdate  
If true, progress update is suppressed during code generation. This increases compile time, but the user gets no progress during compile, all messages will be produced once after compile. The callback is called before each code generation, you should return true only in case of a suspected fast online change.  
CDS-82229 | Improvement | Runtime: Define Clienttype for CODESYS Go | Fixed |   
CDS-82216 | Bug | Internal error on generate code on specific project | Fixed |   
CDS-82212 | Improvement | [Setup] Update CODESYS Risc Front End to 4.0.1.0 | Fixed |   
CDS-82197 | Bug | Setup installation: Progress bar does not show any progress during package installation | Fixed |   
CDS-82194 | Improvement | UnitTest: DeviceUserManagement: Add configurable lock, if a user tries to login with wrong password | Fixed |   
CDS-82193 | Bug | Task Deployment: Outputs are not shown correctly if symbolic access is enabled. | Duplicate | [[GENERAL]]  
Already fixed with CDS-81436  
CDS-82192 | Bug | LibMan: Problems with long paths | Won't Fix | [[GENERAL]]  
The library manager itself can be converted to long path without to much problems(see attached patch). But there are still problems with other plugins(BinaryArchive, Engine), when trying to use the libraries. I think supporting long paths requires a bigger time investment over multiple teams.  
CDS-82191 | Bug | Build: FOSS info is outdated in setup build | Fixed |   
CDS-82190 | Bug | PLCHandler on Windows 10 or newer: Sporadic crash during reconnect | Fixed |   
CDS-82188 | Bug | DeviceObject: Icons for symbolic access I/O channels are wrong. | Won't Fix | [[GENERAL]]  
this is by design.   
Outputs at the io channel must be inputs at the FB instance and Inputs at the io channels must be outputs at the fb instance.  
The intellisense shows only the icon for the fb instance and this is correct.   
Won't fix.  
CDS-82185 | Bug | Package Manager: Installation fails on turkish machines | Fixed |   
CDS-82180 | Bug | Package Manager: Performance problem, because already unpacked packages are ignored | Fixed | [[GENERAL]]  
Complete installation time of PackageManagerCLI.exe --installAll option could be improved up to 30%.  
CDS-82179 | Bug | __LAZY : shadowing issues if Lib.ChildLib.ERROR exists, and __LAZY is Lib.ERROR | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82174 | Bug | Crash when trying to update library in old project | Fixed |   
CDS-82170 | Bug | Crash: Codesys crashes when Double Click onto a IEC Object variable | Fixed |   
CDS-82162 | Bug | Compiler: Checkbounds is not working for dynamic arrays with VAR_IN_OUT as index access | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82160 | Improvement | RTS OnlineHelp: RUN/STOP transition must be specified and documented | Fixed |   
CDS-82157 | Bug | Compile error C0064 after update to 3.5.18.0 | Duplicate | [[GENERAL]]  
Duplicates CDS-82162  
CDS-82155 | Bug | Japanese: cut texts in Login Dialog | Fixed |   
CDS-82152 | Bug | Monitoring for THIS pointer in methods does not work as expected | Fixed |   
CDS-82146 | Improvement | [Setup] Update CODESYS Security Agent to 1.3.0 | Fixed |   
CDS-82144 | Improvement | [Setup] OEM docu should explicitly require an empty installation folder | Fixed | [[GENERAL]]  
Setup must check that the INSTALLDIR installation folder does not exist or is empty before installation. Do not allow multiple installations in the same directory. Do not install different versions with one installation in the same folder. This means that each version must be installed in a different folder.  
CDS-82107 | Bug | [PackageManagerCLI] Wrong error message if the MinimumPlugInVersion does not match | Fixed |   
CDS-82103 | Bug | SFC: AnalyzeExpressionCombined dont work in libraries | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82101 | Improvement | SecuritySettings: Settings must only be modified by Administrator user | Fixed |   
CDS-82098 | Bug | SIL2: CmpSIL2: SwitchToDebugMode service handler needs to check the permission | Fixed |   
CDS-82095 | Bug | SHD: SharedQueue kills Taskcycle while reset warm | Fixed |   
CDS-82092 | Bug | Install Package ends with Exception 'Path access denied c:\users\<user>\AppData\Local\Temp\UserInstall.log' | Fixed |   
CDS-82089 | Bug | DeviceObject: Update IO while in stop does not work if no boot application is created | Fixed | [[GENERAL]]  
compiler version >= 3.5.19.0 required to change the code  
CDS-82088 | Bug | Attribute 'instance-path' does not work | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-82087 | Bug | Monitoring / Tracing from values of libraries isn't possible | Fixed |   
CDS-82085 | Improvement | DeviceObject: Copy/Paste of multiple IO modules in slots should be possible | Fixed |   
CDS-82083 | Bug | Compiler: GoToInstance not working properly on FB instance below interface variable | Fixed |   
CDS-82082 | Bug | DeviceEditor: The size of an editor does not auto-adjust when the window size gets reduced | Fixed |   
CDS-82078 | Improvement | CODESYS: Check new runtime-passwords against given PasswordPolicy | Fixed |   
CDS-82076 | Improvement | Support of 'covariant return types' | Won't Fix | [[GENERAL]]  
Implementing this issue is a very complex undertaking with a high risk of regressions, while a simple workaround is available.  
CDS-82075 | Bug | VxWorks: Fix SysEthernetLLWrite | Fixed |   
CDS-82074 | Improvement | Library: DisplayPlaceholdersDialog Methode in ILibraryUIServices4 | Fixed | [[GENERAL]]  
New interface ILibraryUIServices4 with method void DisplayPlaceholdersDialog(IWin32Window, IPlaceholderDialogConsumer)  
CDS-82073 | Bug | DeviceObject: Compile error after drag and drop of slot modules | Fixed |   
CDS-82061 | Bug | Device Object, Refactoring: Renaming a specific Chinese variable in IO Mapping results in wrong name | Fixed |   
CDS-82059 | Bug | Compiler: warning C0542 cannot be disabled using pragmas | Fixed | [[GENERAL]]  
Pragmas are not possible for objects like variable or POU declarations.  
Therefore with compilerversion >= 3.5.19.0  
there is a new attribute 'suppress_warning'. The value of the attribute contains a comma seperated list of the warning ids (the plain numerical value) to be disabled for the following POU declaration.  
CDS-82055 | Improvement | CODESYS / DeviceUserManagement: Configure delay, if a user tries to login with wrong user name or password | Fixed | see spec.  
CDS-82043 | Improvement | CODESYS Control: Enforce password strength: F1.4: Unit tests | Fixed |   
CDS-82042 | Improvement | CODESYS Control: Enforce password strength: F1.4: Implementation | Fixed |   
CDS-82041 | Bug | Compiler: NullReferenceException is thrown(only in debugger) if Initializer is used on FB without FB_Init | Fixed |   
CDS-82040 | Bug | Browse Commands: "Go to definition" does not work in online mode | Fixed |   
CDS-82038 | Bug | DeviceObject: empty warning if IoConfigLateInit is set and english language | Fixed |   
CDS-82034 | Bug | Compiler: Exception after adding the library CmpIecTask | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
Report a better error message for this project  
CDS-82010 | Bug | Monitoring: Indexing POINTER TO ARRAY of ARRAY | Fixed |   
CDS-82003 | Bug | DeviceObject: missing devices for update in project environment window | Fixed |   
CDS-81994 | Bug | Compiler: After unticking "Exclude from build", a Clean All is required, before the errors of a POU are shown in Build | Fixed |   
CDS-81985 | Bug | LibMan: List items and scrollbar control element not fully displayed | Fixed |   
CDS-81984 | Bug | Deviceobject: IO-Mapping of enumeration is lost if no default value is set | Fixed |   
CDS-81978 | Bug | Delivery SP18 and newer with define RTS_ENABLE_PROFILING fails | Fixed |   
CDS-81966 | Improvement | [Setup] Update CAS Connector to 1.25.0 | Fixed |   
CDS-81959 | Bug | LibMan: Changed library parameters are ignored if same library is also present in the pool libman | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-81958 | Bug | [MessageServiceWithKeys] MultipleChoicePrompt uses wrong parameter as message key | Fixed |   
CDS-81912 | Epic | Online Change Improvement Bundle | Fixed |   
CDS-81908 | Bug | Online Change: A constant default initialized POU is not updated if the default value is changed in the POU | Fixed | [[GENERAL]]  
The project has many issues that are problematic. First: a function block instance should not be declared as constant. Second: if an instance is declared as CONST, it should get an initial value and it should not be default initialized.   
Third: array borders should never be declared with not replaced constants.  
In the project reported, we have the following situation:  
  
dutt : ARRAY[GVL.xx.x..GVL.xx.y] OF DINT;  
  
VAR_GLOBAL CONSTANT  
xx: DUT;  
END_VAR  
  
TYPE DUT :  
STRUCT  
x : DINT := 0;  
y : DINT := 29;  
END_STRUCT  
END_TYPE  
  
If the Initial value in the DUT changes, the instance of the DUT will not be initialized again: the default initial value in the Type will change, the initial value in DUT will remain the same until the next reset. This is also true for a constant value.  
A constant value should always be initialized, if this initial value changes, the constant will be newly initialized at online change. CODESYS generates a warning for this case that you shouldn't ignore.  
Since initialization can be very complex, in order to guarantee newly initialisation of not replaced constants, we would need to initialize constants always at any online change.  
To force initialization of a constant, you can use the attribute  
{attribute 'init_on_onlchange'}. Be careful, you also have to turn off fast-online change (compiler define no_fast_online_change) in this case.  
  
Still: it is very dangerous to use a structure or a function block variable as array borders. Note that a constant function block might be used via pointer or interface, and the values might be changed without noticing. The compiler does not have an issue with the following code:  
  
ptest := ADR(GVL.xx);  
ptest^.x := 88;  
  
So, the behaviour remains unchanged. But in the case that init_on_onlchange is used and fast-online-change is disabled with compile attribute, an assertion during online change occured. We fixed this assertion.  
CDS-81904 | Bug | CDS: CDS in Japanese, the buttons on the UI are hidden | Fixed |   
CDS-81897 | Bug | RTE, CmpLog: LT_TS_BACKEND_LOCALTIME breaks runtime | Duplicate |   
CDS-81890 | Bug | Remove ScriptingEngine from SVN | Fixed |   
CDS-81889 | Improvement | CmpOPCUAProviderIecVarAccess: Return different error code for sampling while online change | Fixed | [[GENERAL]]  
The OPC UA Server will return BadNoCommunication while an onlinechange is running for sampled monitored items. If the item is not valid after the onlinechange BadDataUnavailable will be returned as before.  
CDS-81887 | Bug | CmpHilscherCIFX: Update configuration failed (after multiple Reset Warm) | Fixed |   
CDS-81886 | Bug | VxWorks-x86 result for LTIME() is not increasing if called serveral times in IEC Code | Fixed |   
CDS-81884 | Improvement | [Setup] Update CODESYS Visualization to 4.2.0.0 | Fixed |   
CDS-81877 | Bug | VxWorks-x86-C++ Exception on SysTaskWaitSleep | Duplicate | [[GENERAL]]  
Duplicate of CDS-81167.  
CDS-81864 | Bug | Project Archive: Inspection dialog appears twice | Fixed | [[GENERAL]]  
Show the inspection dialog only once when an projectarchive is opened  
CDS-81849 | Bug | SysFile.IsConfigFile should check absolute path too | Fixed | [[GENERAL]]  
For more details see Advisory 2022-02, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17089&token=cc5041e24fc744a397a6f6e3b78200a40e6fcd53&download=  
CDS-81838 | Bug | Module type CT_OEM_END should end with 0xffff | Fixed |   
CDS-81835 | Bug | Linux: remove dependency to libstdc++ from linux runtimes without targetvisualisation | Fixed |   
CDS-81831 | Bug | SVGRenderer: No longer working on older Windows versions | Fixed |   
CDS-81829 | Bug | Compiler: Goto Definition leads to null reference exception if an FB is in offline mode | Fixed |   
CDS-81828 | Improvement | PLCHandler: Remove or autogenerate Features and Changes_Addressed Defects PLC Handler | Fixed | [[GENERAL]]  
Features and Changes_Addressed Defects PLC Handler_<version>.xlsx is no longer part of the delivery  
CDS-81807 | Bug | DeviceObject: Warning "Device Description missing" is displayed for empty slots | Fixed |   
CDS-81805 | Bug | Refactoring: does not work on Application Name | Fixed |   
CDS-81799 | Bug | Simulation: Stack size setting should be ignored | Won't Fix | [[GENERAL]]  
For consistency reasons the same limitations should apply in simulation mode as with the real plc. It would be confusing for the user if the application is compilable and works in simulation and is not compilable when switching back to the real device.  
CDS-81798 | Bug | Missing translations in japanese UI of InstallerIntegration | Duplicate |   
CDS-81784 | Improvement | VxWorks: Build has problems and doesnt use cubicle | Fixed |   
CDS-81782 | Bug | Compiler: Compile error with x86 when using "TO_BOOL" on a boolean value | Fixed |   
CDS-81776 | Improvement | Setup: Update to .Net Framework 4.8 | Fixed | [[GENERAL]]  
Microsoft .NET Framework 4.8 is required for CODESYS  
CDS-81764 | Improvement | [Setup] Update CODESYS Installer to 1.3.0 | Fixed |   
CDS-81763 | Bug | LMM: External functions from Pool-Library referenced despite not supported by device | Won't Fix | [[GENERAL]]  
The new resolution resolves first according to the device. If the device does not resolve the library the placeholder is then resolved according to the pool.  
This mechanism only works if the device contains an explicit resolution "NotResolved" for not supported libraries.  
An improvement to address this issue is planned with CDS-83534.  
Older device description may miss this entry. In this case the resoltion NotImplementedByDevice can be set directly in the Applications library manager as a workaround.  
CDS-81761 | Bug | RTE, Datasources OPC UA Server, Net Base Services, SysSocket : In RTE, SysSocketGetHostByName always outputs iHostAddrType = 0 | Fixed |   
CDS-81760 | Bug | Optional parameters leads to an exception | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
CDS-81751 | Bug | Performance Problems with large Recipes | Fixed |   
CDS-81750 | Improvement | SysCpuMultiCore: Configuration of TaskGroups: Iterator should start with 0 | Fixed |   
CDS-81735 | Improvement | DeviceUserManagement: Improve error message if a user cannot be added to a group because missing access rights | Fixed |   
CDS-81730 | Bug | Compiler, OnlineChange: Changing the order of outputs in a function/method without return type is not handled correctly | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
CDS-81681 | Bug | Compiler: "Implicit conversion" compiler warning (C0196) missing for converted data type | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
CDS-81671 | Bug | SVN: PLC settings change shows only "Hidden Object change" | Fixed |   
CDS-81668 | Improvement | PackageManagerCLI: Option to provide signature varification data for a list of packages | Fixed |   
CDS-81666 | Bug | Refactoring: New suffix of renaming process is added multiple times to method of an inheriting class | Fixed | [[GENERAL]]  
Investigating this issue revealed that there are two separate issues: One is a redundant renaming of the POU3_Member declaration (fixed by this JIRA) and the other one is the invalid cross reference leading to the problems in the POU2_Independent. The second problem needs to be fixed in the Language Model Manager in the separate issue CDS-82941.  
CDS-81665 | Bug | Compiler: String Online value representation wrong | Fixed |   
CDS-81662 | Bug | Create new library: CBML is missing | Fixed |   
CDS-81661 | Bug | CmpIecTask.IecTaskDelete3: with C++ build async task does not finish operation | Fixed |   
CDS-81657 | Improvement | NBS: Introduce a new UseCase Library for the "new" NBS library | Fixed |   
CDS-81650 | Improvement | Investigate usage of standard toolchains in deliverymanager for ARM / Cortex cpus | Fixed |   
CDS-81649 | Improvement | Compiler: Speed up PrecompileChecks.Disable and display it in Lengthy operation | Fixed |   
CDS-81648 | Improvement | Compiler: Project with many precompile message is laggy | Fixed |   
CDS-81644 | Improvement | DeviceObject: Increase speed of project loading with many StringRefs | Fixed |   
CDS-81643 | Improvement | ProjectCompare: Library placeholder changes are not recognized | Fixed |   
CDS-81642 | Improvement | MemGC: detect double free and add log message | Fixed |   
CDS-81638 | Bug | Precompile: C0222 shown while library development, not after 'Check all Pool Objects' | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-81635 | Bug | Redundancy: Synchronizing online write commands for Bits fail on PPC systems | Fixed |   
CDS-81629 | Bug | Library Manager: Paintbug in German GUI | Fixed |   
CDS-81628 | Bug | Persistent Vars: a changed array causes an error message to appear, but no error is displayed | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-81624 | Bug | CEF: Remote debugging enabled in chromium embedded framework | Won't Fix | [[GENERAL]]  
As CEF was removed from CODESYS (and has been replaced by Microsoft's WebView2) there is no more any need for this issue.  
CDS-81585 | Bug | IntelliSense: IntelliSense for fluent code/chained methods no longer working | Fixed |   
CDS-81583 | Bug | IEC-TextEditor: Errors are only underlined the first time an application is compiled | Fixed |   
CDS-81577 | Bug | OnlineExpressionInterpreter: Problems when evaluating SEL expression | Fixed |   
CDS-81574 | Improvement | NBS: Load certificate while start the application | Fixed |   
CDS-81573 | Improvement | DeviceObject: import/export mapping as csv file should use list separator from region setting | Fixed |   
CDS-81572 | Improvement | Linux QS builds/targets: improve integration with vscode for build and debugging | Fixed |   
CDS-81568 | Improvement | Symbol configuration: Button/option to delete all no longer existing variables from the symbol configuration | Won't Fix | [[GENERAL]]  
New improvements for the old Symbol Configuration will not be implemented anymore. The new Symbol Configuration (added below the Communication Manager) has a new workflow and checks which solve this issue already.  
CDS-81566 | Improvement | Symbol configuration: Opening a "no longer existing" variable error should jump directly to the entry in the Symbol configuration | Won't Fix | [[GENERAL]]  
This will not be fixed for the legacy symbol configuration anymore. The new editor as part of the communication manager already supports this.  
CDS-81564 | Bug | License Manager (SoftContainer) : Necessity of manual ‘refresh’ after first license is installed | Fixed | [[GENERAL]]  
  
Automatically load licenses and remain on selected container after a refresh  
CDS-81556 | Bug | Tooltip for VAR_IN_OUT wrong | Duplicate | [[GENERAL]]  
Compilerversion 3.5.19.0  
Duplicates CDS-79272  
CDS-81549 | Bug | DeviceObject: PLCopenXML slot device imported to wrong place | Fixed |   
CDS-81548 | Bug | Compiler: Monitoring Range can become unusable with large arrays | Fixed | [[GENERAL]]  
The monitoring range for arrays exceeding a given threshold of elements (by default 20000 elements, see CDS-34538) can be only entered manually.  
In this case the trackbars are not available and a hint is displayed in the presentation layer, why these controls are disabled.  
This approach is used, because in case of very large arrays only an inexact mapping of trackbar positions to array indices exists.  
CDS-81541 | Bug | Omitted cycle watchdog blocks task watchdog | Won't Fix | [[GENERAL]]  
With the first watchdog, the start/stop process begins and no further task watchdogs are checked.  
If the task with the endless loop has IOs, the IOs are set to default after 10s. If not, the task will be interrupted after 25s.  
This is explained in detail in the runtime documentation (see chapter /Architecture Manual/Overview of the Kernel Components and Main Functions/Application Handling/RUN-STOP transition).  
=>as designed  
CDS-81535 | Bug | Setup: Check for WebView2 Runtime Kit does handle installation in user mode | Fixed |   
CDS-81524 | Improvement | DeviceUserManagement: GB40050: Support configuration of password expiration update cycle | Fixed |   
CDS-81520 | Bug | Flow control not working for POUs | Cannot Reproduce | [[GENERAL]]  
With SP 19, Flow Control is fast enough. A crash on the occured, though. For this problem a new issue was created: CDS-83411.  
CDS-81515 | Improvement | CEF: Update CEFSharp to latest version 104.4.180 | Fixed |   
CDS-81506 | Bug | CODESYS Control SysFile system file access vulnerability | Fixed | [[COMPATIBILITY_INFORMATION]]  
With the activation of ForceIecFilePath the file access from IEC is now restricted to the configured paths only (file sandbox)!  
  
[SysFile]  
ForceIecFilePath=1 (new default)  
  
The standard path is the current directory, the PlcLogic subfolder or a configured path. Every file access outside of this path is configured via PlaceholderFilePath, for example access to temporary files or removable media:  
  
[SysFile]  
PlaceholderFilePath.1=/tmp, $TMP$  
PlaceholderFilePath.2=/media/usb, $USB$  
PlaceholderFilePath.2.Volatile=1  
  
For more information see our tutorial FilePath & Placeholders.  
  
To restore the old behavior ForceIecFilePath may be configured as follows:  
  
[SysFile]  
ForceIecFilePath=0  
  
BUT WE HIGHLY RECOMMEND TO LEAVE THIS SETTING AT ITS NEW DEFAULT VALUE!  
  
[[GENERAL]]  
For more details see Advisory 2023-01, which is available on the CODESYS website:  
https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17553&token=cf49757d232ea8021f0c0dd6c65e71ea5942b12d&download=  
CDS-81504 | Improvement | Compiler: Avoid standard code+data areas for online change, if target wants separate areas | Fixed | [[GENERAL]]  
Online change typically takes place in the areas that were allocated during download. If the areas are not sufficient, an additional area could be allocated. This additional area is then allocated for code, data and constant data.  
  
A new Targetsetting memory-layout\\\single-online-change-area is required in order to allocate the data in separate areas. The default is "true", in this case online change behaves in the same way as ever. One single area is allocated in the case that there is not enough data or code in the existing areas.  
When this setting is false, areas for data, code and constant data are allocated according to the settings in the memory-layout. E.g: if code and constant data are in a single area, then also for online change one area for code and constants and one area for data will be allocated.  
Note that an additional data area could be allocated even if only a new area for code is required.  
CDS-81503 | Bug | Compiler: Method without Return value is accepted within assignment. | Won't Fix | [[GENERAL]]  
It is the desired behaviour that a function/method without explicit return value, returns the first output. Making this an error might break a lot of programs.  
CDS-81493 | Bug | Wrongful precompile error C0072 with ADR of method | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-81491 | Bug | Compiler, C0543: source position of the message is no longer opened | Duplicate | [GENERAL]]  
Duplicates CDS-82296  
CDS-81488 | Bug | SysSock/SysSock2: Wrong documentation of the iWidth parameter of the functions SysSockSelect and SysSock2Select | Won't Fix | [[GENERAL]]  
Won't fix, since there is at least one Platform implementation (namely LWIP) that evaluates the iWidth parameter.  
CDS-81486 | Bug | SysTaskLinux: dont use hTask handle after invalidation in SysTaskExit | Fixed |   
CDS-81483 | Improvement | VxWorks: SysEthernet - sendethframe: improve performance sending messages | Fixed |   
CDS-81482 | Improvement | VxWorks: SysEthernet - improve performance of receiving ethernet frames | Won't Fix | [[GENERAL]]  
The proposed change has no measurable effect on the duration of the call to SysEthernetEthFrameReceive(), regardless of the length of the received Ethernet frame.  
The time improvement here is less than one µs  
  
\--> Wont fix  
CDS-81481 | Bug | VxWorks: openethernet fails to open last Ethernet adapter | Fixed |   
CDS-81480 | Bug | ST: Internal Line IDs are not kept leading to unwanted changes in custom OEM editor | Won't Fix | [[GENERAL]]  
There is no need to change anything because the problem can easily be fixed by in the OEM code by using the newly introduced initialization method. See attached mail for more information.  
CDS-81476 | Bug | DeviceObject: wrong task mapping with BOOL datatypes and always update variables | Fixed |   
CDS-81474 | Bug | Visu, HMI-Redundancy: Not working in SP18 environment | Fixed |   
CDS-81461 | Bug | Deviceobject: EDS Export in CANopen Local Device is not working after update from old config version to new version | Fixed |   
CDS-81457 | Bug | Monitoring: Precision of floating point decimals rounded in Watch window | Fixed | [[GENERAL]]  
There are two different settings. One for the ST editor (option) and one for monitoring (project settings). With the same value for the setting "Number of displayed digits" both times will now output the same.  
CDS-81455 | Bug | Incremental Compile: Change of initialization of Function block is not detected in some cases | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
CDS-81449 | Bug | Compiler: It's not possible to define -1 in hexadecimal. | Won't Fix | [[GENERAL]]  
The compiler correctly produces an error message for a constant definition SINT#16#FF  
16#FF is just a different notation for 255.  
255 is not in the range of SINT.   
Allowed is this   
si := TO_SINT(16#FF)  
And this  
si := -16#1;  
CDS-81445 | Bug | CODESYSControl: Possible very rare crash in CmpPlcShell component | Fixed |   
CDS-81444 | Bug | CODESYSControl: Denial of Service via CmpDevice component | Fixed | [[GENERAL]]  
For more details see Advisory 2022-16, which is available on the CODESYS website:  
https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17351&token=a7c02b2825fea2bcaf80c1a8e62097d72ec90f1a&download=  
CDS-81443 | Bug | NetVars: Monitoring of the implicit variables does not work anymore | Fixed |   
CDS-81440 | Bug | Placeholder Redirection is not set correctly by RequiredLib in Devdesc | Fixed |   
CDS-81436 | Improvement | DeviceObject: Improve behavior for symbolic access and update all variables | Fixed | [[GENERAL]]  
Compiler version >= 3.5.19.0 required  
CDS-81432 | Bug | Library CAA FB Factory: Link to example project archive does not work | Fixed | [[GENERAL]] External links are not allowed anymore, since project is included in library anyway the library documentation was updated.  
CDS-81431 | Bug | Required add-on(s): CODESYS Code Generator PowerPC is not suggested | Fixed | [[GENERAL]]  
CODESYS Code Generator PowerPC and CODESYS Code Generator ARM will be prompted accordingly.  
CDS-81428 | Improvement | Scripting: Allow configuring Profinet topology | Won't Fix | [[GENERAL]]  
Not necessary, can be solved with existing features (also see comment).  
Future develpment (graphical Topology-Editor) will make it obsolete anyway.  
CDS-81410 | Bug | DeviceObject: Plc Xml import will not import slot devices in a special case | Fixed |   
CDS-81406 | Bug | Compile errors when switching compiler version | Cannot Reproduce | [[GENERAL]]  
This problem is not reproducible with V3.5 SP19, because it has been fixed with CDS-79950 for V3.5 SP17 Patch3 HF1  
CDS-81405 | Bug | Remove LMDownloadedApplicationService dependency from the plug-in ProjectLanguageModelProvider | Fixed |   
CDS-81401 | Bug | CmpUserDBEmbedded.c: Remaining Tasks from RTSV-850 | Fixed |   
CDS-81399 | Bug | [Technical Dept] Fix Code Complexity issues in PLCopenXML | Fixed |   
CDS-81391 | Improvement | SysEthernet: hAdapter should be added to events to filter per adapter | Fixed |   
CDS-81388 | Improvement | UDP Library: Use recvmsg | Fixed |   
CDS-81386 | Bug | ITF not recognized as POU in attribute pou:<interface_name> | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-81382 | Bug | DeviceObject: wrong taskmapping for BOOL datatype | Fixed |   
CDS-81380 | Bug | LMM: AfterCompileEvent produces sometimes a wrong argument ErrorsOccured | Fixed | [[GENERAL]]  
The AfterCompile-Event ist mainly used for codeinstrumentation. The code is then typified, the set of POUs to compile is fix.  
Before SP17, the checks were also done in this phase. For SP17 we restructured the compile phases, in order to increase the performance. Now the checks are done in a later phase and in parallel.  
Therefore the list of messages in the AfterCompile-Event will no longer include the error messages that are generated in a later phase. However, you should still check for errors, if you use the event for code instrumentation. Only if no errors occured during the compile, the next compiler phase will take place.  
However, since the AfterGenerateCode-Event is only triggered for successfull compilation, there is no way to get an event for unsuccessfull compilation. Therefere we now introduced a new event "ILMCompileService3.AfterUnsuccessfullGenerateCode" which is triggered when errors occured during code generation.  
CDS-81377 | Improvement | CmpCodeMeter: Setting needed to deactivate creation of initial softcontainer | Fixed |   
CDS-81376 | Improvement | Online Manager: Support of UTF-8 passwords | Fixed | [[COMPATIBILITY_INFORMATION]]  
If you have only used standard ASCII characters in your passwords in the device user management (a..z, A..Z, 0..9, special characters like: !#$&( )*-+,%[ ]/_'^{ }~|") , nothing changes.   
  
In case you have used non standard ASCII character in your passwords in the device user management (German umlauts, Chinese characters, etc.), please consider this compatibility information.  
  
In the past CODESYS used a slightly different encoding for the passwords than other clients (e.g. DataSources, PLCHandler). This has now been adapted in CODESYS to the other clients so that one account (user/password combination) can be used across all clients. The newly used UTF-8 encoding for passwords in transmission is only enabled for devices with runtime version 3.5.18.30 or newer.  
  
So if you have set a password in a device with runtime version V3.5.18.30 or later with a CODESYS version prior to V3.5.18.30, users who have non-standard ASCII characters in their passwords will not be able to log in with CODESYS V3.5.18.30 or later using their password. The same is true if you download old user management files ("dum2") with non-standard ASCII characters in the passwords to a new device.  
  
If you have used non-standard ASCII characters in your passwords, you have to reset the device user management like this:  
\- Use CODESYS <3.5.18.30  
\- Do a reset origin device with deleting the users and groups  
\- Use CODESYS >=3.5.18.30 to create newly your user management and configure the passwords   
  
Alternatively, with a CODESYS version prior to V3.5.18.30, you can change the passwords to use only standard ASCII characters.  
CDS-81367 | Bug | Project Compare: Sporadic message when comparing projects due to Auto Save | Fixed | [[GENERAL]]  
The fix introduces a message box that can be disabled by the user so that it does not show up again for the current CODESYS session.  
CDS-81366 | Bug | "Assertion Failed" message appears with customer project | Fixed | [[GENERAL]]  
Add new messages to report if a compile context can not be loaded.  
CDS-81359 | Bug | TO_INT does not work | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.19.0  
CDS-81358 | Bug | InputAssistant: unhandled exception appears if we press cancel | Fixed |   
CDS-81357 | Improvement | DeviceEditor: improve performance for tab change | Fixed |   
CDS-81340 | Bug | DeliveryManager: linux build: default optimization level collides with environment setups of yocto toolchains | Fixed |   
CDS-81339 | Bug | CmpIecTask.c : After PLC 'reset origin' watchdog is thrown because of Time slice error | Duplicate |   
CDS-81331 | Bug | Compiler: Changes of attributes at pou are not considered during download | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-81325 | Improvement | IO-Mapping: Double Input Mappings - Inconsistent Update Behaviour | Fixed | [[GENERAL]]  
Compiler version >= 3.5.19.0 is required to show the new warning for inputs  
CDS-81319 | Improvement | Linux x86_64: implement function "set next statement" | Fixed | [[General]]  
Linux x64 runtimes now support "set next statement" debug action.  
CDS-81316 | Bug | Internal compiler error when assigning a function_block to an interface inside a condition | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
CDS-81311 | Improvement | NBS: Update UseCase Library to the "new" NBS library | Won't Fix | [[GENERAL]]  
It is not allowed to change a library in an incompatible way  
CDS-81289 | Improvement | PLCHandler: Protect V2 PLC password on transport | Fixed |   
CDS-81285 | Bug | TaskConfig: NullReference Exception | Fixed |   
CDS-81284 | Bug | QNX 7 / CodeMeterEmbedded : posix adaption w_dirent_3s.c does not work correctly for QNX7 | Fixed |   
CDS-81279 | Improvement | PackageManagerCLI: Allow package installation into essentials and additional folders | Fixed | [[GENERAL]]  
PackageManagerCLI provides a new option "applyToAdditionalFolder" which applies all profile changes the to given list of additional folder. Accepted additional folders are:  
\- "All": operation will be applied to all additional folders within <RootFolder>\AdditionalFolders  
\- "<Name>": operation will be applied to the additonal folder within <RootFolder>\AdditionalFolders\<Name>  
\- "<Name1>,<Name2>,<NameN>": operation will be applied to the additonal folders given by a comma seperated list  
\- "<Full qualified path to the additional folder>": operation will be applied to the additonal folder with the given path  
  
For uninstallation the "applyToAdditionalFolder" has to be set accordingly.  
CDS-81278 | Improvement | CAA NetBaseServices: Possibility to bind TCP_Client to a specific interface. | Fixed |   
CDS-81277 | Improvement | CmpAppItf: APPVALUE_STRING_RETAIN_TYPE_DEFAULT should be overloadable during compile time | Fixed |   
CDS-81276 | Bug | DM: Documentation missing for Runtime Toolkit deliveries | Cannot Reproduce | [[GENERAL]]  
When delivering a runtime toolkit, the "Documents" version has to be specified, otherwise, the documentation is not contained in the delivery.  
Usually, this version is preselected if it is available in the same version as the selected runtime version. But this is not the case for hotfixes.  
So if a "Documents" version is selected, the documentation is contained in the delivery as expected.  
=> Cannot Reproduce.  
CDS-81244 | Bug | AutoDeclare: Unhandled exception appears in the customer project | Fixed |   
CDS-81242 | Bug | Fast Online Change: No Fast Online Change after call of new function | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-81241 | Bug | FOSS license info is showing redundant information | Fixed |   
CDS-81240 | Improvement | LMM: Message output events should provide contextual information | Fixed | [[GENERAL]]  
Starting with compilerversion 3.5.19.0 the event handler  
ILMCompileService.BeforeMessageOutput and ILMCompileService.AfterMessageOutput pass instances of MessageOutputEventArgs2, containing also the guid of the application that is currently compiled.  
The event handler ILMCompileService.FilterMessageOutput pass an instance of FilterMessageOutputEventArgs2, that also contains the application guid.  
CDS-81234 | Improvement | InstallerIntegration: OEM should be able to define an absolute path to their custom installer | Fixed | [[GENERAL]]  
Implemented an OEM Customization hook to overload the path to the installer.  
Section: InstallerIntegration  
Key: InstallerLocation  
Value: string - Folder of the OEM Installer  
CDS-81233 | Bug | PackageManager: Migration to additionalfolder considers hotfix packages | Fixed | [[GENERAL]]  
Hotfix packages will not be migrated any more.  
CDS-81223 | Bug | Project Compare: Modification possible, which should be prevented | Fixed | [[GENERAL]]  
Please note that due to CDS-31985, the error popups will only be displayed once per project transaction. This is "as designed" and matches the behaviour in the project diff view.  
Therefore, there will be no error popup in the step #6 of the "Steps to Repeat". But the modification is not possible anymore.  
CDS-81221 | Bug | Project Compare: Cursor position lost while committing changes | Fixed |   
CDS-81220 | Bug | Precompile: error when using non-initialized enum values as dimension for array type used at VAR_IN_OUT | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-81206 | Epic | Library Manager: Improvement Bundle | Fixed | [[GENERAL]]  
Usage of library parameters was deprecated with SP15 and could only be used for existing libraries. From SP19 onwards it is a supported feature again. For this the usage and configuration in an applications is redesigned. A centralized editor allows to change all parameters for referenced libraries in one location. The adding of the library parameter object to libraries has also been reenabled. The usage in libraries has not changed compared to previous versions.  
CDS-81202 | Bug | Flow Control: Deadlock possible | Fixed |   
CDS-81196 | Bug | CmpIecTask: Exception if you use CmpIecTask.IecTaskCreate with compiler version 3.5.17.3 | Fixed | [[GENERAL]]  
[[GENERAL]]  
Functions that are supposed to be called from the runtime System, should get the flag "Enable System call" in the build parameters.  
However, if a function pointer is retrieved in the code with ADR(fun), the compiler sets automatically this flag.  
This did no longer work for assignments in initial values.  
With Compilerversion 3.5.19.0 the automatism works again.  
CDS-81195 | Improvement | LMM, LMUtils, LibManObject: Fix S3949 violations | Fixed |   
CDS-81194 | Improvement | ControlWin Setup 32bit: SysDrv3S should be installed in the appropriate version for windows | Fixed |   
CDS-81189 | Improvement | [Setup] Update CODESYS Installer to 1.2.1 | Fixed |   
CDS-81188 | Bug | SymbolConfiguration: Sporadically, the "SymbolAccessRight" service is sent from a timer before the IOnlineDevice is fully logged in | Fixed |   
CDS-81177 | Bug | Persistent variables are changed on reset warm with special target settings | Won't Fix | [[GENERAL]]  
The device description contains a codegenerator target setting "do-persistent-code" with false. That means, that the compiler ignores persistent variables and doesn't generate any code to handle those. The setting is used by OEM-customers who have their own management of persistent variables.  
CDS-81175 | Bug | CmpUserDBEmbedded: error in UserObjectsDBGetFather | Fixed |   
CDS-81172 | Bug | DeviceObject: Insert fieldbus devices may create Internal error .... Object reference not set to... | Fixed |   
CDS-81171 | Bug | Internal error with method interface (of FB or PRG) | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce with compiler version 3.5.19.0  
CDS-81167 | Bug | VxWorks C++: Online change test project leads to InvalidOpCode exception | Fixed |   
CDS-81166 | Bug | Diagnose, Login: Encrypted Communication Error does not provide helpful information for the user to fix the problem | Fixed | [[GENERAL]]  
This fix only changes the text of the error message and gives a hint to the user how to fix the problem. The hint relies on functionality of the package "CODESYS Security Agent" that is installed with the regular setup of CODESYS SP18.  
CDS-81157 | Bug | Util library: STATISTICS_INT returns average+1 for negative numbers | Fixed |   
CDS-81149 | Bug | Internal Error: NullreferenceException with specific customer project | Cannot Reproduce | [[GENERAL]]  
Starting from 3.5.17.3 the issue cannot be reproduced. There is a error message that "HMI_PRG" cannot be found. This is correct since it is excluded from build. Removing the "exclude from build"-flag from the "Visualizations"-Folder fixes the issue and the project compiles without error.  
CDS-81143 | Bug | Library Repository: Removing location leads to endless loop | Fixed |   
CDS-81133 | Bug | Open a project without access to internet takes a few minutes | Fixed | [[GENERAL]]  
As soon as a certificate of a library cannot be verified because of a missing internet connection all further certificates will not be checked. The corresponding libraries will be treated as unsigned with the reason "CRL cannot be checked because of missing internet access".  
This behaviour is kept until CODESYS is restarted.  
CDS-81132 | Bug | Task Object: Double-click on POU below IEC task to pop up window for a moment | Fixed |   
CDS-81125 | Bug | TransitionObject: unexpected error messages for comment with semicolon | Fixed |   
CDS-81121 | Bug | Installation of Codesys on a system with many users can takes hours | Fixed | [[GENERAL]]  
Configruation items will only be appeared for existing users which already had started CODESYS.  
CDS-81111 | Bug | Compile, Online Change: No call of reinit if a function block in a complex declaration situation | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
CDS-81097 | Improvement | DeviceObject should implement IObjectNameConflictChecker | Fixed |   
CDS-81088 | Bug | Online Change: if you change the array size of an interface, online change overwrites arrays even if they are not used | Fixed |   
CDS-81082 | Bug | Library Manager: Project compare shows differences with library parameters | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP19  
CDS-81074 | Bug | SysTimeRtc / SysTimeRtcVxWorks : SysTimeRtcConvertHighResToLocal( ) problems with TIMEZONE env variable set | Fixed |   
CDS-81069 | Improvement | NBS: Introduce UDP_Peer.Receive2 | Fixed |   
CDS-81056 | Bug | DeviceObject: startSlotNumber and SlotName does not work for explicit connectors and slots | Fixed |   
CDS-81053 | Improvement | CM: Cleanup Imports of Dep.m4 | Fixed |   
CDS-81051 | Bug | CmpXMLParser / expat: Update to most recent version 2.4.9 | Fixed |   
CDS-81042 | Bug | Compiler: Internal errors appear when FB extends an Alias of type STRING | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce with compilerversion 3.5.19.0.  
Compilerversion 3.5.19.0 reports the following error:  
C0090: No definition found for base class 'MyAlias'  
CDS-81037 | Bug | RUN/STOP transition: Exception at RUN/STOP with background job task from IEC | Won't Fix | [[GENERAL]]  
Reason is a wrong usage of EVT_PrepareStop in linked jiras and so dynamically created async task hangs after STOP and does not run out gracefully!  
CDS-81036 | Bug | CmpUserDBEmbedded.c::UserGroupsDBGetNextUser implementation correction | Fixed |   
CDS-81034 | Bug | OPC DA Server installation deactivates Gateway | Cannot Reproduce | [[GENERAL]]  
The problem could not be reproduced.  
The setups CODESYS, CODESYS 64, CODESYS OPC DA Server, CODESYS Control Win, Control Win 64 and CODESYS Gateway) are installing the Gateway Service per default and overwrite an existing Gateway service.  
You can deactivate the installation of the feature Gateway, if you choose Type "Custom".   
If the Gateway SysTray is not running after an installation, you can start it with the start menu shortcut.  
CDS-81029 | Bug | Redundancy: Deadlock if too many write commands from OPC UA | Fixed |   
CDS-81026 | Bug | Project Permissions: Not enough rights to Remove an Ethernet/IP Scanner | Fixed |   
CDS-81019 | Improvement | [PackageManagement] Optimize plugin handling | Fixed | [[GENERAL]]  
Plugin handling has been optimized to speed up plugin installation. This will reduce the plugin installation time about 20%.  
CDS-81013 | Improvement | CmpCodeMeter: Handle number of cached licenses and improve debug logging | Fixed |   
CDS-81003 | Bug | Precompile: C0201 precompile error shown for Array based on GPL constant connected to VAR_IN_OUT of FB | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
CDS-81001 | Improvement | It should not be possible to modify a static adr with command “Find & Replace” | Fixed |   
CDS-80999 | Bug | Compiler: Variable keeps the old initialization value | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-80996 | Improvement | Logging option of ICommand executions in CODESYS | Fixed | [[GENERAL]]  
For diagnostic it is now possible to launch the CODESYS.exe with the command line switch "\--enableEventLog="CommandManager"" to be able to record command executions to the Windows event log. First time using this switch must be done in Admin mode.  
These Messages will appear in the section "AP" then.  
CDS-80995 | Improvement | x64: Compiler Setting needed to prevent Jump optimizations in code generator | Fixed | [[GENERAL]]  
There is a new (undocumentet) attribute 'no_jumpinstruction_optimization'  
CDS-80991 | Bug | SysTask / CmpSchedule / Linux: Exception in external call is not catched cleanly | Fixed |   
CDS-80987 | Improvement | Visu, Targetvisu, NativeControl: Documented example necessary | Fixed |   
CDS-80982 | Bug | LibMan: Library documentation PDF in the library manager doesn't open | Fixed | [[GENERAL]]  
Opening embedded objects of an unsigned library is not allowed due to security concerns (introduced with V3.5 SP17). With CDS-77195 a detailed message is displayed if the user tries to open an embedded object of an unsigned library.  
  
Nevertheless under certain circumstances is was possible to open an embedded object of an unsigned compiled library.  
This issue provides a bugfix for this erroneous behaviour.  
CDS-80974 | Bug | Check all Pool Objects leads to errors because of __MEMCOPY | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-80971 | Bug | Visu, Linux: Problems with display and entering L-Values using properties | Fixed | [[GENERAL]]  
Compiler Version>= 3.5.18.0  
CDS-80970 | Bug | Difference in behaviour with WSTRING definitions | Won't Fix | [[GENERAL]]  
An explicit escape sequence ($R$N) has to be used for this purpose.  
CDS-80965 | Bug | Shadowing Rules: Incompatible change when using same library in both Aplication and Pool Library Manager | Duplicate | [[GENERAL]]  
duplicates CDS-81959  
CDS-80960 | Improvement | Make it possible to remove a connector | Fixed |   
CDS-80942 | Improvement | DeviceRepository: There should be a command to export the selected device | Fixed |   
CDS-80929 | Bug | Compiler: Inappropriate compiler error message for undeclared variable | Fixed | [[GENERAL]]  
Fix compiler exception when a performing an indexaccess to an undeclared variable, in a POU that also contains an access to a variable with a direct address.  
CDS-80927 | Improvement | MessageView: Only load position text if the message provides a position | Fixed |   
CDS-80911 | Improvement | DeviceUserManagement: Possibility to read out the user name by handle | Fixed |   
CDS-80893 | Improvement | OPC UA Server: change message for OPC UA not activated in symbol config | Fixed | [[GENERAL]]  
The two macros RTS_OPCUA_SERVER_BROWSENAME_Missconfigured and RTS_OPCUA_SERVER_VALUE_Missconfigured have been renamed to  
CMPOPCUAPROVIDER_IECVARACCESS_BROWSENAME_Missconfigured  
and   
CMPOPCUAPROVIDER_IECVARACCESS_VALUE_Missconfigured  
  
Both macros can be overloaded.  
CDS-80891 | Improvement | SysFileLinux: SysFileCopy should use sync | Fixed |   
CDS-80883 | Bug | Compiler: Internal error if THIS pointer is assigned to a property of type REFERENCE TO FB | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
CDS-80882 | Bug | Compiler: Compile error at login with online change if a new instance of an FB with additional input parameters in FB_init is declared in another FB | Cannot Reproduce | [[GENERAL]]  
Starting with compilerversion 3.5.18.0 this problem is no longer reproducible  
CDS-80876 | Bug | SysFile Linux: SysFileCopyAsync is successfully copying of files happens despite incorrect entries in "pulOut" or "pulCopied" | Won't Fix | [[GENERAL]]  
Wont fix as we cannot reproduce, identify and fix the behavior.  
With CDS-80816 the implementation is changed from "rts_system" to posix spawn.  
CDS-80875 | Bug | Refactoring: wrong text in Auto Declare dialog | Fixed |   
CDS-80870 | Bug | Scripting: IO-Mapping is not added if you import a Excel-File with a Python-script | Fixed |   
CDS-80868 | Bug | Generic FBs: A breakpoint set in the implementation editor is not hit | Fixed | [[GENERAL]]  
Now there is an error message: Cannot set a breakpoint in the implementation view of a generic function block. Set the breakpoint in an instance of the function block.  
CDS-80867 | Bug | Deliverymanager fails to build Runtimes without feature OPCUA | Fixed |   
CDS-80857 | Bug | SVG-Renderer: Missing license info for indirect dependencies | Cannot Reproduce | [[GENERAL]]  
This issue cannot be reproduced as the according license hints for the mentioned components can be found within GatewayPLC/SourceLicenses/SVG-license.txt  
CDS-80856 | Bug | DeviceObject: Memory consumption increases when adding/removing IO mappings/parameters | Fixed |   
CDS-80821 | Improvement | NetBaseServices: Possibility to bind a client socket. | Fixed |   
CDS-80804 | Bug | Compiler: Internal error instead of correct error is shown in specific case | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-80803 | Bug | Compiler: Comments in interface methods may lead to error when implementing the interface | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce with compilerversion SP19. A new FB is implemented  
without the local variables defined in the interface. This error was fixed with CDS-79056.  
There is also a compile error if local variables are used in interfaces.  
  
[[KNOWN_LIMITATIONS]]  
Comments in interface methods get lost when implementing the interface if the comment cannot be assigned to an object of the language model (e.g. if the comment is located after a variable).  
The functionality to implement the interface must use the language model and cannot use the textual representation of the interface, because when implementing interfaces from compiled libraries no textual representation of the interface is available.  
CDS-80792 | Improvement | Signing of Libraries: allow signing of old libraries | Fixed |   
CDS-80776 | Bug | Compiler: FB_init is not executed as expected if a new FB instance is added in another FB and an online change is performed | Won't Fix | [[GENERAL]]  
The problem is the following. A function block FB1 contains an FB_Init-method in which a member variable shall be initialized. This should be done only once at the first initialization of the function block instance.  
Therefore, the code for initialization of the member is like this:  
  
if (bInCopyCode) then RETURN; end_if  
_i := 100;  
  
Now, since the variable is not specially attributed, the FB_Init first initializes the variable implicitly with its default initialization.  
  
If an instance of this function block FB1 is now added to a function block FB2, then we have the following situation:  
The instance FB2.FB1 is new, the instance FB2 is changed. First FB2.FB1 is initialized with bInCopyCode = FALSE. Then FB2 is initialized with bInCopyCode = TRUE, and the FB2.FB_Init calls FB1.FB_Init with bInCopyCode = TRUE.  
So the member is first initialized correctly then reinitialized with the default initialization and then not copied, because the old instance of FB2 didn't contain a FB1.  
This is a problematic behavior and certainly not as expected.  
The best way to solve this problem would be to generate specialized FB_Init-Methods for each copy code. The main problem with that solution, is that we don't know what effects it would have on existing applications. Applications could rely on the current behavior.  
We therefore just recommend to attribute variables that are initialized explicitly in the FB_INIT-method with {attribute 'no-init'}. Then the user code is responsible for the initialization of the variable.  
Since the behaviour is basically the same since version 3.0 and a workaround exists, we close this issue with Won't Fix.  
CDS-80775 | Improvement | Persistent Variables: Better error message for REFERENCE TO in VAR PERSISTENT RETAIN | Fixed |   
CDS-80757 | Epic | CAA File: Strengthening of the resource management system | Fixed | [[GENERAL]]  
The management of file handles has been enhanced in a way that there are no more processing time anomalies when using function blocks from the CAA_File library.  
CDS-80756 | Bug | Persistent Variables, __XINT-Type: Persistent Variables are initialized too often | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.19.0  
CDS-80744 | Bug | Setting the CommCycleInterval doesn't work on Linux Systems | Cannot Reproduce |   
CDS-80280 | Bug | Persistent Variables, Library Parameters: Library Parameters used in persistent variable lists are handled wrongly | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-80272 | Bug | Persistent Variables: Writing bits of a struct leads to unexpected results | Won't Fix | [[GENERAL]]  
Wont fix: investigations showed the special kind of memory on that device cannot be used in a "direct and random access" way.  
The same assembler instructions that work on normal memory (RAM), do not succeed on this special nvram. See screenshots and examples.  
As the CODESYS codegenerator but also the CODESYS runtime itself cannot distinguish different kind of memory with different behavior (and cannot rely on basic instruction like "move" to work properly), this kind of memory cannot be used directly from the IEC code or runtime (in a random access way). This kind of memory must be handled by a special driver (code), that can handle the specifics in access to that memory.  
We recommend using a buffered / discoupled implementation, where the retains/persistent are handled in RAM (from runtime point of view), and later pushed to NVRAM "en block" in some driver/runtime-adaption code.  
CDS-80271 | Improvement | DeviceEditor: show better description why a io channel is not updated | Fixed |   
CDS-80269 | Bug | CmpOpenSSL: TlsContextCreateDHParameters evaluates the result not correct | Fixed |   
CDS-80265 | Bug | CmpIecTask : On App Download blocking of IecTaskSync Sem sets up customer watchdog | Fixed |   
CDS-80262 | Improvement | SigningCompiledLibs: A signed lib, which certificate is signed by a trusted CA, is displayed as expired | Fixed |   
CDS-80261 | Improvement | RTE: update Realtek 8119i LAN to CODESYS CmpRTL8169Mpd driver: add specific VendorID to driver inf file | Fixed |   
CDS-80260 | Bug | Inputassistant: Deviceinstances are displayed two times | Fixed |   
CDS-80257 | Bug | VxWorks : Bitwise access to PERSISTENT RETAIN fails | Won't Fix | [[GENERAL]]  
Wont fix: investigations showed the special kind of memory on that device cannot be used in a "direct and random access" way.  
The same assembler instructions that work on normal memory (RAM), do not succeed on this special nvram. See screenshots and examples.  
As the CODESYS codegenerator but also the CODESYS runtime itself cannot distinguish different kind of memory with different behavior (and cannot rely on basic instruction like "move" to work properly), this kind of memory cannot be used directly from the IEC code or runtime (in a random access way). This kind of memory must be handled by a special driver (code), that can handle the specifics in access to that memory.  
We recommend using a buffered / discoupled implementation, where the retains/persistent are handled in RAM (from runtime point of view), and later pushed to NVRAM "en block" in some driver/runtime-adaption code.  
CDS-80256 | Bug | Compiler: Method with call_after_init is executed twice for sub class | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-80238 | Bug | Error Dialog but no message when using Input Registers (%QW) in the ST code | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-80230 | Bug | OnlineManager: File transfer service called with scripting in noUI-Mode does not complete | Won't Fix | [[GENERAL]]  
Investigation turned out that the endless loop is directly caused by the OEM code that does not actively wait for a service response but puts the executing main thread to sleep instead.   
  
In the attached screenshots there is a simple fix for the OEM code. This fix follows the preferred way to handle file operations as described in AP_Concepts_OnlineManager.pdf, Section 8.5.  
CDS-80223 | Bug | CDS Crash: Opening the project leads to an crash on Codesys side | Fixed |   
CDS-80222 | Bug | Start Page: Confusing behavior when creating project and closing Codesys with "delete project" | Fixed |   
CDS-80065 | Bug | VAR_CONFIG - Add All Instance Paths can't be used directly | Fixed | [[GENERAL]]  
Executing the command "Add All Instance Paths" automatically triggers a build if necessary.  
CDS-80059 | Bug | License manager: exception appears if device is not found | Fixed |   
CDS-80029 | Bug | CmpOPCUAProviderIecVarAccess: Enum is not transportes as Int32 but as the base type used in IEC. | Fixed |   
CDS-80023 | Bug | AutoDeclare: Unhandled Exception on using Input Assistant | Cannot Reproduce | Cannot reproduce with CODESYS 3.5.19.0 CurDev16  
CDS-80020 | Improvement | Backup and Restore a project via .project + WorkingFolder + SharedDataStorage | Fixed |   
CDS-80019 | Improvement | Update components should be easier | Fixed | [[GENERAL]]  
"Learn more" links now opens the affected installation and automatically opens the "updates" tab.  
  
[[KNOWN_LIMITATIONS]]  
Requires CODESYS Installer version 1.3.0 and later.  
CDS-80018 | Bug | Package Manager: Uninstalling old version removes devices | Fixed | [[GENERAL]]  
Setup uninstallation does not delete shared repository content.  
  
[[COMPATIBILITY_INFORMATION-OEM]]  
OEM Setups need to update their uninstallation procedure. The call the PackageManagerCLI --uninstallAll must be extended by --keepRepositories. Otherwise, the repository entries will be removed.  
CDS-80016 | Improvement | DM: Extend SDK delivery for single licence (encryption) | Duplicate | [[GENERAL]]  
Duplicate of CDS-78671  
CDS-80011 | Improvement | CODESYS Control Linux: remove DEBUGP messages | Fixed |   
CDS-80007 | Bug | CDS Crash: When modifying task definitions in the device tree | Duplicate | [[GENERAL]]  
Duplicate of CDS-74841  
CDS-80006 | Bug | CDS Crash: When edit new tasks in the device tree | Duplicate | [[GENERAL]]  
Duplicates CDS-74841 (TaskConfig: When deleting a task in the navigator, a column in the task configuration editor is accidentally removed)  
CDS-79999 | Bug | Wrong message: Project has been stored with different version message | Fixed |   
CDS-79996 | Bug | Wrong notification about new updates | Fixed | [[GENERAL]]  
Notifications are no longer displayed when one of the updates has been installed  
CDS-79985 | Improvement | DeviceUserManagement: GB40050 / FSA-CR 1.11B: Session lock timeout must be configurable | Duplicate | [[GENERAL]]  
Implemented by CDS-70761.  
CDS-79984 | Improvement | DeviceUserManagement: IEC 62443: FSA-CCSC 1A: Administrator account should not be locked | Duplicate | [[GENERAL]]  
Implemented by CDS-70761.  
CDS-79983 | Improvement | DeviceUserManagement: IEC 62443: FSA-CR 1.11A: unsuccessful login attempt should be configurable | Duplicate | [[GENERAL]]  
Implemented by CDS-70761.  
CDS-79978 | Bug | Access violation at download with long running callback function in CommCycle | Duplicate |   
CDS-79962 | Bug | User Management: adding another user allows only default group "Administrator" | Won't Fix | [[GENERAL]]  
This issue will not be fixed because the described behaviour is exactly as designed and will not be changed. We call this behaviour the "Simple User Management" because it is used by the majority of the users and provides exactly the functionality that is needed: Minimum number of clicks without the risk of breaking something accidentally.  
CDS-79961 | Bug | Breakpoint: IDE freeze if you use breakpoints and step forward | Fixed |   
CDS-79946 | Improvement | Project Load: Consolidate all automatic APIs and events | Fixed | [[GENERAL]]  
New API IProjectUpdateConfigurator for configuring default responses for project update prompts and checks. The defined setting will only take effect for the next single run.  
CDS-79928 | Improvement | Visu, IEC: Provide an event when a client was first painted completely | Fixed |   
CDS-79922 | Improvement | Encrypted Linux Toolkit delivery via Delivery Manager | Duplicate | [[GENERAL]]  
Duplicate of CDS-78671  
CDS-79915 | Improvement | [Technical Debt] LibManObject, Refactor LibraryLoader | Fixed |   
CDS-79907 | Improvement | XML Import: Evaluate included profile information | Fixed | [[GENERAL]]  
Before importing native xml files the content will be check whether all types are available. If so, the missing add-ons will be offered to install.  
CDS-79891 | Bug | App Backup&Restore: Certificates get lost if restore is called by CODESYS | Fixed |   
CDS-79859 | Bug | Project Compare: Differences of more than one line are not displayed correctly | Fixed | [[GENERAL]]  
Unfortunately, the UI control used for the project compare is not able to display multi-line strings. Therefore, the fix for this issue is limited to displaying strings with line feed in a shortened way by replacing the first line feed with "...".   
This fixes the ugly display. For shortened strings, the tooltip will display more information.  
CDS-79855 | Bug | IO Mapping Editor displays only the first 2048 Words in Array | Fixed |   
CDS-79853 | Improvement | License Handling: Improve Handling of several Wibu container | Fixed | [[GENERAL]]  
License Manager UI has been reworked to display all available containers in a single control. Every container displays its licenses.  
During license activation there is an additional drop down list to select a dedicated container. Depending on the given ticket there is a suitable container preselection.  
  
[[KNOWN_LIMITATIONS]]  
Licenses servers will not be listed on default because they may increase loading time significally. The can be actived on demand with the new Licsense Manager's option page.  
CDS-79841 | Bug | parameter lists: Value from pool takes precedence over value from application | Duplicate | [[GENERAL]]  
Duplicate of CDS-81959  
CDS-79837 | Improvement | Monitoring: Make it possible to monitor return values of methods in the online view | Won't Fix | [[GENERAL]]  
Flow control is the preferred solution for this. By using the attribute the methods will be called and executed repeatedly outside of any IEC task cycle. This might cause performance problems or application issues depending on the implemenation of the methods.  
CDS-79835 | Bug | Textual View: Declaration in textual view changed if a new variable is added and removed in tabular view | Won't Fix | [[GENERAL]]  
This issue will not be fixed because it is a feature of the declaration editor to consolidate the sections with the same scope.  
CDS-79810 | Improvement | DeviceUserManagement: More than one admin in user management should be possible | Fixed |   
CDS-79808 | Improvement | BACnet23: CmpBACnet2 - remove InitMidnightTimer | Fixed |   
CDS-79806 | Bug | OptionHandler: LiveOption Handler should become more robust | Fixed |   
CDS-79790 | Bug | External file: Access denied on download even if file is embedded into project | Fixed |   
CDS-79777 | Improvement | Compiler: Improve error message "No matching FB_init method found for instantiation of POU" (C0138) | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-79742 | Bug | Project Information: "Placeholder" field is skipped while using Tab-key | Fixed |   
CDS-79741 | Improvement | PLCopenXML Import: Allow to replace existing objects in case of a name collision | Fixed |   
CDS-79738 | Bug | VxWorks: SysTimeRtc - Wrong TIMEZONE handling | Fixed | [[GENERAL]]  
From SR630, SysTimeRtcConvertUtcToDate() and SysTimeRtcConvertDateToUtc() do not use the TIMEZONE information.  
  
[[KNOWN_LIMITATIONS]]  
As of SR630 and newer, the format of the TIMEZONE environment variable changed.  
This new format is not supported and thus, SysTimeRtcSetTimezone() is deactivated for SR630 and newer.  
  
[[COMPATIBILITY_INFORMATION]]  
Due to incompatible changes of VxWorks from SR630 and newer, SysTimeRtcSetTimezone() is not supported.  
Our internal structure cannot store all information needed, to set the timezone in the new format correctly.  
Changes to this structure are planned with CDS-15880  
CDS-79736 | Improvement | Online Change Details Dialog: Automatically switch to Online Comparsion tab on generate code | Fixed |   
CDS-79602 | Improvement | LibMan: Report corrupt lib repository in message view | Fixed | [[GENERAL]]  
New interface _3S.CoDeSys.LibManObject.IRepositoryConsistencyChecker  
An instance of the implementation can be obtained by IManagedLibraryManager16.GetRepositoryConsistencyChecker()  
CDS-79542 | Bug | SafeNetVars, MappingApp: Internal Error if ReceiverList does not reference any variable | Fixed |   
CDS-79535 | Bug | Unexpected warning about implicit conversion | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-79519 | Improvement | QNX 7.1: Set up test device | Fixed | DevrackSL-QNX71-x64 (see https://confluence.codesys.com/x/mgAIAw) is now available.  
CDS-79449 | Improvement | Installation: Corrupted file should contain detailed error description | Fixed | [[GENERAL]]  
Detailed error descriptions have been added to the file. Furthermore error messages can be appended if the file already exists.  
CDS-79420 | Improvement | [Technical Debt] LibManEditor, Refactor LibManControl | Fixed |   
CDS-79362 | Improvement | FloatingPointUtils: improve performance by using AND_THEN/OR_ELSE | Duplicate | [[GENERAL]]  
Duplicates CDS-41793  
CDS-79349 | Improvement | POU Object Wizard: Adding an FB that EXTENDS a BaseFB should only create methods for not yet implemented Interface methods | Won't Fix | [[GENERAL]]  
Even when methods are implemented in a base POU the user might still want to override them in the extending POU. Sometimes he also might not be aware of methods that might need specialize implementation for his extension. So it is preferred to generate all methods and let the user delete the unneeded ones afterwards.  
CDS-79342 | Bug | CmpOPCUAClient: Crash when monitored items are deleted within the ConnectionCallback with session timeout | Fixed |   
CDS-79293 | Improvement | CAA Mathematics: atan2 generates warning, because reserved by compiler for future versions | Fixed | [[COMPATIBILITY_INFORMATION]] A new function named atan2_func replaces the function atan2. The function atan2 has been marked as obsolete.  
CDS-79272 | Bug | VAR_INOUT in a FB shows wrong hint | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-79270 | Bug | Linux, AccessViolation: Return of very large variables in functions leads to an exception | Fixed | [[GENERAL]]  
The maximal stack size for an IEC task on a Linux system is now limited to 0x20000 according to the default stack size defined in the runtime.  
CDS-79259 | Bug | SysMsgQVxWorks.c : Used timeout calculation can result in zero (no wait) | Fixed | [[GENERAL]]  
SysMsgQRecv for VxWorks now properly calculates the timeout based on systemticks. Possible range for timout is 1s to 1us, but at least one systemtick.  
CDS-79222 | Bug | Task Config Object: "Task Configuration" in Properties incorrectly localized | Fixed | [[GENERAL]]  
The object name of the Task Configuration will now be displayed in a consistent way in the topmost textbox of the properties dialog. This name is the object's BASE NAME and should not be localized. Therefore, it may differ from the localized DISPLAY NAME in the navigator (e.g. "Taskkonfiguration"). This is "as designed".  
CDS-79205 | Bug | CmpBlkDrvTcp: Possible socket blocking DoS vulnerability | Fixed | [[GENERAL]]  
For more details see Advisory 2022-09, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17128&token=bee4d8a57f19be289d623ec90135493b5f9179e3&download=  
CDS-79189 | Bug | RTE: an exception appears when calling SysTimeRtcGetTimezone | Fixed |   
CDS-79144 | Bug | SysDirAsync, tSysDirCreate: Parameter szDir String size limited to 80 characters | Fixed |   
CDS-79101 | Bug | Add support for qualifier INTERNAL for Type Alias of arrays in IEC Libraries | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-79081 | Bug | Compiler: Initialization of multidimensional nested array with FB as type, does not work if declared like 'array of array' | Fixed | [[GENERAL]]  
The syntax for FB_Init parameters for   
ARRAY [0..1] OF ARRAY [0..1] OF FB is now the same as for   
ARRAY[0..1, 0..1] OF FB and for   
ARRAY[0..3] OF FB.  
[(...), (...), (...), (...)]  
CDS-79074 | Improvement | [Technical Debt] LibManEditor, Refactor DocumentationView | Fixed |   
CDS-79058 | Bug | Compiler: Short array initialization does not work with a global constant for arrays of FB or STRUCT | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.19.0  
CDS-78955 | Improvement | CODESYS Control: SysCryptoLinux make it work for non-root users, use "write" instead of "ioctl" | Won't Fix | [[GENERAL]]  
Increasing entropy without being root or having the capability "CAP_SYS_ADMIN" cannot be achived at the moment. The problem comes from the inability to credit the bits written to /dev/random. Therefore the entropy-pool does not increase. For this process the mentioned capability is needed.  
The linux kernel currently implements this at random.c (e.g. https://github.com/torvalds/linux/blob/v5.10/drivers/char/random.c).   
We cannot work around this.  
CDS-78952 | Bug | Profinet GSDML Import: error "object reference not set" reported | Cannot Reproduce | Already fixed with CDS-53210 for V3.5 SP13  
CDS-78844 | Improvement | CmpIecTask: New IEC and API interface function IecTaskDelete3() needed to get status of async operation | Fixed |   
CDS-78830 | Improvement | VxWorks : Year 2038 Problem - step 1: convert to ui32 | Fixed | [[KNOWN_LIMITATIONS]]  
SysTimeRtcVxWorks is using functions like "localtime_r". These functions rely on datatype "time_t". If the system is configured to use "long" as datatype for "time_t" this restricts the timestamps to the year 2038 (problem).   
  
We recommend using _WRS_CONFIG_TIME_T_LONG_LONG for VxWorks systems to avoid the year 2038 problem.  
CDS-78811 | Improvement | Support for GenericTypes in TabularDeclarationEditor | Fixed | [[GENERAL]]  
This improvements corrects the display of "VAR_GENERIC" in the Tabular Declaration Editor. For generic variables, editing functionality is supported except for changing the "Scope" to/from "VAR_GENERIC". The reason for this is, that the declaration block for generic variables has to be topmost (even BEFORE the "implements" keyword) and changing the scope would therefore require variables to be moved up/down in the declaration list (see ProblemOrderOfDeclarationBlock.png). This is not desirable, because the user can easily lose track of her variables.  
CDS-78810 | Bug | NBS, ResolveHostname: "AsyncProperty" does not work after "Reset Warm" or "Reset Cold" | Fixed |   
CDS-78802 | Bug | NBS: UDP_Peer, TCP_Server, TCP_Client repair AsyncProperty | Cannot Reproduce | [[GENERAL]] This issue cannot been reproduced in CODESYS V3.5 SP19, it was fixed during some other issues e.g. CDS-78810  
CDS-78791 | Improvement | BACnet23: CmpBACnet2 - update component to MBS BACnet Stack rev. 23 | Fixed |   
CDS-78790 | Improvement | BACnet: create new CmpBACnet23 component | Fixed |   
CDS-78779 | Epic | Package Manager: Display release notes | Fixed |   
CDS-78766 | Bug | Trace: Unable to start a trace after a PLC reboot, if the trace window is still open in encrypted communication mode. | Cannot Reproduce | [[GENERAL]]  
Neither with V3.5 SP17 nor with V3.5 SP18 this problem is reproducible.  
CDS-78764 | Improvement | [CyberSecurity][Pentest] Weak Password Policy | Duplicate | [[GENERAL]]  
Duplicates CDS-74382  
CDS-78757 | Improvement | Store: Adjust store page to work with the new MS Edge browser | Fixed | [[GENERAL]]   
Username and password is now stored in browser, not in CODESYS anymore.  
CDS-78756 | Improvement | LibMan: Adjust library viewer to work with the new MS Edge browser | Duplicate | [[GENERAL]]  
Duplicates CDS-78755  
CDS-78755 | Improvement | WebBrowserIntegration: Replace referenced Google CEF components by MS Edge components | Fixed |   
CDS-78730 | Bug | CmpEventMgr: Application deletion not synchronized with event-callbacks from background task | Fixed |   
CDS-78671 | Improvement | Runtime Toolkit Linux: New feature for runtime encryption | Fixed | [[KNOWN_LIMITATIONS]]  
Starting the encrypted binary of the x86 runtime will result in an error that is caused by the encryption. Therefore encrypted binaries will not be delivered for now. This only affects x86. Not x86_64, ARM or ARM64.  
CDS-78608 | Bug | Compiler: Internal Error during download | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-78523 | Bug | OPC UA Server: RTS_Server_EventField typdef or delete required | Cannot Reproduce | [[GENERAL]]  
The affected datatype is not available anymore  
CDS-78512 | Bug | Runtime: Possible channel blocking DoS vulnerability | Fixed | [[GENERAL]]  
For more details see Advisory 2022-09, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17128&token=bee4d8a57f19be289d623ec90135493b5f9179e3&download=  
CDS-78505 | Bug | AsyncJobManager: Background tasks started from two tasks do not disable correctly | Fixed |   
CDS-78457 | Bug | DM / Linux: Source Deliveries are missing Makefiles and Objects | Fixed |   
CDS-78297 | Improvement | SysCryptoLinux: Improve logging when running as non-root user | Fixed |   
CDS-78255 | Bug | Variables Configuration - VAR_CONFIG: Does not work as described in the documentation | Duplicate | [[GENERAL]]  
Duplicates CDS-80065  
CDS-78133 | Bug | PackageMgr, Visu, Commands: Lots of empty commands in Customize window | Cannot Reproduce | [[GENERAL]]  
Can not be reproduced any more.  
CDS-78094 | Epic | Diff view for textual objects: add results view (ex. 3-way-merger ST) | Fixed |   
CDS-77915 | Improvement | Switch development system to .NET 4.8 | Fixed | [[GENERAL]]  
Development system now runs on .NET Framework 4.8.  
CDS-77886 | Bug | Compile: CODESYS crashes when calling SUPER^ of a non-existing base fb | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-77778 | Improvement | DM / Buildsystem: enhance profile.h regarding NOTIMPLEMENTED / EXTERNAL interfaces to support AddOns for runtimes | Fixed |   
CDS-77629 | Improvement | Platforms: Cleanup obsolete Runtime Adaptations | Fixed |   
CDS-77603 | Improvement | Update InstallShield to latest version 2022 R1 | Fixed | [[GENERAL]]  
InstallShield 2022 R1 is used to build the setups.  
CDS-77534 | Bug | ANY : Does not work in a library | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.0  
CDS-77505 | Improvement | Request for direct extension of FB (EN/ENO) in FBD | Won't Fix | [[GENERAL]]  
This issue will not be implemented because we think it is not suitable for our regular user base and there is already a OEMCustomizationHook to activate the proposed functionality in an OEM environment.   
  
Key: NWL  
Section: EnableToggleEnEnoCommand  
  
-> Return TRUE to activate the command.  
CDS-77407 | Bug | Compiler: Compile error if a library contains an object with the same name as the library's namespace | Won't Fix | [[GENERAL]]  
With CDS-63808 a new syntax for explicitly accessing a library namespace was introduced with V3.5 SP15. Using this new syntax allows to solve this issue by writing "Test#Test();"  
CDS-77221 | Bug | Reset precompile error works not properly | Won't Fix | [[GENERAL]]  
The editors do not push the new content to the compiler after every change. The logic for updating content tries to optimize timings to improve overall IDE performance.  
CDS-77209 | Bug | PLCopenXML: Exporting FBs with flex arrays results in arrays being re-declared in VAR_INPUT section | Fixed |   
CDS-77100 | Improvement | LibDevSummary: Document for OEMs how to setup their own library and device description download server | Fixed |   
CDS-76991 | Bug | CmpIecTask.IecTaskDelete2 / IecTaskCreate: In case of multiple simultaneous call not all threads are deleted or created | Fixed |   
CDS-76893 | Bug | Compiler, OOP: Incorrect precompile error for METHOD which returns a REFERENCE TO | Duplicate | [[GENERAL]]  
Already fixed with CDS-81638  
CDS-76886 | Bug | Runtime deadlock on reset application | Duplicate | [[GENERAL]] Duplicates CDS-76590  
CDS-76639 | Bug | Precompile Warning for Controllers with long Parameter Values | Fixed | [[GENERAL]]  
Compiler version >= 3.5.19.0 required  
CDS-76638 | Bug | Wrong status color of POU because of other build errors | Won't Fix | [[GENERAL]]  
Behviour is as expected. The state can only be determined reliably after successfully compiling the project. Until then the status of the last successfull compilation is used.  
CDS-76633 | Bug | Unclear compile error after project update | Cannot Reproduce | [[GENERAL]]  
Starting with compilerversion 3.5.18.0 this problem is no longer reproducible  
CDS-76622 | Bug | Double Datatype selection in Library Repostory | Duplicate | [[GENERAL]]  
Duplicates CDS-75589  
CDS-76593 | Bug | IECTextTeditor: Text within attribute value is evaluated and converted to keywords | Fixed |   
CDS-76590 | Bug | AsyncJobManager library kills Taskcycle on the fly | Fixed |   
CDS-76537 | Bug | Input-Assistant starts always with focus on register ‘Categories’ | Fixed |   
CDS-76531 | Bug | Pasting over existing code removes breakpoints on unchanged lines | Won't Fix | [[GENERAL]]  
When editing code matching breakpoints to the new code is a complicated process. Because of this we always choose the safe solution of deleting breakpoints.  
CDS-76518 | Bug | Library manager: The design attributes pin_presentation_order_inputs/outputs are not respected in the input/output and documentation tab | Fixed |   
CDS-76248 | Bug | Sporadic PLC deadlock after processorload watchdog at 100% load | Fixed |   
CDS-76130 | Improvement | PLCopen Export/Import of Dynamic Parameter Types with multiple namespaces | Fixed |   
CDS-76045 | Bug | Dynamic Parameter Types are not loaded as expected | Fixed |   
CDS-75993 | Improvement | UTF8-Strings: Support for Remote-Targetvisu | Duplicate |   
CDS-75990 | Improvement | UTF8-Strings: Support for Targetvisu | Fixed |   
CDS-75974 | Bug | SmartCoding: Namespace automatically added in FBD/LD if ctr+space is used while it is deactivated | Cannot Reproduce | [[GENERAL]]  
This issue is handling only the problem in FBD/LD, other editors are not taken into account because they are in different AddOns.  
CDS-75903 | Bug | OPC UA Server: Not all usages of SysCpuAtomicAdd handle failures correctly | Won't Fix | [[GENERAL]]  
In all cases when this error happened, the cause was a broken implementation of SysCpuCompareAndSwap. The fixes should be made at this place. See: CDS-82810  
CDS-75666 | Improvement | BlkDriverCANServer/Client: Ignore Error Passive | Won't Fix | [[GENERAL]]  
A Blockdriver needs autorecovery. Otherwise service communication will not work after bus error.  
==> Won't Fix  
CDS-75664 | Improvement | BlockDriverCANServer/Client: Possibility to deactivate auto recovery | Won't Fix | [[GENERAL]]  
A Blockdriver needs autorecovery. Otherwise service communication will not work after bus error.  
==> Won't Fix  
CDS-75493 | Bug | Compiler: behaviour for "C0224" inconsistent - Recursive call is not detected | Fixed | [[COMPATIBILITY_INFORMATION-EndUser]]  
Compilerversion >= 3.5.19.0  
Recursive method calls are allowed. The check for recursive calls therefore ends at a method scope. However, if a method calls a recursive program/function, this was not reported until now. For compatibility reasons, in the future all recursive calls will be issued as warnings.  
CDS-75474 | Improvement | CodeMeter: Support of CodeMeter Universal Firm Code in SL Runtimes | Fixed |   
CDS-75290 | Improvement | [Build] Check Timestamp of Signature | Fixed |   
CDS-75224 | Bug | Linux MainLinux.c: add defines to disable rts_system | Duplicate | Duplicate of CDS-80816  
CDS-75223 | Bug | Linux SysProcessLinux: add defines to disable rts_system | Duplicate | Duplicate of CDS-80816  
CDS-75222 | Bug | Linux SysTaskLinux: add defines to disable rts_system | Duplicate | Duplicate of CDS-80816  
CDS-75160 | Improvement | Compiler: Conditional compiling for inheritance | Won't Fix | [[GENERAL]]  
Supporting conditional inheritance and interfaces would impose severe restrictions on all smart coding features (e.g. refactoring, cross references, etc.). Will not be implemented for this reason.  
CDS-75155 | Bug | Targetvisu, Overlay: EGLFS should be supported | Fixed | [[GENERAL]]  
With Linux.KeepMainWindowOpen=1 the application will define the window type with the first target visualization (legacy/overlay) for the remaining time.  
  
A new setting is available in the CODESYSControl.cfg.  
Linux.KeepMainWindowOpenWindowType=0/1  
A value of 0 means legacy, a value of 1 means overlay. The default is 0.  
The default value can be overridden by defining KEEP_MAIN_WINDOW_OPEN_WINDOW_TYPE_DEFAULT  
This setting is only relevant when you have relevant for Linux.KeepMainWindowOpen=1& Linux.KeepMainWindowOpenShowImmediately=1.  
CDS-74700 | Bug | NBS: Recover TCP_Reader, TCP_Processor, TCP_Writer | Fixed |   
CDS-74699 | Bug | NBS: Recover UDP_Receiver, UDP_Processor, UDP_Sender | Fixed |   
CDS-74698 | Improvement | NBS: Recover Documentation and Examples | Fixed |   
CDS-74382 | Improvement | CODESYS: Enforce password strength | Fixed | [[GENERAL]]  
Validation of passwords against given policy is currently done by the runtime only, because an additional pre-check in the CODESYS IDE would have required new interfaces and therefore would not be patchable any more.  
CDS-74381 | Improvement | DeviceUserManagement: Enforce password strength | Fixed |   
CDS-74305 | Improvement | Text Editor: simplify Ctrl+Mousewheel zoom | Duplicate | already fixed with CDS-67209  
CDS-73635 | Bug | OPC UA Server: Server/ServiceLevel is always zero (Maintenance Mode) | Fixed | Tested, Result is OK  
CDS-73389 | Improvement | CanDl - CmpNetXCanDlDrv: Must be separated from the runtime kernel | Fixed |   
CDS-73388 | Improvement | SIECA132API - CmpCANFoxDrv: Must be separated from the runtime kernel | Fixed |   
CDS-73387 | Improvement | vcinpl - CmpIxxatCANDrv: Must be separated from the runtime kernel | Fixed |   
CDS-73386 | Improvement | PCANBasicAPI - CmpPCANBasicDrv: Must be separated from the runtime kernel | Fixed |   
CDS-72988 | Bug | Package Manager: Menu items are not added for all Windows users | Fixed |   
CDS-72903 | Epic | Compile: support byte and word access of bitfields | Fixed | [[KNOWN_LIMITATIONS]]  
The Trace does not support displaying of partial access expressions.  
Not all Visualization elements support partial access expressions.  
CDS-72714 | Improvement | Create example project | Duplicate | [[GENERAL]]  
Example is created with STORE-4419  
CDS-72629 | Improvement | Language Model Provider: Allow to specify order of language model provision for dependencies | Won't Fix | [[GENERAL]]  
Improvement is obsolete after ProjectDB has been discontinued.  
CDS-72615 | Bug | [OnlineManager] COMPACT_DOWNLOAD => complete ApplicationInfo | Won't Fix | [[GENERAL]]  
The CompactDownload does not contain the timestamp of the last application modification, which is available in the normal download format. The reason is, the the boot application would change every time it is created (online/offline boot application).   
The last modification time stamp is set to 0 in the CompactDownload  
CDS-72051 | Bug | CAA NBS , NBS: UDP_Peer TCP_SERVER, does not give an error itfIPAddress := 255.255.255.255 | Fixed |   
CDS-72000 | Improvement | Possibility to delete a user lib profile | Won't Fix | [[GENERAL]]  
Usage of the library profile has been deprecated with V3.5 SP18. Compiler Versions >= V3.5 SP18 do not consider the profile anymore for placeholder resolutions.  
CDS-71564 | Improvement | Project Information: Library compatibility, improve sorting order | Won't Fix | [[GENERAL]]  
The field has been deprecated since CODESYS V3.5 SP17 and is not displayed anymore.  
CDS-71256 | Bug | LibMan: POU tree not displayed if no precompile context | Won't Fix | [[GENERAL]]  
The primary use case of libraries is to bundle POUs for use in the application. It is not meant to be used only as archive for other files or content.  
CDS-71171 | Bug | Linux SysFileCopy: optionally dont use rts_system | Duplicate | Duplicate of CDS-80816  
CDS-71008 | Improvement | Standard library: New string functions with REFERENCE input types for better performance | Won't Fix | [[GENERAL]]  
Not required anymore with the introduction of the new String Builder library (CDS-61221)  
CDS-70958 | Improvement | LMM: Statusfield for Codestate should be able to compare offline | Fixed |   
CDS-70761 | Improvement | DeviceUserManagement: Add configurable lock, if a user tries to login with wrong password | Fixed |   
CDS-70121 | Improvement | ProjectDB: Merge into trunk | Won't Fix | [[GENERAL]]  
This issue is not needed anymore because the whole project has been cancelled.  
CDS-69811 | Improvement | CmpIecTask: Additional watchdog information for commissioning purposes | Fixed |   
CDS-69694 | Improvement | CmpOpenSSL: Add support for CRL checks | Fixed |   
CDS-69616 | Bug | OPC UA: UA Expert shows different icon if the instance is defined in a GVL | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with CODESYS 3.5.18.30 and Communication 4.2.0.0  
CDS-69502 | Bug | EasyUnit: inconsistent mocks in SVN | Duplicate | Duplicates CDS-82302.  
CDS-69445 | Bug | M4 Export: error exporting VAR_IN_OUT parameters | Fixed |   
CDS-68945 | Improvement | OPC UA Server: Improve certificate validation within the OPC UA Server to pass latest CTT | Fixed | [[GENERAL]]  
The OPC UA Server now supports CRLs when validating client certificates. These checks can be enabled via the corresponding security setting or via the security settings editor:  
[CmpOPCUAServer]  
SECURITY.EnableCRLChecks=YES  
  
Additionally, intermediate CAs can be downloaded into the OPCUAServer/Intermediate folder. These certificates are then used to build up trust chains. The chain has to end within the trusted root CA inside the trusted certificate store.  
CDS-68913 | Bug | IECTextEditor: The inner text document is not thread-save and may lead to a freeze of the IDE | Fixed |   
CDS-68368 | Improvement | SymbolConfig, OPC UA: Avoid shadowing of methods by variables with the same name | Won't Fix | [[GENERAL]]  
Can easily be avoided by adapting the application. Also this issue only affects the legacy symbol configuration and will not be implemented anymore.  
CDS-67272 | Bug | Compiler: Syntactically wrong initialization of ARRAY OF ARRAY not detected | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
The error "C0075: Too many initializers for array" is reported.  
CDS-67209 | Improvement | Editor: A horizontal scrolling with the mouse should be possible | Fixed | [[GENERAL]]  
The changes work fine in the ST editor. Our other graphical IEC editors should also work fine but they need to be rebuild with the SP19 SDK and therefore they will not benefit from this right now.  
CDS-67114 | Improvement | Lib: Reset parameters in parameter list to default | Cannot Reproduce | [[GENERAL]]  
Already implemented with CDS-81371  
CDS-67040 | Improvement | SymbolConfig: Use Checkboxes for view settings | Won't Fix | [[GENERAL]]  
This will not be implemented anymore for the legacy symbol configuration.  
CDS-66991 | Improvement | Application Object: Changes for .Net-Standard Compatibility | Won't Fix | [[GENERAL]]  
Idea to share code between Desktop CODESYS and Go is obsolete.  
CDS-66411 | Bug | LibMan: Exception when inserting specific libraries in POUs | Won't Fix | [[GENERAL]]  
Usage of old compiler versions is discouraged  
CDS-66331 | Bug | LibMan: Libraries that have a CompanyName with '.' at the end cannot be loaded | Duplicate | [[GENERAL]]  
Duplicates CDS-68306 and was fixed with V3.5 SP16  
CDS-66303 | Improvement | Attribute 'obsolete': user defined text for POU with attribute 'obsolete' is only displayed abbreviated in the tooltip | Won't Fix | [[GENERAL]]  
Text in tooltip has to be cut at a certain length to avoid other display issues. The text is displayed completely in the message view though.  
CDS-66174 | Improvement | PLC Logger: Multiselect for filtering Components | Cannot Reproduce | [[GENERAL]]  
Already implemented by CDS-68914, see TestOK.png  
CDS-66172 | Bug | LibMan: the Documentaion tab is not updated correctly. | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-66049 | Bug | Compiler: Error at step over, lines are skipped during step over (F10) | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18 anymore  
CDS-66036 | Improvement | LibMan: New file selection filter "All libraries" in library installation | Duplicate | [[GENERAL]]  
Duplicates CDS-75589  
CDS-65547 | Improvement | Compiler: option to export variable/symbol list | Won't Fix | [[GENERAL]]  
The use case is not described. Because of this it is not clear how the exported list should be structured and what it should contain exactly.  
CDS-65380 | Improvement | BACnet23: IEC-lib-CmpBACnet23 - remove CmpBACnet.GVL_BAC_MEM.g_BACnetExStackMemCollector | Fixed |   
CDS-64852 | Improvement | LibMan: Possibility to display the occurrences of a library within the library hierarchy | Cannot Reproduce | [[GENERAL]]  
No longer reproducible because already implemented with CDS-72341  
CDS-64423 | Bug | LibMan: In customer project the compiler does not resolve included library | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-64382 | Bug | Symbol Rights: Does not work as expected for the group "Administrator" | Won't Fix | [[GENERAL]]  
This is desired behaviour for the special adiministrator group. It always has access to all symbols and ignores any limitations applied.   
This applies not only to the symbol configuration but in general to all features supporting access rights in CODESYS.  
CDS-64199 | Bug | Compiler: Unclear effect of expression RETURN(<Boolean value/variable>) | Cannot Reproduce | [[GENERAL]]  
The RETURN is only executed if the expression is true. So it is a conditional return statement. It's primary use case is to support special return statements in graphical languages.  
CDS-63648 | Improvement | Compiler: ADR & Pointer deref^ in one line | Won't Fix | [[GENERAL]]  
The described use case is very dangerous, write access is limited for good reasons and it should not be possible to override that using any kind of special syntax.  
CDS-63616 | Improvement | BACnet23: CmpBACnet2 - add BACnet[G|S]etDeviceAddressBindingsCacheOptions / BACnet[G|S]etObjectIdNameBindingsCacheOptions bUseGlobalBcastWhoIs | Duplicate |   
CDS-63605 | Bug | Library Manager: Placeholder redirection is changed in combination with container library | Duplicate | [[GENERAL]]  
Duplicates CDS-77030  
CDS-63121 | Bug | CFC, FBD, LD: Auto Declar does not open with old compiler version | Won't Fix | [[GENERAL]]  
Usage of old compiler versions is discouraged since V3.5 SP18 and the modularization of CODESYS.  
CDS-63091 | Improvement | Util.lib: GetSystemTimezone function should be removed | Fixed |   
CDS-62785 | Bug | LibMan: "Object reference not set to an instance of an object" Error occurs when adding a library | Won't Fix | [[GENERAL]]  
Usage of old compiler versions in new CODESYS versions is discouraged as of V3.5 SP18. Beginning with modularization in V3.5 SP17 projects should either be edited with the old version or updated to the new version completely, including the compiler version.  
CDS-62016 | Bug | The use of a variable in function "__NEW" generates the warning "C0195: Implicit conversion...." | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP19  
CDS-61878 | Bug | Compile: Generate warning if library is produced with newer compiler version than used in the project | Cannot Reproduce | [[GENERAL]]  
Signed compiled libraries store the compiler version they were created with and CODESYS checks this when the library is used in a project since V3.5 SP15. If the compiler version used in the project is older than the one the library was created with an compile error is reported early on.  
CDS-61435 | Bug | Symbolconfig: Symbol tree is collapsed when symbol set is changed | Won't Fix | [[GENERAL]]  
Will not be fixed anymore for the legacy symbol configuration  
CDS-61244 | Improvement | Symbolconfig: There should be an overview of all symbolsets | Won't Fix | [[GENERAL]]  
This will not be implemented anymore in the legacy symbol configuration. The symbol configuration has one object for each symbol set and they can be viewed in parallel.  
CDS-60153 | Bug | TaskConfig Editor: Wrong error message: "Invalide core Number." | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-59412 | Improvement | OPC UA and online services: Make use of new user based interface for types | Won't Fix | [[GENERAL]]  
Usermanagement on type description will not be implemented. If this is needed, use the new OPC UA Server publishing editor.  
CDS-59367 | Improvement | NVL, DeviceApplication: allow multiple lists of network variables for different applications on same device | Won't Fix | [[GENERAL]]  
Device application feature has been discontinued.  
CDS-59172 | Bug | Input Assistant: Not all FBs are shown in Input Assistant dialogue | Duplicate | [[GENERAL]]  
Duplicates CDS-62259  
CDS-58791 | Bug | Default setting of the option "Show symbols from system libraries in input assistant" have no effect | Duplicate | [[GENERAL]]  
Duplicates CDS-62259  
CDS-58672 | Bug | LibMan: Message "C0046: Identifier 'COL' not defined" appears when compiling a new project | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP19  
CDS-58507 | Bug | Input Assistent: Own function name is not displayed | Cannot Reproduce | [[GENERAL]]  
Steps to repeat are unclear, the issue cannot be reproduced.  
CDS-58118 | Bug | Compiler: Monitoring of Variable values are only displayed in the declaration part and not in the implementation part | Won't Fix | [[GENERAL]]  
Issue will not be fixed for V3.4 compiler version anymore.  
CDS-58106 | Improvement | BACnet: CmpBACnet - ensure that there is just one of the BACnet-revision-releated instances of CmpBACnet is runing | Duplicate | [[GENERAL]]  
Done creating new CmpBACnet23 CDS-78790.  
CDS-57332 | Bug | SmartCoding: Selections list differs between declaration and coding area | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP19  
CDS-57313 | Improvement | Changing the upper/lower case of a variable should not require an online change | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-57196 | Bug | Compiler: Message "Application is up to date" is missing | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP19 anymore. Rebuild command has been deprecated and is not available anymore.  
CDS-57129 | Bug | OPC UA Server: Subscription handling fails for priorized subscriptions | Duplicate |   
CDS-57040 | Improvement | Symbol configuration: Attribute to propagate global settings needed | Won't Fix | [[GENERAL]]  
The preferred solution is CDS-75368.  
CDS-56632 | Bug | LibMan: Example "RecipeManagement" have unresolved libraries after update the device | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18 anymore  
CDS-56536 | Bug | Add POU: Namespace not inserted for implemented methods in some cases | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-56535 | Bug | Implement Interfaces: The command "Implement Interfaces" will handle some interfaces not properly | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-56471 | Bug | Compile: Use of uninitialized value is not reported, if a variable is used as parameter in FB_INIT | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-56453 | Bug | Compiler: new compiler features lead to undefined behavior in older CompiledLibs | Cannot Reproduce | [[GENERAL]]  
Signed compiled libraries know the compiler version they were created with and can will emit a compile error if an older compiler version is used in the project. This is supported since V3.5 SP15.  
CDS-56173 | Improvement | IecTaskDelete2: Rework usage of JobParams & New interface for status | Duplicate |   
CDS-56159 | Bug | Online Mode: Go to definition should directly open the declaration of the variable | Cannot Reproduce | StR: Ok  
CDS-56109 | Bug | TraceManager: Input assistant inserts wrong object for TraceState | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP19  
CDS-56062 | Improvement | LibMan: multi-selection has an untypical behavior | Duplicate | [[GENERAL]]  
Duplicates CDS-80878  
CDS-55998 | Bug | Messge "C0192: Input 'x' of 'FB_Init' cannot accessed outside of call" should not occur | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP19  
CDS-55891 | Improvement | LibMan: OEM customization hook for providing an opportunity to set a placeholder to the newest version of a library | Won't Fix | [[GENERAL]]  
The use case can be solved by using unbound placeholders in CODESYS. They will refer to the latest library version available when the reference is inserted. Updates are recognized and offered in the Project Environment dialog.  
CDS-55877 | Bug | Compile: unexpected error messages for overloaded FB_Init-Method | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-55782 | Bug | NVL: View the network settings create a compiler message, if we work with several sender lists | Cannot Reproduce | StR: Ok  
CDS-55761 | Bug | Web-based Online Help: page opens with default Language | Cannot Reproduce | [[GENERAL]]StR: Ok  
CDS-55750 | Improvement | SymbolConfig: change of more than one "access-rights" should be possible (multi-selection) | Won't Fix | [[GENERAL]]  
Will not be implemented for the legacy symbol configuration anymore. It is already supported in the new editors as part of the communication manager.  
CDS-55713 | Bug | Compile: call a method differ between CFC and ST | Cannot Reproduce | StR: works great.  
CDS-55499 | Improvement | WSTRING, Standard64.library: WSTRING-Functions should handle surrogate characters | Won't Fix | [[GENERAL]]  
New projects should use UTF-8 encoding and the new StringBuilder library.  
CDS-55494 | Bug | Attribute 'enable_dynamic_creation' leads to assertion failure | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-55466 | Bug | Add Interface Dialog: it is not possible to extends an new interface from "__SYSTEM.IQueryInterface" | Cannot Reproduce | [[GENERAL]] StR: It is possible.  
CDS-55422 | Bug | CallTreeView: Does not work with "REFERENCE TO" | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V 3.5 SP19  
CDS-55326 | Bug | Initialization Dialog: do not show cascaded structures from library | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP19  
CDS-55272 | Bug | FBD: Exception opening a POU written in FBD | Cannot Reproduce | [[GENERAL]] StR: no exception. There is a question mark explaining the problem. Perfect!  
CDS-55269 | Bug | FlowControl: No value for qualified-only variable in some cases | Cannot Reproduce | StR: Ok  
CDS-55139 | Bug | Project environment: When opening a library, newer library versions are not displayed | Cannot Reproduce | [[GENERAL]] StR: Is now correct.  
CDS-55084 | Bug | Task Configuration: Changing existing POU call via manual input assistant call does not update task call in device tree | Cannot Reproduce | StR: Ok  
CDS-55066 | Bug | GVL, ArrayBounds: Tooltip of global variable does not appear when used as array bounds in combination with qualified access | Cannot Reproduce | [[GENERAL]] StR: All tooltips are correct.  
CDS-55040 | Bug | Device Log: Components are listed multiple times | Cannot Reproduce | [[GENERAL]] StR: no duplicates  
CDS-55030 | Bug | Ladder: Expressions are shown without white spaces in Online monitoring | Cannot Reproduce | [[GENERAL]] Spaces are correct with SP 18  
CDS-55012 | Bug | Intellisense: creating of variables with an "point operator" requires correction within the auto-declaration | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP19  
CDS-55007 | Bug | Conditional Breakpoint: If condition uses a string comparison, an assertion fails and BP won't be hit | Cannot Reproduce | [[GENERAL]] StR: Now there is a message "Condition too complex". Could be improved, but not a bug.  
CDS-54986 | Bug | Retain, message view: size of retain is displayed incorrectly | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-54893 | Bug | SmartCoding: SUPER^. does not list methods from a library | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP19  
CDS-54873 | Bug | Package Manager: CODESYS crashes if only an empty text file is in package | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-54613 | Bug | LibMan: Container Library is not resolved for POUs LibMan | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP19  
CDS-54556 | Bug | Generate Code: Using __VARINFO/__SYSTEM.VAR_INFO in library leads to compile error | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP19  
CDS-54554 | Bug | Monitoring: Improve the error message in the watchview for unmonitorable properties | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-54421 | Bug | PlcShell: Deadlock if command is resent in short time intervals | Cannot Reproduce |   
CDS-54394 | Bug | Error: "C0138: No matching FB_init method..." occur if a reference used in interface editor | Cannot Reproduce | [[GENERAL]]  
Compile errors are due to actual syntax errors in the declaration. This is not a specific issue of using references.  
CDS-54259 | Bug | Intellisense: doesn't work on return type of properties | Cannot Reproduce | [[GENERAL]]  
Cannot reproduce with V3.5 SP18  
CDS-54222 | Bug | Editor, Tabular: unhandled exception on changing the Tabular view | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-54198 | Bug | Undo/Redo: it isn't possible to restore the initual situation in the device tree | Cannot Reproduce | StR: Ok  
All 3 examples are working.   
Alarmconfig Undo/Redo Ok  
CNC: Undo disabled (Ok)  
Device Application is no longer supported.  
CDS-54175 | Bug | Debug, Breakpoints: Stepping with multiple __DELETE calls in POU is skipping statements | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-54170 | Bug | MethodObject: Add method dialog only listing 1st level inherited methods | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-54137 | Bug | Project Compare: Library Manager is marked as changed without any changes | Cannot Reproduce | [[GENERAL]]  
One of the referenced libraries contains a parameter list and the value of a parameter changed. This is the reason for the changed library manager. This is displayed much clearer in V3.5 SP19.  
CDS-54128 | Bug | Exception: Object reference not set... creating new project pressing ENTER 2 times | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-54125 | Bug | LMM: Compile-Messages from interface method reported twice | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-54113 | Bug | PLC Applictaion status : wrong application status | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-54106 | Improvement | Compiler: checkbox for the option „with name space insert“ should be set, like the lib-developer intended | Won't Fix | [[GENERAL]]  
Whether a library requires qaulified access is determined by the library developer using the "LanguageModelAttribute (Text) := qualified-access-only" project property. The checkbox is just a way for the user to enable qualified access only in cases the library does not force it anyway. But the user can never override that behaviour by disabling the checkbox.  
CDS-54069 | Bug | Refactoring: the type of the property in IMain is not renamed, if we renaming the Interface "IBase" | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-54062 | Bug | Implements Interfaces: properties from external interfaces are missing | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced anymore with V3.5 SP18  
CDS-54029 | Bug | Refactoring: Input variable of FB_Init not renamed in declaration part | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-53996 | Bug | Generate Code: Exception with nested implementation of interfaces in library | Cannot Reproduce | [[GENERAL]] StR: Ok Only tested with simple project.  
CDS-53995 | Bug | Task Config: Undo/Redo doesn't work with added/removed POU | Cannot Reproduce | [[GENERAL]] POU in tasklist has to be deleted seperately. This behaviour is correct.  
CDS-53983 | Bug | AutoDeclare: incomplete Namespace inserted in type declaration | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-53924 | Bug | OnlineManager: Object reference not set exception when logging in | Won't Fix | [[GENERAL]]  
Profiler and UI was reworked with V2.0 release. No attempt will be made to reproduce this bug anymore after several years.  
CDS-53827 | Bug | Online Help: Unhandled exception while searching | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-53706 | Bug | Internal error on login if library manager has been removed | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-53520 | Bug | Compile: Cannot convert type 'Bool' to type 'ANY_BIT' | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-53479 | Improvement | Device Application: Standard project needs a bus cyclic task | Won't Fix | [[GENERAL]]  
The device application feature has been discontinued.  
CDS-53380 | Bug | SFC: Error message doesn't lead to bug cause | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-53327 | Bug | Ladder: Insertion of contact does not work correctly in this project | Cannot Reproduce | [[GENERAL]] tested with latest version and various combinations. Always worked as expected.  
CDS-53236 | Bug | SAL: Static analysis rule "unused variabled" does not report errors on initial generate code based on an existing compile info | Cannot Reproduce |   
CDS-53100 | Bug | IDE crash on opening the input assistent in customer projekt | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-52974 | Bug | Breakpoints: Setting instance specific breakpoint in library FB might fail | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-52907 | Bug | Compiler: Message C0004 occur after update customer project | Won't Fix | [[GENERAL]]  
This is the new behaviour for over 5 years now. As such it cannot be changed anymore without creating new incompatibilities.  
CDS-52828 | Bug | Monitoring Range: does not work if a constant in array declaration | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-52756 | Bug | Refactoring/CrossReferences: Missing cross reference for parameter list declaration to compo access in init expression | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-52742 | Bug | ST: Zooming by mousewheel does not work any more if text has been selected by mouse | Duplicate | already fixed with CDS-67209  
CDS-52739 | Bug | PLCopen: ladder export/import losing elements | Cannot Reproduce | [[GENERAL]] With SP 18, first export and then import of the POU works fine.  
CDS-52630 | Bug | Smart Coding: Inserting elements via library namespace does not work properly | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-52628 | Bug | project template: configured task time have no effect | Cannot Reproduce | [[GENERAL]] tested with SP 18.  
CDS-52600 | Bug | Compile: NullReferenceException due to FB call in input of FB | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-52599 | Bug | Exception in global initialisation code after several application downloads | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-52594 | Bug | Compile, SFC: No error generated if local Program Variable is accessed in Transition or Action | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-52531 | Improvement | Debugging: The instance pointer from a function block should be in the variable list (declaration part) when a method is debugged | Duplicate | [[GENERAL]]  
Duplicates CDS-46735  
CDS-52466 | Improvement | Auto Declare: Global variables should be inserted with GVL namespace if declaring them on GVL with attribute 'qualified_only' | Cannot Reproduce |   
CDS-52448 | Bug | Refactoring: Input variable is added without a comma in ST | Cannot Reproduce | [[GENERAL]] Tested with SP 18.  
CDS-52445 | Bug | LMM: Compile error if reference assignment to base type within declaration | Cannot Reproduce | [[GENERAL]] no compile error with SP 18.  
CDS-52290 | Bug | Compile, Online Change: Area for Online Change mixes Code and Data | Duplicate | [[GENERAL]]  
duplicates CDS-81504  
CDS-52286 | Bug | LD: Paintbug in a special case | Cannot Reproduce | [[GENERAL]] No paint bug with latest version.  
CDS-52270 | Bug | Smart Coding: Insert with namespace is not working in ST | Fixed |   
CDS-52161 | Bug | Compile: Internal error in call to fb with dynamic array as input | Cannot Reproduce | [[GENERAL]] Works great with SP 19.  
CDS-52149 | Bug | CrossRef, Refactoring: No CrossReference to Object created with __NEW | Cannot Reproduce | [[GENERAL]] works great with SP 18.  
CDS-52096 | Bug | Library Manager: update from documentation window on change of libraray incorrect | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-52092 | Improvement | DeviceApplication: Re-Enable breakpoints for POUs called by parent task (programming system) | Won't Fix | [[GENERAL]]  
Device application feature has been discontinued.  
CDS-52086 | Bug | LanguageModel: Application content on PLC not shown any more if project is not compiled | Fixed | [[GENERAL]]  
The LinkLabel "Generate code now to show online comparison" is now available after "Clean" was performed  
CDS-51993 | Bug | IecVarAccess: Access to arrays of structs with odd sizes does not work | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-51925 | Bug | Wrong Precompile Error on assigning an enumeration value | Cannot Reproduce | [[GENERAL]] no precompile error with SP 18.  
CDS-51890 | Bug | Enumeration Initial Value for DWORD > 16#800000 leads to assertion on generate code | Cannot Reproduce | [[GENERAL]] no assertion with SP18  
CDS-51784 | Bug | Watchlist, Forcelist: Null reference exception on unforcing values | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with 3.5 SP18  
CDS-51771 | Bug | LMM/CrossRefs: FindExpressionAtSourcePosition returns null for Compo-Access-Index-Expression | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-51738 | Improvement | Enable optional parameters on methods of FBs and functions | Duplicate | [[GENERAL]]  
Duplicates CDS-56722  
CDS-51486 | Bug | Profiler doesn't work with device application | Won't Fix | [[GENERAL]]  
The device application has been discontinued.  
CDS-51410 | Bug | Wrong error message when trying to use SEH on CORTEX | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with Cortex devices based on V3.5 SP18.  
CDS-51384 | Bug | [TS_DeviceApp] Add tests for task mechanisms | Won't Fix | [[GENERAL]]  
The device application feature has been discontinued.  
CDS-51357 | Bug | Compile: Confusing message when cancelling Online Change | Cannot Reproduce |   
CDS-51184 | Bug | LMM: Unassigned IN_OUT var of dynamic array type is not reported as error | Cannot Reproduce | [[GENERAL]] With SP 18, compiler shows error.  
CDS-50978 | Bug | CFC: 'BOOL' cannot be converted to type '__LAZY' | Cannot Reproduce | [[GENERAL]] project compiles without problems.  
CDS-50957 | Bug | LMM: Null Reference exception when parsing certain pragma expression | Cannot Reproduce |   
CDS-50954 | Improvement | Symbol Configuration: Symbol configuration should use LanguageModelManager.IsHiddenSignature and IsHiddenVariable. | Won't Fix | [[GENERAL]]  
This will not be changed anymore in the legacy symbol configuration.  
CDS-50854 | Bug | Operation mode switching: for the user a no conclusive error message is stated | Cannot Reproduce | [[GENERAL]] Operating mode "gesperrt" can always be set. This problem cant be reproduced with SP 18.  
CDS-50787 | Bug | Compiler: Blobinit attribute with LTIME datatype in DUT has no initial value | Cannot Reproduce | [[GENERAL]] works fine with SP 18.  
CDS-50746 | Improvement | CAN: Give a possibilty to hide controls in CAN editor | Won't Fix | [[GENERAL]]  
Issue cannot be implemented due to unclear requirements.  
CDS-50637 | Bug | Visu, UnitConversion: When editing a converted LREAL value it is initialy set to the unconverted value | Cannot Reproduce | [[GENERAL]] Homag example works fine.  
CDS-50334 | Bug | Wrong Literal Folding for comparisons | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-50322 | Bug | LibMan: Library is not resolved after cut and paste | Cannot Reproduce | [[GENERAL]] Tested with SP 18. Ok.  
CDS-50229 | Bug | CrossRefView: values from options file not loaded on project switched | Cannot Reproduce | [[GENERAL]] StR: Ok  
CDS-50176 | Bug | FBD editor, search: no results for variables in EXECUTE Element | Cannot Reproduce | [[GENERAL]] Text is also found within the execute block  
CDS-50079 | Bug | CmpSchedule.c: Schedule on IEC task cycle end leads to a larger jitter although the schedule tick is exact | Won't Fix | [[GENERAL]]  
No longer requested by the customer  
CDS-50063 | Improvement | Symbolconfig: change for entire groups the access right inside the symbol configuration | Won't Fix | [[GENERAL]]  
This will not implemented anymore for the legacy symbol configuration. It is already supported by the new editors as part of the communication manager.  
CDS-49849 | Bug | SFC: Refactoring of action object sometimes produces wrong result | Cannot Reproduce | [[GENERAL]] tested with SP 18. Ok.  
CDS-49848 | Bug | SymbolConfigEditor: Erroneous warning if variable is referenced by parent application | Cannot Reproduce | [[GENERAL]] Works fine with SP 18.  
CDS-49818 | Bug | Watchlist online: Monitoring values are not visible after sorting a column | Cannot Reproduce | [[GENERAL]] Works fine with SP 18.  
CDS-49763 | Bug | FBD, LD: Multiselection: delete operation produces unexpected result | Cannot Reproduce | [[GENERAL]] problem one tested. Not reproduceable with SP 18.  
CDS-49730 | Bug | Visualisierung: Using the search functionality in the input assistant for element properties leads to errors | Cannot Reproduce |   
CDS-49547 | Bug | Device Tree: double-click on somewhere in the device tree immediately after login then the POU is opened but it is not possible to open other Editors | Cannot Reproduce | [[GENERAL]] I couldn't reproduce the problem with SP19. All editors could be opened.  
CDS-49515 | Improvement | Compile: Use of LOWER_BOUND, UPPER_BOUND also for arrays with fixed length | Duplicate | [[GENERAL]]  
Duplicates CDS-60871  
CDS-49505 | Bug | Precompile: There are false errors by library structure elements | Cannot Reproduce | [[GENERAL]] No problem with SP 18.  
CDS-49457 | Bug | FBD/LD: Update parameters does not work correctly | Cannot Reproduce | [[GENERAL]] Is solved with the latest version.  
CDS-49375 | Bug | FBD, LD: Corrupted network leads to crash | Cannot Reproduce | [[GENERAL]] Behaviour exactly as expected.  
CDS-49361 | Improvement | Allow reinitialization of persistent vars via context menu command. | Won't Fix | [[GENERAL]]  
The device application feature has been discontinued.  
CDS-49359 | Improvement | New TargetSetting UniqueTaskNames | Won't Fix | [[GENERAL]]  
The device application feature has been discontinued.  
CDS-49207 | Bug | Warning for "backwards compatibility" in specific project | Cannot Reproduce | [[GENERAL]] tested with SP 18  
CDS-49116 | Bug | Compile: Conversion of SIZEOF-Operator may be confusing | Won't Fix | [[GENERAL]]  
Usage of the XSIZEOF operator is recommended to avoid this kind of issues.  
CDS-49083 | Bug | Compile: Global variables with attribute 'qualified_only' cannot be declared as VAR_EXTERNAL | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced in V3.5 SP18.  
CDS-48980 | Improvement | Compiler,Compileroptionen: customer wants a option "always use this compiler version" | Won't Fix | [[GENERAL]]  
The compiler version is not freely choosable since V3.5 SP18 and its usage changed fundamentally with introduction of the modularization.  
CDS-48886 | Bug | Generate Code: Assertion with declaration of huge array to IO address | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced in V3.5 SP18.  
CDS-48868 | Improvement | LMM, PersistentVars: Add application name to dialogs regarding persistent var changes | Won't Fix | [[GENERAL]]  
The device application feature has been discontinued.  
CDS-48856 | Bug | C-Integration does not support non-top-level applications | Won't Fix | [[GENERAL]]  
The device application feature has been discontinued.  
CDS-48845 | Bug | Debugging: Errors during setting a breakpoint in the runtime are not reported to the user | Won't Fix | [[GENERAL]]  
Minor issues which has not been touched the last five years. Will not be fixed or investigated anymore. Issue never came up again.  
CDS-48843 | Improvement | Watchlist: Improve UI feedback when monitoring large arrays with more than 1000 values. | Duplicate | [[GENERAL]]  
Duplicates CDS-64062 and was implemented with V3.5 SP17.  
CDS-48836 | Improvement | DeviceApplication, Online: Query multiple IO access | Won't Fix | [[GENERAL]]  
Device application feature has been discontinued.  
CDS-48833 | Improvement | DeviceApplication: Warn users about effects of online actions | Won't Fix | [[GENERAL]]  
Device application feature has been discontinued.  
CDS-48532 | Bug | LMM: Handle out of memory during code generation consistently | Won't Fix | [[GENERAL]]  
Minor bug closed because not touched for more than 5 years. Also an issue that only very few users might ever encounter.  
CDS-48496 | Bug | Precompile: A precompile error occurs if a variable of GVL has the same name as a base class | Cannot Reproduce | [[GENERAL]] testet with SP 18. not reproducable.  
CDS-48488 | Bug | LMM: Build with non-existing compiler version does not trigger an error. | Cannot Reproduce | [[GENERAL]] Compilerversion can't be changed anymore.  
CDS-48422 | Bug | Compiler: Exception when declaring a variable with name containing just numerals | Cannot Reproduce | [[GENERAL]] No object reference error, no exception.  
CDS-48201 | Bug | Monitoring: tooltip for online view of binary or hexadecimal values too short in FBD | Cannot Reproduce | [[GENERAL]] Tested according to steps to repeat. Works fine with SP 19.  
CDS-47932 | Bug | Intellisense, Tooltip: the tooltip is cut, for variables in the visueditor elementproperties | Cannot Reproduce | [[GENERAL]] tested according to StR. full tooltip is shown.  
CDS-47900 | Improvement | SymbolConfig Editor: Improve view of hidden symbols | Won't Fix | [[GENERAL]]  
This will not be changed anymore for the legacy symbol configuration.  
CDS-47876 | Bug | Symbol Configuration: Header in English is shown as "Maximal" instead of "Maximum" | Won't Fix | [[GENERAL]]  
Will not be fixed anymore for the legacy symbol configuration.  
CDS-47862 | Bug | SymbolConfig: Do not hide variables just because their type has members preconfigured via symbol attribute | Won't Fix | [[GENERAL]]  
This will not be fixed anymore for the legacy symbol configuration  
CDS-47758 | Bug | Find & Replace: Switching between find and replace doesn't change text to find | Cannot Reproduce | [[GENERAL]] When I close the find dialog, b is correctly inserted. To leave the dialo open is no use case 8I didn't check).  
CDS-47221 | Improvement | Performance LMM: The return value of "IsUpToDate()" should be cached where possible | Duplicate | [[GENERAL]]  
Duplicates CDS-57362  
CDS-47159 | Bug | Compiler, StaticAnalysis: The attribute 'naming' is unknown | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with Static Analysis 4.4.1.0  
CDS-46790 | Improvement | LibMan: Add Library: Difference of the buttons "Extended Libraries" and "Extended..." not clear | Cannot Reproduce | [[GENERAL]]  
No longer reproducible because the button were removed with CDS-76542  
CDS-46764 | Bug | CODESYS Monitoring mixes up device instances | Cannot Reproduce |   
CDS-46623 | Bug | SymbolConfig: Variables with direct Addresses in STRUCTs are not handled cleanly | Won't Fix | [[GENERAL]]  
Issue did not come up for years in customer projects. Will not be fixed anymore for the old symbol configuration.  
CDS-46608 | Improvement | SymbolConfig: Backwards compatibility mode for BitFields needed. | Won't Fix | [[GENERAL]]  
Issue has not been touched in several years. It will not be implemented for the legacy symbol configuration anymore.  
CDS-46473 | Bug | LibMan: Button for "Download of missing libraries" is not always shown immediately | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-46457 | Bug | Autodeclare: Library attribute 'qualified-access-only' is not considered in certain case | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-46241 | Bug | Input Assistent: Documentation of POU does not support ReStructured text | Cannot Reproduce | [[GENERAL]] tested and works.  
CDS-46148 | Improvement | Symbolconfig: Difficult to see symbols that aren't exported due to missing Access Rights | Won't Fix | [[GENERAL]]  
Issue not touched for several years. This will not be changed anymore in the legacy symbol configuration.  
CDS-46137 | Bug | External Files: Embedded files not synchronized if original file is empty | Fixed |   
CDS-46097 | Improvement | Compiler: Rework GenerateCode to use Task API | Won't Fix | [[GENERAL]]  
Technology and .NET libraries and version evolved during the last 7 years. This idea is probably obsolete.  
CDS-46084 | Bug | LD: Copy a Network with Drag&Drop via ctrl-Key doesn't work like expected | Cannot Reproduce | [[GENERAL]] Just works fine with SP 18  
CDS-45972 | Bug | Symbolconfiguration file: typeclass changed from BOOL to BIT | Won't Fix | [[GENERAL]]  
The issue seems to be a minor problem since the addresses of BIT-Values are correct, and only the type changes from BOOL to BIT.  
The old symbolconfiguration will be replaced in the future by new symbol editor.  
CDS-45934 | Bug | Compile: exception by handling VAR_TEMP with { attribute 'noinit' } | Cannot Reproduce | [[GENERAL]] Not reproducable with SP 18.  
CDS-45933 | Bug | Refactoring: Initial value for output variable shouldn't be assinged in call-expression | Cannot Reproduce | [[GENERAL]] I checked the problem. Not reproducable with SP 18.  
CDS-45880 | Bug | Flowcontrol ST: call of FB shows not all values | Cannot Reproduce |   
CDS-45786 | Bug | CmpApp: Exception in GlobalInit / FB_Init Code leads to an inconsistent application | Cannot Reproduce | [[GENERAL]] Application is no longer listed.  
CDS-45747 | Improvement | LMM: There should be a compile error for direct addresses in structures, etc. | Won't Fix | [[GENERAL]]  
New compile errors cannot be introduced for compatibility reasons. Furthermore there is already a Static Analysis Rule (#48) for using direct addresses in declarations which reports this case. This is to be preferred to new compile warnings.  
CDS-45560 | Improvement | CrossReferenceView: Implement filters for hiding special cross references | Won't Fix | [[GENERAL]]  
The use case is unclear. If certain objects provide incorrect or no positions at all that should be fixed, instead of adding special filtering options. Also not requested anymore for several years.  
CDS-45426 | Bug | IecTextEditor: Disappearing text and unhandled exceptions with {impl_ident} pragma | Cannot Reproduce | [[GENERAL]] Works fine.  
CDS-45314 | Bug | LibMan: not possible to add a library having been installed for the first time after opening the project | Cannot Reproduce | [[GENERAL]] works fine with SP 18  
CDS-45211 | Improvement | PowerPC, PPC: Generate external Function calls according to c-calling-convention | Won't Fix | [[GENERAL]]  
This feature is not actively used on any platform is was already implemented for. Will not be done anymore for PowerPC.  
CDS-45052 | Improvement | Compile: Targetsetting needed to avoid memcpy in compiled code | Won't Fix | [[GENERAL]]  
A better solution is already available with CDS-73120  
CDS-45038 | Bug | Refactoring: "OK button" is selected but not activated if we press Enter | Cannot Reproduce | [[GENERAL]] Buttons are selected and active. Works fine.  
CDS-44954 | Bug | User Management Project: Buttons in communication editor bypass check of access rights | Cannot Reproduce |   
CDS-44774 | Bug | Ladder, Breakpoint, Stepping: Stepping does not work in Networks ending with a Set-Statement | Cannot Reproduce | [[GENERAL]] Duplicates CDS-44773  
Tested and also not reproducable.  
CDS-44773 | Bug | Ladder: Debugging: Stepping does not work if edge detection is used | Cannot Reproduce | [[GENERAL]] Stepping works fine in both cases.  
CDS-44651 | Bug | Simulation: mouse context menu item > Simulation disappears on login | Cannot Reproduce | [[GENERAL]]works with the latest released version.  
CDS-44617 | Bug | CreateOfflineBootapplication: wording of error message not correct and it is not localised | Cannot Reproduce | [[GENERAL]]  
Message got changed in the meantime, cannot be reproduced with 3.5 SP18  
CDS-44507 | Improvement | Usability: Provide an easy way for users to include explicitly implemented FB_Init and FB_Exit methods | Cannot Reproduce | [[GENERAL]]  
Works as described in V3.5 SP18 already.  
CDS-44386 | Bug | SymbolConfig: Fix the remaining cases of shadowing | Won't Fix | [[GENERAL]]  
Relevant cases already got fixed in the after implementing the namespace syntax. All other will not be fixed anymore since the symbol ocnfiguration is a legacy feature now.  
CDS-44354 | Improvement | Compile: new Syntax for namespace access | Duplicate | [[GENERAL]]  
Duplicates CDS-63808  
CDS-44302 | Improvement | LibMan: Provide "download missing Library" functionality for Scripting Engine | Cannot Reproduce | [[GENERAL]]  
No longer reproducible since with CDS-40857 a command was implemented to launch the library download. This command is also usable from scripting  
CDS-44263 | Improvement | SymbolConfig: If a GVL with all variables is selected in the SymbolConfiguration new variables are not added automatically | Won't Fix | [[GENERAL]]  
Will not be implemented anymore for the legacy symbol configuration. The new editors as part of the communication manager implement logic to explicitly notify the user about changed objects and configurations.  
CDS-44159 | Improvement | Simplified Task Configuration: Eliminate Wrapper function | Won't Fix | [[GENERAL]]  
This issue has not been touched for several years and the problem or requirement to be solved is unclear.  
CDS-44100 | Improvement | LibDoc: Try to show documentation even for libraries with missing licenses | Won't Fix | [[GENERAL]]   
Licensing libraries on engineering system got deprecated. All libraries have now device licenses.  
CDS-44099 | Bug | Refactoring,DiffViewer,ST: rejection of a change does not allways work correct | Cannot Reproduce | [[GENERAL]] Not reproducable with SP 19.  
CDS-44059 | Improvement | LibMan:It is not possible to select more then one library in the Add Library Dialogue | Duplicate | [[GENERAL]]  
Duplicates CDS-80878  
CDS-44051 | Improvement | SymbolConfig: Expose GetXMLFileName() method | Won't Fix | [[GENERAL]]  
Issue has not been touched for years and will not be implemented anymore for the legacy symbol configuration.  
CDS-43960 | Improvement | Compile: Detail Application information, extra code creation required. | Won't Fix | [[GENERAL]]  
Issue unclear and did not come up several years anymore.  
CDS-43952 | Improvement | LMM: Create PrecompileCrossRef nodes in ICrossReferenceNode ICrossReferenceService2.CreateNode | Won't Fix | [[GENERAL]]  
Not touched for several years anymore and issue never came up again,  
CDS-43948 | Improvement | SymbolConfig: Support for generating the SymbolConfig as a child application should be phased out. | Won't Fix | [[GENERAL]]  
Will not be implemented anymore for the old symbol configuration.  
CDS-43935 | Improvement | Compile: should be possible to call methods without already initialized parameters | Duplicate | [[GENERAL]]  
Duplicates CDS-56722 and was already implemented with V3.5 SP16.  
CDS-43873 | Improvement | LibMan:The category of a library should be visible in human readable way. | Cannot Reproduce | [[GENERAL]]  
The library categories are displayed as human readable text.  
CDS-43859 | Bug | UserManagement: Pattern for password fields | Cannot Reproduce | [[GENERAL]] It's blank in both cases.  
CDS-43795 | Bug | Export/Import: "Overwrite file" message appears again | Cannot Reproduce | [[GENERAL]] was solved somehow somewhen.  
CDS-43751 | Bug | Library: Default library resolution different to device description | Cannot Reproduce | [[GENERAL]]  
The default resolution is no longer evaluated from V3.5 SP18 onwards in the POUs library manager.  
CDS-43658 | Improvement | SymbolConfig: Always export all available information in the XML file | Won't Fix | [[GENERAL]]  
Issue has not been touched in several years. Will not be fixed anymore for the old symbol configuration.  
CDS-43521 | Bug | Auto Declare: works different in declaration for selected vars | Cannot Reproduce | [[GENERAL]] Works fine with Sp 18  
CDS-43498 | Bug | Check all pool objects: 64-Bit error C0032 not detected | Duplicate | [[GENERAL]]  
Duplicates CDS-62064  
CDS-43485 | Improvement | SymbolConfig: It is very difficult to see the activation state of the options, like "Include Comments in XML" | Won't Fix | [[GENERAL]]  
Issue not touched for several years. This will not be changed anymore in the legacy symbol configuration.  
CDS-43372 | Improvement | OPC UA: Implement handling of priority of subscriptions | Fixed |   
CDS-43127 | Bug | Compile: Warning 'C0200: There is no resolution for the placeholder CmpCodeMeter' should not occure | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.8 SP18  
CDS-43046 | Bug | Tooltip:Tooltip of variable value disappears directly under certain conditions | Cannot Reproduce | [[GENERAL]] Cursor is flickering, but the tooltip is visible and stable.  
CDS-43025 | Improvement | SymbolConfig: Better error messages when the device does not support the Symbol Configuration | Won't Fix | [[GENERAL]]  
Will not be implemented anymore for the old symbol configuration. The new one has new target settings enabling the device to specifically state compatibility.  
CDS-43007 | Improvement | Symbol configuration: Editor should work on precompile information | Won't Fix | [[GENERAL]]  
The new symbol configuration works on precompile information. The old symbol configuration will not be changed anymore.  
CDS-42999 | Bug | Online Help: MC_CamIn: data type of output Tappets is wrong | Cannot Reproduce | [[GENERAL]] Ok with SP 19  
CDS-42997 | Improvement | Improve Add Method-Dialog | Cannot Reproduce | [[GENERAL]]  
In V3.5 SP18 the improvement is already implemented.  
* FB_Init, FB_Exit and base methods are selectable in the Wizard and are inserted with correct declaration of parameters  
* The Static Analysis does not report unused inputs or unassigned return values for FB_Init and FB_Exit  
CDS-42857 | Bug | SynEdControl: Exception when clicking in margin area near to the horizontal splitter | Cannot Reproduce | [[GENERAL]] I clicked many times. no exception.  
CDS-42835 | Bug | UserManagement: Not granted Dialogue appears twice | Cannot Reproduce | [[GENERAL]] behaviour is different now. Cannot repr. the bug with current version.  
CDS-42690 | Bug | Project Compare: device is taken, even not supported message comes before | Cannot Reproduce | [[GENERAL]] Tested and Ok.  
CDS-42682 | Improvement | Targetsettings: Mandatory target settings needed | Won't Fix | [[GENERAL]]  
Exact use case is unclear and issue has not been touched for several years. Will not be fixed.  
CDS-42549 | Improvement | SymbolConfig: The export of not directly accessible objects should be prevented | Won't Fix | [[GENERAL]]  
The new symbol configuration does not offer properties, references, pointers, etc. for export. Will not be changed for the old symbol configuration anymore.  
CDS-42546 | Improvement | Utilities: Performance Optimization: Replace LStringBuilder with StringBuilder | Fixed |   
CDS-42526 | Bug | PLCopenXML: error by export when a coil contact is not set to TRUE | Cannot Reproduce | [[GENERAL]] is working meanwhile.  
CDS-42488 | Bug | Precompile, CFC: misleading precompile error C0046 if struct type is used in selector | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
CDS-42473 | Bug | Intellisense: The respective Enum-value for Inputs in FB's are difficult to find | Cannot Reproduce | [[GENERAL]] working as expected.  
CDS-42463 | Improvement | SymbolConfig: Provide structured language model instead of textual one | Won't Fix | [[GENERAL]]  
Not relevant anymore, the new objects implemented for the communication manager use structured language model creation. The old symbol configuration will not be changed anymore.  
CDS-42355 | Bug | Project Compare shows error message but does not cancel operation | Cannot Reproduce | [[GENERAL]] tested according to Str. Works fine now.  
CDS-42209 | Improvement | CmpBlkDrvUsb: CmpUsbMpdUsbLib: Adapt driver to new LibUsb 1.0.26 | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]:  
To enable the CmpBlkDrvUsb to be used by 64-bit CODESYS Control runtimes or the Gateway, we updated the CmpUsbMpdUsbLib to the latest version of the libusb.dll. Due to a incompatibilty to the legacy version (before 1.0) of libusb, it is necessary to update also the libusb.sys driver, provided by the device vendor/manufacturer. According to Libusb following drivers should be used: WinUSB.sys (recommended) - libusbk.sys - libusb0.sys (latest version).  
CDS-42123 | Improvement | Utilities: Performance Optimization: Replace LList with standard .Net types | Won't Fix | [[GENERAL]]  
Reviewing the source code of the List implementation in .Net 4.8 revealed that there is no built-in "chunking" of the list members (in contrast to StringBuilder). Switching from our chunked LList to the unchunked List implementation may result in memory allocation problems on the Large Object Heap. Therefore, we will not fix this issue.  
CDS-42014 | Bug | Project wizard could not be created after reuse the name of deleted project | Cannot Reproduce | [[GENERAL]] tested and Ok  
CDS-42011 | Bug | Device Tree context menu some times inconsistent and selection lost | Cannot Reproduce | [[GENERAL]] tested. Correct behaviour.  
CDS-42006 | Bug | Project compare tab does not appear in the opened window list | Cannot Reproduce | [[GENERAL]] Tested with SP 18. Is Ok now.  
CDS-41978 | Bug | Docu: Scrolling not possible in index-list | Cannot Reproduce | [[GENERAL]] New online help is completely different regarding index list.  
CDS-41791 | Bug | Refactoring: Error provider in rename dialog not completely within window bounds | Cannot Reproduce | [[GENERAL]] looks great with SP 19  
CDS-41778 | Bug | Autodeclare: Dialog not initialised after Shift+F2 in declaration part | Cannot Reproduce | [[GENERAL]] works fine.  
CDS-41714 | Bug | Devices: Inconsistent naming of 64-Bit devdesc of ControlWin | Cannot Reproduce | [[GENERAL]] is Ok now.  
CDS-41532 | Improvement | M4Export should recognize the c-calling-convention attribute | Won't Fix | [[GENERAL]]  
Issue did not come up again for the last several years. Will not be implemented.  
CDS-41447 | Improvement | Compiler: Project Property to define a recommended compiler version | Won't Fix | [[GENERAL]]  
The described behaviour is obsolete with the changes to compiler versions introduced with the modularization in SP17. Also libraries now store the compiler version were created with and the compiler reports an error if the version used in the project is older than the version the library was created with.  
CDS-41429 | Bug | Auto Declare: the "Type" information for certain inputs/outputs on the SoftMotion function blocks is non-standard | Cannot Reproduce | [[GENERAL]] now SMCError is the type.  
CDS-41408 | Improvement | LibraryManager: it is not possible to add more then one library at the same time | Duplicate | [[GENERAL]]  
Duplicates CDS-80878  
CDS-41386 | Bug | RecipeManagement: Different behavior between ULINT and WORD when exceeding the range | Cannot Reproduce | [[GENERAL]] StR: works fine  
CDS-41294 | Bug | Symbolconfiguration: It should not possible to define a 'readwrite' attribute for Get accessor of Property | Cannot Reproduce | [[GENERAL]] readwrite not accessable with SP18.  
CDS-41293 | Bug | Symbolconfiguration: missing access modifier and comments at user defined properties | Cannot Reproduce | [[GENERAL]] not reproducable with SP 19  
CDS-41168 | Bug | LMM: Incorrect precompile warning C0035 for call on FB reference | Cannot Reproduce | [[GENERAL]] no precompile messages.  
CDS-41129 | Bug | Simulation: Very unfriendly behaviour when the simulation DevDesc is missing. | Fixed |   
CDS-40960 | Bug | Find/Replace: Regular expression: Match beginning/end of string (^/$) does not work | Cannot Reproduce | [[GENERAL]] tested with SP19. If you don't use '', just write foo$, it works perfect.  
CDS-40880 | Bug | Compile: Internal Error (Code386): Unsupported conversion! on compile | Won't Fix | [[GENERAL]]  
Errors are caused by deactivated floating point unit for x86 in the device description.  
CDS-40721 | Bug | Close Project : Cancel closing of CODSYS closes CODESYS anyway | Cannot Reproduce | [[GENERAL]] Tested and Ok.  
CDS-40569 | Epic | OPC UA Server: Complete Micro Embedded Device 2017 Server Profile | Fixed | [[GENERAL]]  
There is a new setting to configure the maximum session timeout. The setting defaults to a timeout of 2 days.  
  
[[COMPATIBILITY_INFORMATION]]  
The ServerDiagnostics have been disabled, as this is not required for the Micro Embedded Profile, and the implementation is not compliant.  
  
The default of the security setting "CommunicationMode" has changed from ALL to SECURE_IF_POSSIBLE. This is a new option, which deactivates the unsecure "None" Policy if a certificate is available. If needed, this setting can be changed easily via the security settings dialog provided by the "CODESYS Security Agent".  
As a result, on existing systems with configured certificates, OPC UA clients using "None" as security policy can not connect without either changing the setting or removing the OPC UA Server certificate.  
CDS-40028 | Bug | Symbol configuration: Reopen of editor required to make library objects visible | Won't Fix | [[GENERAL]]  
Will not be fixed anymore for the legacy symbol configuration.  
CDS-39848 | Bug | Tooltip: tooltip for global instance is not displayed correctly | Cannot Reproduce | [[GENERAL]] not reproducable with SP 18.  
CDS-39800 | Bug | LanguageModelManager: Online Change may cause assertion if application is too big for target | Cannot Reproduce | [[GENERAL]]  
Online changes are not possible anymore after changing the device type  
CDS-39799 | Bug | LanguageModelManager: Online Change may cause assertion if application is too big for target | Cannot Reproduce | [[GENERAL]]  
Doing an online change after an device update is not possible anymore.  
CDS-39757 | Bug | CFC: Run to Cursor not working between different editors | Cannot Reproduce | [[GENERAL]] works fine with SP 18 P2  
CDS-39741 | Bug | ST: Tooltip is not displayed correctly | Cannot Reproduce | [[GENERAL]] tested with SP 18 P 2.  
CDS-39696 | Improvement | Iomapping export: Make CSV file separator configurable | Duplicate |   
CDS-39433 | Improvement | Symbolconfig: it should be possible to declare unused global vars | Won't Fix | [[GENERAL]]  
The new symbol configuration works on precompile information and simply supports this. The old editor will not be changed anymore.  
CDS-39395 | Bug | SymbolConfiguration: When the current configuration corresponds to the reference context, the XML file is not updated during code generation. | Won't Fix | [[GENERAL]]  
This issue is conceptually fixed by the new symbol configuration by providing precompile lm instead of late language model. For the legacy editor it will not be fixed anymore.  
CDS-38749 | Bug | Watch: Intellisense does not recognize VAR_INST variables | Fixed |   
CDS-38456 | Bug | M4 Export: Enum values that are assigned to other enum values are not exported | Cannot Reproduce | [[GENERAL]]  
Cannot be reproduced with V3.5 SP18  
CDS-38444 | Improvement | Intellisens: representation of the Intellisense function unfavorable | Cannot Reproduce | [[GENERAL]]  
The issue cannot be reproduced anymore with V3.5 SP18  
CDS-37940 | Improvement | Compile, Online Change: display the amount of data to copy | Cannot Reproduce | [[GENERAL]]  
The total amount of bytes to be copied is displayed in the online change details dialog.  
CDS-37903 | Bug | Cross reference: Drop down box loses focus the first time it is selected | Cannot Reproduce | [[GENERAL]]  
The scope drow down does not exist anymore in the cross reference view.  
CDS-37773 | Bug | Options: mistake in spelling 'namepace' instead of 'namespace' | Cannot Reproduce | [[GENERAL]] tested with SP 19. Perfect.  
CDS-37625 | Improvement | OPC Server: Secure password used for PLC login | Fixed | [[COMPATIBILITY_INFORMATION]]  
After updating the CODESYS OPC DA Server via the setup, the new CODESYS OPC DA Server removes plain text passwords from the configuration file at startup and stores them in the Microsoft Windows Credential Manager instead.  
  
Further password specific information can be found in the chapter "Passwords in OPCConfig" of the CODESYS_OPC_Server_V3_User_Guide.pdf, which is available in the installation directory of the CODESYS OPC DA Server. Especially the use of the CODESYS OPCConfig tool, the deployment of CODESYS OPC DA Server configuration files to multiple PCs and other compatibility aspects are described there in detail.  
  
For more details see Advisory 2022-10, which is available on the CODESYS website: https://customers.codesys.com/index.php?eID=dumpFile&t=f&f=17129&token=1c1485c4a700c04f2069699f5be7558d276ca117&download=  
CDS-37402 | Improvement | Compile: Compiled library should not generate warnings. | Cannot Reproduce | [[GENERAL]]  
Warnings originating in POUs of compiled libraries are not output as warnings during compile anymore, at least since V3.5 SP17.  
CDS-37080 | Bug | LMM: static initialization of Array elements with references to strings are failing | Cannot Reproduce | [[GENERAL]]  
Regular compile errors are reported at least since V3.5 SP18:  
"C0032: Cannot convert type 'STRING(INT#5)' to type 'REFERENCE TO STRING'"  
CDS-37039 | Bug | OPCServer: Gateway not found if Interface changes from GATEWAY3 to GATEWAY | Cannot Reproduce |   
CDS-37031 | Bug | ST-Editor: tool tip remains visible, although caret has been moved | Cannot Reproduce | [[GENERAL]] StR: Ok with SP 18.  
CDS-37029 | Bug | AutoDeclare: Autodeclare does not work within a CASE loop | Cannot Reproduce | [[GENERAL]] Could not be reproduced with SP 18.  
CDS-36708 | Bug | ChangeNodeName is not working properly when using non-ASCII characters. | Cannot Reproduce | [[GENERAL]] No problem with SP 18.  
CDS-36672 | Bug | Find&Replace: FindNext does not search through all objects | Cannot Reproduce | [[GENERAL]] There are 11 findings which were all found.  
CDS-36659 | Bug | Online Help:"Welcome to CODESYS" page does not open | Cannot Reproduce | [[GENERAL]] Online Help changed completely.  
CDS-36649 | Improvement | Symbol configuration, settings: it should be better displayed if the "Include Comments in XML" is activated or deactivated | Won't Fix | [[GENERAL]]  
Usability improvements will not be implemented for the old Symbol Configuration anymore. Use the new editors available below the Communication Manager object.  
CDS-36526 | Bug | MappingEditor/TreeTableView: Pressing CTRL+ not only expands branch but also changes column width | Cannot Reproduce | [[GENERAL]] tested with SP 18. works fine.  
CDS-36166 | Improvement | IOConfig: IO-Mapping shoud be generated in a normal VAR_CONFIG Environment | Won't Fix | [[GENERAL]]  
VAR_CONFIG is a very rarely used feature  
CDS-36145 | Bug | Project Settings, Library Categories: Assertion if description file is invalid. | Cannot Reproduce | [[GENERAL]] Tested with SP 18. no crash.  
CDS-32911 | Improvement | Compile, 61131-3 3rd Edition: partial access to ANY_BIT types | Duplicate | [[GENERAL]]  
Is implemented by CDS-72903  
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2023 CODESYS GmbH  | A member of the CODESYS Group 
