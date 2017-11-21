Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25694

This directory contains the Win32 binaries.

Build Date:       Tue, 21 Nov 2017 03:11:52 Pacific Standard Time
Last Changed Rev: 25691

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25689
  BootSectImage Version 1.0 Build Build 25453
  Brotli Version 0.5.2 Build 25453
  Brotli Version 0.5.2 Build 25453
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25453
  EfiRom Version 0.1 Build 25453
  GenBootSector Version 0.2 Build 25453
  GenCrc32 Version 0.2 Build 25453
  GenDepex.exe Version 0.04 Build 25689
 *GenFds.exe 1.0 Build 25694
  GenFfs Version 0.1 Build 25453
  GenFv Version 0.1 Build 25453
  GenFw Version 0.2 Build 25453
  GenPage Version 0.2 Build 25453
  GenPatchPcdTable.exe Version 0.10 Build 25689
  GenSec Version 0.1 Build 25453
  GenVtf Version 0.1 Build 25453
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25453
  LzmaF86Compress Version 0.2 Build 25453
  PatchPcdValue.exe Version 0.10 Build 25689
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25453
  TargetTool.exe Version 0.01 Build 25689
  TianoCompress Version 0.1 Build 25453
  Trim.exe Version 0.10 Build 25689
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25614
  VolInfo Version 1.0 Build Build 25453
 *build.exe Version 0.60 Build 25694

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/21/2017 3:11:53AM Engine version = 5900.7806
  11/21/2017 3:11:53AM AntiVirus DAT version = 8721.0
  11/21/2017 3:11:53AM Number of detection signatures in EXTRA.DAT = None
  11/21/2017 3:11:53AM Names of detection signatures in EXTRA.DAT = None
  11/21/2017 3:11:53AM Scan Started On-Demand Scan
  11/21/2017 3:12:02AM Scan Summary
  11/21/2017 3:12:02AM Processes scanned : 0
  11/21/2017 3:12:02AM Processes detected : 0
  11/21/2017 3:12:02AM Processes cleaned : 0
  11/21/2017 3:12:02AM Boot sectors scanned : 2
  11/21/2017 3:12:02AM Boot sectors detected: 0
  11/21/2017 3:12:02AM Boot sectors cleaned : 0
  11/21/2017 3:12:02AM Files scanned : 64
  11/21/2017 3:12:02AM Files with detections: 0
  11/21/2017 3:12:02AM File detections : 0
  11/21/2017 3:12:02AM Files cleaned : 0
  11/21/2017 3:12:02AM Files deleted : 0
  11/21/2017 3:12:02AM Files not scanned : 0
  11/21/2017 3:12:02AM Scan Summary (Registry Scanning)
  11/21/2017 3:12:02AM Keys scanned : 0
  11/21/2017 3:12:02AM Keys detected : 0
  11/21/2017 3:12:02AM Keys cleaned : 0
  11/21/2017 3:12:02AM Keys deleted : 0
  11/21/2017 3:12:02AM Run time : 0:00:10
  11/21/2017 3:12:02AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25689:HEAD Source
------------------------------------------------------------------------  r25690 | edk2buildsystem | 2017-11-21 02:05:26 -0800 (Tue, 21 Nov 2017) | 12 lines
  BaseTools: Guid.xref contain information from FILE statements in FDF
  Update Guid.xref to contain information from FILE statements in FDF
  file.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=778
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Dmitry Antipov <dmanti@microsoft.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5e9256cd7f54ffd6f1fd9837df92a911fcd2d7c2)

------------------------------------------------------------------------  r25691 | edk2buildsystem | 2017-11-21 02:05:32 -0800 (Tue, 21 Nov 2017) | 11 lines
  BaseTools: Fix a bug for single module build with GenC/GenMake option
  when build a single module with GenC/GenMake option, currently it will
  direct return after create Autogen code files, then it cause MaList is
  empty, which cause an incorrect error message is reported.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b8c6c545385da1fec9f0851e2d4f1b769ff121af)

------------------------------------------------------------------------