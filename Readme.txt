Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20600

This directory contains the Win32 binaries.

Build Date:       Fri, 15 Apr 2016 03:11:26 Pacific Daylight Time
Last Changed Rev: 20596

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20600
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20600
 *GenFds.exe 1.0 Build 20600
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
 *GenFw Version 0.2 Build 20600
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20600
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20600
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20600
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20600
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20528
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
 *VolInfo Version 1.0 Build Build 20600
 *build.exe Version 0.60 Build 20600

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/15/2016 3:11:28AM Engine version = 5700.7163
  4/15/2016 3:11:28AM AntiVirus DAT version = 8135.0
  4/15/2016 3:11:28AM Number of detection signatures in EXTRA.DAT = None
  4/15/2016 3:11:28AM Names of detection signatures in EXTRA.DAT = None
  4/15/2016 3:11:28AM Scan Started On-Demand Scan
  4/15/2016 3:11:35AM Scan Summary
  4/15/2016 3:11:35AM Processes scanned : 0
  4/15/2016 3:11:35AM Processes detected : 0
  4/15/2016 3:11:35AM Processes cleaned : 0
  4/15/2016 3:11:35AM Boot sectors scanned : 2
  4/15/2016 3:11:35AM Boot sectors detected: 0
  4/15/2016 3:11:35AM Boot sectors cleaned : 0
  4/15/2016 3:11:35AM Files scanned : 57
  4/15/2016 3:11:35AM Files with detections: 0
  4/15/2016 3:11:35AM File detections : 0
  4/15/2016 3:11:35AM Files cleaned : 0
  4/15/2016 3:11:35AM Files deleted : 0
  4/15/2016 3:11:35AM Files not scanned : 0
  4/15/2016 3:11:35AM Scan Summary (Registry Scanning)
  4/15/2016 3:11:35AM Keys scanned : 0
  4/15/2016 3:11:35AM Keys detected : 0
  4/15/2016 3:11:35AM Keys cleaned : 0
  4/15/2016 3:11:35AM Keys deleted : 0
  4/15/2016 3:11:35AM Run time : 0:00:07
  4/15/2016 3:11:35AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20589:HEAD Source
------------------------------------------------------------------------  r20593 | edk2buildsystem | 2016-04-15 02:05:32 -0700 (Fri, 15 Apr 2016) | 13 lines
  BaseTools: Fix the bug to correctly handle the [BuildOptions]
  the last fix call os.path.normpath() function, which removes the
  trailing slash character, it cause NASM failure for ResetVector
  driver.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Laszlo Ersek <lersek@redhat.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Tested-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 67a69059f714c0728676d13d97f10bd12730b378)

------------------------------------------------------------------------  r20594 | edk2buildsystem | 2016-04-15 02:05:38 -0700 (Fri, 15 Apr 2016) | 10 lines
  BaseTools/GenFw: Update to handle PE image with .code section only
  current GenFw rebase the image which only has .code section, but no other
  section, the tool return error. this patch fix this bug to support it.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 3c4db2dfe2f1ea2cf8529671765111319bbadca4)

------------------------------------------------------------------------  r20595 | edk2buildsystem | 2016-04-15 02:05:42 -0700 (Fri, 15 Apr 2016) | 10 lines
  BaseTools/VolInfo: Update to handle PE image with .code section only
  rebase the image which only has .code section, but no other section, the
  tool return error. this patch fix this bug to support it.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 670bf6a7223125cf48c52a2ab272195fbc59e68a)

------------------------------------------------------------------------  r20596 | edk2buildsystem | 2016-04-15 02:05:46 -0700 (Fri, 15 Apr 2016) | 10 lines
  BaseTools: Fix PLATFORM_DIR variable value.
  In commit 017fb1cd4c5e3c8b914eb217ac1760223687dad7, the PLATFORM_DIR
  macro has been updated to resolve to the correct path. However, it is
  incorrectly accessed via curved rather than curly braces by GenMake.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Marvin Haeuser <Marvin.Haeuser@outlook.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7a5f1426c57bcaaa87c5c9a86c5ab2090c890453)

------------------------------------------------------------------------