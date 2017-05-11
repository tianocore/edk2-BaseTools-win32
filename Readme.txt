Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24602

This directory contains the Win32 binaries.

Build Date:       Thu, 11 May 2017 03:13:16 Pacific Daylight Time
Last Changed Rev: 24587

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24602
  BootSectImage Version 1.0 Build Build 23431
  Brotli Version 0.5.2 Build 24577
  Brotli Version 0.5.2 Build 24577
 *Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 24602
 *GenFds.exe 1.0 Build 24602
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 24602
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 24602
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 24602
  TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 24602
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24507
 *build.exe Version 0.60 Build 24602

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/11/2017 3:13:19AM Engine version = 5700.7163
  5/11/2017 3:13:19AM AntiVirus DAT version = 8524.0
  5/11/2017 3:13:19AM Number of detection signatures in EXTRA.DAT = None
  5/11/2017 3:13:19AM Names of detection signatures in EXTRA.DAT = None
  5/11/2017 3:13:19AM Scan Started On-Demand Scan
  5/11/2017 3:13:24AM Scan Summary
  5/11/2017 3:13:24AM Processes scanned : 0
  5/11/2017 3:13:24AM Processes detected : 0
  5/11/2017 3:13:24AM Processes cleaned : 0
  5/11/2017 3:13:24AM Boot sectors scanned : 2
  5/11/2017 3:13:24AM Boot sectors detected: 0
  5/11/2017 3:13:24AM Boot sectors cleaned : 0
  5/11/2017 3:13:24AM Files scanned : 64
  5/11/2017 3:13:24AM Files with detections: 0
  5/11/2017 3:13:24AM File detections : 0
  5/11/2017 3:13:24AM Files cleaned : 0
  5/11/2017 3:13:24AM Files deleted : 0
  5/11/2017 3:13:24AM Files not scanned : 0
  5/11/2017 3:13:24AM Scan Summary (Registry Scanning)
  5/11/2017 3:13:24AM Keys scanned : 0
  5/11/2017 3:13:24AM Keys detected : 0
  5/11/2017 3:13:24AM Keys cleaned : 0
  5/11/2017 3:13:24AM Keys deleted : 0
  5/11/2017 3:13:24AM Run time : 0:00:06
  5/11/2017 3:13:24AM Scan Complete On-Demand Scan

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

------------------------------------------------------------------------  r24583 | edk2buildsystem | 2017-05-11 02:05:33 -0700 (Thu, 11 May 2017) | 8 lines
  BaseTools/Ecc: Add line break support for exception list
  Add line break support for exception list.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit bcd999d2377d1a34bb3b5c02e4206a8d149999a2)

------------------------------------------------------------------------  r24587 | edk2buildsystem | 2017-05-11 02:05:53 -0700 (Thu, 11 May 2017) | 10 lines
  BaseTools: Correct VOID* PatchPcd Size in Library Autogen
  This patch correct the VOID* PatchPcd Size info generated in the
  Library's autogen file. Update it to use the MaxDatumSize.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a6c31c6d6349a51041d8b77df375c340043e36bd)

------------------------------------------------------------------------