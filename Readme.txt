Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22183

This directory contains the Win32 binaries.

Build Date:       Wed, 27 Jul 2016 03:11:23 Pacific Daylight Time
Last Changed Rev: 22168

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22183
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
 *GenDepex.exe Version 0.04 Build 22183
 *GenFds.exe 1.0 Build 22183
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 20909
  GenFw Version 0.2 Build 20909
  GenPage Version 0.2 Build 20909
 *GenPatchPcdTable.exe Version 0.10 Build 22183
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
 *PatchPcdValue.exe Version 0.10 Build 22183
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
 *TargetTool.exe Version 0.01 Build 22183
  TianoCompress Version 0.1 Build 20909
 *Trim.exe Version 0.10 Build 22183
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20909
  VolInfo Version 1.0 Build Build 20909
 *build.exe Version 0.60 Build 22183

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  7/27/2016 3:11:24AM Engine version = 5700.7163
  7/27/2016 3:11:24AM AntiVirus DAT version = 8238.0
  7/27/2016 3:11:24AM Number of detection signatures in EXTRA.DAT = None
  7/27/2016 3:11:24AM Names of detection signatures in EXTRA.DAT = None
  7/27/2016 3:11:24AM Scan Started On-Demand Scan
  7/27/2016 3:11:34AM Scan Summary
  7/27/2016 3:11:34AM Processes scanned : 0
  7/27/2016 3:11:34AM Processes detected : 0
  7/27/2016 3:11:34AM Processes cleaned : 0
  7/27/2016 3:11:34AM Boot sectors scanned : 2
  7/27/2016 3:11:34AM Boot sectors detected: 0
  7/27/2016 3:11:34AM Boot sectors cleaned : 0
  7/27/2016 3:11:34AM Files scanned : 55
  7/27/2016 3:11:34AM Files with detections: 0
  7/27/2016 3:11:34AM File detections : 0
  7/27/2016 3:11:34AM Files cleaned : 0
  7/27/2016 3:11:34AM Files deleted : 0
  7/27/2016 3:11:34AM Files not scanned : 0
  7/27/2016 3:11:34AM Scan Summary (Registry Scanning)
  7/27/2016 3:11:34AM Keys scanned : 0
  7/27/2016 3:11:34AM Keys detected : 0
  7/27/2016 3:11:34AM Keys cleaned : 0
  7/27/2016 3:11:34AM Keys deleted : 0
  7/27/2016 3:11:34AM Run time : 0:00:10
  7/27/2016 3:11:34AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22067:HEAD Source
------------------------------------------------------------------------  r22168 | edk2buildsystem | 2016-07-27 02:05:50 -0700 (Wed, 27 Jul 2016) | 12 lines
  BaseTools: report error if source module INF is only list in FDF file
  If source module INF is not listed in DSC, it will not be built. And it
  is listed in FDF, GenFds will fail to find its build output. To reminder
  user this issue early, build tool should report failure to user in early
  phase.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 2502b73557ae2a9014b4367e85740e209d14c06e)

------------------------------------------------------------------------