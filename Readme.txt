Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25300

This directory contains the Win32 binaries.

Build Date:       Mon, 11 Sep 2017 03:12:00 Pacific Daylight Time
Last Changed Rev: 25300

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25300
  BootSectImage Version 1.0 Build Build 25090
  Brotli Version 0.5.2 Build 25090
  Brotli Version 0.5.2 Build 25090
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25090
  EfiRom Version 0.1 Build 25171
  GenBootSector Version 0.2 Build 25090
  GenCrc32 Version 0.2 Build 25090
 *GenDepex.exe Version 0.04 Build 25300
 *GenFds.exe 1.0 Build 25300
  GenFfs Version 0.1 Build 25090
  GenFv Version 0.1 Build 25090
  GenFw Version 0.2 Build 25145
  GenPage Version 0.2 Build 25090
 *GenPatchPcdTable.exe Version 0.10 Build 25300
  GenSec Version 0.1 Build 25090
  GenVtf Version 0.1 Build 25090
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25090
  LzmaF86Compress Version 0.2 Build 25090
 *PatchPcdValue.exe Version 0.10 Build 25300
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25090
 *TargetTool.exe Version 0.01 Build 25300
  TianoCompress Version 0.1 Build 25090
 *Trim.exe Version 0.10 Build 25300
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25090
  VolInfo Version 1.0 Build Build 25090
 *build.exe Version 0.60 Build 25300

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  9/11/2017 3:12:02AM Engine version = 5900.7806
  9/11/2017 3:12:02AM AntiVirus DAT version = 8650.0
  9/11/2017 3:12:02AM Number of detection signatures in EXTRA.DAT = None
  9/11/2017 3:12:02AM Names of detection signatures in EXTRA.DAT = None
  9/11/2017 3:12:02AM Scan Started On-Demand Scan
  9/11/2017 3:12:24AM Scan Summary
  9/11/2017 3:12:24AM Processes scanned : 0
  9/11/2017 3:12:24AM Processes detected : 0
  9/11/2017 3:12:24AM Processes cleaned : 0
  9/11/2017 3:12:24AM Boot sectors scanned : 2
  9/11/2017 3:12:24AM Boot sectors detected: 0
  9/11/2017 3:12:24AM Boot sectors cleaned : 0
  9/11/2017 3:12:24AM Files scanned : 64
  9/11/2017 3:12:24AM Files with detections: 0
  9/11/2017 3:12:24AM File detections : 0
  9/11/2017 3:12:24AM Files cleaned : 0
  9/11/2017 3:12:24AM Files deleted : 0
  9/11/2017 3:12:24AM Files not scanned : 0
  9/11/2017 3:12:24AM Scan Summary (Registry Scanning)
  9/11/2017 3:12:24AM Keys scanned : 0
  9/11/2017 3:12:24AM Keys detected : 0
  9/11/2017 3:12:24AM Keys cleaned : 0
  9/11/2017 3:12:24AM Keys deleted : 0
  9/11/2017 3:12:24AM Run time : 0:00:23
  9/11/2017 3:12:24AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25298:HEAD Source
------------------------------------------------------------------------  r25298 | edk2buildsystem | 2017-09-09 02:05:36 -0700 (Sat, 09 Sep 2017) | 11 lines
  BaseTools: Not show *B when Pcd value in build option same with DEC
  Per build spec, If the value obtained from either a build option, the
  DSC or FDF is the same as the value in the DEC, then *B , *P or *F
  will not be shown in the report.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 0e6be43fd3e9a6de4c036935787c1d037ff76888)

------------------------------------------------------------------------  r25300 | edk2buildsystem | 2017-09-11 02:05:30 -0700 (Mon, 11 Sep 2017) | 10 lines
  BaseTools: Fix a bug for Mixed Pcd value display in the report
  the case is that override the mixed pcd value in DSC [Components]
  section, the value display in the report is incorrect.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit aa9aa47e06ac0082948b880c226c8bdf2a12102b)

------------------------------------------------------------------------