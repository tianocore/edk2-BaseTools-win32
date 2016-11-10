Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23226

This directory contains the Win32 binaries.

Build Date:       Thu, 10 Nov 2016 03:11:07 Pacific Standard Time
Last Changed Rev: 23226

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23090
  BootSectImage Version 1.0 Build Build 23211
  Ecc.exe Version 1.0 Build Build 22854
  EfiLdrImage Version 1.0 Build Build 23211
  EfiRom Version 0.1 Build 23211
  GenBootSector Version 0.2 Build 23211
  GenCrc32 Version 0.2 Build 23211
  GenDepex.exe Version 0.04 Build 23090
  GenFds.exe 1.0 Build 23090
 *GenFfs Version 0.1 Build 23226
  GenFv Version 0.1 Build 23211
  GenFw Version 0.2 Build 23211
  GenPage Version 0.2 Build 23211
  GenPatchPcdTable.exe Version 0.10 Build 23095
 *GenSec Version 0.1 Build 23226
  GenVtf Version 0.1 Build 23211
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23211
  LzmaF86Compress Version 0.2 Build 23211
  PatchPcdValue.exe Version 0.10 Build 23090
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 23211
  TargetTool.exe Version 0.01 Build 23090
  TianoCompress Version 0.1 Build 23211
  Trim.exe Version 0.10 Build 23090
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23211
  VolInfo Version 1.0 Build Build 23211
  build.exe Version 0.60 Build 23095

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/10/2016 3:11:08AM Engine version = 5700.7163
  11/10/2016 3:11:08AM AntiVirus DAT version = 8344.0
  11/10/2016 3:11:08AM Number of detection signatures in EXTRA.DAT = None
  11/10/2016 3:11:08AM Names of detection signatures in EXTRA.DAT = None
  11/10/2016 3:11:08AM Scan Started On-Demand Scan
  11/10/2016 3:11:11AM Scan Summary
  11/10/2016 3:11:11AM Processes scanned : 0
  11/10/2016 3:11:11AM Processes detected : 0
  11/10/2016 3:11:11AM Processes cleaned : 0
  11/10/2016 3:11:11AM Boot sectors scanned : 1
  11/10/2016 3:11:11AM Boot sectors detected: 0
  11/10/2016 3:11:11AM Boot sectors cleaned : 0
  11/10/2016 3:11:11AM Files scanned : 63
  11/10/2016 3:11:11AM Files with detections: 0
  11/10/2016 3:11:11AM File detections : 0
  11/10/2016 3:11:11AM Files cleaned : 0
  11/10/2016 3:11:11AM Files deleted : 0
  11/10/2016 3:11:11AM Files not scanned : 0
  11/10/2016 3:11:11AM Scan Summary (Registry Scanning)
  11/10/2016 3:11:11AM Keys scanned : 0
  11/10/2016 3:11:11AM Keys detected : 0
  11/10/2016 3:11:11AM Keys cleaned : 0
  11/10/2016 3:11:11AM Keys deleted : 0
  11/10/2016 3:11:11AM Run time : 0:00:04
  11/10/2016 3:11:11AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23211:HEAD Source
------------------------------------------------------------------------  r23225 | edk2buildsystem | 2016-11-10 02:07:01 -0800 (Thu, 10 Nov 2016) | 15 lines
  BaseTools/GenFfs: Fix return too early when input file is of size 0
  Commit 2cb874352423fcfd180199e6de8298567dff8e7f eliminates possible NULL
  pointer dereference in GenFfs tool source codes. However, it doesn't
  correctly handle the case when the input file is of size 0. This will lead
  to possible build issues.
  This commits refine the logic to handle the above case.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b390737ad03a354f5d11954950a580df715e2935)

------------------------------------------------------------------------  r23226 | edk2buildsystem | 2016-11-10 02:07:06 -0800 (Thu, 10 Nov 2016) | 8 lines
  BaseTools/GenSec: Return correct status when input file size is 0
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c52f00d6e1e14b9eaf5c5a58501f075d2a64920c)

------------------------------------------------------------------------