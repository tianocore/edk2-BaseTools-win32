Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17887

This directory contains the Win32 binaries.

Build Date:       Wed, 08 Jul 2015 06:44:51 Pacific Daylight Time
Last Changed Rev: 17876

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17823
  BootSectImage Version 0.1 Build 17815
  Ecc.exe Version 0.01 Build 17712
  EfiLdrImage Version 0.1 Build 17815
  EfiRom Version 0.1 Build 17815
  GenBootSector Version 0.2 Build 17815
  GenCrc32 Version 0.2 Build 17815
  GenDepex.exe Version 0.04 Build 17823
  GenFds.exe 1.0 Build 17823
  GenFfs Version 0.1 Build 17815
 *GenFv Version 0.1 Build 17887
  GenFw Version 0.2 Build 17815
  GenPage Version 0.2 Build 17815
  GenPatchPcdTable.exe Version 0.10 Build 17823
  GenSec Version 0.1 Build 17815
  GenVtf Version 0.1 Build 17815
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 17887
  LzmaF86Compress Version 0.2 Build 17887
  PatchPcdValue.exe Version 0.10 Build 17823
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 17815
  TargetTool.exe Version 0.01 Build 17823
  TianoCompress Version 0.1 Build 17815
  Trim.exe Version 0.10 Build 17823
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17674
  VfrCompile version  2.00 (UEFI 2.4) Build 17815
  VolInfo Version 0.83 Build 17815, Jul  2 2015
  build.exe Version 0.60 Build 17823

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  7/8/2015 6:44:53AM Engine version = 5700.7163
  7/8/2015 6:44:53AM AntiVirus DAT version = 7855.0
  7/8/2015 6:44:53AM Number of detection signatures in EXTRA.DAT = None
  7/8/2015 6:44:53AM Names of detection signatures in EXTRA.DAT = None
  7/8/2015 6:44:53AM Scan Started On-Demand Scan
  7/8/2015 6:45:14AM Scan Summary
  7/8/2015 6:45:14AM Processes scanned : 0
  7/8/2015 6:45:14AM Processes detected : 0
  7/8/2015 6:45:14AM Processes cleaned : 0
  7/8/2015 6:45:14AM Boot sectors scanned : 2
  7/8/2015 6:45:14AM Boot sectors detected: 0
  7/8/2015 6:45:14AM Boot sectors cleaned : 0
  7/8/2015 6:45:14AM Files scanned : 56
  7/8/2015 6:45:14AM Files with detections: 0
  7/8/2015 6:45:14AM File detections : 0
  7/8/2015 6:45:14AM Files cleaned : 0
  7/8/2015 6:45:14AM Files deleted : 0
  7/8/2015 6:45:14AM Files not scanned : 0
  7/8/2015 6:45:14AM Scan Summary (Registry Scanning)
  7/8/2015 6:45:14AM Keys scanned : 0
  7/8/2015 6:45:14AM Keys detected : 0
  7/8/2015 6:45:14AM Keys cleaned : 0
  7/8/2015 6:45:14AM Keys deleted : 0
  7/8/2015 6:45:14AM Run time : 0:00:22
  7/8/2015 6:45:14AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17823:HEAD Source
------------------------------------------------------------------------  r17866 | yingke | 2015-07-07 18:06:25 -0700 (Tue, 07 Jul 2015) | 12 lines
  BaseTools: Fix build on FreeBSD and allow use of non-gcc system compiler
  On FreeBSD, uuid.h is in /usr/include, not /usr/include/uuid.
  Fix some errors when building using clang caused by self-assignment: the
  preferred way to 'use' a variable is '(void)x;', not 'x = x;'.
  Where the system provides $(CC) etc. by default, don't override it to be gcc.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Bruce Cran <bruce@cran.org.uk>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------  r17872 | hchen30 | 2015-07-07 20:00:17 -0700 (Tue, 07 Jul 2015) | 7 lines
  BaseTools/Upt: Update UPT to ignore "!include" statement when parsing UNI file
  Update UPT to ignore "!include" statement when parsing UNI file
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: YangX Li <yangx.li@intel.com>

------------------------------------------------------------------------  r17876 | hchen30 | 2015-07-07 22:43:22 -0700 (Tue, 07 Jul 2015) | 7 lines
  BaseTools/Upt: Add a BOM check for UNI file and fix some help message error
  Add a BOM check for UNI file and fix some help message error
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: YangX Li <yangx.li@intel.com>

------------------------------------------------------------------------