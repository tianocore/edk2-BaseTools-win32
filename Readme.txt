Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26355

This directory contains the Win32 binaries.

Build Date:       Sun, 11 Feb 2018 03:23:44 Pacific Standard Time
Last Changed Rev: 10

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26355
  BootSectImage Version 1.0 Build Build 26263
  Brotli Version 0.5.2 Build 26263
  Brotli Version 0.5.2 Build 26263
  DevicePath Version 0.1 Build 26263
  Ecc.exe Version 1.0 Build Build 26237
  EfiLdrImage Version 1.0 Build Build 26263
  EfiRom Version 0.1 Build 26263
  GenBootSector Version 0.2 Build 26263
  GenCrc32 Version 0.2 Build 26263
 *GenDepex.exe Version 0.04 Build 26355
 *GenFds.exe 1.0 Build 26355
  GenFfs Version 0.1 Build 26263
  GenFv Version 0.1 Build 26263
  GenFw Version 0.2 Build 26263
  GenPage Version 0.2 Build 26263
 *GenPatchPcdTable.exe Version 0.10 Build 26355
  GenSec Version 0.1 Build 26263
  GenVtf Version 0.1 Build 26263
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26263
  LzmaF86Compress Version 0.2 Build 26263
 *PatchPcdValue.exe Version 0.10 Build 26355
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
  Split Version 1.0 Build Build 26263
 *TargetTool.exe Version 0.01 Build 26355
  TianoCompress Version 0.1 Build 26263
 *Trim.exe Version 0.10 Build 26355
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26263
  VolInfo Version 1.0 Build Build 26263
 *build.exe Version 0.60 Build 26355

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/11/2018 3:23:55AM Engine version = 5900.7806
  2/11/2018 3:23:55AM AntiVirus DAT version = 8801.0
  2/11/2018 3:23:55AM Number of detection signatures in EXTRA.DAT = None
  2/11/2018 3:23:55AM Names of detection signatures in EXTRA.DAT = None
  2/11/2018 3:23:55AM Scan Started On-Demand Scan
  2/11/2018 3:24:34AM Scan Summary
  2/11/2018 3:24:34AM Processes scanned : 0
  2/11/2018 3:24:34AM Processes detected : 0
  2/11/2018 3:24:34AM Processes cleaned : 0
  2/11/2018 3:24:34AM Boot sectors scanned : 2
  2/11/2018 3:24:34AM Boot sectors detected: 0
  2/11/2018 3:24:34AM Boot sectors cleaned : 0
  2/11/2018 3:24:34AM Files scanned : 64
  2/11/2018 3:24:34AM Files with detections: 0
  2/11/2018 3:24:34AM File detections : 0
  2/11/2018 3:24:34AM Files cleaned : 0
  2/11/2018 3:24:34AM Files deleted : 0
  2/11/2018 3:24:34AM Files not scanned : 0
  2/11/2018 3:24:34AM Scan Summary (Registry Scanning)
  2/11/2018 3:24:34AM Keys scanned : 0
  2/11/2018 3:24:34AM Keys detected : 0
  2/11/2018 3:24:34AM Keys cleaned : 0
  2/11/2018 3:24:34AM Keys deleted : 0
  2/11/2018 3:24:34AM Run time : 0:00:40
  2/11/2018 3:24:34AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26352:HEAD Source
------------------------------------------------------------------------  r26353 | edk2buildsystem | 2018-02-10 14:05:34 -0800 (Sat, 10 Feb 2018) | 11 lines
  BaseTools: Fix VOID* type bug
  Code miss UINT32 and UINT64 value type setting in
  VOID*, like as {UINT32({TRUE})}
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a35918caae4d0b9bb51d0d4765117d7ca9a4d641)

------------------------------------------------------------------------