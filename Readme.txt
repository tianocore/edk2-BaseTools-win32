Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23694

This directory contains the Win32 binaries.

Build Date:       Fri, 06 Jan 2017 03:11:09 Pacific Standard Time
Last Changed Rev: 23694

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23459
  BootSectImage Version 1.0 Build Build 23431
  Ecc.exe Version 1.0 Build Build 23673
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
  GenDepex.exe Version 0.04 Build 23459
 *GenFds.exe 1.0 Build 23694
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 23431
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 23459
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 23431
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 23459
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 23431
  TargetTool.exe Version 0.01 Build 23459
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 23459
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23633
  VolInfo Version 1.0 Build Build 23468
 *build.exe Version 0.60 Build 23694

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/6/2017 3:11:11AM Engine version = 5700.7163
  1/6/2017 3:11:11AM AntiVirus DAT version = 8399.0
  1/6/2017 3:11:11AM Number of detection signatures in EXTRA.DAT = None
  1/6/2017 3:11:11AM Names of detection signatures in EXTRA.DAT = None
  1/6/2017 3:11:11AM Scan Started On-Demand Scan
  1/6/2017 3:11:14AM Scan Summary
  1/6/2017 3:11:14AM Processes scanned : 0
  1/6/2017 3:11:14AM Processes detected : 0
  1/6/2017 3:11:14AM Processes cleaned : 0
  1/6/2017 3:11:14AM Boot sectors scanned : 1
  1/6/2017 3:11:14AM Boot sectors detected: 0
  1/6/2017 3:11:14AM Boot sectors cleaned : 0
  1/6/2017 3:11:14AM Files scanned : 62
  1/6/2017 3:11:14AM Files with detections: 0
  1/6/2017 3:11:14AM File detections : 0
  1/6/2017 3:11:14AM Files cleaned : 0
  1/6/2017 3:11:14AM Files deleted : 0
  1/6/2017 3:11:14AM Files not scanned : 0
  1/6/2017 3:11:14AM Scan Summary (Registry Scanning)
  1/6/2017 3:11:14AM Keys scanned : 0
  1/6/2017 3:11:14AM Keys detected : 0
  1/6/2017 3:11:14AM Keys cleaned : 0
  1/6/2017 3:11:14AM Keys deleted : 0
  1/6/2017 3:11:14AM Run time : 0:00:04
  1/6/2017 3:11:14AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23684:HEAD Source
------------------------------------------------------------------------  r23684 | edk2buildsystem | 2017-01-04 02:05:58 -0800 (Wed, 04 Jan 2017) | 10 lines
  BaseTools: fix the bug for Mixed Pcd display in the report
  Fix the bug to not display the mixed PCD in the Global PCD section, and
  correct the Pcd display name.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 7cb63c870bac7a986936aeb6e70b22ebf80d4ba9)

------------------------------------------------------------------------  r23694 | edk2buildsystem | 2017-01-06 02:05:54 -0800 (Fri, 06 Jan 2017) | 12 lines
  BaseTools: not report error for the optional items in the FmpTokens
  <FmpTokens> in the FDF spec defined some optional items, eg: IMAGE_INDEX,
  HARDWARE_INSTANCE. but current tool report error if no such item is exist
  in the FDF file.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=293
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9ce9bf5339f8a5a9acfd77d9fbc70bb92a55dd6a)

------------------------------------------------------------------------