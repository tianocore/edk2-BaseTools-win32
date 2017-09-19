Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25366

This directory contains the Win32 binaries.

Build Date:       Tue, 19 Sep 2017 03:12:27 Pacific Daylight Time
Last Changed Rev: 25366

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25366
  BootSectImage Version 1.0 Build Build 25090
  Brotli Version 0.5.2 Build 25090
  Brotli Version 0.5.2 Build 25090
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25090
  EfiRom Version 0.1 Build 25171
  GenBootSector Version 0.2 Build 25090
  GenCrc32 Version 0.2 Build 25090
 *GenDepex.exe Version 0.04 Build 25366
 *GenFds.exe 1.0 Build 25366
  GenFfs Version 0.1 Build 25090
  GenFv Version 0.1 Build 25090
  GenFw Version 0.2 Build 25145
  GenPage Version 0.2 Build 25090
 *GenPatchPcdTable.exe Version 0.10 Build 25366
  GenSec Version 0.1 Build 25090
  GenVtf Version 0.1 Build 25090
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25090
  LzmaF86Compress Version 0.2 Build 25090
 *PatchPcdValue.exe Version 0.10 Build 25366
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25090
 *TargetTool.exe Version 0.01 Build 25366
  TianoCompress Version 0.1 Build 25090
 *Trim.exe Version 0.10 Build 25366
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25090
  VolInfo Version 1.0 Build Build 25090
 *build.exe Version 0.60 Build 25366

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  9/19/2017 3:12:28AM Engine version = 5900.7806
  9/19/2017 3:12:28AM AntiVirus DAT version = 8658.0
  9/19/2017 3:12:28AM Number of detection signatures in EXTRA.DAT = None
  9/19/2017 3:12:28AM Names of detection signatures in EXTRA.DAT = None
  9/19/2017 3:12:29AM Scan Started On-Demand Scan
  9/19/2017 3:12:52AM Scan Summary
  9/19/2017 3:12:52AM Processes scanned : 0
  9/19/2017 3:12:52AM Processes detected : 0
  9/19/2017 3:12:52AM Processes cleaned : 0
  9/19/2017 3:12:52AM Boot sectors scanned : 2
  9/19/2017 3:12:52AM Boot sectors detected: 0
  9/19/2017 3:12:52AM Boot sectors cleaned : 0
  9/19/2017 3:12:52AM Files scanned : 64
  9/19/2017 3:12:52AM Files with detections: 0
  9/19/2017 3:12:52AM File detections : 0
  9/19/2017 3:12:52AM Files cleaned : 0
  9/19/2017 3:12:52AM Files deleted : 0
  9/19/2017 3:12:52AM Files not scanned : 0
  9/19/2017 3:12:52AM Scan Summary (Registry Scanning)
  9/19/2017 3:12:52AM Keys scanned : 0
  9/19/2017 3:12:52AM Keys detected : 0
  9/19/2017 3:12:52AM Keys cleaned : 0
  9/19/2017 3:12:52AM Keys deleted : 0
  9/19/2017 3:12:52AM Run time : 0:00:24
  9/19/2017 3:12:52AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25300:HEAD Source
------------------------------------------------------------------------  r25300 | edk2buildsystem | 2017-09-11 02:05:30 -0700 (Mon, 11 Sep 2017) | 10 lines
  BaseTools: Fix a bug for Mixed Pcd value display in the report
  the case is that override the mixed pcd value in DSC [Components]
  section, the value display in the report is incorrect.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit aa9aa47e06ac0082948b880c226c8bdf2a12102b)

------------------------------------------------------------------------  r25366 | edk2buildsystem | 2017-09-19 02:06:21 -0700 (Tue, 19 Sep 2017) | 13 lines
  BaseTools: Fix a bug to correct SourceFileList
  We met a case that use two microcode files in the Microcode.inf file,
  one is .mcb file, another is .txt file. then it cause build failure
  because the SourceFileList include the .txt file's output file, while
  this output file is still not be generated, so it cause
  GetFileDependency report failure.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a3a4737051010a94832f7bceaa1fa414d7259da0)

------------------------------------------------------------------------