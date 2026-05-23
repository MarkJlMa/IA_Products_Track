# CODESYS Safety Extension Release Notes

---

## Version 4.2.0.0

[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS Safety Extension 4.2.0.0

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
SAFETY-129 | Bug | CLONE - Addon "Safety Extension" crashes if specific OPT files exist | Won't Fix | [[GENERAL]]  
This clone is not needed anymore because the main issue is in the same version and does not need to be patched.  
SAFETY-125 | Improvement | Safety Color: Interface to set SafetyIcons | Fixed |   
SAFETY-123 | Bug | SafetyEditor: Opening editor for particular safety device does not work | Fixed |   
SAFETY-120 | Bug | Addon "Safety Extension" crashes if specific OPT files exist | Fixed |   
SAFETY-105 | Improvement | Safety AppBased: License metrics for safety PLCs | Fixed | [[GENERAL]]  
Added two new metrics to support AppBasedLicenses for SAFETY SIL3 Extension.  
1\. Number of safe connections: Counts all safety logical IOs unter the device.  
2\. PROFIsafe modules present: 1, if any safety logical IOs that are PROFIsafe devices under the main device exist. 0 otherwise.  
SAFETY-90 | Epic | SafetyExtension for CODESYS SP17 | Won't Fix | [[GENERAL]]  
This epic is not needed anymore as there will be no migration to SP17. Instead, SIL3 will be migrated to run on SP19 and newer as part of SAFETY-12.  
SAFETY-89 | Improvement | Deactivate auto-creation of variables in IO mapping for type SAFESTRUCT | Won't Fix | [[GENERAL]]  
As already implemented with SCDS-1848, creation of default mappings for I/O channels can be inhibited by serving the following OEM customization with value "true":  
Section: SafetyEditor  
Key: NoDefaultMappings  
SAFETY-84 | Improvement | Change description text (package manifest) for safety add-on CODESYS Safety | Fixed |   
SAFETY-65 | Improvement | PSH 2.6 Support: Support protocol type id for PROFIsafe Host 2.6 | Fixed |   
SAFETY-54 | Bug | ExtensionSafetyOnline: Wrong calculation of communication buffer | Won't Fix | [[GENERAL]]  
This issue is not needed anymore because it was caused by an inconsistent configuration of buffer settings on the runtime sides. The problem has already been solved by correctly increasing the communication buffer on the standard PLC. Now the standard buffer is bigger than the buffer of the safety communication that needs to be tunnelled by the standard PLC. This configuration ensures the best possible performance of the communication and no additional tweaking on the IDE side is needed.  
SAFETY-50 | Improvement | SafetyEditor: Use LongPath-Utilities when accessing SDD files | Fixed |   
SAFETY-44 | Bug | Logical IOs: Ambiguous use of name in Safety-related project | Fixed |   
SAFETY-42 | Improvement | [Dev] Adapt "SafetyVersion" and the related unit test to match its Tool Integrity Level (=TIL-1) | Fixed |   
SAFETY-39 | Bug | Template for Empty Safety Project references old Visualization profile | Fixed |   
SAFETY-37 | Improvement | Safety Color: Interface to set Safety Color | Fixed |   
SAFETY-31 | Epic | Safety SIL3: Support Backtick Identifiers | Fixed |   
SAFETY-24 | Bug | SIL3: IDE crashes when creating/working with the network variables | Fixed |   
SAFETY-19 | Bug | Package: Package dependencies missing | Won't Fix | [[GENERAL]]  
The reference to the ARM Code Generator in old device descriptions is an unfortunate legacy. It has been removed from the current device description with SAFETY-75. Device manufacturers can adapt their device descriptions accordingly.  
  
Therefore, there is no need to update the package references because the new Safety Extension v4.2.0.0 has no requirements to other packages.  
SAFETY-18 | Improvement | [Config] Use nuget package for Newtonsoft.json and update to latest version 13.0.1 | Duplicate | [[GENERAL]]  
This issue was already fixed with SAFETY-27.  
SAFETY-12 | Epic | SafetyExtension for CODESYS 64bit | Fixed | [[KNOWN_LIMITATIONS]]  
As the safety addon cannot handle precompile caches, using the cache will get deactivated, when the Safety Extension is installed.  
SAFETY-1 | Epic | Tool Qualification SIL3 AddOn | Fixed |   
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2024 CODESYS GmbH  | A member of the CODESYS Group 


---

## Version 4.3.0.0

[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS Safety Extension 4.3.0.0

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
SAFETY-241 | Bug | Canceling the "clean" command still deletes the compile information | Fixed |   
SAFETY-226 | Improvement | Copy Safety Application ID to clipboard | Duplicate |   
SAFETY-202 | Bug | [IO]: Repeating names in IO-mappings when adding them via "Scan for Devices" | Fixed |   
SAFETY-201 | Bug | Exception on closing CODESYS | Fixed |   
SAFETY-191 | Bug | CODESYS GIT Safety Task commit not possible | Fixed |   
SAFETY-190 | Bug | Incorrect communication TAN after update device | Won't Fix | [[GENERAL]]  
There is nothing to fix for this issue in the Safety Extension because the TANs sent to the runtime are already correct and there is no need to change anything. Instead, the problem is caused by a suboptimal check of the connection IDs on the runtime side and will be handled independently with SIL3SL-646.  
SAFETY-188 | Bug | Auto Declare: It is not possible to select the instance of the available FSoEMaster | Fixed |   
SAFETY-186 | Improvement | New application state: No online application state within the state "Wait for operator confirmation to start the bootapplication" | Fixed |   
SAFETY-184 | Improvement | Safety Oberfläche: Logout auf Sys_Err response bei Appstatus service | Fixed |   
SAFETY-176 | Bug | SafetyTaskEditor: Editor cannot be opened on Chinese Windows | Fixed |   
SAFETY-82 | Improvement | SoftSafety: Show app based license metrics for safety applications | Duplicate | [[GENERAL]]  
Duplicates SAFETY-105  
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2025 CODESYS GmbH  | A member of the CODESYS Group 


---

## Version 4.4.0.0

[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS Safety Extension 4.4.0.0

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
SAFETY-306 | Improvement | Weak Code Checksum: Adapt View of Checksum | Fixed | [[GENERAL]]  |
SAFETY-300 | Bug | SafetyObjects: Drag'n'Drop of a SafePOU on a SafeTask deletes the SafePOU | Fixed| 
SAFETY-298 | Improvement | Read Safety Application ID: Enable command in context menu | Fixed |   
SAFETY-295 | Bug | Online Change vPLC: connection loss, not possible to send application | Fixed |   
SAFETY-293 | Improvement | SafeNetVar: Increase number of receivers per sender | Fixed | [[GENERAL]]|
SAFETY-290 | Bug | SafetyEditor: Remove OEMCustomization for disabling precompile cache. | Fixed |   
SAFETY-274 | Bug | Exception in editor when doubleclicking a variable and moving mouse while holding second click | Fixed |   
SAFETY-268 | Improvement | Safety Extension: Adjustments to the function "Read Safety Application ID" | Duplicate |   
SAFETY-266 | Bug | Multiple dialogs with "Mapping channel type "float" is not supported", no further input in CODESYS possible | Fixed |   
SAFETY-239 | Bug | Input Assistent: Assistent does not show FB instances of logical devices | Cannot Reproduce |   

© 2025 CODESYS GmbH  | A member of the CODESYS Group 


