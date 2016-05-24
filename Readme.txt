Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20964

This directory contains the Win32 binaries.

Build Date:       Tue, 24 May 2016 03:11:06 Pacific Daylight Time
Last Changed Rev: 20957

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20909
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
  GenDepex.exe Version 0.04 Build 20909
  GenFds.exe 1.0 Build 20909
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 20909
  GenFw Version 0.2 Build 20909
  GenPage Version 0.2 Build 20909
  GenPatchPcdTable.exe Version 0.10 Build 20909
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
  PatchPcdValue.exe Version 0.10 Build 20909
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
  TargetTool.exe Version 0.01 Build 20909
  TianoCompress Version 0.1 Build 20909
  Trim.exe Version 0.10 Build 20909
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20909
  VolInfo Version 1.0 Build Build 20909
 *build.exe Version 0.60 Build 20964

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/24/2016 3:11:08AM Engine version = 5700.7163
  5/24/2016 3:11:08AM AntiVirus DAT version = 8174.0
  5/24/2016 3:11:08AM Number of detection signatures in EXTRA.DAT = 1
  5/24/2016 3:11:08AM Names of detection signatures in EXTRA.DAT = W97M/Downloader.bdj (ED)
  5/24/2016 3:11:08AM Scan Started On-Demand Scan
  5/24/2016 3:11:10AM Scan Summary
  5/24/2016 3:11:10AM Processes scanned : 0
  5/24/2016 3:11:10AM Processes detected : 0
  5/24/2016 3:11:10AM Processes cleaned : 0
  5/24/2016 3:11:10AM Boot sectors scanned : 1
  5/24/2016 3:11:10AM Boot sectors detected: 0
  5/24/2016 3:11:10AM Boot sectors cleaned : 0
  5/24/2016 3:11:10AM Files scanned : 55
  5/24/2016 3:11:10AM Files with detections: 0
  5/24/2016 3:11:10AM File detections : 0
  5/24/2016 3:11:10AM Files cleaned : 0
  5/24/2016 3:11:10AM Files deleted : 0
  5/24/2016 3:11:10AM Files not scanned : 0
  5/24/2016 3:11:10AM Scan Summary (Registry Scanning)
  5/24/2016 3:11:10AM Keys scanned : 0
  5/24/2016 3:11:10AM Keys detected : 0
  5/24/2016 3:11:10AM Keys cleaned : 0
  5/24/2016 3:11:10AM Keys deleted : 0
  5/24/2016 3:11:10AM Run time : 0:00:02
  5/24/2016 3:11:10AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20909:HEAD Source
------------------------------------------------------------------------  r20957 | edk2buildsystem | 2016-05-23 14:05:35 -0700 (Mon, 23 May 2016) | 14 lines
  BaseTools: Add error condition for the path in PACKAGES_PATH env
  This patch adds two error conditions:
  1) if one path in PACKAGES_PATH doesn't exist.
  2) if the space exists in the PACKAGES_PATH.
  In V2, highlight one path in PACKAGES_PATH env doesn't exist.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed by: Andrew Fish <afish@apple.com>
  (cherry picked from commit f6190a01c13a6b4dd01a1765b28964db7dc58e35)

------------------------------------------------------------------------