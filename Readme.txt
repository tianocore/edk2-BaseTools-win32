Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23263

This directory contains the Win32 binaries.

Build Date:       Tue, 15 Nov 2016 03:12:08 Pacific Standard Time
Last Changed Rev: 23256

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
 *GenFds.exe 1.0 Build 23263
  GenFfs Version 0.1 Build 23226
  GenFv Version 0.1 Build 23211
  GenFw Version 0.2 Build 23211
  GenPage Version 0.2 Build 23211
  GenPatchPcdTable.exe Version 0.10 Build 23095
  GenSec Version 0.1 Build 23226
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
 *build.exe Version 0.60 Build 23263

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/15/2016 3:12:09AM Engine version = 5700.7163
  11/15/2016 3:12:09AM AntiVirus DAT version = 8349.0
  11/15/2016 3:12:09AM Number of detection signatures in EXTRA.DAT = None
  11/15/2016 3:12:09AM Names of detection signatures in EXTRA.DAT = None
  11/15/2016 3:12:09AM Scan Started On-Demand Scan
  11/15/2016 3:12:20AM Scan Summary
  11/15/2016 3:12:20AM Processes scanned : 0
  11/15/2016 3:12:20AM Processes detected : 0
  11/15/2016 3:12:20AM Processes cleaned : 0
  11/15/2016 3:12:20AM Boot sectors scanned : 2
  11/15/2016 3:12:20AM Boot sectors detected: 0
  11/15/2016 3:12:20AM Boot sectors cleaned : 0
  11/15/2016 3:12:20AM Files scanned : 62
  11/15/2016 3:12:20AM Files with detections: 0
  11/15/2016 3:12:20AM File detections : 0
  11/15/2016 3:12:20AM Files cleaned : 0
  11/15/2016 3:12:20AM Files deleted : 0
  11/15/2016 3:12:20AM Files not scanned : 0
  11/15/2016 3:12:20AM Scan Summary (Registry Scanning)
  11/15/2016 3:12:20AM Keys scanned : 0
  11/15/2016 3:12:20AM Keys detected : 0
  11/15/2016 3:12:20AM Keys cleaned : 0
  11/15/2016 3:12:20AM Keys deleted : 0
  11/15/2016 3:12:20AM Run time : 0:00:11
  11/15/2016 3:12:20AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23226:HEAD Source
------------------------------------------------------------------------  r23226 | edk2buildsystem | 2016-11-10 02:07:06 -0800 (Thu, 10 Nov 2016) | 8 lines
  BaseTools/GenSec: Return correct status when input file size is 0
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c52f00d6e1e14b9eaf5c5a58501f075d2a64920c)

------------------------------------------------------------------------  r23255 | edk2buildsystem | 2016-11-15 02:06:20 -0800 (Tue, 15 Nov 2016) | 11 lines
  BaseTools: Fix the bug to support generate FFS by Align=Auto
  FDF spec support to use 'Auto' as <FfsAlignmentValues>, but current Tool
  report error about -a=Auto is invalid option when we set Align=Auto for
  RAW File.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f475f1e2361877e9947ecda98a697bc55fb9d85a)

------------------------------------------------------------------------  r23256 | edk2buildsystem | 2016-11-15 02:06:25 -0800 (Tue, 15 Nov 2016) | 10 lines
  BaseTools: FILE DATA to support relative path under Multiple workspace
  Fix the bug that FILE DATA to support relative path under Multiple
  workspace.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 94e4bcbb5efaf86440e89293d80b0a73781fff12)

------------------------------------------------------------------------