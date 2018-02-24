Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26405

This directory contains the Win32 binaries.

Build Date:       Sat, 24 Feb 2018 03:12:54 Pacific Standard Time
Last Changed Rev: 26400

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.14 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26405
  BootSectImage Version 1.0 Build Build 26263
  Brotli Version 0.5.2 Build 26263
  Brotli Version 0.5.2 Build 26263
  DevicePath Version 0.1 Build 26263
  Ecc.exe Version 1.0 Build Build 26237
  EfiLdrImage Version 1.0 Build Build 26263
  EfiRom Version 0.1 Build 26263
  GenBootSector Version 0.2 Build 26263
  GenCrc32 Version 0.2 Build 26263
 *GenDepex.exe Version 0.04 Build 26405
 *GenFds.exe 1.0 Build 26405
  GenFfs Version 0.1 Build 26263
  GenFv Version 0.1 Build 26263
  GenFw Version 0.2 Build 26263
  GenPage Version 0.2 Build 26263
 *GenPatchPcdTable.exe Version 0.10 Build 26405
  GenSec Version 0.1 Build 26263
  GenVtf Version 0.1 Build 26263
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26263
  LzmaF86Compress Version 0.2 Build 26263
 *PatchPcdValue.exe Version 0.10 Build 26405
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
  Split Version 1.0 Build Build 26263
 *TargetTool.exe Version 0.01 Build 26405
  TianoCompress Version 0.1 Build 26263
 *Trim.exe Version 0.10 Build 26405
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26263
  VolInfo Version 1.0 Build Build 26263
 *build.exe Version 0.60 Build 26405

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/24/2018 3:12:55AM Engine version = 5900.7806
  2/24/2018 3:12:55AM AntiVirus DAT version = 8813.0
  2/24/2018 3:12:55AM Number of detection signatures in EXTRA.DAT = None
  2/24/2018 3:12:55AM Names of detection signatures in EXTRA.DAT = None
  2/24/2018 3:12:55AM Scan Started On-Demand Scan
  2/24/2018 3:13:06AM Scan Summary
  2/24/2018 3:13:06AM Processes scanned : 0
  2/24/2018 3:13:06AM Processes detected : 0
  2/24/2018 3:13:06AM Processes cleaned : 0
  2/24/2018 3:13:06AM Boot sectors scanned : 2
  2/24/2018 3:13:06AM Boot sectors detected: 0
  2/24/2018 3:13:06AM Boot sectors cleaned : 0
  2/24/2018 3:13:06AM Files scanned : 66
  2/24/2018 3:13:06AM Files with detections: 0
  2/24/2018 3:13:06AM File detections : 0
  2/24/2018 3:13:06AM Files cleaned : 0
  2/24/2018 3:13:06AM Files deleted : 0
  2/24/2018 3:13:06AM Files not scanned : 0
  2/24/2018 3:13:06AM Scan Summary (Registry Scanning)
  2/24/2018 3:13:06AM Keys scanned : 0
  2/24/2018 3:13:06AM Keys detected : 0
  2/24/2018 3:13:06AM Keys cleaned : 0
  2/24/2018 3:13:06AM Keys deleted : 0
  2/24/2018 3:13:06AM Run time : 0:00:11
  2/24/2018 3:13:06AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26355:HEAD Source
------------------------------------------------------------------------  r26399 | edk2buildsystem | 2018-02-23 14:05:54 -0800 (Fri, 23 Feb 2018) | 9 lines
  BaseTools: Add check for INF statement must be a .inf file
  Per FDF spec, INF statement must use a .inf file, we add this error
  check.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a87e79d9d64a73f1c8368e2b7f309954271c69a7)

------------------------------------------------------------------------  r26400 | edk2buildsystem | 2018-02-23 14:06:03 -0800 (Fri, 23 Feb 2018) | 10 lines
  BaseTools: Fix the bug to display the single SKUID info
  when defined SKUID_IDENTIFIER = DEFAULT|TEST in DSC [Defines] section,
  per spec it means current SKUID is single, the bug is build report print
  both DEFAULT and TEST info, it should only print TEST.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 8aaa8f7bc0f5dc79bce476e2ffa8a956c4db8bb0)

------------------------------------------------------------------------