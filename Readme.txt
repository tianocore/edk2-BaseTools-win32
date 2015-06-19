Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17674

This directory contains the Win32 binaries.

Build Date:       Fri, 19 Jun 2015 03:16:00 Pacific Daylight Time
Last Changed Rev: 17665

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17674
  BootSectImage Version 0.1 Build 17553
  Ecc.exe Version 0.01 Build 17553
  EfiLdrImage Version 0.1 Build 17553
  EfiRom Version 0.1 Build 17553
  GenBootSector Version 0.2 Build 17553
  GenCrc32 Version 0.2 Build 17553
 *GenDepex.exe Version 0.04 Build 17674
 *GenFds.exe 1.0 Build 17674
  GenFfs Version 0.1 Build 17553
  GenFv Version 0.1 Build 17553
  GenFw Version 0.2 Build 17553
  GenPage Version 0.2 Build 17553
 *GenPatchPcdTable.exe Version 0.10 Build 17674
  GenSec Version 0.1 Build 17553
  GenVtf Version 0.1 Build 17553
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 17553
  LzmaF86Compress Version 0.2 Build 17553
 *PatchPcdValue.exe Version 0.10 Build 17674
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17553
  Split Version 0.1 Build 17553
 *TargetTool.exe Version 0.01 Build 17674
  TianoCompress Version 0.1 Build 17553
 *Trim.exe Version 0.10 Build 17674
 *UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17674
  VfrCompile version  2.00 (UEFI 2.4) Build 17553
  VolInfo Version 0.83 Build 17553, Jun  3 2015
 *build.exe Version 0.60 Build 17674

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1247
  6/19/2015 3:16:02AM Engine version = 5700.7163
  6/19/2015 3:16:02AM AntiVirus DAT version = 7836.0
  6/19/2015 3:16:02AM Number of detection signatures in EXTRA.DAT = None
  6/19/2015 3:16:02AM Names of detection signatures in EXTRA.DAT = None
  6/19/2015 3:16:02AM Scan Started On-Demand Scan
  6/19/2015 3:16:12AM Scan Summary
  6/19/2015 3:16:12AM Processes scanned : 0
  6/19/2015 3:16:12AM Processes detected : 0
  6/19/2015 3:16:12AM Processes cleaned : 0
  6/19/2015 3:16:12AM Boot sectors scanned : 2
  6/19/2015 3:16:12AM Boot sectors detected: 0
  6/19/2015 3:16:12AM Boot sectors cleaned : 0
  6/19/2015 3:16:12AM Files scanned : 55
  6/19/2015 3:16:12AM Files with detections: 0
  6/19/2015 3:16:12AM File detections : 0
  6/19/2015 3:16:12AM Files cleaned : 0
  6/19/2015 3:16:12AM Files deleted : 0
  6/19/2015 3:16:12AM Files not scanned : 0
  6/19/2015 3:16:12AM Scan Summary (Registry Scanning)
  6/19/2015 3:16:12AM Keys scanned : 0
  6/19/2015 3:16:12AM Keys detected : 0
  6/19/2015 3:16:12AM Keys cleaned : 0
  6/19/2015 3:16:12AM Keys deleted : 0
  6/19/2015 3:16:12AM Run time : 0:00:11
  6/19/2015 3:16:12AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17645:HEAD Source
------------------------------------------------------------------------  r17661 | hchen30 | 2015-06-18 17:02:34 -0700 (Thu, 18 Jun 2015) | 7 lines
  BaseTools/Upt: Update error message
  Update error message of installation failure to avoid confusion.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: lhauch <larry.hauch@intel.com>

------------------------------------------------------------------------  r17662 | hchen30 | 2015-06-18 17:05:25 -0700 (Thu, 18 Jun 2015) | 7 lines
  BaseTools/Upt: Update help message
  Update help message of UPT to remove Intel(R) from the string.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: lhauch <larry.hauch@intel.com>

------------------------------------------------------------------------  r17665 | yingke | 2015-06-18 18:43:45 -0700 (Thu, 18 Jun 2015) | 7 lines
  BaseTools: Fixed Build Option override bugs.
  if '==' is specified, it overrides all options that specified by '='; if no '==' is specified, all options that match current build criteria are combined.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------