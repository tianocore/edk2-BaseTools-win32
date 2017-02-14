Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23868

This directory contains the Win32 binaries.

Build Date:       Tue, 14 Feb 2017 03:11:22 Pacific Standard Time
Last Changed Rev: 23868

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23868
  BootSectImage Version 1.0 Build Build 23431
  Ecc.exe Version 1.0 Build Build 23673
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 23868
 *GenFds.exe 1.0 Build 23868
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 23431
  GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 23868
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 23431
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 23868
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 23868
  TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 23868
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23818
  VolInfo Version 1.0 Build Build 23468
 *build.exe Version 0.60 Build 23868

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/14/2017 3:11:23AM Engine version = 5700.7163
  2/14/2017 3:11:23AM AntiVirus DAT version = 8438.0
  2/14/2017 3:11:23AM Number of detection signatures in EXTRA.DAT = None
  2/14/2017 3:11:23AM Names of detection signatures in EXTRA.DAT = None
  2/14/2017 3:11:23AM Scan Started On-Demand Scan
  2/14/2017 3:11:26AM Scan Summary
  2/14/2017 3:11:26AM Processes scanned : 0
  2/14/2017 3:11:26AM Processes detected : 0
  2/14/2017 3:11:26AM Processes cleaned : 0
  2/14/2017 3:11:26AM Boot sectors scanned : 1
  2/14/2017 3:11:26AM Boot sectors detected: 0
  2/14/2017 3:11:26AM Boot sectors cleaned : 0
  2/14/2017 3:11:26AM Files scanned : 62
  2/14/2017 3:11:26AM Files with detections: 0
  2/14/2017 3:11:26AM File detections : 0
  2/14/2017 3:11:26AM Files cleaned : 0
  2/14/2017 3:11:26AM Files deleted : 0
  2/14/2017 3:11:26AM Files not scanned : 0
  2/14/2017 3:11:26AM Scan Summary (Registry Scanning)
  2/14/2017 3:11:26AM Keys scanned : 0
  2/14/2017 3:11:26AM Keys detected : 0
  2/14/2017 3:11:26AM Keys cleaned : 0
  2/14/2017 3:11:26AM Keys deleted : 0
  2/14/2017 3:11:26AM Run time : 0:00:03
  2/14/2017 3:11:26AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23852:HEAD Source
------------------------------------------------------------------------  r23868 | edk2buildsystem | 2017-02-14 02:05:36 -0800 (Tue, 14 Feb 2017) | 15 lines
  BaseTools: Enhance BaseTools supports FixedAtBuild usage in VFR file
  This patch is to update BaseTools generate Fixed PCD APIs and Value into
  $(MODULE_NAME)StrDefs.h for VFR only. If the module has VFR files, and it
  directly consumes FixedAtBuild PCD, BaseTool will generate those
  FixedAtBuild PCD value into its $(MODULE_NAME)StrDefs.h. FixedPcdGetXX
  macro are always generated. Every FixedPcd _PCD_VALUE_PcdName will be
  generated without the postfix U or UL or ULL.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=348
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5b97eb4c35316cbe8235ae526209263da818e1a4)

------------------------------------------------------------------------