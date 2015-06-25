Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17712

This directory contains the Win32 binaries.

Build Date:       Thu, 25 Jun 2015 03:16:23 Pacific Daylight Time
Last Changed Rev: 17711

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17712
  BootSectImage Version 0.1 Build 17702
 *Ecc.exe Version 0.01 Build 17712
  EfiLdrImage Version 0.1 Build 17702
  EfiRom Version 0.1 Build 17702
  GenBootSector Version 0.2 Build 17702
  GenCrc32 Version 0.2 Build 17702
 *GenDepex.exe Version 0.04 Build 17712
 *GenFds.exe 1.0 Build 17712
  GenFfs Version 0.1 Build 17702
  GenFv Version 0.1 Build 17702
  GenFw Version 0.2 Build 17702
  GenPage Version 0.2 Build 17702
 *GenPatchPcdTable.exe Version 0.10 Build 17712
  GenSec Version 0.1 Build 17702
  GenVtf Version 0.1 Build 17702
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 17702
  LzmaF86Compress Version 0.2 Build 17702
 *PatchPcdValue.exe Version 0.10 Build 17712
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17553
  Split Version 0.1 Build 17702
 *TargetTool.exe Version 0.01 Build 17712
  TianoCompress Version 0.1 Build 17702
 *Trim.exe Version 0.10 Build 17712
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17674
  VfrCompile version  2.00 (UEFI 2.4) Build 17702
  VolInfo Version 0.83 Build 17702, Jun 24 2015
 *build.exe Version 0.60 Build 17712

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1263
  6/25/2015 3:16:24AM Engine version = 5700.7163
  6/25/2015 3:16:24AM AntiVirus DAT version = 7842.0
  6/25/2015 3:16:24AM Number of detection signatures in EXTRA.DAT = None
  6/25/2015 3:16:24AM Names of detection signatures in EXTRA.DAT = None
  6/25/2015 3:16:25AM Scan Started On-Demand Scan
  6/25/2015 3:16:30AM Scan Summary
  6/25/2015 3:16:30AM Processes scanned : 0
  6/25/2015 3:16:30AM Processes detected : 0
  6/25/2015 3:16:30AM Processes cleaned : 0
  6/25/2015 3:16:30AM Boot sectors scanned : 1
  6/25/2015 3:16:30AM Boot sectors detected: 0
  6/25/2015 3:16:30AM Boot sectors cleaned : 0
  6/25/2015 3:16:30AM Files scanned : 55
  6/25/2015 3:16:30AM Files with detections: 0
  6/25/2015 3:16:30AM File detections : 0
  6/25/2015 3:16:30AM Files cleaned : 0
  6/25/2015 3:16:30AM Files deleted : 0
  6/25/2015 3:16:30AM Files not scanned : 0
  6/25/2015 3:16:30AM Scan Summary (Registry Scanning)
  6/25/2015 3:16:30AM Keys scanned : 0
  6/25/2015 3:16:30AM Keys detected : 0
  6/25/2015 3:16:30AM Keys cleaned : 0
  6/25/2015 3:16:30AM Keys deleted : 0
  6/25/2015 3:16:30AM Run time : 0:00:06
  6/25/2015 3:16:30AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17702:HEAD Source
------------------------------------------------------------------------  r17705 | hchen30 | 2015-06-25 00:43:03 -0700 (Thu, 25 Jun 2015) | 7 lines
  BaseTools/Ecc: Add a Configuration item
  Add a ‘SkipFileList’ in config.ini to exclude the files not be scanned.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: YangX Li <yangx.li@intel.com>

------------------------------------------------------------------------  r17706 | hchen30 | 2015-06-25 00:50:55 -0700 (Thu, 25 Jun 2015) | 7 lines
  BaseTools/Ecc: Add a checkpoint for invalid UNI file.
  Add a checkpoint to check that the UNI file which is associated by INF or DEC file need define the prompt and help information.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: YangX Li <yangx.li@intel.com>

------------------------------------------------------------------------  r17707 | hchen30 | 2015-06-25 00:59:16 -0700 (Thu, 25 Jun 2015) | 7 lines
  BaseTools/Ecc: Add a checkpoint for invalid PCD info.
  Add a checkpoint to check invalid format of @ValidRange, @ValidList and @Expression for a PCD
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: YangX Li <yangx.li@intel.com>

------------------------------------------------------------------------  r17708 | hchen30 | 2015-06-25 01:01:59 -0700 (Thu, 25 Jun 2015) | 7 lines
  BaseTools/Ecc: Add a checkpoint for invalid DEC file.
  Add a checkpoint to check whether a header file in 'include' directory is defined in DEC file
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: YangX Li <yangx.li@intel.com>

------------------------------------------------------------------------  r17709 | hchen30 | 2015-06-25 01:05:42 -0700 (Thu, 25 Jun 2015) | 7 lines
  BaseTools/Ecc: Fix a bug in parser
  Fix a bug to not break when parsing a macro and not find its value
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: YangX Li <yangx.li@intel.com>

------------------------------------------------------------------------  r17710 | hchen30 | 2015-06-25 01:08:55 -0700 (Thu, 25 Jun 2015) | 8 lines
  BaseTools/Ecc: Fix two bugs for the checkpoint of GUID
  a) Fix a bug of displaying wrong format of a GUID
  b) Fix a bug of setting wrong exception keyword
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: YangX Li <yangx.li@intel.com>

------------------------------------------------------------------------  r17711 | hchen30 | 2015-06-25 01:10:51 -0700 (Thu, 25 Jun 2015) | 7 lines
  BaseTools/Ecc: Fix a bug of determining boolean variable incorrectly
  Fix a bug of determining boolean variable incorrectly in C parser
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: YangX Li <yangx.li@intel.com>

------------------------------------------------------------------------