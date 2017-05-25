Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24714

This directory contains the Win32 binaries.

Build Date:       Thu, 25 May 2017 03:12:07 Pacific Daylight Time
Last Changed Rev: 24701

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24714
  BootSectImage Version 1.0 Build Build 23431
  Brotli Version 0.5.2 Build 24577
  Brotli Version 0.5.2 Build 24577
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 24714
 *GenFds.exe 1.0 Build 24714
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 24714
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 24714
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 24714
  TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 24714
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24507
 *build.exe Version 0.60 Build 24714

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/25/2017 3:12:08AM Engine version = 5700.7163
  5/25/2017 3:12:08AM AntiVirus DAT version = 8539.0
  5/25/2017 3:12:08AM Number of detection signatures in EXTRA.DAT = None
  5/25/2017 3:12:08AM Names of detection signatures in EXTRA.DAT = None
  5/25/2017 3:12:08AM Scan Started On-Demand Scan
  5/25/2017 3:12:13AM Scan Summary
  5/25/2017 3:12:13AM Processes scanned : 0
  5/25/2017 3:12:13AM Processes detected : 0
  5/25/2017 3:12:13AM Processes cleaned : 0
  5/25/2017 3:12:13AM Boot sectors scanned : 2
  5/25/2017 3:12:13AM Boot sectors detected: 0
  5/25/2017 3:12:13AM Boot sectors cleaned : 0
  5/25/2017 3:12:13AM Files scanned : 64
  5/25/2017 3:12:13AM Files with detections: 0
  5/25/2017 3:12:13AM File detections : 0
  5/25/2017 3:12:13AM Files cleaned : 0
  5/25/2017 3:12:13AM Files deleted : 0
  5/25/2017 3:12:13AM Files not scanned : 0
  5/25/2017 3:12:13AM Scan Summary (Registry Scanning)
  5/25/2017 3:12:13AM Keys scanned : 0
  5/25/2017 3:12:13AM Keys detected : 0
  5/25/2017 3:12:13AM Keys cleaned : 0
  5/25/2017 3:12:13AM Keys deleted : 0
  5/25/2017 3:12:13AM Run time : 0:00:05
  5/25/2017 3:12:13AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24697:HEAD Source
------------------------------------------------------------------------  r24701 | edk2buildsystem | 2017-05-25 02:05:35 -0700 (Thu, 25 May 2017) | 11 lines
  BaseTools: Correct if condition expression for DatumType == 'VOID*'
  Correct the if condition expression for DatumType == 'VOID*'. Current
  this condition is not work since the DatumType is changed before we do
  the value judgement.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 687bde9cac2ce1a45d916bc26caa370d15d58fce)

------------------------------------------------------------------------