[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS V3.5 SP21 Patch 2

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
CDS-94742 | Bug | CLONE - NVL: Activating NVL leads to Exception on PLC | Fixed | [[GENERAL]]  
Disable concurrent online change for NVLs.  
CDS-94709 | Bug | CLONE - Targetvisu, Linux: Browser might block Visu with D&D operations | Fixed | [[GENERAL]]  
Using a newly introduced mechanism for injecting scripts into websites loaded within the Qt Webbrowser, it is possible to circumvent these problems by disabling drag&drop entirely.  
For details see the runtime documentation of the setting "BrowserScriptExtensionFile". If activating this setting, please especially respect the hints regarding file access from that documentation.  
CDS-94691 | Bug | CLONE - CODESYS Control Runtime: Crash at login with CODESYS protocol clients before 3.5.16.0 | Fixed | [[GENERAL]]  
Accident caused by CDS-93240, patched with CDS-93618 to version 3.5.21.10.   
  
For more details see CODESYS Security Advisory 2025-08, which is available on the CODESYS website:  
https://codesys.com/fileadmin/user_upload/CODESYS_Group/Ecosystem/Up-to-Date/Security/Security-Advisories/Advisory2025-08_CDS-94690.pdf  
CDS-94652 | Bug | CLONE - Import PLCopen xml format generates Object reference not set message | Fixed |   
CDS-94475 | Bug | CLONE - TargetVisu (Remote) Linux: Visu does not start as fullscreen with OverlayMode=1 | Fixed |   
CDS-94454 | Bug | CLONE - DeviceObject: Compile errors after adding Ethernet device | Fixed |   
CDS-94453 | Bug | CLONE - SVG-Renderer: Security issues in OSS versions before (libxml2 2.14.4, libcurl 8.14.1) | Fixed |   
CDS-94429 | Bug | CLONE - RTS: Security issues in sqlite versions before 3.50.1 | Fixed |   
CDS-94427 | Bug | CLONE - Access Violation at Online Change with FB in SFC header and LD2 Transtion. | Fixed |   
CDS-94370 | Improvement | CLONE - SysFile: In case a placeholder is added to the black list also add the file path to it | Fixed |   
CDS-94369 | Improvement | CLONE - FileTransfer/SysDir: Deny directory access via blacklist | Fixed |   
CDS-94353 | Bug | CLONE - CmpOpenSSL: "cert-createcsr" plcshell command does not work a second time after calling with invalid paramater | Fixed |   
CDS-94321 | Bug | CLONE - SysTimeRtcVxWorks.c : Bad parameter conversion for used localtime_r function | Fixed |   
CDS-94320 | Bug | CLONE - Breakpoints menu has 2 Step out but no Step over | Fixed |   
CDS-94310 | Improvement | CLONE - Linux SysCpuHandling X64/X86: remove warning about executable stack | Fixed | ,  
CDS-94269 | Bug | CLONE - DeviceEditor: CODESYS Crashes if Modules are Updated | Fixed |   
CDS-94268 | Bug | CLONE - Compiler: Wrong value for property without monitoring attribute | Fixed |   
CDS-94266 | Bug | CLONE - ProjectCompare: Compare might crash if only one SafetyDiffViewerNotImplementedFactory is present | Fixed |   
CDS-94264 | Bug | CLONE - EtherCAT, Scan Dialog: SubDevices are not inserted if no entry is selected in the list of slaves found | Fixed |   
CDS-94263 | Bug | CLONE - Compiler: Output of Function block called in Method leads to assigned variable being TRUE | Fixed | [[GENERAL]]  
Fixed for Compiler Version >= 3.5.21.20  
CDS-94229 | Improvement | CLONE - DM / VxWorks : implement exclude external for Contrib/OpenSSL in VxWorks buildsystem | Fixed | [[CompatibilityNote]]  
Delivery manager Feature is not available for SP21 P2, actions must be added manually to customer build profile. See comments for details.  
CDS-94221 | Improvement | CLONE - Library Repository: Hook or OEM customization needed to select libraries to be installed into local-repository | Fixed |   
CDS-94218 | Bug | CLONE - Project settings, Users and Groups: Unhandled exception after three failed attempts to change usergroup password | Fixed |   
CDS-94197 | Bug | CLONE - FileBasedStorage: Application properties are marked as modified even though nothing has been changed | Won't Fix | [[GENERAL]]  
Won't Fix because the intended small scale changes to fix this issue lead to regressions with the existing svn and git integrations. We plan to create a better solution with SP22 but since this better solution affects much more code and needs changes in the UI we don't intend to patch it.  
CDS-94196 | Bug | CLONE - "EXCEPTION [License invalid]" after modifying symbol configuration and download of application in logged in state | Cannot Reproduce |   
CDS-94194 | Bug | CLONE - PLCHandler: Array variable communication failure by wrong data size from PLCHandler | Fixed |   
CDS-94193 | Improvement | CLONE - SecurityScreen: MinAsymmetricKeySize from RTS should be used in Addon Security Manager | Fixed | [[GENERAL]]  
\- When creating new certificates from the SecurityScreen, the configured SecuritySetting "RSAMinKeyLen" of the PLC will be now queried to prevent creating invalid certificates for the PLC.  
\- requires the Addon "CODESYS Security Agent" in Verion >= 1.4.0.0  
CDS-94191 | Bug | CLONE - Wrong code generated for output assignment in call-by-reference | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.21.20  
CDS-94161 | Bug | CLONE - Structure of Syslog message is not RFC conforming | Won't Fix | [[GENERAL]]  
Fixes for non-major issues are released as service packs, not patches.  
CDS-94159 | Improvement | CLONE - Update Device Dialog: Redirect Pre-Selection (Usability) | Fixed |   
CDS-94109 | Improvement | CLONE - Runtime Password Policy: Change default of maximum values | Won't Fix | [[GENERAL]]  
It was decided that this issue will not be fixed for patch 2.  
CDS-94108 | Bug | CLONE - Event EVT_EthPacketArrived not always triggered under load | Fixed |   
CDS-94087 | Bug | CLONE - CmpOPCUAClient: Exception in OPCUAClient task | Fixed |   
CDS-94051 | Bug | CLONE - Update Device: after update device the datatype (declared as rangetype) is not updated | Fixed |   
CDS-94050 | Bug | CLONE - Compile: Internal error for static variable in Functionblock initialized with local constant | Fixed | [[GENERAL]]  
Fixed for Compilerversion >= 3.5.21.20  
CDS-94031 | Improvement | CLONE - CmpOPCUAStack: Add audit logs to OpenSecureChannel and CloseSecureChannel as well as to ValidateCertificate | Won't Fix | [[GENERAL]]  
Cannot be patched, because the codebase is not existing in 3.5.21.x  
CDS-93982 | Bug | CLONE - Runtime doesn't compile wit openwrt-sdk-21.2.7 | Fixed |   
CDS-93979 | Bug | CLONE - Device: IO Addresses get modified on Open project in SP20P31 | Fixed |   
CDS-93966 | Bug | CLONE - VxWorks Multicore : IEC FreeFloating tasks require setting of global variable before runtime start and CFG file setting | Fixed |   
CDS-93944 | Bug | CLONE - Trace Packet Configuration, UpdatesAfterTrigger: it is not possible to use a PostTrigger > 255 with the Traceconfig file. | Fixed |   
CDS-93927 | Bug | CLONE - Refactoring: Renaming an FB instance leads to rename of call (FBD, LD & CFC) | Won't Fix | [[GENERAL]]  
Investigation showed that the described problems are located within the LDFBD and CFC Addons and cannot be fixed in CODESYS itself and therefore the fix also cannot be applied to Patch 2.  
CFC-248 and LDFBD-408 will be used for individual fixes within the Addons.  
CDS-93862 | Bug | CLONE - Linux SysEventWait returns after arbitrary time | Fixed | [[GENERAL]]  
If runtime is build with toolchain glibc >= 2.30, SysEventWait uses static call of sem_clockwait  
CDS-93861 | Bug | CLONE - LMM: NullRef Exception in SideCarEntryHelper in case of no primary project | Fixed |   
CDS-93860 | Improvement | CLONE - Customization of license finder | Won't Fix | [[GENERAL]]  
The CODESYS Store button can already be hidden by returning null for the OEM Customization  
Section: LicenseManager  
Key: LicenseFinderUri  
CDS-93859 | Bug | CLONE - IoDrvSafetySP: crash with attached project | Fixed |   
CDS-93820 | Improvement | CLONE - SysCpuMultiCore: Provide SysMCGetCurrentCoreID for IEC code | Fixed |   
CDS-93800 | Bug | CLONE - CmpOPCUAServer, CmpOPCUAStack, CmpOPCUAClient: Missing USEEXTERN_STMT in some files | Fixed |   
CDS-93760 | Bug | CLONE - CmpRetain: Error in the management of retain segments | Fixed |   
CDS-93759 | Improvement | CLONE - Remove placeholder resolution of "CAA FB Factory" from all Devices | Won't Fix | [[GENERAL]]  
Currently, placeholder resolution of "CAA FB Factory" is still necessary.  
CDS-93758 | Bug | CLONE - Drag and Drop: If an object in the device tree is not dropped exactly on the right spot, object gets moved to POU-pool | Cannot Reproduce | [[GENERAL]]  
The described behaviour ist not reproducable anymore, as it was already fixed with CDS-93260.  
CDS-93755 | Bug | CLONE - First and Last Slave change position during insert into project | Fixed |   
CDS-93728 | Bug | CLONE - RTE: Scheduler: Possible Jitter in highest priority IEC Task in case of dynamic task creation. | Fixed |   
CDS-93699 | Bug | CLONE - CmpRetain: Define of CMPPLCSHELL_NOTIMPLEMENTED is not used for calling RetainAddSRAMPlcShellCommands() | Fixed |   
CDS-93664 | Bug | CLONE - TargetVisu: Security issues in Qt versions before 6.9.1 | Fixed |   
CDS-93661 | Bug | CLONE - ControlWin: Login takes much longer in special environments and could lead to network license blockings | Fixed | [[COMPATIBILITY_INFORMATION-EndUser]]  
The use of the CmRuntime server-search list (default is broadcast) is now deactivated. If this feature is needed, it can be activated with [CmpCodeMeter] UseCodeMeterServerSearchList=1  
  
[[KNOWN_LIMITATIONS]]  
The CmRuntime server-search list does not work with application based licenses.  
Use the setting [CmpCodeMeter] LicenseServer.[1-9]=<IP> instead.  
CDS-93656 | Improvement | CLONE - CmpStd.h: Add support for new data type RTS_IEC_LDATE, RTS_IEC_LDATE_AND_TIME/RTS_IEC_LDT and RTS_IEC_LTIME_OF_DAY/RTS_IEC_LTOD | Fixed |   
CDS-93655 | Bug | CLONE - Application Info: Garbled characters in Application Info | Fixed |   
CDS-93625 | Improvement | CLONE - CmpOPCUAServer: Add AuditLog message for session services | Fixed |   
CDS-93324 | Bug | CLONE - Generate Code: ELSIF without condition in pragma leads to Internal Error | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.21.20  
CDS-93286 | Improvement | CLONE - Logger: New feature needed to upload all stored logfiles of a logger instance on request | Won't Fix | [[GENERAL]]  
It was deceded that this issue is not needed for Patch 2 and will therefore not be fixed for this version.  
CDS-93032 | Improvement | CLONE - CmpOpenSSL: MinAsymmetricKeySize from RTS should be used in Addon Security Manager | Fixed | [[GENERAL]]  
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
CDS-93026 | Bug | CLONE - CmpSchedule : Incorrect processor load calculation for external triggered + freewheeling tasks | Fixed |   
CDS-92928 | Bug | CLONE - CmpRedundancy: Memleak in automatic synchronization under certain conditions | Cannot Reproduce |   
CDS-92005 | Improvement | CLONE - Add Option for Connection Timeout Gateway <-> PLC | Won't Fix | [[GENERAL]]  
This Issue was already implemented in SP20 with CDS-85801, therefore there is nothing to do here.  
CDS-92002 | Improvement | CLONE - Online: Add logging functionality for exeptions | Won't Fix | [[GENERAL]]  
This issue cannot be fixed for technical reasons - the amount of code changes exceeds the maximum number of commits.  
  
 

CODESYS AddOns  |  Version   
---|---  
CODESYS Automation Server Connector | 1.36.0.0  
CODESYS Base Libraries | 4.0.0.0  
CODESYS SoftMotion | 4.18.0.0  
CODESYS Security Agent | 1.4.0.0  
CODESYS C Code Integration | 4.0.0.0  
CODESYS Core Dump | 4.2.0.0  
CODESYS Code Generator ARM | 4.0.3.0  
CODESYS Code Generator ARM64 | 4.0.1.0  
CODESYS Code Generator Blackfin | 4.0.0.0  
CODESYS Code Generator Cortex M3 | 4.0.1.0  
CODESYS Code Generator PowerPC | 4.0.1.0  
CODESYS Code Generator RX | 4.0.0.0  
CODESYS Code Generator SH | 4.0.0.0  
CODESYS Code Generator TIC28x | 4.0.0.0  
CODESYS Code Generator TriCore | 4.0.1.0  
CODESYS Compiler Versions Archive | 4.0.0.0  
CODESYS Communication | 4.6.0.0  
CODESYS RISC Front End | 4.0.2.0  
CODESYS Target Settings Export | 4.0.0.0  
CODESYS Trace | 4.2.0.0  
CODESYS IO-Link | 4.3.0.0  
CODESYS Safety Support | 4.0.0.0  
CODESYS Redundancy | 4.2.0.0  
CODESYS NetX | 4.0.0.0  
CODESYS Memory Tools | 4.1.0.0  
CODESYS Modbus | 4.4.0.0  
CODESYS Ethernet Adapter | 4.2.0.0  
CODESYS EtherCAT | 4.9.0.0  
CODESYS CANopen | 4.3.0.0  
CODESYS EDS Import | 4.2.0.0  
CODESYS EtherNetIP | 4.7.1.0  
CODESYS PROFIBUS | 4.2.0.0  
CODESYS SAE J1939 | 4.2.0.0  
CODESYS PROFINET | 4.7.0.0  
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
CODESYS String Libraries | 4.0.0.0  
CODESYS Library Dependency Inspection | 1.1.0.0  
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2025 CODESYS GmbH  | A member of the CODESYS Group 
