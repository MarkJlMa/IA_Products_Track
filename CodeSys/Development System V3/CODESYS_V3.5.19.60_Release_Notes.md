[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Product: CODESYS V3.5 SP19 Patch 6

Key  |  Issue Type  |  Summary  |  Resolution  |  Release Note   
---|---|---|---|---  
CDS-88792 | Bug | CLONE - RTE: Control RTE MC SL license not working any more | Fixed |   
CDS-88743 | Bug | CLONE - PLCHandler memory leak with parameter DontLoadSymbolsFromPlc set to 1 | Fixed |   
CDS-88580 | Bug | CLONE - AppBased Licenses: Exception on Download after downloading an application with zero I/O data | Fixed |   
CDS-88575 | Bug | CLONE - PLCHandler: Linux: Disconnect blocks for several seconds when exiting old update threads | Fixed |   
CDS-87870 | Bug | CLONE - SysTaskLinux: Add missing SysTaskSetDeleted in SysTaskEnd | Won't Fix | [[GENERAL]]  
Wont fix as original problem will be solved in PLChandler.  
CDS-87819 | Bug | CLONE - Compiler: Null reference exception from locator if using method with any type | Fixed | [[GENERAL]]  
With Compiler Version >= 3.5.19.60 the changes for the issue CDS-86765 are reverted. So the problem described in CDS-86765 will occur again in Patch 6. A proper resolution of the problem will be released with SP 20.  
CDS-87817 | Bug | CLONE - DeviceRepository: stack overflow with new ESI file | Fixed |   
CDS-87816 | Bug | CLONE - PLCHandler Interface Gateway3: delete[] / delete mismatch | Fixed |   
CDS-87747 | Improvement | CLONE - [Setup] OEM adaption for productPathComponent and repositoryRoot | Fixed | [[GENERAL]]  
For more information see the documentations "CODESYS Installation Extended OEM Adaptions".  
CDS-87702 | Improvement | CLONE - Add CODEYS Ladder to setup | Cannot Reproduce | [[GENERAL]]  
CODESYS Ladder was added with Patch 3  
CDS-87699 | Improvement | CLONE - [Setup] Sandbox light: install the repositories in a separate path | Fixed | [[GENERAL]]  
If the CDS_SEPARATE_REPO property is set to 1, the setup installs the repositories in a separate path. This path is deleted on uninstallation.  
The default value for the property is 0, so the repositories continue to be installed in the default folder %PROGRAMDATA%\CODESYS.  
For more information see the documentation "CODESYS Installation Extended OEM Adaptions" and CODESYS Installation OEM Adaptions"  
CDS-87692 | Improvement | CLONE - Package Manager: Resolve REPOSITORY_LOCATION from RepositoryLocations ini | Fixed |   
CDS-87648 | Bug | CLONE - DeviceObject: Changing PLC settings results in an unhandled exception of CODESYS | Fixed |   
CDS-87647 | Bug | CLONE - VFTable and FPVariables might not be initialized with enabled multithreading | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.60  
CDS-87425 | Bug | [WinCE] PLCHandler builds fails with openssl update | Fixed |   
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2024 CODESYS GmbH  | A member of the CODESYS Group 
