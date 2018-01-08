Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26092

This directory contains the Win32 binaries.

Build Date:       Mon, 08 Jan 2018 03:12:07 Pacific Standard Time
Last Changed Rev: 26090

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26092
  BootSectImage Version 1.0 Build Build 26075
  Brotli Version 0.5.2 Build 26075
  Brotli Version 0.5.2 Build 26075
  DevicePath Version 0.1 Build 26075
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 26075
  EfiRom Version 0.1 Build 26075
  GenBootSector Version 0.2 Build 26075
  GenCrc32 Version 0.2 Build 26075
 *GenDepex.exe Version 0.04 Build 26092
 *GenFds.exe 1.0 Build 26092
  GenFfs Version 0.1 Build 26075
  GenFv Version 0.1 Build 26075
  GenFw Version 0.2 Build 26075
  GenPage Version 0.2 Build 26075
 *GenPatchPcdTable.exe Version 0.10 Build 26092
  GenSec Version 0.1 Build 26075
  GenVtf Version 0.1 Build 26075
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26075
  LzmaF86Compress Version 0.2 Build 26075
 *PatchPcdValue.exe Version 0.10 Build 26092
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 26075
 *TargetTool.exe Version 0.01 Build 26092
  TianoCompress Version 0.1 Build 26075
 *Trim.exe Version 0.10 Build 26092
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26075
  VolInfo Version 1.0 Build Build 26075
 *build.exe Version 0.60 Build 26092

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/8/2018 3:12:08AM Engine version = 5900.7806
  1/8/2018 3:12:08AM AntiVirus DAT version = 8767.0
  1/8/2018 3:12:08AM Number of detection signatures in EXTRA.DAT = None
  1/8/2018 3:12:08AM Names of detection signatures in EXTRA.DAT = None
  1/8/2018 3:12:08AM Scan Started On-Demand Scan
  1/8/2018 3:12:18AM Scan Summary
  1/8/2018 3:12:18AM Processes scanned : 0
  1/8/2018 3:12:18AM Processes detected : 0
  1/8/2018 3:12:18AM Processes cleaned : 0
  1/8/2018 3:12:18AM Boot sectors scanned : 2
  1/8/2018 3:12:18AM Boot sectors detected: 0
  1/8/2018 3:12:18AM Boot sectors cleaned : 0
  1/8/2018 3:12:18AM Files scanned : 65
  1/8/2018 3:12:18AM Files with detections: 0
  1/8/2018 3:12:18AM File detections : 0
  1/8/2018 3:12:18AM Files cleaned : 0
  1/8/2018 3:12:18AM Files deleted : 0
  1/8/2018 3:12:18AM Files not scanned : 0
  1/8/2018 3:12:18AM Scan Summary (Registry Scanning)
  1/8/2018 3:12:18AM Keys scanned : 0
  1/8/2018 3:12:18AM Keys detected : 0
  1/8/2018 3:12:18AM Keys cleaned : 0
  1/8/2018 3:12:18AM Keys deleted : 0
  1/8/2018 3:12:18AM Run time : 0:00:10
  1/8/2018 3:12:18AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26075:HEAD Source
------------------------------------------------------------------------  r26075 | edk2buildsystem | 2018-01-03 02:05:50 -0800 (Wed, 03 Jan 2018) | 8 lines
  BaseTools: Fix compile error on VS2010
  VS2010 also defined RSIZE_MAX, so we undef it first.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e4fb8f1d313858bd5e415725e65e65679f2b05a0)

------------------------------------------------------------------------  r26088 | edk2buildsystem | 2018-01-08 02:05:30 -0800 (Mon, 08 Jan 2018) | 10 lines
  BaseTools: Fix an issue in HiiPcd generation
  DynamicHiiPcd may be used by PEIM or DXE driver.
  All used DynamicHiiPcd value should be collected and placed into
  the default setting PCD PcdNvStoreDefaultValueBuffer.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a3623244b9a45386bcdce81b24f033bc86e28683)

------------------------------------------------------------------------  r26089 | edk2buildsystem | 2018-01-08 02:05:36 -0800 (Mon, 08 Jan 2018) | 8 lines
  BaseTools: Fix Pcd value override issue caused by SKU inherit
  Pcd default value in DEC should only be assigned once.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 4cc824283ce5d87d974a9b5677d925684201b0f5)

------------------------------------------------------------------------  r26090 | edk2buildsystem | 2018-01-08 02:05:41 -0800 (Mon, 08 Jan 2018) | 8 lines
  BaseTools: Fix Sku inherit issue.
  The final Pcd value should only be override by its parents.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Feng Bob C <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 09c80b07b4a9d3a8b89ffdc55967d38cc651e27e)

------------------------------------------------------------------------