Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22067

This directory contains the Win32 binaries.

Build Date:       Mon, 18 Jul 2016 03:11:44 Pacific Daylight Time
Last Changed Rev: 22030

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22067
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
 *GenDepex.exe Version 0.04 Build 22067
 *GenFds.exe 1.0 Build 22067
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 20909
  GenFw Version 0.2 Build 20909
  GenPage Version 0.2 Build 20909
 *GenPatchPcdTable.exe Version 0.10 Build 22067
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
 *PatchPcdValue.exe Version 0.10 Build 22067
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
 *TargetTool.exe Version 0.01 Build 22067
  TianoCompress Version 0.1 Build 20909
 *Trim.exe Version 0.10 Build 22067
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20909
  VolInfo Version 1.0 Build Build 20909
 *build.exe Version 0.60 Build 22067

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  7/18/2016 3:11:45AM Engine version = 5700.7163
  7/18/2016 3:11:45AM AntiVirus DAT version = 8229.0
  7/18/2016 3:11:45AM Number of detection signatures in EXTRA.DAT = None
  7/18/2016 3:11:45AM Names of detection signatures in EXTRA.DAT = None
  7/18/2016 3:11:45AM Scan Started On-Demand Scan
  7/18/2016 3:11:47AM Scan Summary
  7/18/2016 3:11:47AM Processes scanned : 0
  7/18/2016 3:11:47AM Processes detected : 0
  7/18/2016 3:11:47AM Processes cleaned : 0
  7/18/2016 3:11:47AM Boot sectors scanned : 1
  7/18/2016 3:11:47AM Boot sectors detected: 0
  7/18/2016 3:11:47AM Boot sectors cleaned : 0
  7/18/2016 3:11:47AM Files scanned : 55
  7/18/2016 3:11:47AM Files with detections: 0
  7/18/2016 3:11:47AM File detections : 0
  7/18/2016 3:11:47AM Files cleaned : 0
  7/18/2016 3:11:47AM Files deleted : 0
  7/18/2016 3:11:47AM Files not scanned : 0
  7/18/2016 3:11:47AM Scan Summary (Registry Scanning)
  7/18/2016 3:11:47AM Keys scanned : 0
  7/18/2016 3:11:47AM Keys detected : 0
  7/18/2016 3:11:47AM Keys cleaned : 0
  7/18/2016 3:11:47AM Keys deleted : 0
  7/18/2016 3:11:47AM Run time : 0:00:02
  7/18/2016 3:11:47AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 21814:HEAD Source
------------------------------------------------------------------------  r22030 | edk2buildsystem | 2016-07-18 02:06:22 -0700 (Mon, 18 Jul 2016) | 11 lines
  BaseTools: Fix a bug for FixedPcd value generation in AutoGen file
  If the library is listed in [Components] section for build only, its
  used FixedPcd Value is not generated into AutoGen code. This patch
  cover this case to generate the FixedPcd Value in AutoGen file.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c9da41b235eaf34248c92839924650f071079dc8)

------------------------------------------------------------------------