Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23459

This directory contains the Win32 binaries.

Build Date:       Fri, 02 Dec 2016 03:11:20 Pacific Standard Time
Last Changed Rev: 23458

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23459
  BootSectImage Version 1.0 Build Build 23431
  Ecc.exe Version 1.0 Build Build 22854
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 23459
 *GenFds.exe 1.0 Build 23459
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 23431
  GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 23459
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 23431
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 23459
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 23459
  TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 23459
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23431
  VolInfo Version 1.0 Build Build 23431
 *build.exe Version 0.60 Build 23459

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/2/2016 3:11:21AM Engine version = 5700.7163
  12/2/2016 3:11:21AM AntiVirus DAT version = 8366.0
  12/2/2016 3:11:21AM Number of detection signatures in EXTRA.DAT = None
  12/2/2016 3:11:21AM Names of detection signatures in EXTRA.DAT = None
  12/2/2016 3:11:21AM Scan Started On-Demand Scan
  12/2/2016 3:11:24AM Scan Summary
  12/2/2016 3:11:24AM Processes scanned : 0
  12/2/2016 3:11:24AM Processes detected : 0
  12/2/2016 3:11:24AM Processes cleaned : 0
  12/2/2016 3:11:24AM Boot sectors scanned : 1
  12/2/2016 3:11:24AM Boot sectors detected: 0
  12/2/2016 3:11:24AM Boot sectors cleaned : 0
  12/2/2016 3:11:24AM Files scanned : 62
  12/2/2016 3:11:24AM Files with detections: 0
  12/2/2016 3:11:24AM File detections : 0
  12/2/2016 3:11:24AM Files cleaned : 0
  12/2/2016 3:11:24AM Files deleted : 0
  12/2/2016 3:11:24AM Files not scanned : 0
  12/2/2016 3:11:24AM Scan Summary (Registry Scanning)
  12/2/2016 3:11:24AM Keys scanned : 0
  12/2/2016 3:11:24AM Keys detected : 0
  12/2/2016 3:11:24AM Keys cleaned : 0
  12/2/2016 3:11:24AM Keys deleted : 0
  12/2/2016 3:11:24AM Run time : 0:00:03
  12/2/2016 3:11:24AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23431:HEAD Source
------------------------------------------------------------------------  r23456 | edk2buildsystem | 2016-12-02 02:05:58 -0800 (Fri, 02 Dec 2016) | 10 lines
  BaseTools: add error check for "#image" for idf file format
  Add new error check for "#image" keyword used in the image definition
  file.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 31bf6304ba2dd97585c0170f0040ea48a6973746)

------------------------------------------------------------------------  r23457 | edk2buildsystem | 2016-12-02 02:06:03 -0800 (Fri, 02 Dec 2016) | 10 lines
  BaseTools: Fix the bug to parse the new map file format
  Current the variable and Pcd format save in the map file is changed, so
  this patch is to support this new format.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 3e7e8571da891122c6821ebc428ce6dbd8a35ff3)

------------------------------------------------------------------------  r23458 | edk2buildsystem | 2016-12-02 02:06:08 -0800 (Fri, 02 Dec 2016) | 11 lines
  BaseTools: Support QuotedString for PREBUILD/POSTBUILD in DSC file
  If the prebuild/postbuild script statement start with double quotations,
  current tool report error, while DSC spec allow this usage. so update
  tool to support it.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c62f1874f4df469e620dd72a9d31b51d9d99be27)

------------------------------------------------------------------------