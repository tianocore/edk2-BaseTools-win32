Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20663

This directory contains the Win32 binaries.

Build Date:       Wed, 27 Apr 2016 03:11:21 Pacific Daylight Time
Last Changed Rev: 20656

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20663
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20663
 *GenFds.exe 1.0 Build 20663
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 20600
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20663
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20663
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20663
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20663
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20600
 *build.exe Version 0.60 Build 20663

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/27/2016 3:11:22AM Engine version = 5700.7163
  4/27/2016 3:11:22AM AntiVirus DAT version = 8147.0
  4/27/2016 3:11:22AM Number of detection signatures in EXTRA.DAT = None
  4/27/2016 3:11:22AM Names of detection signatures in EXTRA.DAT = None
  4/27/2016 3:11:22AM Scan Started On-Demand Scan
  4/27/2016 3:11:25AM Scan Summary
  4/27/2016 3:11:25AM Processes scanned : 0
  4/27/2016 3:11:25AM Processes detected : 0
  4/27/2016 3:11:25AM Processes cleaned : 0
  4/27/2016 3:11:25AM Boot sectors scanned : 1
  4/27/2016 3:11:25AM Boot sectors detected: 0
  4/27/2016 3:11:25AM Boot sectors cleaned : 0
  4/27/2016 3:11:25AM Files scanned : 55
  4/27/2016 3:11:25AM Files with detections: 0
  4/27/2016 3:11:25AM File detections : 0
  4/27/2016 3:11:25AM Files cleaned : 0
  4/27/2016 3:11:25AM Files deleted : 0
  4/27/2016 3:11:25AM Files not scanned : 0
  4/27/2016 3:11:25AM Scan Summary (Registry Scanning)
  4/27/2016 3:11:25AM Keys scanned : 0
  4/27/2016 3:11:25AM Keys detected : 0
  4/27/2016 3:11:25AM Keys cleaned : 0
  4/27/2016 3:11:25AM Keys deleted : 0
  4/27/2016 3:11:25AM Run time : 0:00:03
  4/27/2016 3:11:25AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20651:HEAD Source
------------------------------------------------------------------------  r20655 | edk2buildsystem | 2016-04-27 02:05:35 -0700 (Wed, 27 Apr 2016) | 12 lines
  BaseTools: Update FMP Capsule support to follow FDF spec
  Current the FMP Capsule feature is supported, but its format has a little
  different with FDF spec. so this patch 1) Align the FMP Capsule with FDF
  spec. 2) fix some style issue, eg: Tab. 3) Add a SectionParser function to
  check the section header info since this method is used in 7 places.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit df81077f77f91b43f32f70e06950b86e20f711da)

------------------------------------------------------------------------  r20656 | edk2buildsystem | 2016-04-27 02:05:40 -0700 (Wed, 27 Apr 2016) | 12 lines
  BaseTools: Fix the bug for .aml to use ASL binary type in Asbuilt inf
  Per build spec, the .aml file should use ASL binary type in the Asbuilt
  inf file. the original bug is .aml file may use BIN as binary type when
  the module type is not BASE or USER_DEFINED. This patch 1) fix this bug.
  2) fix some indent coding style issue.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 481252bbc9c0883e444bcbedd990d8164d10cf89)

------------------------------------------------------------------------