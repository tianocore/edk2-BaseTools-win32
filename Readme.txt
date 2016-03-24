Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20357

This directory contains the Win32 binaries.

Build Date:       Thu, 24 Mar 2016 03:32:34 Pacific Daylight Time
Last Changed Rev: 20332

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20357
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20331
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20357
 *GenFds.exe 1.0 Build 20357
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20357
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20357
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20331
  Rsa2048Sha256Sign Version 0.9 Build 20331
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20357
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20357
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20331
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20182
 *build.exe Version 0.60 Build 20357

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/24/2016 3:32:35AM Engine version = 5700.7163
  3/24/2016 3:32:35AM AntiVirus DAT version = 8113.0
  3/24/2016 3:32:35AM Number of detection signatures in EXTRA.DAT = None
  3/24/2016 3:32:35AM Names of detection signatures in EXTRA.DAT = None
  3/24/2016 3:32:35AM Scan Started On-Demand Scan
  3/24/2016 3:32:46AM Scan Summary
  3/24/2016 3:32:46AM Processes scanned : 0
  3/24/2016 3:32:46AM Processes detected : 0
  3/24/2016 3:32:46AM Processes cleaned : 0
  3/24/2016 3:32:46AM Boot sectors scanned : 2
  3/24/2016 3:32:46AM Boot sectors detected: 0
  3/24/2016 3:32:46AM Boot sectors cleaned : 0
  3/24/2016 3:32:46AM Files scanned : 55
  3/24/2016 3:32:46AM Files with detections: 0
  3/24/2016 3:32:46AM File detections : 0
  3/24/2016 3:32:46AM Files cleaned : 0
  3/24/2016 3:32:46AM Files deleted : 0
  3/24/2016 3:32:46AM Files not scanned : 0
  3/24/2016 3:32:46AM Scan Summary (Registry Scanning)
  3/24/2016 3:32:46AM Keys scanned : 0
  3/24/2016 3:32:46AM Keys detected : 0
  3/24/2016 3:32:46AM Keys cleaned : 0
  3/24/2016 3:32:46AM Keys deleted : 0
  3/24/2016 3:32:46AM Run time : 0:00:12
  3/24/2016 3:32:46AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20331:HEAD Source
------------------------------------------------------------------------  r20332 | edk2buildsystem | 2016-03-23 10:21:44 -0700 (Wed, 23 Mar 2016) | 14 lines
  BaseTools: not include the undefined macro in response file
  In last Nmake patch, when we generate the response file, we would replace
  all the Macros in the make file. Once there have undefined macro used,
  the tool direct report error. In this patch, we use following solution to
  resolve the failure.
  1. Add all the defined macros into AutoGenObject macro dict
  2. For the undefined macros which used in the Make file, when we generate
  the response file, we not include this macro, let make phase to handle.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 3570e3324835ba08fa68a1d0bf59290750ff797d)

------------------------------------------------------------------------