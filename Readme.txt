Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24577

This directory contains the Win32 binaries.

Build Date:       Tue, 09 May 2017 22:23:56 Pacific Daylight Time
Last Changed Rev: 24555

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24555
  BootSectImage Version 1.0 Build Build 23431
 *Brotli Version 0.5.2 Build 24577
 *Brotli Version 0.5.2 Build 24577
  Ecc.exe Version 1.0 Build Build 24382
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
  GenDepex.exe Version 0.04 Build 24555
  GenFds.exe 1.0 Build 24555
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 24555
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 24555
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 23431
  TargetTool.exe Version 0.01 Build 24555
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 24555
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24507
  build.exe Version 0.60 Build 24555

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/9/2017 10:23:57PM Engine version = 5700.7163
  5/9/2017 10:23:57PM AntiVirus DAT version = 8523.0
  5/9/2017 10:23:57PM Number of detection signatures in EXTRA.DAT = None
  5/9/2017 10:23:57PM Names of detection signatures in EXTRA.DAT = None
  5/9/2017 10:23:57PM Scan Started On-Demand Scan
  5/9/2017 10:23:59PM Scan Summary
  5/9/2017 10:23:59PM Processes scanned : 0
  5/9/2017 10:23:59PM Processes detected : 0
  5/9/2017 10:23:59PM Processes cleaned : 0
  5/9/2017 10:23:59PM Boot sectors scanned : 0
  5/9/2017 10:23:59PM Boot sectors detected: 0
  5/9/2017 10:23:59PM Boot sectors cleaned : 0
  5/9/2017 10:23:59PM Files scanned : 64
  5/9/2017 10:23:59PM Files with detections: 0
  5/9/2017 10:23:59PM File detections : 0
  5/9/2017 10:23:59PM Files cleaned : 0
  5/9/2017 10:23:59PM Files deleted : 0
  5/9/2017 10:23:59PM Files not scanned : 0
  5/9/2017 10:23:59PM Scan Summary (Registry Scanning)
  5/9/2017 10:23:59PM Keys scanned : 0
  5/9/2017 10:23:59PM Keys detected : 0
  5/9/2017 10:23:59PM Keys cleaned : 0
  5/9/2017 10:23:59PM Keys deleted : 0
  5/9/2017 10:23:59PM Run time : 0:00:02
  5/9/2017 10:23:59PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24555:HEAD Source
------------------------------------------------------------------------  r24555 | edk2buildsystem | 2017-05-06 14:05:22 -0700 (Sat, 06 May 2017) | 10 lines
  BaseTools: PCD can only use single access method by source build
  Add the error check that A PCD can only use one type for all source
  modules.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 97cdb33b575a80ca5c20ad862331f3c6d9415575)

------------------------------------------------------------------------