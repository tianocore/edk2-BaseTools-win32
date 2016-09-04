Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22543

This directory contains the Win32 binaries.

Build Date:       Sun, 04 Sep 2016 03:11:13 Pacific Daylight Time
Last Changed Rev: 22543

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22444
  BootSectImage Version 1.0 Build Build 22449
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 22449
  EfiRom Version 0.1 Build 22449
  GenBootSector Version 0.2 Build 22449
  GenCrc32 Version 0.2 Build 22449
  GenDepex.exe Version 0.04 Build 22444
  GenFds.exe 1.0 Build 22489
  GenFfs Version 0.1 Build 22449
 *GenFv Version 0.1 Build 22543
  GenFw Version 0.2 Build 22466
  GenPage Version 0.2 Build 22449
  GenPatchPcdTable.exe Version 0.10 Build 22444
  GenSec Version 0.1 Build 22449
  GenVtf Version 0.1 Build 22449
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 22449
  LzmaF86Compress Version 0.2 Build 22449
  PatchPcdValue.exe Version 0.10 Build 22444
 *Pkcs7Sign Version 0.9 Build 22543
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 22444
  Split Version 1.0 Build Build 22449
  TargetTool.exe Version 0.01 Build 22444
  TianoCompress Version 0.1 Build 22449
  Trim.exe Version 0.10 Build 22444
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22316
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22449
  VolInfo Version 1.0 Build Build 22449
  build.exe Version 0.60 Build 22444

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  9/4/2016 3:11:14AM Engine version = 5700.7163
  9/4/2016 3:11:14AM AntiVirus DAT version = 8277.0
  9/4/2016 3:11:14AM Number of detection signatures in EXTRA.DAT = 2
  9/4/2016 3:11:14AM Names of detection signatures in EXTRA.DAT = Generic.Tra!3c09cefe0e8d (ED) Generic.Tra!5876ae4f5bf5 (ED)
  9/4/2016 3:11:14AM Scan Started On-Demand Scan
  9/4/2016 3:11:17AM Scan Summary
  9/4/2016 3:11:17AM Processes scanned : 0
  9/4/2016 3:11:17AM Processes detected : 0
  9/4/2016 3:11:17AM Processes cleaned : 0
  9/4/2016 3:11:17AM Boot sectors scanned : 1
  9/4/2016 3:11:17AM Boot sectors detected: 0
  9/4/2016 3:11:17AM Boot sectors cleaned : 0
  9/4/2016 3:11:17AM Files scanned : 63
  9/4/2016 3:11:17AM Files with detections: 0
  9/4/2016 3:11:17AM File detections : 0
  9/4/2016 3:11:17AM Files cleaned : 0
  9/4/2016 3:11:17AM Files deleted : 0
  9/4/2016 3:11:17AM Files not scanned : 0
  9/4/2016 3:11:17AM Scan Summary (Registry Scanning)
  9/4/2016 3:11:17AM Keys scanned : 0
  9/4/2016 3:11:17AM Keys detected : 0
  9/4/2016 3:11:17AM Keys cleaned : 0
  9/4/2016 3:11:17AM Keys deleted : 0
  9/4/2016 3:11:17AM Run time : 0:00:03
  9/4/2016 3:11:17AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22489:HEAD Source
------------------------------------------------------------------------  r22489 | edk2buildsystem | 2016-08-30 02:05:40 -0700 (Tue, 30 Aug 2016) | 11 lines
  BaseTools: UpdateImageSize include Image auth info for FMP Auth capsule
  Per UEFI spec UpdateImageSize may or may not include Firmware Image
  Authentication information. so for FMP auth capsule, UpdateImageSize
  should include the Image auth info.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5f53a7aa59d4df1fe4326af18a9240d4dfebc129)

------------------------------------------------------------------------  r22543 | edk2buildsystem | 2016-09-04 02:05:28 -0700 (Sun, 04 Sep 2016) | 7 lines
  BaseTools: Change source files to DOS format
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 11eaa7affb8b325b3e00bbe9e4357705ce3b2b08)

------------------------------------------------------------------------