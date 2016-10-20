Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22845

This directory contains the Win32 binaries.

Build Date:       Thu, 20 Oct 2016 03:11:49 Pacific Daylight Time
Last Changed Rev: 22843

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22837
 *BootSectImage Version 1.0 Build Build 22845
  Ecc.exe Version 1.0 Build Build 22700
 *EfiLdrImage Version 1.0 Build Build 22845
 *EfiRom Version 0.1 Build 22845
 *GenBootSector Version 0.2 Build 22845
 *GenCrc32 Version 0.2 Build 22845
  GenDepex.exe Version 0.04 Build 22837
  GenFds.exe 1.0 Build 22837
 *GenFfs Version 0.1 Build 22845
 *GenFv Version 0.1 Build 22845
 *GenFw Version 0.2 Build 22845
 *GenPage Version 0.2 Build 22845
  GenPatchPcdTable.exe Version 0.10 Build 22837
 *GenSec Version 0.1 Build 22845
 *GenVtf Version 0.1 Build 22845
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 22845
  LzmaF86Compress Version 0.2 Build 22845
  PatchPcdValue.exe Version 0.10 Build 22837
  Pkcs7Sign Version 0.9 Build 22810
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 22815
 *Split Version 1.0 Build Build 22845
  TargetTool.exe Version 0.01 Build 22837
 *TianoCompress Version 0.1 Build 22845
  Trim.exe Version 0.10 Build 22837
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22316
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 22845
 *VolInfo Version 1.0 Build Build 22845
  build.exe Version 0.60 Build 22837

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/20/2016 3:11:50AM Engine version = 5700.7163
  10/20/2016 3:11:50AM AntiVirus DAT version = 8323.0
  10/20/2016 3:11:50AM Number of detection signatures in EXTRA.DAT = None
  10/20/2016 3:11:50AM Names of detection signatures in EXTRA.DAT = None
  10/20/2016 3:11:50AM Scan Started On-Demand Scan
  10/20/2016 3:11:53AM Scan Summary
  10/20/2016 3:11:53AM Processes scanned : 0
  10/20/2016 3:11:53AM Processes detected : 0
  10/20/2016 3:11:53AM Processes cleaned : 0
  10/20/2016 3:11:53AM Boot sectors scanned : 1
  10/20/2016 3:11:53AM Boot sectors detected: 0
  10/20/2016 3:11:53AM Boot sectors cleaned : 0
  10/20/2016 3:11:53AM Files scanned : 77
  10/20/2016 3:11:53AM Files with detections: 0
  10/20/2016 3:11:53AM File detections : 0
  10/20/2016 3:11:53AM Files cleaned : 0
  10/20/2016 3:11:53AM Files deleted : 0
  10/20/2016 3:11:53AM Files not scanned : 0
  10/20/2016 3:11:53AM Scan Summary (Registry Scanning)
  10/20/2016 3:11:53AM Keys scanned : 0
  10/20/2016 3:11:53AM Keys detected : 0
  10/20/2016 3:11:53AM Keys cleaned : 0
  10/20/2016 3:11:53AM Keys deleted : 0
  10/20/2016 3:11:53AM Run time : 0:00:03
  10/20/2016 3:11:53AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22837:HEAD Source
------------------------------------------------------------------------  r22843 | edk2buildsystem | 2016-10-20 02:05:44 -0700 (Thu, 20 Oct 2016) | 16 lines
  BaseTools: Fix typos in comments and variables
  - Pacakge -> Package
  - outputed -> outputted
  - successull -> successfully
  - Libary -> Library
  - Pointion -> Position
  - paramter -> parameter
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 99e55970ff0778ad46177a9c0fafb0766d4e6837)

------------------------------------------------------------------------