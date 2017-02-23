Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23940

This directory contains the Win32 binaries.

Build Date:       Thu, 23 Feb 2017 03:11:15 Pacific Standard Time
Last Changed Rev: 23937

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23940
  BootSectImage Version 1.0 Build Build 23431
  Ecc.exe Version 1.0 Build Build 23673
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 23940
 *GenFds.exe 1.0 Build 23940
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 23431
  GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 23940
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 23431
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 23940
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 23940
  TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 23940
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 23468
 *build.exe Version 0.60 Build 23940

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/23/2017 3:11:16AM Engine version = 5700.7163
  2/23/2017 3:11:16AM AntiVirus DAT version = 8447.0
  2/23/2017 3:11:16AM Number of detection signatures in EXTRA.DAT = None
  2/23/2017 3:11:16AM Names of detection signatures in EXTRA.DAT = None
  2/23/2017 3:11:16AM Scan Started On-Demand Scan
  2/23/2017 3:11:25AM Scan Summary
  2/23/2017 3:11:25AM Processes scanned : 0
  2/23/2017 3:11:25AM Processes detected : 0
  2/23/2017 3:11:25AM Processes cleaned : 0
  2/23/2017 3:11:25AM Boot sectors scanned : 2
  2/23/2017 3:11:25AM Boot sectors detected: 0
  2/23/2017 3:11:25AM Boot sectors cleaned : 0
  2/23/2017 3:11:25AM Files scanned : 62
  2/23/2017 3:11:25AM Files with detections: 0
  2/23/2017 3:11:25AM File detections : 0
  2/23/2017 3:11:25AM Files cleaned : 0
  2/23/2017 3:11:25AM Files deleted : 0
  2/23/2017 3:11:25AM Files not scanned : 0
  2/23/2017 3:11:25AM Scan Summary (Registry Scanning)
  2/23/2017 3:11:25AM Keys scanned : 0
  2/23/2017 3:11:25AM Keys detected : 0
  2/23/2017 3:11:25AM Keys cleaned : 0
  2/23/2017 3:11:25AM Keys deleted : 0
  2/23/2017 3:11:25AM Run time : 0:00:09
  2/23/2017 3:11:25AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23932:HEAD Source
------------------------------------------------------------------------  r23937 | edk2buildsystem | 2017-02-23 02:05:32 -0800 (Thu, 23 Feb 2017) | 12 lines
  BaseTools: Fix the regression issue caused by commit dc4c77
  In the last commit dc4c77, the _GetHeaderInfo will be called more than
  once, which cause the self._ConstructorList.append(Value) append some
  duplicate value.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Tested-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1d8cebf91040e74f6c82352edd5c5cccf6b69853)

------------------------------------------------------------------------