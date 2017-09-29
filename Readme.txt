Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25450

This directory contains the Win32 binaries.

Build Date:       Fri, 29 Sep 2017 03:12:10 Pacific Daylight Time
Last Changed Rev: 25428

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25450
  BootSectImage Version 1.0 Build Build 25415
  Brotli Version 0.5.2 Build 25415
  Brotli Version 0.5.2 Build 25415
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25415
  EfiRom Version 0.1 Build 25415
  GenBootSector Version 0.2 Build 25415
  GenCrc32 Version 0.2 Build 25415
 *GenDepex.exe Version 0.04 Build 25450
 *GenFds.exe 1.0 Build 25450
  GenFfs Version 0.1 Build 25415
  GenFv Version 0.1 Build 25415
  GenFw Version 0.2 Build 25415
  GenPage Version 0.2 Build 25415
 *GenPatchPcdTable.exe Version 0.10 Build 25450
  GenSec Version 0.1 Build 25415
  GenVtf Version 0.1 Build 25415
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25415
  LzmaF86Compress Version 0.2 Build 25415
 *PatchPcdValue.exe Version 0.10 Build 25450
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25415
 *TargetTool.exe Version 0.01 Build 25450
  TianoCompress Version 0.1 Build 25415
 *Trim.exe Version 0.10 Build 25450
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25415
  VolInfo Version 1.0 Build Build 25415
 *build.exe Version 0.60 Build 25450

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  9/29/2017 3:12:12AM Engine version = 5900.7806
  9/29/2017 3:12:12AM AntiVirus DAT version = 8668.0
  9/29/2017 3:12:12AM Number of detection signatures in EXTRA.DAT = None
  9/29/2017 3:12:12AM Names of detection signatures in EXTRA.DAT = None
  9/29/2017 3:12:12AM Scan Started On-Demand Scan
  9/29/2017 3:12:32AM Scan Summary
  9/29/2017 3:12:32AM Processes scanned : 0
  9/29/2017 3:12:32AM Processes detected : 0
  9/29/2017 3:12:32AM Processes cleaned : 0
  9/29/2017 3:12:32AM Boot sectors scanned : 2
  9/29/2017 3:12:32AM Boot sectors detected: 0
  9/29/2017 3:12:32AM Boot sectors cleaned : 0
  9/29/2017 3:12:32AM Files scanned : 64
  9/29/2017 3:12:32AM Files with detections: 0
  9/29/2017 3:12:32AM File detections : 0
  9/29/2017 3:12:32AM Files cleaned : 0
  9/29/2017 3:12:32AM Files deleted : 0
  9/29/2017 3:12:32AM Files not scanned : 0
  9/29/2017 3:12:32AM Scan Summary (Registry Scanning)
  9/29/2017 3:12:32AM Keys scanned : 0
  9/29/2017 3:12:32AM Keys detected : 0
  9/29/2017 3:12:32AM Keys cleaned : 0
  9/29/2017 3:12:32AM Keys deleted : 0
  9/29/2017 3:12:32AM Run time : 0:00:21
  9/29/2017 3:12:32AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25417:HEAD Source
------------------------------------------------------------------------  r25417 | edk2buildsystem | 2017-09-26 02:05:31 -0700 (Tue, 26 Sep 2017) | 11 lines
  BaseTools: report build time measured by module of EDKII Build
  In the build report, we add AutoGen Phase, Make Phase and GenFds Phase
  time duration in the Platform Summary section, and we also add a item
  in Module section to display module and library's build time.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1b8eca8b1affc81357c9f685ac90e5de75ba4b87)

------------------------------------------------------------------------  r25426 | edk2buildsystem | 2017-09-28 14:05:34 -0700 (Thu, 28 Sep 2017) | 30 lines
  BaseTools: add support for BIOS build with binary cache
  Add three new options:
  --hash enables hash-based caching during build process. when --hash is
  enabled, build tool will base on the module hash value to do the
  incremental build, without --hash, build tool will base on the
  timestamp to do the incremental build. --hash option use md5 method to
  get every hash value, DSC/FDF, tools_def.txt, build_rule.txt and build
  command are calculated as global hash value, Package DEC and its
  include header files are calculated as package hash value, Module
  source files and its INF file are calculated as module hash value.
  Library hash value will combine the global hash value and its dependent
  package hash value. Driver hash value will combine the global hash
  value, its dependent package hash value and its linked library hash
  value.
  When --hash and --binary-destination are specified, build tool will
  copy generated binary files for each module into the directory specified
  by binary-destination at the build phase. Binary-destination directory
  caches all generated binary files.
  When --hash and --binary-source are specified, build tool will try to
  get the binary files from the binary source directory at the build
  phase.If the cached binary has the same hash value, it will be directly
  used. Otherwise, build tool will compile the source files and generate
  the binary files.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 36d083ef0018b78ea12db1a5f2e8df5336541fea)

------------------------------------------------------------------------  r25428 | edk2buildsystem | 2017-09-28 14:05:45 -0700 (Thu, 28 Sep 2017) | 10 lines
  BaseTools: Fix the regression bug to build single module
  The bug is introduced by 1b8eca to collect single module's build time.
  Now the fix solution is copied from Platform build.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 119d8c42ab8b80301d6dbbac2ab19f67a7b2e617)

------------------------------------------------------------------------