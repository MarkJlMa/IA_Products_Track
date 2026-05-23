[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS V3.5 SP21 Patch 3

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
CDS-95154 | Bug | CLONE - CmpUserObjectDBFile: A folder named "a,b,c" destroys the new file format | Won't Fix | [[GENERAL]]  
[[KNOWN_LIMITATIONS]]  
Access rights cannot be configured for directories that contain commas in their names. These directories inherit the access rights of their parent directory.  
CDS-95151 | Improvement | CLONE - Add new AddOn CODESYS Math Libraries to Setup | Fixed | [[GENERAL]]  
The AddOn "CODESYS Math Libraries" is included with version 4.0.0.0 in the setup.  
CDS-95071 | Bug | CLONE - License Manager: An unhandled exception occurs during license activation | Fixed |   
CDS-95035 | Improvement | CLONE - CmpMemGC: enhanced debugging feature: enable exception on double free and bounds check | Fixed |   
CDS-95025 | Improvement | CLONE - MBM: Incorporate TaskLock and TaskUnlock from CAATypes | Fixed |   
CDS-94963 | Bug | CLONE - Untranslated texts in Codesys during application download when create boot application is disabled | Fixed |   
CDS-94918 | Bug | CLONE - Onlinechange is possible for parameter changes but it should force a full download | Fixed | [[GENERAL]]  
Caused by CDS-87310  
CDS-94900 | Bug | CLONE - CmpUserObjectDBFile: Rights database file is written at shutdown even if no UserManagement is configured | Fixed |   
CDS-94899 | Improvement | CLONE - CmpUserObjectDBFile: Improve file format | Fixed | [[GENERAL]]  
[[KNOWN_LIMITATIONS]]  
Access rights cannot be configured for directories that contain commas in their names. These directories inherit the access rights of their parent directory.  
CDS-94897 | Bug | CLONE - SysDirAsync: Restriction of diMaxDirLen/diMaxDirEntry to 80bytes is no longer needed | Fixed |   
CDS-94840 | Improvement | CLONE - Online: Add logging functionality for exceptions | Won't Fix | [[GENERAL]]  
This CLONE will not be fixed because the improvement is still under construction for SP22 and cannot be patched due to its complexity.  
CDS-94836 | Bug | CLONE - Scripting: Creating a secondary library project and adding code to it fails | Fixed |   
CDS-94828 | Bug | CLONE - Compiler, M4: Duplicate definition for RTS_IEC-types | Fixed |   
CDS-94827 | Bug | CLONE - Compiler, M4: Wrong casing for enum types in some cases | Fixed |   
CDS-94730 | Improvement | CLONE - LibDoc: Attribute 'conditionalshow' should work similar for objects in tree and library documentation | Won't Fix | [[GENERAL]]  
Changing the behaviour of the documentation generation for libraries is a high risk change which cannot be done in a patch version. It has the potential to break working customer workflows or change the resulst in unexpected ways.  
CDS-94695 | Improvement | CLONE - Linux: Make Signal SIG_EXIT configurable | Fixed |   
CDS-94694 | Improvement | CLONE - Update AxProtector to 11.60a | Fixed | [[GENERAL]]  
On systems with older CPU generations, a timeout may occur when starting the CODESYS Control service. An indicator of the problem is high CPU usage when starting for more than 30 seconds and an event 7000 or 7011 logged in the windows event viewer.  
To work around this problem, the ServicesPipeTimeout can be increased in the registry.  
CDS-94655 | Improvement | CLONE - Runtime Password Policy: Change default of maximum values | Fixed |   
CDS-94580 | Improvement | CLONE - SysTimeRtc / VxWorks: Support of SysTimeSetTimezone2() interface needed | Fixed | [[GENERAL]]  
SysTimeRTCVxWorks now provides a new interface SysTimeRtcSetTimezone2. This is enabled by default for VxWorks >= 7 but can be enabled/disabled at buildtime via preprocessor define.  
If enabled a call to SysTimeRtcSetTimezone2 sets the environment variable "TZ" with the given string and persists the string in the runtime configuration file as new setting "VxWorks.Timezone". When the runtime starts and this setting is set, the configured value will be set via SysTimeRtcSetTimezone2 automatically.  
CDS-94579 | Improvement | CLONE - Runtime Password Policy: Change default of maximum values in Runtime code | Fixed |   
CDS-94578 | Improvement | CLONE - SysTimeRtc: Support of SysTimeSetTimezone2() interface needed | Fixed | [[GENERAL]]  
Added new C and IEC interface function SysTimeRtcSetTimezone2(RTS_CSTRING* pszTimezone). With which the timezone of the PLC can be set via the POSIX environent variable TZ. See POSIX 1.2024 for details on how this variable is formatted.  
Added function to IEC library SysTimeRtc  
CDS-94577 | Bug | CLONE - SysFileCopy on VxWorks: A non existing destination folder is not created any more | Fixed |   
CDS-94576 | Bug | CLONE - Deadlock on runtime startup | Fixed |   
CDS-94575 | Bug | CLONE - Security issues in CodeMeter versions before 8.30a | Fixed |   
CDS-94574 | Bug | CLONE - DeviceObject: Compile errors after adding Ethernet device | Won't Fix | [[GENERAL]]  
Already cloned in SP21 Patch 2. Therefore won't fix  
CDS-94573 | Bug | CLONE - Security issues in WibuCmNet versions before 8.30a | Fixed | [[GENERAL]]  
WibuCmNet is now on version 8.30  
CDS-94450 | Bug | CLONE - Overloaded conversion "TO_WORD": Exception when converting ULINT variable | Fixed |   
CDS-94438 | Bug | CLONE - ImagePool: Loading embedded images is slow | Fixed | [[Known Limitations]]  
This fix addresses one of two possible causes for the behaviour. The other will be addressed with VSPRT-234.  
CDS-94432 | Bug | CLONE - Build - Internal error: Sytem.AggregateException... | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.22.0  
CDS-94430 | Bug | CLONE - Signing application only works for implicitly created boot application | Fixed |   
CDS-94322 | Improvement | CLONE - Scripting: Context object for Python calls needed | Fixed |   
CDS-94311 | Bug | CLONE - FindReplace: Unhandled exception in device editor | Fixed |   
CDS-94288 | Bug | CLONE - Compiler: Initial values of existing FB instance lost if FB_init is changed and a new instance is added | Fixed | [[GENERAL]]  
Changing the implementation of FB_Init now performs a standard online change instead of a fast one.  
CDS-94222 | Bug | CLONE - Project Documentation: Export device IO mapping | Fixed |   
CDS-94220 | Improvement | CLONE - Native Import: Add conflict resolution | Fixed | [[GENERAL]]  
For the native import, it's now possible to select a conflict resolution for objects with a name conflict.  
CDS-94219 | Bug | CLONE - Device security settings, access rights: Visible even though no rights are given | Fixed |   
CDS-93662 | Improvement | CLONE - CmpCodeMeter: should be possible to get detailed container information / broken / valid | Won't Fix | [[GENERAL]]  
\- Isolated implementation in the runtime system makes no sense without implementation in CODESYS LicenseManager (CDS-94154)  
  
 

CODESYS AddOns  |  Version   
---|---  
CODESYS Automation Server Connector | 1.36.0.0  
CODESYS Base Libraries | 4.0.0.0  
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
CODESYS Communication | 4.6.1.0  
CODESYS RISC Front End | 4.0.2.0  
CODESYS Target Settings Export | 4.0.0.0  
CODESYS Trace | 4.2.0.0  
CODESYS IO-Link | 4.3.0.0  
CODESYS Safety Support | 4.0.0.0  
CODESYS Redundancy | 4.2.0.0  
CODESYS NetX | 4.0.0.0  
CODESYS Memory Tools | 4.1.0.0  
CODESYS Modbus | 4.5.0.0  
CODESYS Ethernet Adapter | 4.2.0.0  
CODESYS EtherCAT | 4.10.0.0  
CODESYS CANopen | 4.3.0.0  
CODESYS EDS Import | 4.2.0.0  
CODESYS EtherNetIP | 4.8.0.0  
CODESYS PROFIBUS | 4.2.0.0  
CODESYS SAE J1939 | 4.2.0.0  
CODESYS PROFINET | 4.7.1.0  
CODESYS Scripting | 4.1.0.0  
CODESYS Recipes | 4.6.0.0  
CODESYS Embedded Runtime Extension | 4.1.0.0  
CODESYS Device Reader | 4.0.0.0  
CODESYS Visualization Support | 4.6.0.0  
CODESYS Visualization | 4.8.0.0  
CODESYS CFC | 4.4.0.0  
CODESYS Application Composer | 4.3.2.0  
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
