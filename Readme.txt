Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24130

This directory contains the Win32 binaries.

Build Date:       Wed, 15 Mar 2017 03:11:07 Pacific Daylight Time
Last Changed Rev: 24111

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23940
  BootSectImage Version 1.0 Build Build 23431
  Ecc.exe Version 1.0 Build Build 24086
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
  GenDepex.exe Version 0.04 Build 23940
  GenFds.exe 1.0 Build 23940
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 23940
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 23940
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 23431
  TargetTool.exe Version 0.01 Build 23940
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 23940
 *UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24130
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24061
  build.exe Version 0.60 Build 23940

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/15/2017 3:11:08AM Engine version = 5700.7163
  3/15/2017 3:11:08AM AntiVirus DAT version = 8467.0
  3/15/2017 3:11:08AM Number of detection signatures in EXTRA.DAT = None
  3/15/2017 3:11:08AM Names of detection signatures in EXTRA.DAT = None
  3/15/2017 3:11:08AM Scan Started On-Demand Scan
  3/15/2017 3:11:19AM Scan Summary
  3/15/2017 3:11:19AM Processes scanned : 0
  3/15/2017 3:11:19AM Processes detected : 0
  3/15/2017 3:11:19AM Processes cleaned : 0
  3/15/2017 3:11:19AM Boot sectors scanned : 2
  3/15/2017 3:11:19AM Boot sectors detected: 0
  3/15/2017 3:11:19AM Boot sectors cleaned : 0
  3/15/2017 3:11:19AM Files scanned : 62
  3/15/2017 3:11:19AM Files with detections: 0
  3/15/2017 3:11:19AM File detections : 0
  3/15/2017 3:11:19AM Files cleaned : 0
  3/15/2017 3:11:19AM Files deleted : 0
  3/15/2017 3:11:19AM Files not scanned : 0
  3/15/2017 3:11:19AM Scan Summary (Registry Scanning)
  3/15/2017 3:11:19AM Keys scanned : 0
  3/15/2017 3:11:19AM Keys detected : 0
  3/15/2017 3:11:19AM Keys cleaned : 0
  3/15/2017 3:11:19AM Keys deleted : 0
  3/15/2017 3:11:19AM Run time : 0:00:11
  3/15/2017 3:11:19AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24096:HEAD Source
------------------------------------------------------------------------  r24111 | edk2buildsystem | 2017-03-14 14:05:45 -0700 (Tue, 14 Mar 2017) | 9 lines
  BaseTools/UPT: Fix an issue in subst command
  UPT used to use "B:" as the temp directory which may cause conflict,
  now it will choose a valid volume. Also UPT now accepts empty sections.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit c03f5b2c42911c6af436beb7bbc4f63dd054fc83)

------------------------------------------------------------------------