Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25532

This directory contains the Win32 binaries.

Build Date:       Mon, 16 Oct 2017 03:12:56 Pacific Daylight Time
Last Changed Rev: 25532

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25532
  BootSectImage Version 1.0 Build Build 25453
  Brotli Version 0.5.2 Build 25453
  Brotli Version 0.5.2 Build 25453
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25453
  EfiRom Version 0.1 Build 25453
  GenBootSector Version 0.2 Build 25453
  GenCrc32 Version 0.2 Build 25453
 *GenDepex.exe Version 0.04 Build 25532
 *GenFds.exe 1.0 Build 25532
  GenFfs Version 0.1 Build 25453
  GenFv Version 0.1 Build 25453
  GenFw Version 0.2 Build 25453
  GenPage Version 0.2 Build 25453
 *GenPatchPcdTable.exe Version 0.10 Build 25532
  GenSec Version 0.1 Build 25453
  GenVtf Version 0.1 Build 25453
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25453
  LzmaF86Compress Version 0.2 Build 25453
 *PatchPcdValue.exe Version 0.10 Build 25532
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25453
 *TargetTool.exe Version 0.01 Build 25532
  TianoCompress Version 0.1 Build 25453
 *Trim.exe Version 0.10 Build 25532
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25453
  VolInfo Version 1.0 Build Build 25453
 *build.exe Version 0.60 Build 25532

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/16/2017 3:12:58AM Engine version = 5900.7806
  10/16/2017 3:12:58AM AntiVirus DAT version = 8685.0
  10/16/2017 3:12:58AM Number of detection signatures in EXTRA.DAT = None
  10/16/2017 3:12:58AM Names of detection signatures in EXTRA.DAT = None
  10/16/2017 3:12:58AM Scan Started On-Demand Scan
  10/16/2017 3:13:16AM Scan Summary
  10/16/2017 3:13:16AM Processes scanned : 0
  10/16/2017 3:13:16AM Processes detected : 0
  10/16/2017 3:13:16AM Processes cleaned : 0
  10/16/2017 3:13:16AM Boot sectors scanned : 2
  10/16/2017 3:13:16AM Boot sectors detected: 0
  10/16/2017 3:13:16AM Boot sectors cleaned : 0
  10/16/2017 3:13:16AM Files scanned : 64
  10/16/2017 3:13:16AM Files with detections: 0
  10/16/2017 3:13:16AM File detections : 0
  10/16/2017 3:13:16AM Files cleaned : 0
  10/16/2017 3:13:16AM Files deleted : 0
  10/16/2017 3:13:16AM Files not scanned : 0
  10/16/2017 3:13:16AM Scan Summary (Registry Scanning)
  10/16/2017 3:13:16AM Keys scanned : 0
  10/16/2017 3:13:16AM Keys detected : 0
  10/16/2017 3:13:16AM Keys cleaned : 0
  10/16/2017 3:13:16AM Keys deleted : 0
  10/16/2017 3:13:16AM Run time : 0:00:19
  10/16/2017 3:13:16AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25514:HEAD Source
------------------------------------------------------------------------  r25532 | edk2buildsystem | 2017-10-16 02:06:07 -0700 (Mon, 16 Oct 2017) | 13 lines
  BaseTools: Fix a bug Build directory should relative to WORKSPACE
  The bug is for build output files it still use mws.join function, it
  cause maybe we will get the build output files in the PACKAGES_PATH
  because mws.join will try WORKSPACE first, if the file doesn't exist
  then try PACKAGES_PATH. But for build output, we expected it should
  relative to WORKSPACE.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 97058144294759ffb64005a8543d5dd9a5bdc1fc)

------------------------------------------------------------------------