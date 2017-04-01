Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24278

This directory contains the Win32 binaries.

Build Date:       Sat, 01 Apr 2017 03:11:34 Pacific Daylight Time
Last Changed Rev: 24276

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24278
  BootSectImage Version 1.0 Build Build 23431
ERROR : This tool is missing --version option: Brotli.exe
ERROR : This tool is missing --version option: BrotliCompress.bat
  Ecc.exe Version 1.0 Build Build 24086
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 24278
 *GenFds.exe 1.0 Build 24278
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 24278
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 24278
  Pkcs7Sign Version 0.9 Build 24239
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24239
  Rsa2048Sha256Sign Version 0.9 Build 24239
  Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 24278
  TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 24278
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24130
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24061
 *build.exe Version 0.60 Build 24278

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/1/2017 3:11:35AM Engine version = 5700.7163
  4/1/2017 3:11:35AM AntiVirus DAT version = 8484.0
  4/1/2017 3:11:35AM Number of detection signatures in EXTRA.DAT = None
  4/1/2017 3:11:35AM Names of detection signatures in EXTRA.DAT = None
  4/1/2017 3:11:36AM Scan Started On-Demand Scan
  4/1/2017 3:11:46AM Scan Summary
  4/1/2017 3:11:46AM Processes scanned : 0
  4/1/2017 3:11:46AM Processes detected : 0
  4/1/2017 3:11:46AM Processes cleaned : 0
  4/1/2017 3:11:46AM Boot sectors scanned : 2
  4/1/2017 3:11:46AM Boot sectors detected: 0
  4/1/2017 3:11:46AM Boot sectors cleaned : 0
  4/1/2017 3:11:46AM Files scanned : 64
  4/1/2017 3:11:46AM Files with detections: 0
  4/1/2017 3:11:46AM File detections : 0
  4/1/2017 3:11:46AM Files cleaned : 0
  4/1/2017 3:11:46AM Files deleted : 0
  4/1/2017 3:11:46AM Files not scanned : 0
  4/1/2017 3:11:46AM Scan Summary (Registry Scanning)
  4/1/2017 3:11:46AM Keys scanned : 0
  4/1/2017 3:11:46AM Keys detected : 0
  4/1/2017 3:11:46AM Keys cleaned : 0
  4/1/2017 3:11:46AM Keys deleted : 0
  4/1/2017 3:11:46AM Run time : 0:00:11
  4/1/2017 3:11:46AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24276:HEAD Source
------------------------------------------------------------------------  r24276 | edk2buildsystem | 2017-04-01 02:06:10 -0700 (Sat, 01 Apr 2017) | 10 lines
  BaseTools: Enhance StrDefs.h to include ImageDefs.h
  Enhance StrDefs.h to include ImageDefs.h for VfrCompiler to support
  IMAGE_TOKEN usage.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit bc7d95c00d9682ca96d8cee9a0be929c2e61a299)

------------------------------------------------------------------------