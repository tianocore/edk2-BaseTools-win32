Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26212

This directory contains the Win32 binaries.

Build Date:       Thu, 25 Jan 2018 03:13:13 Pacific Standard Time
Last Changed Rev: 26210

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26199
 *BootSectImage Version 1.0 Build Build 26212
 *Brotli Version 0.5.2 Build 26212
  Brotli Version 0.5.2 Build 26212
 *DevicePath Version 0.1 Build 26212
  Ecc.exe Version 1.0 Build Build 26163
 *EfiLdrImage Version 1.0 Build Build 26212
 *EfiRom Version 0.1 Build 26212
 *GenBootSector Version 0.2 Build 26212
 *GenCrc32 Version 0.2 Build 26212
  GenDepex.exe Version 0.04 Build 26199
  GenFds.exe 1.0 Build 26199
 *GenFfs Version 0.1 Build 26212
 *GenFv Version 0.1 Build 26212
 *GenFw Version 0.2 Build 26212
 *GenPage Version 0.2 Build 26212
  GenPatchPcdTable.exe Version 0.10 Build 26199
 *GenSec Version 0.1 Build 26212
 *GenVtf Version 0.1 Build 26212
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 26212
  LzmaF86Compress Version 0.2 Build 26212
  PatchPcdValue.exe Version 0.10 Build 26199
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
 *Split Version 1.0 Build Build 26212
  TargetTool.exe Version 0.01 Build 26199
 *TianoCompress Version 0.1 Build 26212
  Trim.exe Version 0.10 Build 26199
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 26212
 *VolInfo Version 1.0 Build Build 26212
  build.exe Version 0.60 Build 26199

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/25/2018 3:13:14AM Engine version = 5900.7806
  1/25/2018 3:13:14AM AntiVirus DAT version = 8784.0
  1/25/2018 3:13:14AM Number of detection signatures in EXTRA.DAT = None
  1/25/2018 3:13:14AM Names of detection signatures in EXTRA.DAT = None
  1/25/2018 3:13:14AM Scan Started On-Demand Scan
  1/25/2018 3:13:25AM Scan Summary
  1/25/2018 3:13:25AM Processes scanned : 0
  1/25/2018 3:13:25AM Processes detected : 0
  1/25/2018 3:13:25AM Processes cleaned : 0
  1/25/2018 3:13:25AM Boot sectors scanned : 2
  1/25/2018 3:13:25AM Boot sectors detected: 0
  1/25/2018 3:13:25AM Boot sectors cleaned : 0
  1/25/2018 3:13:25AM Files scanned : 83
  1/25/2018 3:13:25AM Files with detections: 0
  1/25/2018 3:13:25AM File detections : 0
  1/25/2018 3:13:25AM Files cleaned : 0
  1/25/2018 3:13:25AM Files deleted : 0
  1/25/2018 3:13:25AM Files not scanned : 0
  1/25/2018 3:13:25AM Scan Summary (Registry Scanning)
  1/25/2018 3:13:25AM Keys scanned : 0
  1/25/2018 3:13:25AM Keys detected : 0
  1/25/2018 3:13:25AM Keys cleaned : 0
  1/25/2018 3:13:25AM Keys deleted : 0
  1/25/2018 3:13:25AM Run time : 0:00:11
  1/25/2018 3:13:25AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26199:HEAD Source
------------------------------------------------------------------------  r26205 | edk2buildsystem | 2018-01-24 02:06:04 -0800 (Wed, 24 Jan 2018) | 13 lines
  BaseTools: Barf on unknown HOST_ARCH in C Makefile
  I was getting `HOST_ARCH` set using the linux arch name ("x86_64"), which
  is different from the MS one ("X64").
  It is not clear anyway we can proceed without valid build variables
  (`ARCH_INCLUDE`, `BIN_PATH`, `LIB_PATH`, `SYS_BIN_PATH`, and
  `SYS_LIB_PATH`).
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Chema Gonzalez <chemag@gmail.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9d5aab05540fd7de26894b05544f1efc424ff595)

------------------------------------------------------------------------  r26210 | edk2buildsystem | 2018-01-25 02:05:43 -0800 (Thu, 25 Jan 2018) | 6 lines
  BaseTools: CommonLib Fix Crash to write the last byte
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4faf5340467a9595b1df7f4faf43f78ec59d3157)

------------------------------------------------------------------------