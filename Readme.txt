Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24344

This directory contains the Win32 binaries.

Build Date:       Tue, 11 Apr 2017 03:11:38 Pacific Daylight Time
Last Changed Rev: 24344

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24310
  BootSectImage Version 1.0 Build Build 23431
ERROR : This tool is missing --version option: Brotli.exe
ERROR : This tool is missing --version option: BrotliCompress.bat
 *Ecc.exe Version 1.0 Build Build 24344
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
  GenDepex.exe Version 0.04 Build 24310
  GenFds.exe 1.0 Build 24310
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 24310
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 24310
  Pkcs7Sign Version 0.9 Build 24239
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24239
  Rsa2048Sha256Sign Version 0.9 Build 24239
  Split Version 1.0 Build Build 23431
  TargetTool.exe Version 0.01 Build 24310
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 24310
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24061
  build.exe Version 0.60 Build 24310

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/11/2017 3:11:40AM Engine version = 5700.7163
  4/11/2017 3:11:40AM AntiVirus DAT version = 8494.0
  4/11/2017 3:11:40AM Number of detection signatures in EXTRA.DAT = None
  4/11/2017 3:11:40AM Names of detection signatures in EXTRA.DAT = None
  4/11/2017 3:11:40AM Scan Started On-Demand Scan
  4/11/2017 3:11:51AM Scan Summary
  4/11/2017 3:11:51AM Processes scanned : 0
  4/11/2017 3:11:51AM Processes detected : 0
  4/11/2017 3:11:51AM Processes cleaned : 0
  4/11/2017 3:11:51AM Boot sectors scanned : 2
  4/11/2017 3:11:51AM Boot sectors detected: 0
  4/11/2017 3:11:51AM Boot sectors cleaned : 0
  4/11/2017 3:11:51AM Files scanned : 64
  4/11/2017 3:11:51AM Files with detections: 0
  4/11/2017 3:11:51AM File detections : 0
  4/11/2017 3:11:51AM Files cleaned : 0
  4/11/2017 3:11:51AM Files deleted : 0
  4/11/2017 3:11:51AM Files not scanned : 0
  4/11/2017 3:11:51AM Scan Summary (Registry Scanning)
  4/11/2017 3:11:51AM Keys scanned : 0
  4/11/2017 3:11:51AM Keys detected : 0
  4/11/2017 3:11:51AM Keys cleaned : 0
  4/11/2017 3:11:51AM Keys deleted : 0
  4/11/2017 3:11:51AM Run time : 0:00:12
  4/11/2017 3:11:51AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24344:HEAD Source
------------------------------------------------------------------------  r24344 | edk2buildsystem | 2017-04-11 02:05:37 -0700 (Tue, 11 Apr 2017) | 9 lines
  BaseTools/ECC: Change check rule for Ifndef statement
  Remove the check of Ifndef statement on .c files, only check on .h
  files.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit f8c1facf34a1f65082fa22fdbc20a6e0ab8887b4)

------------------------------------------------------------------------