Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23431

This directory contains the Win32 binaries.

Build Date:       Wed, 30 Nov 2016 03:12:15 Pacific Standard Time
Last Changed Rev: 23424

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23431
 *BootSectImage Version 1.0 Build Build 23431
  Ecc.exe Version 1.0 Build Build 22854
 *EfiLdrImage Version 1.0 Build Build 23431
 *EfiRom Version 0.1 Build 23431
 *GenBootSector Version 0.2 Build 23431
 *GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 23431
 *GenFds.exe 1.0 Build 23431
 *GenFfs Version 0.1 Build 23431
 *GenFv Version 0.1 Build 23431
 *GenFw Version 0.2 Build 23431
 *GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 23431
 *GenSec Version 0.1 Build 23431
 *GenVtf Version 0.1 Build 23431
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 23431
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
 *Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 23431
 *TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 23431
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 23431
 *VolInfo Version 1.0 Build Build 23431
 *build.exe Version 0.60 Build 23431

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/30/2016 3:12:16AM Engine version = 5700.7163
  11/30/2016 3:12:16AM AntiVirus DAT version = 8364.0
  11/30/2016 3:12:16AM Number of detection signatures in EXTRA.DAT = None
  11/30/2016 3:12:16AM Names of detection signatures in EXTRA.DAT = None
  11/30/2016 3:12:16AM Scan Started On-Demand Scan
  11/30/2016 3:12:26AM Scan Summary
  11/30/2016 3:12:26AM Processes scanned : 0
  11/30/2016 3:12:26AM Processes detected : 0
  11/30/2016 3:12:26AM Processes cleaned : 0
  11/30/2016 3:12:26AM Boot sectors scanned : 2
  11/30/2016 3:12:26AM Boot sectors detected: 0
  11/30/2016 3:12:26AM Boot sectors cleaned : 0
  11/30/2016 3:12:26AM Files scanned : 78
  11/30/2016 3:12:26AM Files with detections: 0
  11/30/2016 3:12:26AM File detections : 0
  11/30/2016 3:12:26AM Files cleaned : 0
  11/30/2016 3:12:26AM Files deleted : 0
  11/30/2016 3:12:26AM Files not scanned : 0
  11/30/2016 3:12:26AM Scan Summary (Registry Scanning)
  11/30/2016 3:12:26AM Keys scanned : 0
  11/30/2016 3:12:26AM Keys detected : 0
  11/30/2016 3:12:26AM Keys cleaned : 0
  11/30/2016 3:12:26AM Keys deleted : 0
  11/30/2016 3:12:26AM Run time : 0:00:10
  11/30/2016 3:12:26AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23359:HEAD Source
------------------------------------------------------------------------  r23416 | edk2buildsystem | 2016-11-29 14:05:44 -0800 (Tue, 29 Nov 2016) | 11 lines
  BaseTools: Fix bug for decimal value of VPDPCD offset display in report
  current if we set VPD PCD's offset to a decimal value, eg: 22, this
  value is displayed incorrectly in the "FD VPD Region" section in the
  report.txt.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 8401d3983d00194b5a9aa77cf65477bfc1716588)

------------------------------------------------------------------------  r23423 | edk2buildsystem | 2016-11-30 02:05:46 -0800 (Wed, 30 Nov 2016) | 11 lines
  BaseTools CommonLib: Update ReadMemoryFileLine() to read line in file scope
  https://bugzilla.tianocore.org/show_bug.cgi?id=255
  Check CurrentFilePointer to make sure it not exceed the end of file.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 60a5378208f8b60e0a04ac724a639ad19158e778)

------------------------------------------------------------------------  r23424 | edk2buildsystem | 2016-11-30 02:05:53 -0800 (Wed, 30 Nov 2016) | 10 lines
  BaseTools: fix the bug to add PaletteSize info into AutoGen
  Fix the bug to add PaletteSize info into AutoGen.c when the flag
  UEFI_HII_RESOURCE_SECTION is set to FALSE.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e148e6e9625f8a0054f131bacba4e5c9a21a4377)

------------------------------------------------------------------------