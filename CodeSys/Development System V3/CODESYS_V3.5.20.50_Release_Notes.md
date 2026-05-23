[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS V3.5 SP20 Patch 5

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
CDS-92908 | Improvement | CLONE - Add new Base Libraries Addon to setup | Fixed | [[GENERAL]]  
Latest versions of six basic libraries have been moved to a new Base Libraries add-on in the setup, which can be updated independently (Element Collections, Common Behaviour Model, Net Base Services, Segmented Buffer Manager, SharedData Utilities for MultiCore, Asynchronous Job Manager).   
  
Package is required by other packages like Visualization (4.7.0.0) or EtherNetIP (4.7.1.0)  
CDS-92829 | Bug | CLONE - LicenseManager: Parse license container serial number out of info string via "SN=" | Fixed |   
CDS-92806 | Bug | CLONE - IntelliSense not working at Conversion Function | Fixed |   
CDS-92706 | Bug | CLONE - CmpCodeMeter: Container field "SerialNumber" broken for service SRV_CODEMETER_READ_CONTAINER_LIST | Fixed |   
CDS-92704 | Improvement | CLONE - Linux: SysTaskLinux: sync/starttime mechanism for cyclic SysTasks via setting | Cannot Reproduce | [[GENERAL]]  
Already got cloned to Patch 1  
CDS-92703 | Improvement | CLONE - Linux: IEC task start offset - configuration from IEC code | Fixed | [[GENERAL]]  
\- New IEC CmpIecTask.library functions available to set and get IEC task offset  
  
FUNCTION IecTaskSetStartOffset : RTS_IEC_RESULT  
VAR_INPUT  
/// IEC task name  
sIecTaskName : STRING;  
/// Start offset in milliseconds from calculated task start  
startOffsetUs : DINT;  
END_VAR  
  
The function must be called for all synchronized tasks, even if the offset is 0.  
  
[[KNOWN_LIMITATIONS]]  
\- Only supported for linux targets yet! Has no effect on other platforms!  
\- A maximum of 30 tasks can be synchronized. Any synchronized task with an index higher than 29 will be ignored.  
\- Task cycle may not be greater than 500ms.   
\- The cycle time of each synchronized tasks must be a divider of 1s (i.e. 500 ms, 250ms, 200 ms etc.).  
\- Only for supported for tasks with realtime priority.  
CDS-92702 | Bug | CLONE - SysTaskLinux: sync/starttime mechanism not working for long Task-names | Fixed |   
CDS-92054 | Improvement | CLONE - Update InstallShield to latest version 2024 R1 | Fixed | [[GENERAL]]  
InstallShield 2024 R1 is used to build the setups.  
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2025 CODESYS GmbH  | A member of the CODESYS Group 
