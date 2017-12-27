Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26048

This directory contains the Win32 binaries.

Build Date:       Wed, 27 Dec 2017 08:20:59 Pacific Standard Time
Last Changed Rev: 26042

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26048
  BootSectImage Version 1.0 Build Build 26005
  Brotli Version 0.5.2 Build 26005
  Brotli Version 0.5.2 Build 26005
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 26005
  EfiRom Version 0.1 Build 26005
  GenBootSector Version 0.2 Build 26005
  GenCrc32 Version 0.2 Build 26005
 *GenDepex.exe Version 0.04 Build 26048
 *GenFds.exe 1.0 Build 26048
  GenFfs Version 0.1 Build 26005
  GenFv Version 0.1 Build 26005
  GenFw Version 0.2 Build 26005
  GenPage Version 0.2 Build 26005
 *GenPatchPcdTable.exe Version 0.10 Build 26048
  GenSec Version 0.1 Build 26005
  GenVtf Version 0.1 Build 26005
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26005
  LzmaF86Compress Version 0.2 Build 26005
 *PatchPcdValue.exe Version 0.10 Build 26048
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 26005
 *TargetTool.exe Version 0.01 Build 26048
  TianoCompress Version 0.1 Build 26005
 *Trim.exe Version 0.10 Build 26048
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26005
  VolInfo Version 1.0 Build Build 26005
 *build.exe Version 0.60 Build 26048

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/27/2017 8:21:00AM Engine version = 5900.7806
  12/27/2017 8:21:00AM AntiVirus DAT version = 8756.0
  12/27/2017 8:21:00AM Number of detection signatures in EXTRA.DAT = None
  12/27/2017 8:21:00AM Names of detection signatures in EXTRA.DAT = None
  12/27/2017 8:21:00AM Scan Started On-Demand Scan
  12/27/2017 8:21:09AM Scan Summary
  12/27/2017 8:21:09AM Processes scanned : 0
  12/27/2017 8:21:09AM Processes detected : 0
  12/27/2017 8:21:09AM Processes cleaned : 0
  12/27/2017 8:21:09AM Boot sectors scanned : 2
  12/27/2017 8:21:09AM Boot sectors detected: 0
  12/27/2017 8:21:09AM Boot sectors cleaned : 0
  12/27/2017 8:21:09AM Files scanned : 64
  12/27/2017 8:21:09AM Files with detections: 0
  12/27/2017 8:21:09AM File detections : 0
  12/27/2017 8:21:09AM Files cleaned : 0
  12/27/2017 8:21:09AM Files deleted : 0
  12/27/2017 8:21:09AM Files not scanned : 0
  12/27/2017 8:21:09AM Scan Summary (Registry Scanning)
  12/27/2017 8:21:09AM Keys scanned : 0
  12/27/2017 8:21:09AM Keys detected : 0
  12/27/2017 8:21:09AM Keys cleaned : 0
  12/27/2017 8:21:09AM Keys deleted : 0
  12/27/2017 8:21:09AM Run time : 0:00:09
  12/27/2017 8:21:09AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26005:HEAD Source
------------------------------------------------------------------------  r26013 | edk2buildsystem | 2017-12-26 02:06:08 -0800 (Tue, 26 Dec 2017) | 9 lines
  BaseTools: Fix building FatPkg failed issue
  Using property instead of vairable for DecPcds.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5644e5cecebeeefea90cfda093df68e0aa6e0361)

------------------------------------------------------------------------  r26022 | edk2buildsystem | 2017-12-27 02:05:54 -0800 (Wed, 27 Dec 2017) | 8 lines
  BaseTools: Update SkuId checker to make sure it be valid UINT64 value
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Bob Feng <bob.c.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit e4ff28c3ac72f946686e715bc32490b35c08ad5b)

------------------------------------------------------------------------  r26023 | edk2buildsystem | 2017-12-27 02:06:00 -0800 (Wed, 27 Dec 2017) | 9 lines
  BaseTools: Update Python Makefile to include the new added python files
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Bob Feng <bob.c.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Bob Feng <bob.c.feng@intel.com>
  (cherry picked from commit 02f6fd1d5f2e21dafc080721e7258bc2a2dc603c)

------------------------------------------------------------------------  r26026 | edk2buildsystem | 2017-12-27 02:06:19 -0800 (Wed, 27 Dec 2017) | 11 lines
  BaseTools: Update copyright year info of DSC/DEC/INF BuilData.py file
  The DecBuildData.py, DscBuildData.py and InfBuildData.py were separated
  from WorkspaceDatabase.py, so we updated to use same copyright year
  info.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a9d9ce8ecc5fa11102b38702e56b9f154a8dda9c)

------------------------------------------------------------------------  r26027 | edk2buildsystem | 2017-12-27 02:06:24 -0800 (Wed, 27 Dec 2017) | 8 lines
  BaseTools: Add Platform Override Build Options for PcdValueInit
  Add Platform's CC_FLAGS /D option for PcdValueInit generation.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 68ba919f7858830cc764b46a00da7e7fdcd1f3ec)

------------------------------------------------------------------------  r26028 | edk2buildsystem | 2017-12-27 02:06:32 -0800 (Wed, 27 Dec 2017) | 9 lines
  BaseTools: Support PCD flexible values format
  https://bugzilla.tianocore.org/show_bug.cgi?id=541
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 726c501c2c9a1ef103fab7846e2d1a34506715d8)

------------------------------------------------------------------------  r26042 | edk2buildsystem | 2017-12-27 02:07:46 -0800 (Wed, 27 Dec 2017) | 10 lines
  BaseTools: Remove 'COMMON' in PCD SkuInfoList
  'COMMON' is an alias of 'DEFAULT' for internal code,
  it should be removed before generating Pcd DataBase.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 98eb13643750a2f3cc3e5a1fc2ea89e5c1d0ae8e)

------------------------------------------------------------------------