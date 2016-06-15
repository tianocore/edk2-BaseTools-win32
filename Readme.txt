Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 21077

This directory contains the Win32 binaries.

Build Date:       Wed, 15 Jun 2016 03:11:19 Pacific Daylight Time
Last Changed Rev: 21074

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 21077
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
 *GenDepex.exe Version 0.04 Build 21077
 *GenFds.exe 1.0 Build 21077
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 20909
  GenFw Version 0.2 Build 20909
  GenPage Version 0.2 Build 20909
 *GenPatchPcdTable.exe Version 0.10 Build 21077
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
 *PatchPcdValue.exe Version 0.10 Build 21077
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
 *TargetTool.exe Version 0.01 Build 21077
  TianoCompress Version 0.1 Build 20909
 *Trim.exe Version 0.10 Build 21077
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20909
  VolInfo Version 1.0 Build Build 20909
 *build.exe Version 0.60 Build 21077

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  6/15/2016 3:11:20AM Engine version = 5700.7163
  6/15/2016 3:11:20AM AntiVirus DAT version = 8196.0
  6/15/2016 3:11:20AM Number of detection signatures in EXTRA.DAT = 3
  6/15/2016 3:11:20AM Names of detection signatures in EXTRA.DAT = W97M/Downloader.ber (ED) W97M/Downloader.bes (ED) W97M/Downloader.bet (ED)
  6/15/2016 3:11:20AM Scan Started On-Demand Scan
  6/15/2016 3:11:22AM Scan Summary
  6/15/2016 3:11:22AM Processes scanned : 0
  6/15/2016 3:11:22AM Processes detected : 0
  6/15/2016 3:11:22AM Processes cleaned : 0
  6/15/2016 3:11:22AM Boot sectors scanned : 1
  6/15/2016 3:11:22AM Boot sectors detected: 0
  6/15/2016 3:11:22AM Boot sectors cleaned : 0
  6/15/2016 3:11:22AM Files scanned : 55
  6/15/2016 3:11:22AM Files with detections: 0
  6/15/2016 3:11:22AM File detections : 0
  6/15/2016 3:11:22AM Files cleaned : 0
  6/15/2016 3:11:22AM Files deleted : 0
  6/15/2016 3:11:22AM Files not scanned : 0
  6/15/2016 3:11:22AM Scan Summary (Registry Scanning)
  6/15/2016 3:11:22AM Keys scanned : 0
  6/15/2016 3:11:22AM Keys detected : 0
  6/15/2016 3:11:22AM Keys cleaned : 0
  6/15/2016 3:11:22AM Keys deleted : 0
  6/15/2016 3:11:22AM Run time : 0:00:02
  6/15/2016 3:11:22AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 21035:HEAD Source
------------------------------------------------------------------------  r21035 | edk2buildsystem | 2016-06-04 14:05:32 -0700 (Sat, 04 Jun 2016) | 10 lines
  BaseTools: fix the bug to build a compressed ROM image via .INF file
  Fix the bug that always use the '-e' as OPTROM_FLAGS even the .INF file
  has statement 'PCI_COMPRESS  = TRUE'.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9ccb26bc99465e16c00fa5cf5e5f43b12dc73f46)

------------------------------------------------------------------------  r21074 | edk2buildsystem | 2016-06-15 02:05:30 -0700 (Wed, 15 Jun 2016) | 10 lines
  BaseTools: ignore the binary LIB file in gen_libs
  For single module build, it would call gen_libs target. then if it use
  binary LIB file, it cause build failure.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 8832c79d6439adc09d7cc89b22268899026ff7f8)

------------------------------------------------------------------------