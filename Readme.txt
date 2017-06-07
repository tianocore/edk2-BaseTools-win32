Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24776

This directory contains the Win32 binaries.

Build Date:       Wed, 07 Jun 2017 03:12:10 Pacific Daylight Time
Last Changed Rev: 24763

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24776
  BootSectImage Version 1.0 Build Build 23431
  Brotli Version 0.5.2 Build 24577
  Brotli Version 0.5.2 Build 24577
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 24776
 *GenFds.exe 1.0 Build 24776
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 24776
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 24776
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 24776
  TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 24776
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24507
 *build.exe Version 0.60 Build 24776

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  6/7/2017 3:12:12AM Engine version = 5700.7163
  6/7/2017 3:12:12AM AntiVirus DAT version = 8552.0
  6/7/2017 3:12:12AM Number of detection signatures in EXTRA.DAT = None
  6/7/2017 3:12:12AM Names of detection signatures in EXTRA.DAT = None
  6/7/2017 3:12:12AM Scan Started On-Demand Scan
  6/7/2017 3:12:22AM Scan Summary
  6/7/2017 3:12:22AM Processes scanned : 0
  6/7/2017 3:12:22AM Processes detected : 0
  6/7/2017 3:12:22AM Processes cleaned : 0
  6/7/2017 3:12:22AM Boot sectors scanned : 2
  6/7/2017 3:12:22AM Boot sectors detected: 0
  6/7/2017 3:12:22AM Boot sectors cleaned : 0
  6/7/2017 3:12:22AM Files scanned : 64
  6/7/2017 3:12:22AM Files with detections: 0
  6/7/2017 3:12:22AM File detections : 0
  6/7/2017 3:12:22AM Files cleaned : 0
  6/7/2017 3:12:22AM Files deleted : 0
  6/7/2017 3:12:22AM Files not scanned : 0
  6/7/2017 3:12:22AM Scan Summary (Registry Scanning)
  6/7/2017 3:12:22AM Keys scanned : 0
  6/7/2017 3:12:22AM Keys detected : 0
  6/7/2017 3:12:22AM Keys cleaned : 0
  6/7/2017 3:12:22AM Keys deleted : 0
  6/7/2017 3:12:22AM Run time : 0:00:10
  6/7/2017 3:12:22AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24714:HEAD Source
------------------------------------------------------------------------  r24762 | edk2buildsystem | 2017-06-07 02:06:18 -0700 (Wed, 07 Jun 2017) | 14 lines
  BaseTools: Fix incremental build failure that override file be removed
  Fix a Incremental build failure. The case is: Both A and B package will
  include a same .h file, and in the driver's packages section, A
  package is listed before B package, so we will use the .h file in the A
  package and build success, then we directly delete the .h file in package
  A, it cause increment build failure since in the AutoGenTimeStamp file
  the .h file in A can't be found.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 4a1167dfef3deff3d96f06ccfd104e26486d7dae)

------------------------------------------------------------------------  r24763 | edk2buildsystem | 2017-06-07 02:06:23 -0700 (Wed, 07 Jun 2017) | 11 lines
  BaseTools: Fix the bug use same FMP_PAYLOAD in different capsule file
  Fix the bug that use same FMP_PAYLOAD in different capsule file. Because
  in previous FMP generation, the FMP already be generated, so we don't
  need to regenerate again.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d4c558e83d8f428393d27816772efc7f4b0e8403)

------------------------------------------------------------------------