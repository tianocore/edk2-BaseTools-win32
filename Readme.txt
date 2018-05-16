Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 27191

This directory contains the Win32 binaries.

Build Date:       Wed, 16 May 2018 11:26:18 Pacific Daylight Time
Last Changed Rev: 27191

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.14 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################

** ALL TOOLS WERE REBUILT **
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 27191
  BootSectImage Version 1.0 Build Build 27191
  Brotli Version 0.5.2 Build 27191
  Brotli Version 0.5.2 Build 27191
  DevicePath Version 0.1 Build 27191
  Ecc.exe Version 1.0 Build Build 27191
  EfiLdrImage Version 1.0 Build Build 27191
  EfiRom Version 0.1 Build 27191
  GenBootSector Version 0.2 Build 27191
  GenCrc32 Version 0.2 Build 27191
  GenDepex.exe Version 0.04 Build 27191
  GenFds.exe 1.0 Build 27191
  GenFfs Version 0.1 Build 27191
  GenFv Version 0.1 Build 27191
  GenFw Version 0.2 Build 27191
  GenPage Version 0.2 Build 27191
  GenPatchPcdTable.exe Version 0.10 Build 27191
  GenSec Version 0.1 Build 27191
  GenVtf Version 0.1 Build 27191
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 27191
  LzmaF86Compress Version 0.2 Build 27191
  PatchPcdValue.exe Version 0.10 Build 27191
  Pkcs7Sign Version 0.9 Build 27191
  Rsa2048Sha256GenerateKeys Version 0.9 Build 27191
  Rsa2048Sha256Sign Version 0.9 Build 27191
  Split Version 1.0 Build Build 27191
  TargetTool.exe Version 0.01 Build 27191
  TianoCompress Version 0.1 Build 27191
  Trim.exe Version 0.10 Build 27191
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 27191
  VfrCompile version  2.01 (UEFI 2.4) Build Build 27191
  VolInfo Version 1.0 Build Build 27191
  build.exe Version 0.60 Build 27191

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/16/2018 11:26:20AM Engine version = 5900.7806
  5/16/2018 11:26:20AM AntiVirus DAT version = 8894.0
  5/16/2018 11:26:20AM Number of detection signatures in EXTRA.DAT = None
  5/16/2018 11:26:20AM Names of detection signatures in EXTRA.DAT = None
  5/16/2018 11:26:20AM Scan Started On-Demand Scan
  5/16/2018 11:26:31AM Scan Summary
  5/16/2018 11:26:31AM Processes scanned : 0
  5/16/2018 11:26:31AM Processes detected : 0
  5/16/2018 11:26:31AM Processes cleaned : 0
  5/16/2018 11:26:31AM Boot sectors scanned : 2
  5/16/2018 11:26:31AM Boot sectors detected: 0
  5/16/2018 11:26:31AM Boot sectors cleaned : 0
  5/16/2018 11:26:31AM Files scanned : 79
  5/16/2018 11:26:31AM Files with detections: 0
  5/16/2018 11:26:31AM File detections : 0
  5/16/2018 11:26:31AM Files cleaned : 0
  5/16/2018 11:26:31AM Files deleted : 0
  5/16/2018 11:26:31AM Files not scanned : 0
  5/16/2018 11:26:31AM Scan Summary (Registry Scanning)
  5/16/2018 11:26:31AM Keys scanned : 0
  5/16/2018 11:26:31AM Keys detected : 0
  5/16/2018 11:26:31AM Keys cleaned : 0
  5/16/2018 11:26:31AM Keys deleted : 0
  5/16/2018 11:26:31AM Run time : 0:00:12
  5/16/2018 11:26:31AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 27082:HEAD Source
------------------------------------------------------------------------  r27086 | edk2buildsystem | 2018-05-09 17:31:08 -0700 (Wed, 09 May 2018) | 22 lines
  BaseTools/VfrCompile: Avoid using uninitialized pointer
  V2:
  Add function _INIT_OPHDR_COND () for variable initialization.
  Make code logic more clean.
  Previously _CLEAR_SAVED_OPHDR () is used for variable
  initialization, and we updated it to clean memory.
  But _CLEAR_SAVED_OPHDR () is still called for variable
  initialization. This will cause uninitialized pointer
  will be checked to free and cause unexpected issue.
  This patch is to add new function for variable initialization
  and keep _CLEAR_SAVED_OPHDR () to clean memory which is
  aligned with its function name.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Gary Lin <glin@suse.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Eric Dong <eric.dong@intel.com>
  (cherry picked from commit 13e3f8c03339ebc8cd25c454fca1abde098fe7ed)

------------------------------------------------------------------------  r27087 | edk2buildsystem | 2018-05-10 02:05:49 -0700 (Thu, 10 May 2018) | 10 lines
  BaseTools: incorrect calculation for 16M
  the "0x" was missing.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1dc287c3a3f1f090ef6b8ff80f7b3b3725071471)

------------------------------------------------------------------------  r27088 | edk2buildsystem | 2018-05-10 02:06:33 -0700 (Thu, 10 May 2018) | 22 lines
  BaseTools: Fix generating array's size is incorrect in AutoGen.c
  case example:
  DSC:
  [PcdsFixedAtBuild]
  PcdToken.PcdName | "A"
  [Components]
  TestPkg/TestDriver.inf {
  PcdToken.PcdName | {0x41,0x42,0x43,0x44}
  }
  Generating the size of array is incorrect in AutoGen.c
  GLOBAL_REMOVE_IF_UNREFERENCED const UINT8
  _gPcd_FixedAtBuild_PcdName[2] = {0x41,0x42,0x43,0x44};
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=950
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 6b285ca3663d3c71cc68d01684a98f0d7537885e)

------------------------------------------------------------------------  r27089 | edk2buildsystem | 2018-05-10 02:06:54 -0700 (Thu, 10 May 2018) | 9 lines
  BaseTools: Remove the redundant code
  the ArraySize and Array already be got in line 1093, so this code are
  redundant.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit c731b5450576a8dd0afb1d2dd013203235395a4f)

------------------------------------------------------------------------  r27185 | edk2buildsystem | 2018-05-11 02:05:30 -0700 (Fri, 11 May 2018) | 9 lines
  BaseTools: Fix python error with --genfds-multi-thread.
  When self.Alignment is None, it ran into python error since there is no
  strip() in None.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Derek Lin <derek.lin2@hpe.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit c61db18e5d11e4c25e32bfb3f999a88e3207eb5f)

------------------------------------------------------------------------  r27191 | edk2buildsystem | 2018-05-16 02:05:29 -0700 (Wed, 16 May 2018) | 10 lines
  BaseTools: Fix --hash Package and Module hash value.
  The order of List enumeration is arbitrary.
  Need to be sorted while calculating Package/Module hash, otherwise it
  generate different hash value even nothing changes.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Derek Lin <derek.lin2@hpe.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 3f34e36d04a8de4992a696f738643b5a11261469)

------------------------------------------------------------------------
"Update
