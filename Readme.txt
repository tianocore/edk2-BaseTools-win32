Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25689

This directory contains the Win32 binaries.

Build Date:       Mon, 20 Nov 2017 03:12:11 Pacific Standard Time
Last Changed Rev: 25687

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25689
  BootSectImage Version 1.0 Build Build 25453
  Brotli Version 0.5.2 Build 25453
  Brotli Version 0.5.2 Build 25453
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25453
  EfiRom Version 0.1 Build 25453
  GenBootSector Version 0.2 Build 25453
  GenCrc32 Version 0.2 Build 25453
 *GenDepex.exe Version 0.04 Build 25689
 *GenFds.exe 1.0 Build 25689
  GenFfs Version 0.1 Build 25453
  GenFv Version 0.1 Build 25453
  GenFw Version 0.2 Build 25453
  GenPage Version 0.2 Build 25453
 *GenPatchPcdTable.exe Version 0.10 Build 25689
  GenSec Version 0.1 Build 25453
  GenVtf Version 0.1 Build 25453
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25453
  LzmaF86Compress Version 0.2 Build 25453
 *PatchPcdValue.exe Version 0.10 Build 25689
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25453
 *TargetTool.exe Version 0.01 Build 25689
  TianoCompress Version 0.1 Build 25453
 *Trim.exe Version 0.10 Build 25689
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25614
  VolInfo Version 1.0 Build Build 25453
 *build.exe Version 0.60 Build 25689

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/20/2017 3:12:13AM Engine version = 5900.7806
  11/20/2017 3:12:13AM AntiVirus DAT version = 8720.0
  11/20/2017 3:12:13AM Number of detection signatures in EXTRA.DAT = None
  11/20/2017 3:12:13AM Names of detection signatures in EXTRA.DAT = None
  11/20/2017 3:12:13AM Scan Started On-Demand Scan
  11/20/2017 3:12:48AM Scan Summary
  11/20/2017 3:12:48AM Processes scanned : 0
  11/20/2017 3:12:48AM Processes detected : 0
  11/20/2017 3:12:48AM Processes cleaned : 0
  11/20/2017 3:12:48AM Boot sectors scanned : 2
  11/20/2017 3:12:48AM Boot sectors detected: 0
  11/20/2017 3:12:48AM Boot sectors cleaned : 0
  11/20/2017 3:12:48AM Files scanned : 64
  11/20/2017 3:12:48AM Files with detections: 0
  11/20/2017 3:12:48AM File detections : 0
  11/20/2017 3:12:48AM Files cleaned : 0
  11/20/2017 3:12:48AM Files deleted : 0
  11/20/2017 3:12:48AM Files not scanned : 0
  11/20/2017 3:12:48AM Scan Summary (Registry Scanning)
  11/20/2017 3:12:48AM Keys scanned : 0
  11/20/2017 3:12:48AM Keys detected : 0
  11/20/2017 3:12:48AM Keys cleaned : 0
  11/20/2017 3:12:48AM Keys deleted : 0
  11/20/2017 3:12:48AM Run time : 0:00:36
  11/20/2017 3:12:48AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25640:HEAD Source
------------------------------------------------------------------------  r25640 | edk2buildsystem | 2017-11-14 02:05:24 -0800 (Tue, 14 Nov 2017) | 13 lines
  BaseTools: Fix the bug to re-build uni file for Library
  The root cause is Module's self.CanSkip() is before LibraryAutoGen,
  then when a uni file of library is changed, Module's self.CanSkip() is
  still true which cause the library is not regenerated.
  This patch change Module's self.CanSkip() after LibraryAutoGen.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=759
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 36513f3a6bcc67a460f63190b27deb3565bd2de3)

------------------------------------------------------------------------  r25687 | edk2buildsystem | 2017-11-20 02:05:58 -0800 (Mon, 20 Nov 2017) | 12 lines
  BaseTools: Fix the bug to collect source files per build rule family
  when collect source files list we should also consider build rule
  family. BuildRuleFamily may be set to the different one. It will
  impact BuildRule and source files in INF file.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=780
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e259779974ea7e109ee75b9b853f73bd0f66a4b3)

------------------------------------------------------------------------