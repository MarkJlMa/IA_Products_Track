[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS V3.5 SP20 Patch 2

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
CDS-90525 | Bug | CLONE - Internal error with online change in LD2 | Fixed | Compiler Version >= 3.5.20.2.  
CDS-90307 | Bug | CLONE - RTE LwIP crash in internal task | Fixed | [GENERAL]  
For CODESYS Control RTE and the use of internal LwIP Tcp/IP protocol stack:  
It seems the timing slightly changed and a problem when using special Profinet slaves was observed during our tests when using "reconfigure" on the PN-master.   
For PN-networks without these special slaves the problem could not be observed. Reconfigure always worked as designed.  
CDS-90289 | Improvement | CLONE - ABL network licenses: Improve license check time with several installed ABL licenses | Fixed | [[GENERAL]]  
Not using the logfilter for CmpCodeMeter for network licenses improves the time for licensing checks by several factors  
CDS-90271 | Bug | CLONE - Security issues in Bouncy Castle versions before 2.4.0 | Fixed |   
CDS-90269 | Bug | CLONE - Remove read only flag does not work | Fixed |   
CDS-90268 | Bug | CLONE - CmpIecVarAccess: Performance issue on channel close / session delete | Fixed |   
CDS-90169 | Bug | CLONE - Display function "Read current metrics from device" Button more prominently | Fixed | [[GENERAL]]  
The table cell displays a LinkLabel, which also reads the license limits from the device.  
CDS-90160 | Bug | CLONE - Storage layer: Support long paths | Fixed | [[GENERAL]]  
Storage implementation now supports long paths.  
CDS-90159 | Bug | CLONE - Compiler: Crossreferences and refactoring for IecSymbolPublishingObject no longer working | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.20  
CDS-90146 | Bug | CLONE - M4 Export: Wrong name for argument struct of properties of interfaces | Fixed | [[GENERAL]]  
There might be conflicts in the generated m4 file with methods starting with "GET" or "SET" and having the name of a property  
CDS-90145 | Bug | CLONE - M4 Export: A interface passed a parameter is not exported correctly | Fixed |   
CDS-90125 | Improvement | CLONE - Support of UTF8 and UTF16 string contants needed | Fixed |   
CDS-90108 | Bug | CLONE - CmpRedundancy: Synchronization sequence deletes the database of the persistence manager | Fixed |   
CDS-90083 | Bug | CLONE - CmpIecVarAccess : Extended mem pool search upon deletion of var lists | Fixed |   
CDS-90082 | Bug | CLONE - compiler: unexpected compile error after clean all | Fixed |   
CDS-90027 | Improvement | CLONE - Frame: Add OEM hook to handle certain windows messages | Fixed | [[GENERAL]]  
Added a new Customization Hook with Section="Frame" and Key="WndProcCustomization".  
This can be set once at startup to modify the WndProc call of Main Frame. This can be used to customize the title bar.  
CDS-90013 | Bug | CLONE - CmpDeviceSrv.c : Possible semaphore deadlock upon closing session | Fixed |   
CDS-90012 | Improvement | CLONE - Licensed Software Metrics: Display usage of MultiCore feature on device | Fixed |   
CDS-90006 | Improvement | CLONE - OPC Server DA setup: Update included Gateway V2 to latest version | Fixed |   
CDS-90004 | Bug | CLONE - Return value from CFC property is not correct | Fixed | [[GENERAL]]  
Requires Compiler Version >= 3.5.20.20  
CDS-90003 | Bug | CLONE - VarStatInitValueChecker: Memory leak due to static reference to scope and compile context | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.20.0  
CDS-90002 | Bug | CLONE - CmpCodeMeter/CmpApp: In case of downloading a second application previous licenses are not unlocked | Fixed |   
CDS-89967 | Bug | CLONE - CmpOpenSSL: Security issues in OpenSSL versions before 3.2.2 | Fixed |   
CDS-89965 | Bug | CLONE - Access violation during/after online change | Fixed |   
CDS-89964 | Bug | CLONE - CmpCodeMeter/CmpApp: In case of downloading a new application while running previous licenses are not unlocked | Fixed |   
CDS-89870 | Improvement | CLONE - PLCHandler: allow adding new user in case User Management is enforced but no user exists yet | Fixed |   
CDS-89869 | Bug | CLONE - Vxworks (LLVM, X86) : With Compiler Optimization O2 exception source position and callstack not returned (again) | Fixed |   
CDS-89860 | Bug | CLONE - CmpOPCUAServer: Server stop publishing if the systemtime is set backward | Fixed |   
CDS-89859 | Bug | CLONE - Linux: signalstack overflow on ARM64 | Fixed |   
CDS-89858 | Bug | CLONE - ESM EtherCAT slaves: opening a project requires Clean All or other re-generation of the LMs | Won't Fix | [[GENERAL]]  
Clone in Essentials from a EtherCAT issue is not possible -> Won't fix.  
CDS-89857 | Improvement | CLONE - License Finder dialog: add option to select store variant (international/North America) | Fixed | [[GENERAL]]  
The view for showing missing licenses now contains a field for changing which shop is supposed to open (international or NA)  
CDS-89856 | Improvement | CLONE - License Finder Dialog: for bundles: list all contained products | Fixed | [[GENERAL]]  
License dialog shows included licenses  
CDS-89854 | Bug | CLONE - Unhandeld exception during clean all While Library with constant is open | Fixed |   
CDS-89810 | Bug | CLONE - OPC Server cannot write to %MX variables. | Fixed |   
CDS-89762 | Bug | CLONE - User Management: Import from Disk leads to message “Not logged in to device” | Fixed |   
CDS-89690 | Bug | CLONE - Error window appears after performing Ctrl+X (Cut) in SFC POU Code declaration area | Fixed |   
CDS-89689 | Bug | CLONE - Tabular Declaration: Initialization of Array of Struct containing Array of Struct leads to error pop-up | Fixed |   
CDS-89688 | Bug | CLONE - Precompile: Some precompile for fieldbus FBs are generated | Duplicate | [[GENERAL]]  
Duplicates CDS-89748  
CDS-89687 | Improvement | CLONE - M4 Export: Export interface types as Wrapper struct around instance-pointer | Fixed |   
CDS-89686 | Improvement | CLONE - M4 Export : Support exporting of Interfaces | Fixed | [[GENERAL]]  
An external interface does not make really sense. Only a concrete implemention can be external not the interface itself. This is why the generated linking code reported errors. After this fix no linking code will be generated for external interface methods.  
CDS-89685 | Improvement | CLONE - M4 export: Export POUs of type function with "Enable System Call" enabled | Fixed | [[GENERAL]]  
This should not be part of the M4-export, if there is a real use for this feature it should be implemented as a new command  
CDS-89683 | Bug | CLONE - External FB Implemtation with Any Input -> Broken Interface.M4 | Fixed |   
CDS-89681 | Bug | CLONE - [M4 Export] Export of calculated constant does not work | Duplicate | [[GENERAL]]  
Duplicate of CDS-89391  
CDS-89680 | Bug | CLONE - M4 Export: Stringvalues in VAR_GLOBAL Constant are not exported | Fixed | [[GENERAL]]  
String constants are now always generated as UTF-8 encoded strings, despite of the compiler setting for the library.  
In the end, the encoding of a constant 'Ä' in a library will always be defined by the compiler setting of a project using the library. UTF-8 is the only way to have an encoding that can be enforced on any platform. We recommend to use STRING-constants only containing characters within the ASCII-set.  
CDS-89679 | Improvement | CLONE - M4-Header-Generation: Support ANY_TYPE | Cannot Reproduce | [[GENERAL]]  
ANY_TYPE is both supported for functions and functionblocks  
CDS-89678 | Improvement | CLONE - M4 export: Missing features. | Cannot Reproduce | [[GENERAL]]  
Strings and WStrings are currently exported as Pointer to RTS_IEC_STRING  
CDS-89675 | Improvement | CLONE - DeviceObject: Change Initial Parameter Value on Online Change | Fixed |   
CDS-89500 | Bug | CLONE - SysSocketLinux.c : For QNX the UpdateNetworkAdapterInfo( ) causes cyclically CPU performance peak | Fixed | A new setting is available to disable the cyclic update of the default gateway, while still initializing it once:  
  
[SysSocket]  
DisableGetDefaultGateway=1  
  
In This case, the event EVTPARAM_SysSocket_GetAdditionalAdapterInfo can still be used to update the default gateway at runtime.  
CDS-89497 | Bug | CLONE - CmpX509CertItf: X509CertGetContent returns wrong value type for alternative name Email | Fixed |   
CDS-89404 | Bug | CLONE - Two new variables in separate modules in the IO mapping cannot be committed individually | Fixed |   
CDS-89391 | Bug | CLONE - [M4 Export] Export of calculated constant does not work | Fixed |   
CDS-89390 | Bug | CLONE - M4 Export: Inconsistent export of enum values | Fixed | [[GENERAL]]  
Additionally the problem with calculations in array borders has been fixed for the following operators: + - * /  
CDS-89316 | Bug | CLONE - PLCOpenXML Import: Object GUID is not preserved on Replace existing object | Fixed |   
CDS-89230 | Improvement | CLONE - Multicore: SchedProcessorLoad tasks are also setup for cores on which IEC tasks must not run | Fixed |   
CDS-89139 | Bug | CLONE - Linux: J1939 doesn't work if CmpSocketCanDrv setting "Loopback=1" is set. The setting RecvOwnMsgs=0 is ignored | Fixed | [[COMPATIBILITY_INFORMATION]]  
The setting RecvOwnMsgs from CmpSocketCanDrv section now has an effect. To not break existing application the default changed from 1 (enabled) to 0 (disabled).  
CDS-88959 | Bug | CLONE - OPC DA, Editor: OPCConfig.exe - User and Password are not saved in .ini file | Fixed |   
CDS-88859 | Improvement | CLONE - Simulation: Extend ISimulationManager with context information | Fixed |   
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2024 CODESYS GmbH  | A member of the CODESYS Group 
