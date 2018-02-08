Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26326

This directory contains the Win32 binaries.

Build Date:       Thu, 08 Feb 2018 03:12:31 Pacific Standard Time
Last Changed Rev: 26323

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26326
  BootSectImage Version 1.0 Build Build 26263
  Brotli Version 0.5.2 Build 26263
  Brotli Version 0.5.2 Build 26263
  DevicePath Version 0.1 Build 26263
  Ecc.exe Version 1.0 Build Build 26237
  EfiLdrImage Version 1.0 Build Build 26263
  EfiRom Version 0.1 Build 26263
  GenBootSector Version 0.2 Build 26263
  GenCrc32 Version 0.2 Build 26263
 *GenDepex.exe Version 0.04 Build 26326
 *GenFds.exe 1.0 Build 26326
  GenFfs Version 0.1 Build 26263
  GenFv Version 0.1 Build 26263
  GenFw Version 0.2 Build 26263
  GenPage Version 0.2 Build 26263
 *GenPatchPcdTable.exe Version 0.10 Build 26326
  GenSec Version 0.1 Build 26263
  GenVtf Version 0.1 Build 26263
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26263
  LzmaF86Compress Version 0.2 Build 26263
 *PatchPcdValue.exe Version 0.10 Build 26326
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
  Split Version 1.0 Build Build 26263
 *TargetTool.exe Version 0.01 Build 26326
  TianoCompress Version 0.1 Build 26263
 *Trim.exe Version 0.10 Build 26326
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26263
  VolInfo Version 1.0 Build Build 26263
 *build.exe Version 0.60 Build 26326

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/8/2018 3:12:32AM Engine version = 5900.7806
  2/8/2018 3:12:32AM AntiVirus DAT version = 8798.0
  2/8/2018 3:12:32AM Number of detection signatures in EXTRA.DAT = None
  2/8/2018 3:12:32AM Names of detection signatures in EXTRA.DAT = None
  2/8/2018 3:12:32AM Scan Started On-Demand Scan
  2/8/2018 3:12:43AM Scan Summary
  2/8/2018 3:12:43AM Processes scanned : 0
  2/8/2018 3:12:43AM Processes detected : 0
  2/8/2018 3:12:43AM Processes cleaned : 0
  2/8/2018 3:12:43AM Boot sectors scanned : 2
  2/8/2018 3:12:43AM Boot sectors detected: 0
  2/8/2018 3:12:43AM Boot sectors cleaned : 0
  2/8/2018 3:12:43AM Files scanned : 66
  2/8/2018 3:12:43AM Files with detections: 0
  2/8/2018 3:12:43AM File detections : 0
  2/8/2018 3:12:43AM Files cleaned : 0
  2/8/2018 3:12:43AM Files deleted : 0
  2/8/2018 3:12:43AM Files not scanned : 0
  2/8/2018 3:12:43AM Scan Summary (Registry Scanning)
  2/8/2018 3:12:43AM Keys scanned : 0
  2/8/2018 3:12:43AM Keys detected : 0
  2/8/2018 3:12:43AM Keys cleaned : 0
  2/8/2018 3:12:43AM Keys deleted : 0
  2/8/2018 3:12:43AM Run time : 0:00:12
  2/8/2018 3:12:43AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26279:HEAD Source
------------------------------------------------------------------------  r26293 | edk2buildsystem | 2018-02-07 14:06:10 -0800 (Wed, 07 Feb 2018) | 26 lines
  BaseTools: Fix build argument --pcd for flexible format bugs
  Build argument --pcd flexible format, like as:
  1. VOID* type
  gTokenSpaceGuid.Test=H"{flexible format}"
  gTokenSpaceGuid.Test=L"string"
  gTokenSpaceGuid.Test="string"
  gTokenSpaceGuid.Test=L'string'
  gTokenSpaceGuid.Test='string'
  2. UINT8/UINT16/UINT32/UINT64 type
  gTokenSpaceGuid.Test=H"{flexible format}"
  gTokenSpaceGuid.Test=L"string"
  gTokenSpaceGuid.Test="string"
  gTokenSpaceGuid.Test=L'string'
  gTokenSpaceGuid.Test='string'
  In linux, single quotes need escape
  gTokenSpaceGuid.Test=L\'string\'
  gTokenSpaceGuid.Test=\'string\'
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit f9bba77495750bb5f9bc5c5864b7c76fece5ec9f)

------------------------------------------------------------------------  r26294 | edk2buildsystem | 2018-02-07 14:06:15 -0800 (Wed, 07 Feb 2018) | 12 lines
  BaseTools: Fix flexible PCD DEVICE_PATH parse issue
  When the format of DEVICE_PATH have string, like as:
  {DEVICE_PATH("BBS(1,"AB",0)")} have string "AB", will
  get the wrong value.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 8ad5f10a2be2c2c8dde111c0478b02da44a781e2)

------------------------------------------------------------------------  r26295 | edk2buildsystem | 2018-02-07 14:06:20 -0800 (Wed, 07 Feb 2018) | 15 lines
  BaseTools: Report error when GUID format is incorrect
  Flexible GUID format of PCD value support following format, so tool should report
  error when it is not correct.
  1. { GUID("11E13869-1896-4A07-8B21-D8B23DD2A2B4") }
  2. { GUID({ 0x11e13869, 0x1896, 0x4a07,{
  0x8b, 0x21, 0xd8, 0xb2, 0x3d, 0xd2, 0xa2, 0xb4 } }) }
  3. { GUID(gEfiBlockIoProtocolGuid) }
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4344a788c472fccd9af559891363374868fb6275)

------------------------------------------------------------------------  r26302 | edk2buildsystem | 2018-02-07 14:07:01 -0800 (Wed, 07 Feb 2018) | 22 lines
  BaseTools: Fix COMPRESS alignment incorrect issue
  Doesn't generate the correct alignment for the leaf section
  in the compression section.
  Below FFS rule doesn't work as the expectation.
  [Rule.Common.PEIM.PE32]
  FILE PEIM = $(NAMED_GUID) {
  PEI_DEPEX PEI_DEPEX Optional $(INF_OUTPUT)/$(MODULE_NAME).depex
  COMPRESS {
  PE32   PE32  Align=Auto    $(INF_OUTPUT)/$(MODULE_NAME).efi
  UI     STRING="$(MODULE_NAME)" Optional
  VERSION  STRING="$(INF_VERSION)" Optional BUILD_NUM=$(BUILD_NUMBER)
  }
  }
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4f735fc8cdd9a7e385d285c771abddfcae8a5e58)

------------------------------------------------------------------------  r26307 | edk2buildsystem | 2018-02-08 02:05:56 -0800 (Thu, 08 Feb 2018) | 11 lines
  BaseTool: Fixed Pcd issues.
  1. Check variable offset when merging Hii Pcds
  2. Fixed the issue of Hii value inherit with default store.
  3. Error handling for incorrect structure pcd declare.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 8aa4db4b807ea7de395acd4018a139745327e374)

------------------------------------------------------------------------  r26308 | edk2buildsystem | 2018-02-08 02:06:02 -0800 (Thu, 08 Feb 2018) | 10 lines
  BaseTools: Fixed Build failed issue.
  If the PCD is not used in DSC file and user set
  that PCD value from Command line, build will fail.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e1511113debf54ec2aceb20ee8eeecb331acd498)

------------------------------------------------------------------------  r26309 | edk2buildsystem | 2018-02-08 02:06:07 -0800 (Thu, 08 Feb 2018) | 10 lines
  BaseTools: Fixed incorrect Structure Pcd Value.
  When structurePCD only has overall value assigned
  in Dsc under different SKU, the value under default sku is used.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 77204d608be05103a68b470fbbcdeccfc887911f)

------------------------------------------------------------------------  r26323 | edk2buildsystem | 2018-02-08 02:07:29 -0800 (Thu, 08 Feb 2018) | 12 lines
  BaseTools: Enhance error handling for unsupported toolchain Flags/Path
  Case1: Cover the Tool PATH is not exist, eg: build MdeModule under GCC5
  toolchain and IPF arch.
  Case2: Cover the Tool FLAGS is not exist, eg: build OvmfPkg under
  CLANG35 toolchain and X64 arch.
  fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=595
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 70d0a7549ef4a5dbdd15c0f78bd2f8ede093f8f4)

------------------------------------------------------------------------