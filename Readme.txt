Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24239

This directory contains the Win32 binaries.

Build Date:       Wed, 29 Mar 2017 03:11:14 Pacific Daylight Time
Last Changed Rev: 24239

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24199
  BootSectImage Version 1.0 Build Build 23431
  Ecc.exe Version 1.0 Build Build 24086
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
  GenDepex.exe Version 0.04 Build 24199
  GenFds.exe 1.0 Build 24199
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 24199
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 24199
 *Pkcs7Sign Version 0.9 Build 24239
 *Rsa2048Sha256GenerateKeys Version 0.9 Build 24239
 *Rsa2048Sha256Sign Version 0.9 Build 24239
  Split Version 1.0 Build Build 23431
  TargetTool.exe Version 0.01 Build 24199
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 24199
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24130
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24061
  build.exe Version 0.60 Build 24199

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/29/2017 3:11:16AM Engine version = 5700.7163
  3/29/2017 3:11:16AM AntiVirus DAT version = 8481.0
  3/29/2017 3:11:16AM Number of detection signatures in EXTRA.DAT = None
  3/29/2017 3:11:16AM Names of detection signatures in EXTRA.DAT = None
  3/29/2017 3:11:16AM Scan Started On-Demand Scan
  3/29/2017 3:11:27AM Scan Summary
  3/29/2017 3:11:27AM Processes scanned : 0
  3/29/2017 3:11:27AM Processes detected : 0
  3/29/2017 3:11:27AM Processes cleaned : 0
  3/29/2017 3:11:27AM Boot sectors scanned : 2
  3/29/2017 3:11:27AM Boot sectors detected: 0
  3/29/2017 3:11:27AM Boot sectors cleaned : 0
  3/29/2017 3:11:27AM Files scanned : 62
  3/29/2017 3:11:27AM Files with detections: 0
  3/29/2017 3:11:27AM File detections : 0
  3/29/2017 3:11:27AM Files cleaned : 0
  3/29/2017 3:11:27AM Files deleted : 0
  3/29/2017 3:11:27AM Files not scanned : 0
  3/29/2017 3:11:27AM Scan Summary (Registry Scanning)
  3/29/2017 3:11:27AM Keys scanned : 0
  3/29/2017 3:11:27AM Keys detected : 0
  3/29/2017 3:11:27AM Keys cleaned : 0
  3/29/2017 3:11:27AM Keys deleted : 0
  3/29/2017 3:11:27AM Run time : 0:00:12
  3/29/2017 3:11:27AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24199:HEAD Source
------------------------------------------------------------------------  r24225 | edk2buildsystem | 2017-03-29 02:06:51 -0700 (Wed, 29 Mar 2017) | 9 lines
  BaseTools: Copy Brotli algorithm 3rd party source code for tool
  - Copy Brotli algorithm 3rd party source code for tool
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Bell Song <binx.song@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 11b7501adcf8af81b3a31702eb4daa799d5f4096)

------------------------------------------------------------------------  r24226 | edk2buildsystem | 2017-03-29 02:07:01 -0700 (Wed, 29 Mar 2017) | 9 lines
  BaseTools: Add Brotli algorithm tool
  - Add Brotli algorithm tool support
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Bell Song <binx.song@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 87d97b6a771a5f81277732d5d9985aa9d14ae63f)

------------------------------------------------------------------------  r24239 | edk2buildsystem | 2017-03-29 02:08:35 -0700 (Wed, 29 Mar 2017) | 10 lines
  BaseTools: Update Pkcs7 and RSA2048 tool with shell=True
  Pkcs7Sign, Rsa2048Sha256Sign and Rsa2048Sha256GenerateKeys doesn't work
  on Linux. It needs to be changed with shell=True.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a5f26fefca2edb7f3b2772966b79351b7edbcc3f)

------------------------------------------------------------------------