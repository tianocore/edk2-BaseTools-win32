Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24554

This directory contains the Win32 binaries.

Build Date:       Sat, 06 May 2017 03:11:52 Pacific Daylight Time
Last Changed Rev: 24552

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24507
  BootSectImage Version 1.0 Build Build 23431
ERROR : This tool is missing --version option: Brotli.exe
ERROR : This tool is missing --version option: BrotliCompress.bat
  Ecc.exe Version 1.0 Build Build 24382
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
  GenDepex.exe Version 0.04 Build 24507
  GenFds.exe 1.0 Build 24507
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 24507
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 24507
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 23431
  TargetTool.exe Version 0.01 Build 24507
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 24507
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24507
 *build.exe Version 0.60 Build 24554

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/6/2017 3:11:53AM Engine version = 5700.7163
  5/6/2017 3:11:53AM AntiVirus DAT version = 8519.0
  5/6/2017 3:11:53AM Number of detection signatures in EXTRA.DAT = None
  5/6/2017 3:11:53AM Names of detection signatures in EXTRA.DAT = None
  5/6/2017 3:11:53AM Scan Started On-Demand Scan
  5/6/2017 3:12:05AM Scan Summary
  5/6/2017 3:12:05AM Processes scanned : 0
  5/6/2017 3:12:05AM Processes detected : 0
  5/6/2017 3:12:05AM Processes cleaned : 0
  5/6/2017 3:12:05AM Boot sectors scanned : 2
  5/6/2017 3:12:05AM Boot sectors detected: 0
  5/6/2017 3:12:05AM Boot sectors cleaned : 0
  5/6/2017 3:12:05AM Files scanned : 64
  5/6/2017 3:12:05AM Files with detections: 0
  5/6/2017 3:12:05AM File detections : 0
  5/6/2017 3:12:05AM Files cleaned : 0
  5/6/2017 3:12:05AM Files deleted : 0
  5/6/2017 3:12:05AM Files not scanned : 0
  5/6/2017 3:12:05AM Scan Summary (Registry Scanning)
  5/6/2017 3:12:05AM Keys scanned : 0
  5/6/2017 3:12:05AM Keys detected : 0
  5/6/2017 3:12:05AM Keys cleaned : 0
  5/6/2017 3:12:05AM Keys deleted : 0
  5/6/2017 3:12:05AM Run time : 0:00:12
  5/6/2017 3:12:05AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24507:HEAD Source
------------------------------------------------------------------------  r24539 | edk2buildsystem | 2017-05-05 02:06:06 -0700 (Fri, 05 May 2017) | 15 lines
  BaseTools: Add --version option in Brotli and BrotliCompress
  https://bugzilla.tianocore.org/show_bug.cgi?id=464
  V2:
  - Add build version
  V1:
  - Add --version option in Brotli and BrotliCompress
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Bell Song <binx.song@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 98cb468435be54c3191f4bca48cf5135b1927eaf)

------------------------------------------------------------------------  r24552 | edk2buildsystem | 2017-05-05 14:05:23 -0700 (Fri, 05 May 2017) | 10 lines
  BaseTools: remove the hardcoded /bin/bash for PreBuild/PostBuild
  This patch remove the hardcoded /bin/bash for PreBuild/PostBuild
  scripts.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 34816e7e16c4c337888d2518222268096f67c4fc)

------------------------------------------------------------------------