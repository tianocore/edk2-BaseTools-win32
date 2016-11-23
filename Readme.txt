Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23359

This directory contains the Win32 binaries.

Build Date:       Wed, 23 Nov 2016 03:11:21 Pacific Standard Time
Last Changed Rev: 23353

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23359
  BootSectImage Version 1.0 Build Build 23211
  Ecc.exe Version 1.0 Build Build 22854
  EfiLdrImage Version 1.0 Build Build 23211
  EfiRom Version 0.1 Build 23211
  GenBootSector Version 0.2 Build 23211
  GenCrc32 Version 0.2 Build 23211
 *GenDepex.exe Version 0.04 Build 23359
 *GenFds.exe 1.0 Build 23359
  GenFfs Version 0.1 Build 23226
  GenFv Version 0.1 Build 23211
  GenFw Version 0.2 Build 23211
  GenPage Version 0.2 Build 23211
 *GenPatchPcdTable.exe Version 0.10 Build 23359
  GenSec Version 0.1 Build 23226
  GenVtf Version 0.1 Build 23211
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23211
  LzmaF86Compress Version 0.2 Build 23211
 *PatchPcdValue.exe Version 0.10 Build 23359
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 23211
 *TargetTool.exe Version 0.01 Build 23359
  TianoCompress Version 0.1 Build 23211
 *Trim.exe Version 0.10 Build 23359
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23211
  VolInfo Version 1.0 Build Build 23211
 *build.exe Version 0.60 Build 23359

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/23/2016 3:11:22AM Engine version = 5700.7163
  11/23/2016 3:11:22AM AntiVirus DAT version = 8357.0
  11/23/2016 3:11:22AM Number of detection signatures in EXTRA.DAT = None
  11/23/2016 3:11:22AM Names of detection signatures in EXTRA.DAT = None
  11/23/2016 3:11:22AM Scan Started On-Demand Scan
  11/23/2016 3:11:26AM Scan Summary
  11/23/2016 3:11:26AM Processes scanned : 0
  11/23/2016 3:11:26AM Processes detected : 0
  11/23/2016 3:11:26AM Processes cleaned : 0
  11/23/2016 3:11:26AM Boot sectors scanned : 1
  11/23/2016 3:11:26AM Boot sectors detected: 0
  11/23/2016 3:11:26AM Boot sectors cleaned : 0
  11/23/2016 3:11:26AM Files scanned : 62
  11/23/2016 3:11:26AM Files with detections: 0
  11/23/2016 3:11:26AM File detections : 0
  11/23/2016 3:11:26AM Files cleaned : 0
  11/23/2016 3:11:26AM Files deleted : 0
  11/23/2016 3:11:26AM Files not scanned : 0
  11/23/2016 3:11:26AM Scan Summary (Registry Scanning)
  11/23/2016 3:11:26AM Keys scanned : 0
  11/23/2016 3:11:26AM Keys detected : 0
  11/23/2016 3:11:26AM Keys cleaned : 0
  11/23/2016 3:11:26AM Keys deleted : 0
  11/23/2016 3:11:26AM Run time : 0:00:04
  11/23/2016 3:11:26AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23263:HEAD Source
------------------------------------------------------------------------  r23353 | edk2buildsystem | 2016-11-23 02:06:37 -0800 (Wed, 23 Nov 2016) | 11 lines
  BaseTools: report error for same Guid's Private definition conflict
  Add error check for the same Guid/Protocol/PPIs/Includes defined as both
  Private and non-Private attribute.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=209
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 24e7435ab474f8a2da43a086d63add4954a3034f)

------------------------------------------------------------------------