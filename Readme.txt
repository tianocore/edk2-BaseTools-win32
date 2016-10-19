Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22837

This directory contains the Win32 binaries.

Build Date:       Wed, 19 Oct 2016 03:11:30 Pacific Daylight Time
Last Changed Rev: 22820

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22837
  BootSectImage Version 1.0 Build Build 22449
  Ecc.exe Version 1.0 Build Build 22700
  EfiLdrImage Version 1.0 Build Build 22752
  EfiRom Version 0.1 Build 22617
  GenBootSector Version 0.2 Build 22449
  GenCrc32 Version 0.2 Build 22449
 *GenDepex.exe Version 0.04 Build 22837
 *GenFds.exe 1.0 Build 22837
  GenFfs Version 0.1 Build 22449
  GenFv Version 0.1 Build 22543
  GenFw Version 0.2 Build 22466
  GenPage Version 0.2 Build 22449
 *GenPatchPcdTable.exe Version 0.10 Build 22837
  GenSec Version 0.1 Build 22449
  GenVtf Version 0.1 Build 22752
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 22449
  LzmaF86Compress Version 0.2 Build 22449
 *PatchPcdValue.exe Version 0.10 Build 22837
  Pkcs7Sign Version 0.9 Build 22810
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 22815
  Split Version 1.0 Build Build 22449
 *TargetTool.exe Version 0.01 Build 22837
  TianoCompress Version 0.1 Build 22449
 *Trim.exe Version 0.10 Build 22837
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22316
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22449
  VolInfo Version 1.0 Build Build 22449
 *build.exe Version 0.60 Build 22837

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/19/2016 3:11:32AM Engine version = 5700.7163
  10/19/2016 3:11:32AM AntiVirus DAT version = 8322.0
  10/19/2016 3:11:32AM Number of detection signatures in EXTRA.DAT = None
  10/19/2016 3:11:32AM Names of detection signatures in EXTRA.DAT = None
  10/19/2016 3:11:32AM Scan Started On-Demand Scan
  10/19/2016 3:11:43AM Scan Summary
  10/19/2016 3:11:43AM Processes scanned : 0
  10/19/2016 3:11:43AM Processes detected : 0
  10/19/2016 3:11:43AM Processes cleaned : 0
  10/19/2016 3:11:43AM Boot sectors scanned : 2
  10/19/2016 3:11:43AM Boot sectors detected: 0
  10/19/2016 3:11:43AM Boot sectors cleaned : 0
  10/19/2016 3:11:43AM Files scanned : 62
  10/19/2016 3:11:43AM Files with detections: 0
  10/19/2016 3:11:43AM File detections : 0
  10/19/2016 3:11:43AM Files cleaned : 0
  10/19/2016 3:11:43AM Files deleted : 0
  10/19/2016 3:11:43AM Files not scanned : 0
  10/19/2016 3:11:43AM Scan Summary (Registry Scanning)
  10/19/2016 3:11:43AM Keys scanned : 0
  10/19/2016 3:11:43AM Keys detected : 0
  10/19/2016 3:11:43AM Keys cleaned : 0
  10/19/2016 3:11:43AM Keys deleted : 0
  10/19/2016 3:11:43AM Run time : 0:00:11
  10/19/2016 3:11:43AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22815:HEAD Source
------------------------------------------------------------------------  r22819 | edk2buildsystem | 2016-10-19 02:06:09 -0700 (Wed, 19 Oct 2016) | 14 lines
  BaseTools: Enhance tool to generate EFI_HII_IIBT_DUPLICATE image block
  When *.IDF file contains multiple definitions of image which point to the
  same image, current build tool generates multiple image blocks which
  contain the same image content.
  This patch enhance tool to generate EFI_HII_IIBT_DUPLICATE image blocks
  for non-first images for such case, to save the HII package size.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=145
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 6d034a2add0551dd0cef36610371585cb79f6aec)

------------------------------------------------------------------------  r22820 | edk2buildsystem | 2016-10-19 02:06:15 -0700 (Wed, 19 Oct 2016) | 9 lines
  BaseTools: support PCD value to use expression in the DEC file
  This patch add the support for Pcd value to use expression in the DEC file.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 67e11e4d5902dc77fc64876da5b71122bf128837)

------------------------------------------------------------------------