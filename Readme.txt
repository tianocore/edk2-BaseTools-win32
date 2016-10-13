Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22801

This directory contains the Win32 binaries.

Build Date:       Thu, 13 Oct 2016 03:11:07 Pacific Daylight Time
Last Changed Rev: 22799

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22700
  BootSectImage Version 1.0 Build Build 22449
  Ecc.exe Version 1.0 Build Build 22700
  EfiLdrImage Version 1.0 Build Build 22752
  EfiRom Version 0.1 Build 22617
  GenBootSector Version 0.2 Build 22449
  GenCrc32 Version 0.2 Build 22449
  GenDepex.exe Version 0.04 Build 22700
 *GenFds.exe 1.0 Build 22801
  GenFfs Version 0.1 Build 22449
  GenFv Version 0.1 Build 22543
  GenFw Version 0.2 Build 22466
  GenPage Version 0.2 Build 22449
  GenPatchPcdTable.exe Version 0.10 Build 22700
  GenSec Version 0.1 Build 22449
  GenVtf Version 0.1 Build 22752
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 22449
  LzmaF86Compress Version 0.2 Build 22449
  PatchPcdValue.exe Version 0.10 Build 22700
  Pkcs7Sign Version 0.9 Build 22543
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 22444
  Split Version 1.0 Build Build 22449
  TargetTool.exe Version 0.01 Build 22700
  TianoCompress Version 0.1 Build 22449
  Trim.exe Version 0.10 Build 22700
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22316
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22449
  VolInfo Version 1.0 Build Build 22449
  build.exe Version 0.60 Build 22731

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/13/2016 3:11:08AM Engine version = 5700.7163
  10/13/2016 3:11:08AM AntiVirus DAT version = 8316.0
  10/13/2016 3:11:08AM Number of detection signatures in EXTRA.DAT = None
  10/13/2016 3:11:08AM Names of detection signatures in EXTRA.DAT = None
  10/13/2016 3:11:08AM Scan Started On-Demand Scan
  10/13/2016 3:11:10AM Scan Summary
  10/13/2016 3:11:10AM Processes scanned : 0
  10/13/2016 3:11:10AM Processes detected : 0
  10/13/2016 3:11:10AM Processes cleaned : 0
  10/13/2016 3:11:10AM Boot sectors scanned : 1
  10/13/2016 3:11:10AM Boot sectors detected: 0
  10/13/2016 3:11:10AM Boot sectors cleaned : 0
  10/13/2016 3:11:10AM Files scanned : 62
  10/13/2016 3:11:10AM Files with detections: 0
  10/13/2016 3:11:10AM File detections : 0
  10/13/2016 3:11:10AM Files cleaned : 0
  10/13/2016 3:11:10AM Files deleted : 0
  10/13/2016 3:11:10AM Files not scanned : 0
  10/13/2016 3:11:10AM Scan Summary (Registry Scanning)
  10/13/2016 3:11:10AM Keys scanned : 0
  10/13/2016 3:11:10AM Keys detected : 0
  10/13/2016 3:11:10AM Keys cleaned : 0
  10/13/2016 3:11:10AM Keys deleted : 0
  10/13/2016 3:11:10AM Run time : 0:00:02
  10/13/2016 3:11:10AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22793:HEAD Source
------------------------------------------------------------------------  r22799 | edk2buildsystem | 2016-10-12 14:06:00 -0700 (Wed, 12 Oct 2016) | 14 lines
  BaseTools/GenFds: Support FDF sections in any order
  https://bugzilla.tianocore.org/show_bug.cgi?id=141
  This patch updates EDK II FDF parser in GenFds to allow sections
  to be placed in any order in the FDF file.
  Cc: Kelly Steele <kelly.steele@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Michael Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit dd170333f6444a4256e75356a8f0758a40bfb77d)

------------------------------------------------------------------------