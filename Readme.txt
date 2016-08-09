Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22316

This directory contains the Win32 binaries.

Build Date:       Tue, 09 Aug 2016 03:11:02 Pacific Daylight Time
Last Changed Rev: 22312

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22308
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
  GenDepex.exe Version 0.04 Build 22308
  GenFds.exe 1.0 Build 22308
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 20909
  GenFw Version 0.2 Build 22308
  GenPage Version 0.2 Build 20909
  GenPatchPcdTable.exe Version 0.10 Build 22308
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
  PatchPcdValue.exe Version 0.10 Build 22308
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
  TargetTool.exe Version 0.01 Build 22308
  TianoCompress Version 0.1 Build 20909
  Trim.exe Version 0.10 Build 22308
 *UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22316
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22308
  VolInfo Version 1.0 Build Build 20909
  build.exe Version 0.60 Build 22308

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/9/2016 3:11:03AM Engine version = 5700.7163
  8/9/2016 3:11:03AM AntiVirus DAT version = 8251.0
  8/9/2016 3:11:03AM Number of detection signatures in EXTRA.DAT = None
  8/9/2016 3:11:03AM Names of detection signatures in EXTRA.DAT = None
  8/9/2016 3:11:03AM Scan Started On-Demand Scan
  8/9/2016 3:11:06AM Scan Summary
  8/9/2016 3:11:06AM Processes scanned : 0
  8/9/2016 3:11:06AM Processes detected : 0
  8/9/2016 3:11:06AM Processes cleaned : 0
  8/9/2016 3:11:06AM Boot sectors scanned : 1
  8/9/2016 3:11:06AM Boot sectors detected: 0
  8/9/2016 3:11:06AM Boot sectors cleaned : 0
  8/9/2016 3:11:06AM Files scanned : 55
  8/9/2016 3:11:06AM Files with detections: 0
  8/9/2016 3:11:06AM File detections : 0
  8/9/2016 3:11:06AM Files cleaned : 0
  8/9/2016 3:11:06AM Files deleted : 0
  8/9/2016 3:11:06AM Files not scanned : 0
  8/9/2016 3:11:06AM Scan Summary (Registry Scanning)
  8/9/2016 3:11:06AM Keys scanned : 0
  8/9/2016 3:11:06AM Keys detected : 0
  8/9/2016 3:11:06AM Keys cleaned : 0
  8/9/2016 3:11:06AM Keys deleted : 0
  8/9/2016 3:11:06AM Run time : 0:00:03
  8/9/2016 3:11:06AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22308:HEAD Source
------------------------------------------------------------------------  r22312 | edk2buildsystem | 2016-08-09 02:05:43 -0700 (Tue, 09 Aug 2016) | 9 lines
  BaseTools/UPT: Fix a install issue
  Fix a corner case issue of installing a module without
  any files which causes installing UNI file failure
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 9e730bd16418d76e400f87cf852b53f960d1d5b3)

------------------------------------------------------------------------