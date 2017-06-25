Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24834

This directory contains the Win32 binaries.

Build Date:       Sun, 25 Jun 2017 03:14:21 Pacific Daylight Time
Last Changed Rev: 24834

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24834
  BootSectImage Version 1.0 Build Build 23431
  Brotli Version 0.5.2 Build 24577
  Brotli Version 0.5.2 Build 24577
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 24834
 *GenFds.exe 1.0 Build 24834
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 24834
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 24834
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 24834
  TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 24834
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24507
 *build.exe Version 0.60 Build 24834

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  6/25/2017 3:14:41AM Engine version = 5700.7163
  6/25/2017 3:14:41AM AntiVirus DAT version = 8570.0
  6/25/2017 3:14:41AM Number of detection signatures in EXTRA.DAT = None
  6/25/2017 3:14:41AM Names of detection signatures in EXTRA.DAT = None
  6/25/2017 3:14:42AM Scan Started On-Demand Scan
  6/25/2017 3:15:15AM Scan Summary
  6/25/2017 3:15:15AM Processes scanned : 0
  6/25/2017 3:15:15AM Processes detected : 0
  6/25/2017 3:15:15AM Processes cleaned : 0
  6/25/2017 3:15:15AM Boot sectors scanned : 2
  6/25/2017 3:15:15AM Boot sectors detected: 0
  6/25/2017 3:15:15AM Boot sectors cleaned : 0
  6/25/2017 3:15:15AM Files scanned : 64
  6/25/2017 3:15:15AM Files with detections: 0
  6/25/2017 3:15:15AM File detections : 0
  6/25/2017 3:15:15AM Files cleaned : 0
  6/25/2017 3:15:15AM Files deleted : 0
  6/25/2017 3:15:15AM Files not scanned : 0
  6/25/2017 3:15:15AM Scan Summary (Registry Scanning)
  6/25/2017 3:15:15AM Keys scanned : 0
  6/25/2017 3:15:15AM Keys detected : 0
  6/25/2017 3:15:15AM Keys cleaned : 0
  6/25/2017 3:15:15AM Keys deleted : 0
  6/25/2017 3:15:15AM Run time : 0:00:34
  6/25/2017 3:15:15AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24776:HEAD Source
------------------------------------------------------------------------  r24828 | edk2buildsystem | 2017-06-24 14:05:29 -0700 (Sat, 24 Jun 2017) | 11 lines
  BaseTools: Copy "MODULE_UNI_FILE" file into OUTPUT directory
  Current the "MODULE_UNI_FILE" item defined in the [Defines] section will
  be copied into As Built INF file, but tool doesn't copy the real file into
  same directory with the As Built INF file.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 78bcd52abb1444c4dec7536d35f1a89dfe7e3625)

------------------------------------------------------------------------  r24829 | edk2buildsystem | 2017-06-24 14:05:35 -0700 (Sat, 24 Jun 2017) | 10 lines
  BaseTools: Copy "TianoCore" userextensions into As Built Inf
  Per build spec to update the tool to copy "TianoCore" userextensions to
  As Built INF file.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit dfa41b4a483e562f3c739acfbc2d911550f50e47)

------------------------------------------------------------------------  r24830 | edk2buildsystem | 2017-06-24 14:05:40 -0700 (Sat, 24 Jun 2017) | 16 lines
  BaseTools: Enhance DEC Defines section format check
  1. break if Dec Defines Section is missing
  2. break if Dec have more than one Defines Section
  3. break if Dec Defines Section have arch attribute
  4. break if no section head, like as:
  #[Defines]
  DEC_SPECIFICATION              = 0x00010005
  PACKAGE_NAME                   = Nt32Pkg
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 778aad47e8eed49cecb7e1bd7650d878d9ea50e3)

------------------------------------------------------------------------  r24831 | edk2buildsystem | 2017-06-24 14:05:44 -0700 (Sat, 24 Jun 2017) | 11 lines
  BaseTools: Enhance the report to not show the empty section
  Enhance the report to not show the empty section, eg: Module Library
  Sub-section, if there is nothing in this section, we will not show it
  in the report.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c2d0a1f6d22f0c743899d9d98cef41e4a46c5921)

------------------------------------------------------------------------  r24832 | edk2buildsystem | 2017-06-24 14:05:49 -0700 (Sat, 24 Jun 2017) | 10 lines
  BaseTools: Fix the bug that use '|' or '||' in DSC file's Pcd value
  Fix the bug to support use '|' or '||' in DSC file's Pcd value.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 413d51cc2bcf608844cf5362535bdd2a9a8b2b5b)

------------------------------------------------------------------------  r24833 | edk2buildsystem | 2017-06-24 14:05:54 -0700 (Sat, 24 Jun 2017) | 10 lines
  BaseTools: report error HiiString in HII format PCD must not be empty
  Add a check that HiiString field in the HII format PCD entry must not
  be an empty string.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9f14de3b8eb9520d0c88b03335d91763a8d64c0f)

------------------------------------------------------------------------  r24834 | edk2buildsystem | 2017-06-24 14:05:58 -0700 (Sat, 24 Jun 2017) | 11 lines
  BaseTools: support building the same INF more than once with -m option
  Currently DSC file [Components] Section can support building the same
  INF more than once for the same arch, this patch support build with -m
  option to generate multiple instances.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 16bad1fbaf897ecd93fb5046f4fed768ac12b6ff)

------------------------------------------------------------------------