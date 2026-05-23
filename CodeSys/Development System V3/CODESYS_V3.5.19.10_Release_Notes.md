[ ![CODESYS GmbH](https://www.codesys.com/fileadmin/data/Images/Download/CODESYS_logo_ds.svg) ](https://www.codesys.com)

  * [ All Release Notes ](https://www.codesys.com/the-system/codesys-release-notes "All Release Notes")

## Product: CODESYS V3.5 SP19 Patch 1

Key  |  Issue Type  |  Summary  |  Resolution  |  Release Note   
---|---|---|---|---  
CDS-85810 | Improvement | CLONE: VxWorks: Support ARM64 | Fixed | [[KNOWN_LIMITATIONS]]  
* Runtime exception handling is not working reliably. See CDS-85733  
* Redundancy feature is not yet tested and should not be used for production.  
CDS-85735 | Bug | CLONE - RTE CX Example Project has a Warning due to old EtherCAT Task | Fixed |   
CDS-85678 | Bug | CLONE - CmpIoMgr : IO driver parameter access fails in specific environment - step2 | Fixed |   
CDS-85593 | Improvement | CLONE - Remove untested CmpBACnet2 from Platforms/VxWorks | Fixed |   
CDS-85502 | Bug | CLONE - DeviceObject: type list from devdesc is not available after new types are added by plugin | Fixed |   
CDS-85495 | Bug | CLONE - MessageView: "InvalidProjectHandle" exceptions are slowing down the loading of projects | Fixed |   
CDS-85487 | Improvement | CLONE - Compile: Fast Online for large projects slows down due to stack check | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.0  
With the compiler define "suppress_stack_check" set in the build options of the application the check for the stack usage can be disabled.  
CDS-85486 | Improvement | CLONE - Online Change: Only retypify complete application if unqualified GVL changes | Won't Fix | [[GENERAL]]  
The change is in very sensitive parts of the code. The fix improves the performance considerably, by about 30 %. But this is not enough to justify the risk of Accidents in Online Change code.  
Full regression tests are required for this issue.  
CDS-85485 | Improvement | CLONE - Online Change: Improve message output regarding actually compiled POUs | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.10  
CDS-85463 | Bug | CLONE - SysDrv3S: Wrong datatype used for PCI_INFO.ulBusNr | Fixed | [[GENERAL]]  
This fix was made to also support CODESYS V2 with the same driver version. We aren't aware of any use case where this fix is relevant for CODESYS V3.  
  
If you nevertheless want to use the new driver version, you must manually update the SysDrv3S.sys driver to the latest version V3.5.19.10:  
\- In the Microsoft Windows Device Manager right-click on the Hilscher device to open the context menu.  
\- Select Update driver within this.  
\- Install the driver from the subdirectory "./Driver" of your CODESYS Development System or CODESYS Control installation directory.  
\- Check the driver version after the update. The driver must have version number 3.5.19.10.  
CDS-85440 | Bug | CLONE - NBS: UDP_Receive output 'udiPortFrom' not working | Fixed |   
CDS-85413 | Bug | CLONE - SVG-Renderer: Update OSS to latest versions (libcurl 8.0.1, cairo 1.17.8, libpng 1.6.39, libjpeg-turbo 2.1.5.1, libxml2 2.10.4) | Fixed | [[GENERAL]]  
Updated libcurl.dll to version 8.0.1  
Updated libxml2.dll to version 2.10.4  
Updated libpng to 1.6.39  
Updated cairo to 1.17.8  
Updated libjpeg-turbo to 2.1.5.1  
  
[[COMPATIBILITY_INFORMATION]]  
The update of cairo might cause some texts that are part of an SVG to be moved by 1px. We consider this as not problematic as images hardly contain texts.  
CDS-85404 | Improvement | CLONE - Installer Integration: RequiredAddonService should be able to be switched off | Fixed | [[GENERAL]]  
Analysis can be skipped during XML import by OEM customization with the following hook  
Section: InstallerIntegration  
Key: DisableAddonService  
Value: true  
The events triggering the service have been switched to project structure changed event.  
CDS-85403 | Improvement | CLONE - BACnet: BACstack - update to BACstack V25.1.2.1 | Duplicate |   
CDS-85402 | Improvement | CLONE - BACnet: BACstack - update to BACstack V25.1.5.1 | Fixed |   
CDS-85401 | Bug | CLONE - Compile: Array of Alias of Array with initialisation reports unexpected errors | Fixed | [[GENERAL]]  
Compiler Version >= 3.5.19.10  
CDS-85325 | Bug | CLONE - Frame: CommandInfoCache causes GDI Leak | Fixed | [[GENERAL]]  
Icons have been removed from command info cache. Missing commands will only have a name and description.  
CDS-85278 | Bug | CLONE - Compiler: Compile errors with special customer device settings | Fixed |   
CDS-85272 | Improvement | CLONE - CmpIecTask: IecTasksWaitForStop( ): Adjust tSleepMs timeout | Fixed |   
CDS-85244 | Bug | CLONE - WebBrowserIntegration: StartPage configured in Options shall be an allowed target | Fixed |   
CDS-85243 | Improvement | CLONE - Project Compare: Add interface so that plugins can better decide to hide/show objects in a diff view | Fixed |   
CDS-85239 | Improvement | CLONE - Licensed Software Metric: OEM Customization Hook to hide metrics in the presentation layer | Fixed | [[GENERAL]]  
There is a new OEMCustomization Hook that returns the product codes of the licenses to hide in the presentation layer  
Section: LicensedSoftwareMetrics  
Key: ProductCodesToHide  
Datatype: HashSet<uint>  
CDS-85237 | Improvement | CLONE - Make it possible to store V3 Libraries without signature | Fixed |   
CDS-85236 | Bug | CLONE - Compiler: Instancepath is not correctly set in Childapplications | Won't Fix | [[GENERAL]]  
.  
CDS-85235 | Bug | CLONE - Software license metrics: Too simple check for not available licenses | Fixed |   
CDS-85228 | Bug | CLONE - ProjectLanguageModelProvider: BackendGuid target setting is evaluated wrong | Fixed |   
CDS-85227 | Bug | CLONE - DeviceObject and ScriptDriverDevices: import_io_mappings_from_csv broken with CODESYS V3.5.19.0 | Fixed | [[GENERAL]]  
Accident by CDS-82588.  
CDS-85226 | Bug | CLONE - License Manager: error dialog only display error code instead of an information of the error | Fixed |   
CDS-85177 | Bug | CLONE - VxWorks: SysSockGetHostbyName() returns wrong values | Fixed |   
CDS-85149 | Improvement | CLONE - Extend AuthZipFile to support additional signatures and use these signatures for usercode detection | Fixed |   
CDS-85119 | Bug | CLONE - NBS: TCP_Client can not work over TLS without CertInfo | Fixed |   
CDS-85118 | Bug | CLONE - Compile: Stack overflow detected although it should not | Won't Fix | [[GENERAL]]  
The stack check is a worst case analysis. The calculated stack seems to be correct. The reported call stack, however, is not complete. The calculated stack size for each function only considers the local stack size, and not the stack size that is allocated by the caller.  
But the functions reported in the call stack are potentially called in this order and allocate large objects on the stack.  
It is absolutely possible that some functions in the call stack are never actually executed and there won't be the same stack consumption at runtime. Nevertheless, you should try to avoid a large stack consumption, and large value objects on the stack.  
The reported project contains several large objects on the stack, that are used to copy information. Check these situations, whether it is possible to use references.  
A new issue has been created : CDS-85446 to fix some problems in the reported call stack.  
CDS-85100 | Bug | CLONE - CmpOpenSSL: Update OpenSSL to most recent version 1.1.1t | Fixed |   
CDS-85098 | Improvement | [Setup] Update CODESYS Softmotion to 4.14.0.0 | Fixed |   
CDS-85083 | Bug | CLONE - CmpIoMgr : IO driver parameter access fails in specific environment | Fixed |   
CDS-85082 | Bug | CLONE - Device Tree: Generate code leads to errors for a project containing devices plugged in slots | Fixed |   
CDS-85080 | Bug | CLONE - CmpRedundancyConnectionIP: Write Settings and Controller reboot lead to Socket Error 0x208 | Won't Fix | [[GENERAL]]  
The problem is that after rebooting the Linux system, the CODESYSControl runtime system starts automatically and tries to open the TCP sockets/communication too early because they are not available at that time. For the specific system, the default (5000 ms) for the BootupWaittime is too short.  
  
Increasing the value of the following setting solves this problem:  
[CmpRedundancy]  
BootupWaitTime  
CDS-85077 | Improvement | CLONE - 3s.dat: Implement switching in CmpCodeMeter for new license model | Fixed |   
CDS-85068 | Bug | CLONE - [Delivery] Setup Sources Zip does not contain MicrosoftEdgeWebview2Setup and Installer | Fixed |   
CDS-84981 | Bug | CLONE - Memory Leak with activated Overlay-Visu | Fixed |   
CDS-84978 | Bug | CLONE - Compile: Stack overflow is not detected, if function block implements derived interface | Won't Fix | [[GENERAL]]  
Due to this fix, the stack usage of methods might be estimated higher since it is a worst case analysis. This might lead to projects that currently compile and also work without errors, now fail with compile errors. So it should not be patched.  
CDS-84907 | Bug | CLONE - License Manager: License activation not possible on dongle connected to PLC | Fixed |   
CDS-84898 | Bug | CLONE - Comparison in GetLocalizedString-Method does not work in every case | Fixed |   
CDS-84896 | Bug | CLONE - SysDrv3S can not be installed on clean systems | Fixed |   
CDS-84882 | Bug | CLONE - Refactoring: Renaming variables declared after an initialized ALIAS variable does not rename the variable declaration | Fixed | [[GENERAL]]  
CompilerVersion >= 3.5.19.10  
CDS-84881 | Bug | CLONE - SmartCoding: Library namespace not shown in case it has same name as enum values inside other library | Won't Fix | [[GENERAL]]  
The bug is of low priority and is in Code since many versions. A patch to a released version is too risky.  
CDS-84880 | Bug | CLONE - Project Compare: Differences shown in Visualization Manager, although it should not | Won't Fix | [[GENERAL]]  
The implementation of this bugfix was done in the Visualization AddOn (-> VIS-2806).   
Therefore the issue cannot be fixed as a Clone in CODESYS Essentials and an update of the CODESYS Visualization can be done instead to solve this problem.  
CDS-84870 | Bug | CLONE - CMUtils / Hash: OPC UA Server: Exception on reset cold with new symbol configuration (Linux Device) | Fixed |   
CDS-84869 | Bug | CLONE - LanguageModelManager: task cross references are not updated as expected | Won't Fix | [[GENERAL]]  
The issue with broken IO-Data was fixed with a seperate profinet issue PN-502.  
The issue that the compiler might report too many crossreferences in some situations. Removing these crossreferences will severly reduce the performance of online changes. After some investigation we are sure that these additional crossreferences will never reference variables that don't exists or that any crossreferences will miss. The next normal onlinechange will fix the crossreferences again.  
CDS-84868 | Bug | CLONE - Go to Definition: Command 'Go to Definition' should open the method in an offline editor | Fixed |   
CDS-84765 | Bug | CLONE - QNX 7.1 / Cortex : Communication Channel timeouts | Fixed | [[COMPATIBILITY_INFORMATION-OEM]]  
QNX Runtimes running on multicore systems now pin to first cpu by default. This behavior might be changed by command line parameter "-c" and providing a cpu mask.  
CDS-84754 | Bug | CLONE - VxWorks / C++ : Definition of max/min in sysspecific.h collides with C++ 17 build | Fixed | [[GENERAL]]  
Fixed clash with min/max macro under VxWorks with c++17  
CDS-84751 | Bug | CLONE - SysSocketVxworks.c : Explicit cast required to avoid compile error (VxWorks 22.06) | Fixed |   
CDS-84743 | Bug | CLONE - Software license metrics: Child applications are not considered in the codesize metric | Fixed |   
CDS-84731 | Bug | CLONE - Linux: assertion in Targetvisu code generates runtime exception | Fixed |   
CDS-84708 | Bug | CLONE - CmpX509CertItf.m4 : Missing dependency for SysTimeItf.m4 | Fixed |   
CDS-84680 | Bug | CLONE - Compiler, Generics: Generic type can only be used with source library | Fixed | [[GENERAL]]  
Compilerversion >= 3.5.19.10  
CDS-84628 | Bug | CLONE - BACnet: BACstack - BACstackV23/24 - fix Audit-Reporter recursive call | Cannot Reproduce | [[GENERAL]]  
Fixed with Update of BACstack to version 25.1.5.1 --> can not reproduce --> close  
CDS-84627 | Improvement | CLONE - BACnet: BACstack - BACstackV24 - BACnetAuthorizationExemption missing | Cannot Reproduce | [[GENERAL]]  
Fixed with Update of BACstack to version 25.1.5.1 --> can not reproduce --> close  
CDS-84626 | Bug | CLONE - BACnet: BACstack - BACstack 24.1.33.1 - error reading number of elements in ARRAY property reading element 0 | Cannot Reproduce | [[GENERAL]]  
Fixed with Update of BACstack to version 25.1.5.1 --> can not reproduce --> close  
CDS-84625 | Bug | CLONE - BACnet: BACstack - BACstack 24.1.33.1 - error creating BISTRING properties with length 0 | Cannot Reproduce | [[GENERAL]]  
Fixed with Update of BACstack to version 25.1.5.1 --> can not reproduce --> close  
CDS-84619 | Bug | CLONE - BACnet23: CmpBACnet2 - make WHO_AM_I_CB and YOU_ARE_CB posting the proper event | Cannot Reproduce |   
CDS-84618 | Improvement | CLONE - BACnet: BACstack - BACstackV24 - BACNET_RAW_CB wrong return type int | Won't Fix | [[GENERAL]]  
Not fixed yet by stack vendor --> wont fix  
CDS-84617 | Improvement | CLONE - BACnet: BACstack - BACstackV24 - BACnetWritePropertyInstance(ByHandle) Argument pValueSrc comment misssing statement about optional semantics of pValueSrc | Won't Fix | [[GENERAL]]  
Not fixed yet by stack vendor --> wont fix  
CDS-84584 | Bug | CLONE - Unjustified storage format upgrade | Fixed |   
CDS-84583 | Bug | CLONE - Device Diagnosis: GetDeviceInfo() fails with Profinet Port-Submodules | Fixed |   
CDS-84548 | Bug | CLONE - AutoDeclare: Exception in ST editor of execute box if autodeclare is activated in SmartCoding | Fixed | [[GENERAL]]  
Initially, this bug reported two individual problems. One was the critical crash that was also present in older versions (e.g. SP17) and the effect, that auto-declaring did not work for the very first try. As both problems are unrelated, the implementation for this bug fixes the critical crash that needs to be patched.  
The minor effect with the missing auto-declare for the first try will be handled by the separate issue CDS-84790.  
CDS-84524 | Improvement | CLONE - OPC UA Server and Client: Check new license codes | Fixed |   
CDS-84496 | Bug | CLONE - On DPI != 100% (or on High-Res screens), scaling of CODESYS MainForm scaling changed when clicking on element in lib man editor | Cannot Reproduce |   
CDS-84483 | Bug | CLONE - Libraries released with an old version cannot be signed | Won't Fix | [[GENERAL]]  
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
CDS-84441 | Bug | CLONE - Find: Searching in online mode with “Find Next” doesn’t jump to right GVL location; “Find All” leads to Freeze of IDE | Fixed | [[General]]  
Little fix to stop the freezing of CODESYS. To fix the less dramatic "not-finding" in the Watchlist there is the new bug CDS-84813.  
CDS-84440 | Bug | CLONE - Refactoring: Null Reference Exception is thrown | Fixed |   
CDS-84416 | Bug | CLONE - Compiler: No error when using %MXn.m where m is greater than the used type range | Won't Fix | [[GENERAL]]  
An error message for a direct address %MX0.8 would produce error messages in many existing projects. It is not a problematic address at all since it either denotes the same bit as %MX1.0 or the 8th bit in the first WORD in memory if bit_word_addressing is set as target setting. In either case, there is nothing wrong with this address.  
CDS-84391 | Bug | CLONE - LibMan: SFC POU and GVLs from source library cannot be opened in library manager | Cannot Reproduce | [[GENERAL]]  
Original issue was already fixed with SP19, no patch necessary.  
CDS-83648 | Bug | CLONE - Windows: Gateway/Runtime may crash, if more than 15 active IP addresses are available | Fixed |   
CDS-83645 | Improvement | CLONE - Webserver, CmpOpenSSL: adjust TLS support for Version TLS1.3 | Fixed | [[GENERAL]]  
With the following security setting, the TLS version can be set to TLS 1.3. Then only TLS1.3 is allowed.  
  
[CmpWebServer]  
SECURITY.TLSVersion=1.3  
  
CODESYS Group | We _software_ Automation.  to software   
[ˈsɒftwɛər]   
transitive verb   
__softwared/softwaring   
: to develop software   
// to software automation: to develop software for automation purposes 

© 2023 CODESYS GmbH  | A member of the CODESYS Group 
