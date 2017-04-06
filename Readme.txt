Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24310

This directory contains the Win32 binaries.

Build Date:       Thu, 06 Apr 2017 03:11:37 Pacific Daylight Time
Last Changed Rev: 24301

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24310
  BootSectImage Version 1.0 Build Build 23431
ERROR : This tool is missing --version option: Brotli.exe
ERROR : This tool is missing --version option: BrotliCompress.bat
  Ecc.exe Version 1.0 Build Build 24086
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 24310
 *GenFds.exe 1.0 Build 24310
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 24310
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 24310
  Pkcs7Sign Version 0.9 Build 24239
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24239
  Rsa2048Sha256Sign Version 0.9 Build 24239
  Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 24310
  TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 24310
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24061
 *build.exe Version 0.60 Build 24310

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/6/2017 3:11:38AM Engine version = 5700.7163
  4/6/2017 3:11:38AM AntiVirus DAT version = 8489.0
  4/6/2017 3:11:38AM Number of detection signatures in EXTRA.DAT = None
  4/6/2017 3:11:38AM Names of detection signatures in EXTRA.DAT = None
  4/6/2017 3:11:38AM Scan Started On-Demand Scan
  4/6/2017 3:11:48AM Scan Summary
  4/6/2017 3:11:48AM Processes scanned : 0
  4/6/2017 3:11:48AM Processes detected : 0
  4/6/2017 3:11:48AM Processes cleaned : 0
  4/6/2017 3:11:48AM Boot sectors scanned : 2
  4/6/2017 3:11:48AM Boot sectors detected: 0
  4/6/2017 3:11:48AM Boot sectors cleaned : 0
  4/6/2017 3:11:48AM Files scanned : 64
  4/6/2017 3:11:48AM Files with detections: 0
  4/6/2017 3:11:48AM File detections : 0
  4/6/2017 3:11:48AM Files cleaned : 0
  4/6/2017 3:11:48AM Files deleted : 0
  4/6/2017 3:11:48AM Files not scanned : 0
  4/6/2017 3:11:48AM Scan Summary (Registry Scanning)
  4/6/2017 3:11:48AM Keys scanned : 0
  4/6/2017 3:11:48AM Keys detected : 0
  4/6/2017 3:11:48AM Keys cleaned : 0
  4/6/2017 3:11:48AM Keys deleted : 0
  4/6/2017 3:11:48AM Run time : 0:00:11
  4/6/2017 3:11:48AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24289:HEAD Source
------------------------------------------------------------------------  r24300 | edk2buildsystem | 2017-04-06 02:06:05 -0700 (Thu, 06 Apr 2017) | 7 lines
  BaseTools: Add the missing copyrights in BrotliCompress.bat
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 8693aa6a13329a8612412789b5471c56e515ed45)

------------------------------------------------------------------------  r24301 | edk2buildsystem | 2017-04-06 02:06:10 -0700 (Thu, 06 Apr 2017) | 10 lines
  BaseTools: update error message for SKUID_IDENTIFIER format
  Per DSC spec, the SkuUiName use '|' as separator, so this patch update
  the error message to use '|' but not space as separator.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 6035094da8b68c0d66cce327309efee551caa5dc)

------------------------------------------------------------------------