Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26258

This directory contains the Win32 binaries.

Build Date:       Thu, 01 Feb 2018 03:13:46 Pacific Standard Time
Last Changed Rev: 26252

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26258
 *BootSectImage Version 1.0 Build Build 26258
 *Brotli Version 0.5.2 Build 26258
  Brotli Version 0.5.2 Build 26258
 *DevicePath Version 0.1 Build 26258
  Ecc.exe Version 1.0 Build Build 26237
 *EfiLdrImage Version 1.0 Build Build 26258
 *EfiRom Version 0.1 Build 26258
 *GenBootSector Version 0.2 Build 26258
 *GenCrc32 Version 0.2 Build 26258
 *GenDepex.exe Version 0.04 Build 26258
 *GenFds.exe 1.0 Build 26258
 *GenFfs Version 0.1 Build 26258
 *GenFv Version 0.1 Build 26258
 *GenFw Version 0.2 Build 26258
 *GenPage Version 0.2 Build 26258
 *GenPatchPcdTable.exe Version 0.10 Build 26258
 *GenSec Version 0.1 Build 26258
 *GenVtf Version 0.1 Build 26258
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 26258
  LzmaF86Compress Version 0.2 Build 26258
 *PatchPcdValue.exe Version 0.10 Build 26258
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
 *Split Version 1.0 Build Build 26258
 *TargetTool.exe Version 0.01 Build 26258
 *TianoCompress Version 0.1 Build 26258
 *Trim.exe Version 0.10 Build 26258
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 26258
 *VolInfo Version 1.0 Build Build 26258
 *build.exe Version 0.60 Build 26258

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/1/2018 3:13:48AM Engine version = 5900.7806
  2/1/2018 3:13:48AM AntiVirus DAT version = 8791.0
  2/1/2018 3:13:48AM Number of detection signatures in EXTRA.DAT = None
  2/1/2018 3:13:48AM Names of detection signatures in EXTRA.DAT = None
  2/1/2018 3:13:48AM Scan Started On-Demand Scan
  2/1/2018 3:14:01AM Scan Summary
  2/1/2018 3:14:01AM Processes scanned : 0
  2/1/2018 3:14:01AM Processes detected : 0
  2/1/2018 3:14:01AM Processes cleaned : 0
  2/1/2018 3:14:01AM Boot sectors scanned : 2
  2/1/2018 3:14:01AM Boot sectors detected: 0
  2/1/2018 3:14:01AM Boot sectors cleaned : 0
  2/1/2018 3:14:01AM Files scanned : 84
  2/1/2018 3:14:01AM Files with detections: 0
  2/1/2018 3:14:01AM File detections : 0
  2/1/2018 3:14:01AM Files cleaned : 0
  2/1/2018 3:14:01AM Files deleted : 0
  2/1/2018 3:14:01AM Files not scanned : 0
  2/1/2018 3:14:01AM Scan Summary (Registry Scanning)
  2/1/2018 3:14:01AM Keys scanned : 0
  2/1/2018 3:14:01AM Keys detected : 0
  2/1/2018 3:14:01AM Keys cleaned : 0
  2/1/2018 3:14:01AM Keys deleted : 0
  2/1/2018 3:14:01AM Run time : 0:00:14
  2/1/2018 3:14:01AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26242:HEAD Source
------------------------------------------------------------------------  r26242 | edk2buildsystem | 2018-01-31 02:05:46 -0800 (Wed, 31 Jan 2018) | 9 lines
  BaseTools: Update BPDG to support L'' and '' format as VPD Pcd Value
  Current Pcd value support flexible format, this patch add support for
  BPDG Tool to support L'' and '' format.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d5988a8ac9716130a323fb12bbf81c41807c7865)

------------------------------------------------------------------------  r26246 | edk2buildsystem | 2018-02-01 02:05:39 -0800 (Thu, 01 Feb 2018) | 9 lines
  BaseTool: Add comments in PcdValueInit.c.
  Add Comments for __FLEXIBLE_SIZE () statement.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 75771aebd39ec7c6d383e98085b54c9419d2546e)

------------------------------------------------------------------------  r26247 | edk2buildsystem | 2018-02-01 02:05:46 -0800 (Thu, 01 Feb 2018) | 7 lines
  BaseTool: Enhance error handling.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5db9414cc1b9b449c70a974f0aa0d17b41d09629)

------------------------------------------------------------------------  r26248 | edk2buildsystem | 2018-02-01 02:05:52 -0800 (Thu, 01 Feb 2018) | 9 lines
  BaseTools: Support multiple .h file
  for structure Pcd declaration in DEC file.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 81add864f4af238a2dfb702904a6abec12738b9d)

------------------------------------------------------------------------  r26249 | edk2buildsystem | 2018-02-01 02:06:00 -0800 (Thu, 01 Feb 2018) | 7 lines
  BaseTools: Structure Pcd in CommandLine.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 6f49996cedfb198beb374ea0cb89a06a71ef960c)

------------------------------------------------------------------------  r26252 | edk2buildsystem | 2018-02-01 02:06:16 -0800 (Thu, 01 Feb 2018) | 6 lines
  BaseTools CommonLib: Remove the unnecessary print message in PcdValueCommon
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 83ba30c5a3e4b285bc2be99308cbe5fcfb1d0e16)

------------------------------------------------------------------------