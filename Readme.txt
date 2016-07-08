Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 21725

This directory contains the Win32 binaries.

Build Date:       Fri, 08 Jul 2016 03:11:21 Pacific Daylight Time
Last Changed Rev: 21607

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 21077
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
  GenDepex.exe Version 0.04 Build 21077
  GenFds.exe 1.0 Build 21077
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 20909
  GenFw Version 0.2 Build 20909
  GenPage Version 0.2 Build 20909
  GenPatchPcdTable.exe Version 0.10 Build 21077
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
  PatchPcdValue.exe Version 0.10 Build 21077
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
  TargetTool.exe Version 0.01 Build 21077
  TianoCompress Version 0.1 Build 20909
  Trim.exe Version 0.10 Build 21077
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20909
  VolInfo Version 1.0 Build Build 20909
 *build.exe Version 0.60 Build 21725

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  7/8/2016 3:11:22AM Engine version = 5700.7163
  7/8/2016 3:11:22AM AntiVirus DAT version = 8216.0
  7/8/2016 3:11:22AM Number of detection signatures in EXTRA.DAT = 3
  7/8/2016 3:11:22AM Names of detection signatures in EXTRA.DAT = W97M/Downloader.ber (ED) W97M/Downloader.bes (ED) W97M/Downloader.bet (ED)
  7/8/2016 3:11:22AM Scan Started On-Demand Scan
  7/8/2016 3:11:24AM Scan Summary
  7/8/2016 3:11:24AM Processes scanned : 0
  7/8/2016 3:11:24AM Processes detected : 0
  7/8/2016 3:11:24AM Processes cleaned : 0
  7/8/2016 3:11:24AM Boot sectors scanned : 1
  7/8/2016 3:11:24AM Boot sectors detected: 0
  7/8/2016 3:11:24AM Boot sectors cleaned : 0
  7/8/2016 3:11:24AM Files scanned : 55
  7/8/2016 3:11:24AM Files with detections: 0
  7/8/2016 3:11:24AM File detections : 0
  7/8/2016 3:11:24AM Files cleaned : 0
  7/8/2016 3:11:24AM Files deleted : 0
  7/8/2016 3:11:24AM Files not scanned : 0
  7/8/2016 3:11:24AM Scan Summary (Registry Scanning)
  7/8/2016 3:11:24AM Keys scanned : 0
  7/8/2016 3:11:24AM Keys detected : 0
  7/8/2016 3:11:24AM Keys cleaned : 0
  7/8/2016 3:11:24AM Keys deleted : 0
  7/8/2016 3:11:24AM Run time : 0:00:02
  7/8/2016 3:11:24AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 21077:HEAD Source
------------------------------------------------------------------------  r21607 | edk2buildsystem | 2016-07-05 02:06:06 -0700 (Tue, 05 Jul 2016) | 10 lines
  BaseTools: Add support for $(FAMILY) macro
  Build spec mentions $(FAMILY) macro be used in DSC/FDF to specify the tool
  chain family, like GCC, MSFT. This patch add the support for this macro.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 40b4e21dbc6c4c3ba2a1748be97bf90acb3b45b8)

------------------------------------------------------------------------