Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24289

This directory contains the Win32 binaries.

Build Date:       Wed, 05 Apr 2017 03:11:09 Pacific Daylight Time
Last Changed Rev: 24285

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24278
  BootSectImage Version 1.0 Build Build 23431
ERROR : This tool is missing --version option: Brotli.exe
ERROR : This tool is missing --version option: BrotliCompress.bat
  Ecc.exe Version 1.0 Build Build 24086
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
  GenDepex.exe Version 0.04 Build 24278
  GenFds.exe 1.0 Build 24278
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 24278
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 24278
  Pkcs7Sign Version 0.9 Build 24239
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24239
  Rsa2048Sha256Sign Version 0.9 Build 24239
  Split Version 1.0 Build Build 23431
  TargetTool.exe Version 0.01 Build 24278
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 24278
 *UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24061
  build.exe Version 0.60 Build 24278

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/5/2017 3:11:10AM Engine version = 5700.7163
  4/5/2017 3:11:10AM AntiVirus DAT version = 8488.0
  4/5/2017 3:11:10AM Number of detection signatures in EXTRA.DAT = None
  4/5/2017 3:11:10AM Names of detection signatures in EXTRA.DAT = None
  4/5/2017 3:11:10AM Scan Started On-Demand Scan
  4/5/2017 3:11:17AM Scan Summary
  4/5/2017 3:11:17AM Processes scanned : 0
  4/5/2017 3:11:17AM Processes detected : 0
  4/5/2017 3:11:17AM Processes cleaned : 0
  4/5/2017 3:11:17AM Boot sectors scanned : 2
  4/5/2017 3:11:17AM Boot sectors detected: 0
  4/5/2017 3:11:17AM Boot sectors cleaned : 0
  4/5/2017 3:11:17AM Files scanned : 64
  4/5/2017 3:11:17AM Files with detections: 0
  4/5/2017 3:11:17AM File detections : 0
  4/5/2017 3:11:17AM Files cleaned : 0
  4/5/2017 3:11:17AM Files deleted : 0
  4/5/2017 3:11:17AM Files not scanned : 0
  4/5/2017 3:11:17AM Scan Summary (Registry Scanning)
  4/5/2017 3:11:17AM Keys scanned : 0
  4/5/2017 3:11:17AM Keys detected : 0
  4/5/2017 3:11:17AM Keys cleaned : 0
  4/5/2017 3:11:17AM Keys deleted : 0
  4/5/2017 3:11:17AM Run time : 0:00:07
  4/5/2017 3:11:17AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24278:HEAD Source
------------------------------------------------------------------------  r24283 | edk2buildsystem | 2017-04-05 02:05:36 -0700 (Wed, 05 Apr 2017) | 9 lines
  BaseTools/UPT: Use a simple way to get package path
  Instead of parsing all content of DEC file, just get the package
  path only to save time.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 5692fa883f4e2583bbef9aae4082b87515ae51e1)

------------------------------------------------------------------------  r24284 | edk2buildsystem | 2017-04-05 02:05:43 -0700 (Wed, 05 Apr 2017) | 8 lines
  BaseTools/UPT: Support Unicode path
  Update the IpiDb.py to support Unicode path for localization
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 09e27ac559c5538a0b86afb0b056ef2a3f705483)

------------------------------------------------------------------------  r24285 | edk2buildsystem | 2017-04-05 02:05:48 -0700 (Wed, 05 Apr 2017) | 8 lines
  BaseTools/UPT: Fix a parser issue
  Update the method to get PCD information and support empty section.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 490433ab847cf318f31f73bbbc1a503ae47370a4)

------------------------------------------------------------------------