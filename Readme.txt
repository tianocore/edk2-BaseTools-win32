Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25415

This directory contains the Win32 binaries.

Build Date:       Mon, 25 Sep 2017 03:13:24 Pacific Daylight Time
Last Changed Rev: 25413

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25415
 *BootSectImage Version 1.0 Build Build 25415
 *Brotli Version 0.5.2 Build 25415
  Brotli Version 0.5.2 Build 25415
  Ecc.exe Version 1.0 Build Build 24602
 *EfiLdrImage Version 1.0 Build Build 25415
 *EfiRom Version 0.1 Build 25415
 *GenBootSector Version 0.2 Build 25415
 *GenCrc32 Version 0.2 Build 25415
 *GenDepex.exe Version 0.04 Build 25415
 *GenFds.exe 1.0 Build 25415
 *GenFfs Version 0.1 Build 25415
 *GenFv Version 0.1 Build 25415
 *GenFw Version 0.2 Build 25415
 *GenPage Version 0.2 Build 25415
 *GenPatchPcdTable.exe Version 0.10 Build 25415
 *GenSec Version 0.1 Build 25415
 *GenVtf Version 0.1 Build 25415
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 25415
  LzmaF86Compress Version 0.2 Build 25415
 *PatchPcdValue.exe Version 0.10 Build 25415
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
 *Split Version 1.0 Build Build 25415
 *TargetTool.exe Version 0.01 Build 25415
 *TianoCompress Version 0.1 Build 25415
 *Trim.exe Version 0.10 Build 25415
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 25415
 *VolInfo Version 1.0 Build Build 25415
 *build.exe Version 0.60 Build 25415

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  9/25/2017 3:13:26AM Engine version = 5900.7806
  9/25/2017 3:13:26AM AntiVirus DAT version = 8662.0
  9/25/2017 3:13:26AM Number of detection signatures in EXTRA.DAT = None
  9/25/2017 3:13:26AM Names of detection signatures in EXTRA.DAT = None
  9/25/2017 3:13:26AM Scan Started On-Demand Scan
  9/25/2017 3:13:36AM Scan Summary
  9/25/2017 3:13:36AM Processes scanned : 0
  9/25/2017 3:13:36AM Processes detected : 0
  9/25/2017 3:13:36AM Processes cleaned : 0
  9/25/2017 3:13:36AM Boot sectors scanned : 2
  9/25/2017 3:13:36AM Boot sectors detected: 0
  9/25/2017 3:13:36AM Boot sectors cleaned : 0
  9/25/2017 3:13:36AM Files scanned : 81
  9/25/2017 3:13:36AM Files with detections: 0
  9/25/2017 3:13:36AM File detections : 0
  9/25/2017 3:13:36AM Files cleaned : 0
  9/25/2017 3:13:36AM Files deleted : 0
  9/25/2017 3:13:36AM Files not scanned : 0
  9/25/2017 3:13:36AM Scan Summary (Registry Scanning)
  9/25/2017 3:13:36AM Keys scanned : 0
  9/25/2017 3:13:36AM Keys detected : 0
  9/25/2017 3:13:36AM Keys cleaned : 0
  9/25/2017 3:13:36AM Keys deleted : 0
  9/25/2017 3:13:36AM Run time : 0:00:11
  9/25/2017 3:13:36AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25386:HEAD Source
------------------------------------------------------------------------  r25413 | edk2buildsystem | 2017-09-25 02:07:01 -0700 (Mon, 25 Sep 2017) | 10 lines
  BaseTools: extend FFS alignment to 16M
  Current FFS only supports 64KiB alignment for data, Per PI 1.6
  requirement, we extend FFS alignment to 16M.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e921f58d44587c77b843a6332b43f171a44b76cb)

------------------------------------------------------------------------