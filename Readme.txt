Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20424

This directory contains the Win32 binaries.

Build Date:       Tue, 29 Mar 2016 03:32:48 Pacific Daylight Time
Last Changed Rev: 20416

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20424
  BootSectImage Version 1.0 Build Build 20182
 *Ecc.exe Version 1.0 Build Build 20424
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20424
 *GenFds.exe 1.0 Build 20424
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20424
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20424
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20331
  Rsa2048Sha256Sign Version 0.9 Build 20331
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20424
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20424
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20331
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20182
 *build.exe Version 0.60 Build 20424

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/29/2016 3:32:49AM Engine version = 5700.7163
  3/29/2016 3:32:49AM AntiVirus DAT version = 8118.0
  3/29/2016 3:32:49AM Number of detection signatures in EXTRA.DAT = None
  3/29/2016 3:32:49AM Names of detection signatures in EXTRA.DAT = None
  3/29/2016 3:32:49AM Scan Started On-Demand Scan
  3/29/2016 3:32:55AM Scan Summary
  3/29/2016 3:32:55AM Processes scanned : 0
  3/29/2016 3:32:55AM Processes detected : 0
  3/29/2016 3:32:55AM Processes cleaned : 0
  3/29/2016 3:32:55AM Boot sectors scanned : 2
  3/29/2016 3:32:55AM Boot sectors detected: 0
  3/29/2016 3:32:55AM Boot sectors cleaned : 0
  3/29/2016 3:32:55AM Files scanned : 55
  3/29/2016 3:32:55AM Files with detections: 0
  3/29/2016 3:32:55AM File detections : 0
  3/29/2016 3:32:55AM Files cleaned : 0
  3/29/2016 3:32:55AM Files deleted : 0
  3/29/2016 3:32:55AM Files not scanned : 0
  3/29/2016 3:32:55AM Scan Summary (Registry Scanning)
  3/29/2016 3:32:55AM Keys scanned : 0
  3/29/2016 3:32:55AM Keys detected : 0
  3/29/2016 3:32:55AM Keys cleaned : 0
  3/29/2016 3:32:55AM Keys deleted : 0
  3/29/2016 3:32:55AM Run time : 0:00:06
  3/29/2016 3:32:55AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20407:HEAD Source
------------------------------------------------------------------------  r20407 | edk2buildsystem | 2016-03-28 02:26:47 -0700 (Mon, 28 Mar 2016) | 9 lines
  BaseTools: Remove the unnecessary check for RAW File
  Because the __VerifyFile function already checked whether the file is
  valid.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 4fa7b3301ef31f2787b9d0bde6694203a67b3ff2)

------------------------------------------------------------------------  r20416 | edk2buildsystem | 2016-03-29 02:27:40 -0700 (Tue, 29 Mar 2016) | 13 lines
  BaseTools: Add two new sections for PCD in the build report
  Build Spec updated to add two new sections for PCD in the build report.
  1.Conditional directives section:If the DSC or FDF file contains
  conditional directive statements.
  2.Unused PCDs section: If the DSC or FDF file define values for PCDs that
  are not used by any module and are not used in conditional directive
  statements.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c8d07c5eeb481e777ad48dc1737d1ab1be67bd44)

------------------------------------------------------------------------