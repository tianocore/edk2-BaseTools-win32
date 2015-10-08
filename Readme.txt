Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18584

This directory contains the Win32 binaries.

Build Date:       Thu, 08 Oct 2015 03:20:31 Pacific Daylight Time
Last Changed Rev: 18581

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18584
  BootSectImage Version 0.1 Build 18276
  Ecc.exe Version 0.01 Build 17712
  EfiLdrImage Version 0.1 Build 18276
  EfiRom Version 0.1 Build 18276
  GenBootSector Version 0.2 Build 18276
  GenCrc32 Version 0.2 Build 18276
 *GenDepex.exe Version 0.04 Build 18584
 *GenFds.exe 1.0 Build 18584
  GenFfs Version 0.1 Build 18276
  GenFv Version 0.1 Build 18276
  GenFw Version 0.2 Build 18552
  GenPage Version 0.2 Build 18276
 *GenPatchPcdTable.exe Version 0.10 Build 18584
  GenSec Version 0.1 Build 18276
  GenVtf Version 0.1 Build 18276
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 18276
  LzmaF86Compress Version 0.2 Build 18276
 *PatchPcdValue.exe Version 0.10 Build 18584
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 18276
 *TargetTool.exe Version 0.01 Build 18584
  TianoCompress Version 0.1 Build 18276
 *Trim.exe Version 0.10 Build 18584
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17927
  VfrCompile version  2.00 (UEFI 2.4) Build 18337
  VolInfo Version 0.83 Build 18276, Aug 24 2015
 *build.exe Version 0.60 Build 18584

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/8/2015 3:20:33AM Engine version = 5700.7163
  10/8/2015 3:20:33AM AntiVirus DAT version = 7947.0
  10/8/2015 3:20:33AM Number of detection signatures in EXTRA.DAT = 3
  10/8/2015 3:20:33AM Names of detection signatures in EXTRA.DAT = GenericR-ECJ (ED) RDN/Generic BackDoor (ED)
  10/8/2015 3:20:33AM Scan Started On-Demand Scan
  10/8/2015 3:20:35AM Scan Summary
  10/8/2015 3:20:35AM Processes scanned : 0
  10/8/2015 3:20:35AM Processes detected : 0
  10/8/2015 3:20:35AM Processes cleaned : 0
  10/8/2015 3:20:35AM Boot sectors scanned : 1
  10/8/2015 3:20:35AM Boot sectors detected: 0
  10/8/2015 3:20:35AM Boot sectors cleaned : 0
  10/8/2015 3:20:35AM Files scanned : 55
  10/8/2015 3:20:35AM Files with detections: 0
  10/8/2015 3:20:35AM File detections : 0
  10/8/2015 3:20:35AM Files cleaned : 0
  10/8/2015 3:20:35AM Files deleted : 0
  10/8/2015 3:20:35AM Files not scanned : 0
  10/8/2015 3:20:35AM Scan Summary (Registry Scanning)
  10/8/2015 3:20:35AM Keys scanned : 0
  10/8/2015 3:20:35AM Keys detected : 0
  10/8/2015 3:20:35AM Keys cleaned : 0
  10/8/2015 3:20:35AM Keys deleted : 0
  10/8/2015 3:20:35AM Run time : 0:00:03
  10/8/2015 3:20:35AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18552:HEAD Source
------------------------------------------------------------------------  r18579 | lgao4 | 2015-10-08 02:27:14 -0700 (Thu, 08 Oct 2015) | 22 lines
  BaseTools: Update Build tool to support multiple workspaces
  WORKSPACE is still kept.
  New PACKAGES_PATH is introduced to specify the additional WORKSPACEs.
  In PACKAGES_PATH, ';' is separator in Windows, ':' is separator in Linux.
  Build directory is in WORKSPACE. Package, BaseTools and Conf directory
  will be found from WORKSPACE and PACKAGES_PATH.
  In implementation, BaseTools adds MultipleWorkspace class for
  the file path conversion from WORKSPACE and PACKAGES_PATH.
  Verify two tree layouts.
  Root\edk2\MdePkg
  Root\edk2\MdeMdeModulePkg
  Root\edk2\...
  1. set WORKSPACE=Root\edk2
  2. set WORKSPACE=Root, and set PACKAGES_PATH=Root\edk2
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Li YangX <yangx.li@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r18580 | lgao4 | 2015-10-08 02:28:15 -0700 (Thu, 08 Oct 2015) | 8 lines
  BaseTools: Update UPT tool to support multiple workspaces
  Update UPT to refer MultipleWorkspace class to convert
  the file path from WORKSPACE and PACKAGES_PATH.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hesheng Chen <hesheng.chen@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r18581 | lgao4 | 2015-10-08 02:28:51 -0700 (Thu, 08 Oct 2015) | 8 lines
  BaseTools: Update ECC tool to support multiple workspaces
  Update ECC to refer MultipleWorkspace class to convert
  the file path from WORKSPACE and PACKAGES_PATH.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Li YangX <yangx.li@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------