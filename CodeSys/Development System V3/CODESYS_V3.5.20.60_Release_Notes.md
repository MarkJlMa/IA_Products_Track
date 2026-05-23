[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Release Notes: CODESYS V3.5 SP20 Patch 6

Key  |  Issue Type  |  Summary  |  Resolution  |  Note   
---|---|---|---|---  
CDS-93404 | Bug | CLONE - Breakpoint, Stepping: Current position not shown for Function blocks in library | Won't Fix | [[GENERAL]]  
The bugfix of CDS-90439 in SP21 source code does not fix the problem in SP20. Other, currently unknown bugfixes are necessary.  
CDS-93350 | Bug | CLONE - UpdateEnvironment: Placeholder is resolved to an old version, despite All To Newest | Fixed |   
CDS-93260 | Bug | CLONE - ObjectManager: Folder turns into project object after undo | Fixed | [[GENERAL]]  
Fix bug with wrong parent information used during undo of removed objects.  
CDS-93230 | Bug | CLONE - LicenseMetrics: TaskGroupAssignmentMetric is not updated correctly after changes to Task Configuration | Fixed |   
CDS-93091 | Bug | CLONE - Specific Project: Duplicated objects (same name, same object) in the POUs part | Won't Fix | [[GENERAL]]  
The causing issue CDS-93260 will be patched instead.  
CDS-93023 | Bug | CLONE - Breakpoints set in FB-Instances of Libraries, will not be shown correctly | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.20.60  
CDS-92954 | Bug | CLONE - IECTextEditor: Missing inline monitoring and breakpoint positions when stepping into compiled library with reloaded source library | Won't Fix | [[GENERAL]]  
The risk analysis for this cloned issue revealed a high risk for migrating the source code of SP22 to the older version SP20 Patch 6. This high risk is due to the fact that the overall infrastucture for the fix is not existing in SP20 Patch 6 and therefore we cannot guarantee that no negative side-effects are introduced. Therefore, development department and product management agreed to not fix this issue in the requested version.  
CDS-92927 | Bug | CLONE - CmpRedundancy: Memleak in automatic synchronization under certain conditions | Won't Fix | [[GENERAL]]  
Main issue not fixed at the time of code close.  
CDS-92873 | Bug | CLONE - Only code of compiled library is shown, when compiled lib would be opened with locally stored library. | Fixed |   
CDS-92872 | Bug | CLONE - [Scan] Missing Subdevice after Scan/Import | Fixed |   
CDS-92755 | Bug | CLONE - License Manager doesn't show unactivated licenses | Fixed |   
CDS-92001 | Bug | CLONE - Downloading Application: not all existing applications are shown with detailed informationor for editing/deleting | Fixed | [[GENERAL]]  
This fix adds an additional prompt to delete or keep unknown applications that are present on the PLC but not in the project. This prompt is triggered when a new application is downloaded.  
This fix does not change the way how a reset of an application is done.  
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2025 CODESYS GmbH  | A member of the CODESYS Group 
