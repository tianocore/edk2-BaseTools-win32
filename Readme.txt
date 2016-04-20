Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20615

This directory contains the Win32 binaries.

Build Date:       Wed, 20 Apr 2016 03:11:28 Pacific Daylight Time
Last Changed Rev: 20615

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20615
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20615
 *GenFds.exe 1.0 Build 20615
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 20600
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20615
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20615
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20615
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20615
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20528
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20600
 *build.exe Version 0.60 Build 20615

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/20/2016 3:11:29AM Engine version = 5700.7163
  4/20/2016 3:11:29AM AntiVirus DAT version = 8140.0
  4/20/2016 3:11:29AM Number of detection signatures in EXTRA.DAT = None
  4/20/2016 3:11:29AM Names of detection signatures in EXTRA.DAT = None
  4/20/2016 3:11:29AM Scan Started On-Demand Scan
  4/20/2016 3:11:31AM Scan Summary
  4/20/2016 3:11:31AM Processes scanned : 0
  4/20/2016 3:11:31AM Processes detected : 0
  4/20/2016 3:11:31AM Processes cleaned : 0
  4/20/2016 3:11:31AM Boot sectors scanned : 1
  4/20/2016 3:11:31AM Boot sectors detected: 0
  4/20/2016 3:11:31AM Boot sectors cleaned : 0
  4/20/2016 3:11:31AM Files scanned : 55
  4/20/2016 3:11:31AM Files with detections: 0
  4/20/2016 3:11:31AM File detections : 0
  4/20/2016 3:11:31AM Files cleaned : 0
  4/20/2016 3:11:31AM Files deleted : 0
  4/20/2016 3:11:31AM Files not scanned : 0
  4/20/2016 3:11:31AM Scan Summary (Registry Scanning)
  4/20/2016 3:11:31AM Keys scanned : 0
  4/20/2016 3:11:31AM Keys detected : 0
  4/20/2016 3:11:31AM Keys cleaned : 0
  4/20/2016 3:11:31AM Keys deleted : 0
  4/20/2016 3:11:31AM Run time : 0:00:02
  4/20/2016 3:11:31AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20605:HEAD Source
------------------------------------------------------------------------  r20610 | edk2buildsystem | 2016-04-19 14:05:52 -0700 (Tue, 19 Apr 2016) | 10 lines
  BaseTools: enhance error handling for DSC file
  Add logic for DSC file validation for Prebuild init. Add logic to detect
  error for DSC parser when '{' is missing.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d429fcd0d25936ff5861e9c6e37f7cf9285217b2)

------------------------------------------------------------------------  r20611 | edk2buildsystem | 2016-04-19 14:05:57 -0700 (Tue, 19 Apr 2016) | 15 lines
  BaseTools/GenFds: remove the old logic since ActivePlatform is abs. path
  We can support the DSC file out of workspace. this old logic first make
  the absolute path to relative path and strips the leading slash off,
  then append it to workspace. it cause GenFds failure on Linux when the
  DSC file is out of workspace. Since we make sure the ActivePlatform is
  abs. path, so we don't need this old logic to change the abs. path to
  relative.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Marvin Haeuser <marvin.haeuser@outlook.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e642ceb8a586571b506a1ae4c00674b291f8395d)

------------------------------------------------------------------------  r20612 | edk2buildsystem | 2016-04-19 14:06:01 -0700 (Tue, 19 Apr 2016) | 10 lines
  BaseTools: fix a bug for PEI VPD Pcd collection
  When a PEI phase VPD PCD only list in the DSC IA32 arch, then build X64
  arch image, it missed to collect this PEI VPD pcd into VPD Pcd map file.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 61ee1dff160dabbb0855d56c925985030af702bc)

------------------------------------------------------------------------  r20614 | edk2buildsystem | 2016-04-20 02:05:29 -0700 (Wed, 20 Apr 2016) | 33 lines
  BaseTools: Add mixed PCD support feature
  Problem statement:
  The current build system requires that a PCD must use the same access
  method for all modules. A Binary Module may use a different PCD access
  method than: 1.A source tree build it is integrated into. 2.Other Binary
  Modules in platform build that use the same PCD.
  Solution:
  1. Source build:
  No change. PCDs must use the same access method for building all Source
  Modules.
  2. Mixed Source & Binary Builds or Binary Only Builds:
  1) Source Modules - No changes
  2) Module that is interpreted as a Binary Module
  a.DSC file may optionally override default value of PatchableInModule
  PCDs in scope of Binary Module.
  b.DSC file must declare DynamicEx PCD subtype for all DynamicEx PCDs
  from Binary Modules.
  c.FDF file must list Binary Module INF
  Build update:
  1. PCDs in a binary module are permitted to use the PatchableInModule
  or DynamicEx access methods (the Binary INF clearly identifies the PCD
  access method for each PCD). The build must support binary modules that
  use the same or different PCD access method than the Source INFs or
  other Binary INFs.
  2. Build report list PCDs that have mixed PCD access methods.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 2a29017e3e305a10ee1003354c0d0c037923341d)

------------------------------------------------------------------------  r20615 | edk2buildsystem | 2016-04-20 02:05:36 -0700 (Wed, 20 Apr 2016) | 10 lines
  BaseTools: add the support for --pcd feature to patch the binary efi
  the original --pcd feature can override the Pcd value when build the
  source driver, while it missed the binary driver. this patch add the
  support to patch the binary efi for --pcd feature.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 6b17c11b6f45b4196adb8a9fcbdba5576a0d872b)

------------------------------------------------------------------------