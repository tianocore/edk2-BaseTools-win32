Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26263

This directory contains the Win32 binaries.

Build Date:       Fri, 02 Feb 2018 03:13:19 Pacific Standard Time
Last Changed Rev: 26262

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26258
 *BootSectImage Version 1.0 Build Build 26263
 *Brotli Version 0.5.2 Build 26263
  Brotli Version 0.5.2 Build 26263
 *DevicePath Version 0.1 Build 26263
  Ecc.exe Version 1.0 Build Build 26237
 *EfiLdrImage Version 1.0 Build Build 26263
 *EfiRom Version 0.1 Build 26263
 *GenBootSector Version 0.2 Build 26263
 *GenCrc32 Version 0.2 Build 26263
  GenDepex.exe Version 0.04 Build 26258
  GenFds.exe 1.0 Build 26258
 *GenFfs Version 0.1 Build 26263
 *GenFv Version 0.1 Build 26263
 *GenFw Version 0.2 Build 26263
 *GenPage Version 0.2 Build 26263
  GenPatchPcdTable.exe Version 0.10 Build 26258
 *GenSec Version 0.1 Build 26263
 *GenVtf Version 0.1 Build 26263
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 26263
  LzmaF86Compress Version 0.2 Build 26263
  PatchPcdValue.exe Version 0.10 Build 26258
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
 *Split Version 1.0 Build Build 26263
  TargetTool.exe Version 0.01 Build 26258
 *TianoCompress Version 0.1 Build 26263
  Trim.exe Version 0.10 Build 26258
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 26263
 *VolInfo Version 1.0 Build Build 26263
  build.exe Version 0.60 Build 26258

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/2/2018 3:13:20AM Engine version = 5900.7806
  2/2/2018 3:13:20AM AntiVirus DAT version = 8792.0
  2/2/2018 3:13:20AM Number of detection signatures in EXTRA.DAT = None
  2/2/2018 3:13:20AM Names of detection signatures in EXTRA.DAT = None
  2/2/2018 3:13:20AM Scan Started On-Demand Scan
  2/2/2018 3:13:34AM Scan Summary
  2/2/2018 3:13:34AM Processes scanned : 0
  2/2/2018 3:13:34AM Processes detected : 0
  2/2/2018 3:13:34AM Processes cleaned : 0
  2/2/2018 3:13:34AM Boot sectors scanned : 2
  2/2/2018 3:13:34AM Boot sectors detected: 0
  2/2/2018 3:13:34AM Boot sectors cleaned : 0
  2/2/2018 3:13:34AM Files scanned : 83
  2/2/2018 3:13:34AM Files with detections: 0
  2/2/2018 3:13:34AM File detections : 0
  2/2/2018 3:13:34AM Files cleaned : 0
  2/2/2018 3:13:34AM Files deleted : 0
  2/2/2018 3:13:34AM Files not scanned : 0
  2/2/2018 3:13:34AM Scan Summary (Registry Scanning)
  2/2/2018 3:13:34AM Keys scanned : 0
  2/2/2018 3:13:34AM Keys detected : 0
  2/2/2018 3:13:34AM Keys cleaned : 0
  2/2/2018 3:13:34AM Keys deleted : 0
  2/2/2018 3:13:34AM Run time : 0:00:14
  2/2/2018 3:13:34AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26258:HEAD Source
------------------------------------------------------------------------  r26262 | edk2buildsystem | 2018-02-02 02:05:49 -0800 (Fri, 02 Feb 2018) | 16 lines
  BaseTools: Fix make PcdValueCommon.c failure on GCC
  error message:
  PcdValueCommon.c: In function '__PcdGetPtr':
  PcdValueCommon.c:315:11: error: variable 'Byte'
  set but not used [-Werror=unused-but-set-variable]
  UINT8   Byte;
  ^
  cc1: all warnings being treated as errors
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 693877f8e593e51f38e67108c4db98e56f68e8d8)

------------------------------------------------------------------------