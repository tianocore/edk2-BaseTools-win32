Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22658

This directory contains the Win32 binaries.

Build Date:       Tue, 20 Sep 2016 03:25:13 Pacific Daylight Time
Last Changed Rev: 22657

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22658
  BootSectImage Version 1.0 Build Build 22449
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 22449
  EfiRom Version 0.1 Build 22617
  GenBootSector Version 0.2 Build 22449
  GenCrc32 Version 0.2 Build 22449
 *GenDepex.exe Version 0.04 Build 22658
 *GenFds.exe 1.0 Build 22658
  GenFfs Version 0.1 Build 22449
  GenFv Version 0.1 Build 22543
  GenFw Version 0.2 Build 22466
  GenPage Version 0.2 Build 22449
 *GenPatchPcdTable.exe Version 0.10 Build 22658
  GenSec Version 0.1 Build 22449
  GenVtf Version 0.1 Build 22449
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 22449
  LzmaF86Compress Version 0.2 Build 22449
 *PatchPcdValue.exe Version 0.10 Build 22658
  Pkcs7Sign Version 0.9 Build 22543
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 22444
  Split Version 1.0 Build Build 22449
 *TargetTool.exe Version 0.01 Build 22658
  TianoCompress Version 0.1 Build 22449
 *Trim.exe Version 0.10 Build 22658
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22316
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22449
  VolInfo Version 1.0 Build Build 22449
 *build.exe Version 0.60 Build 22658

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  9/20/2016 3:25:14AM Engine version = 5700.7163
  9/20/2016 3:25:14AM AntiVirus DAT version = 8293.0
  9/20/2016 3:25:14AM Number of detection signatures in EXTRA.DAT = 2
  9/20/2016 3:25:14AM Names of detection signatures in EXTRA.DAT = Generic.Tra!3c09cefe0e8d (ED) Generic.Tra!5876ae4f5bf5 (ED)
  9/20/2016 3:25:14AM Scan Started On-Demand Scan
  9/20/2016 3:25:17AM Scan Summary
  9/20/2016 3:25:17AM Processes scanned : 0
  9/20/2016 3:25:17AM Processes detected : 0
  9/20/2016 3:25:17AM Processes cleaned : 0
  9/20/2016 3:25:17AM Boot sectors scanned : 1
  9/20/2016 3:25:17AM Boot sectors detected: 0
  9/20/2016 3:25:17AM Boot sectors cleaned : 0
  9/20/2016 3:25:17AM Files scanned : 62
  9/20/2016 3:25:17AM Files with detections: 0
  9/20/2016 3:25:17AM File detections : 0
  9/20/2016 3:25:17AM Files cleaned : 0
  9/20/2016 3:25:17AM Files deleted : 0
  9/20/2016 3:25:17AM Files not scanned : 0
  9/20/2016 3:25:17AM Scan Summary (Registry Scanning)
  9/20/2016 3:25:17AM Keys scanned : 0
  9/20/2016 3:25:17AM Keys detected : 0
  9/20/2016 3:25:17AM Keys cleaned : 0
  9/20/2016 3:25:17AM Keys deleted : 0
  9/20/2016 3:25:17AM Run time : 0:00:03
  9/20/2016 3:25:17AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22650:HEAD Source
------------------------------------------------------------------------  r22650 | edk2buildsystem | 2016-09-15 02:05:42 -0700 (Thu, 15 Sep 2016) | 11 lines
  BaseTools: Fix the bug to handle the read-only file
  change the 'r+b' to 'rb' for some file's open, since these files we only
  read it and no need to write. It can fix the bug that the file's attribute
  had been set to read-only.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f8db6527da8678f1480f08ba99b745279e8d104a)

------------------------------------------------------------------------  r22657 | edk2buildsystem | 2016-09-20 02:05:41 -0700 (Tue, 20 Sep 2016) | 26 lines
  BaseTools: Follow PI1.4a to fix artificial limitation of PCD SkuId range
  Current BaseTools follow previous PI spec to use UINT8 for SkuId, to
  follow PI1.4a, BaseTools need to be updated to fix artificial limitation
  of PCD SkuId range.
  This patch is to update BaseTools to use UINT64 for SkuId, since the
  PCD database structure needs to be naturally aligned, the PCD database
  structure layout is adjusted to keep the natural alignment and version
  is updated to 6.
  Note: As the PCD database structure layout is adjusted, the structure
  definition in MdeModulePkg/Include/Guid/PcdDataBaseSignatureGuid.h and
  PCD drivers also need to be updated. That means the source code and
  BaseTools need to be upgraded at the same time, and if they are not
  upgraded at the same time, build error like below will be triggered
  to help user identify the problem.
  "Please make sure the version of PCD PEIM Service and the generated
  PCD PEI Database match."
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a01f68bd9bd95d6cda2ddbe469d9e82e42726208)

------------------------------------------------------------------------