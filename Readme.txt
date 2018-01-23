Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26199

This directory contains the Win32 binaries.

Build Date:       Tue, 23 Jan 2018 03:12:32 Pacific Standard Time
Last Changed Rev: 26198

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26199
  BootSectImage Version 1.0 Build Build 26163
  Brotli Version 0.5.2 Build 26163
  Brotli Version 0.5.2 Build 26163
  DevicePath Version 0.1 Build 26163
  Ecc.exe Version 1.0 Build Build 26163
  EfiLdrImage Version 1.0 Build Build 26163
  EfiRom Version 0.1 Build 26163
  GenBootSector Version 0.2 Build 26163
  GenCrc32 Version 0.2 Build 26163
 *GenDepex.exe Version 0.04 Build 26199
 *GenFds.exe 1.0 Build 26199
  GenFfs Version 0.1 Build 26163
  GenFv Version 0.1 Build 26163
  GenFw Version 0.2 Build 26163
  GenPage Version 0.2 Build 26163
 *GenPatchPcdTable.exe Version 0.10 Build 26199
  GenSec Version 0.1 Build 26163
  GenVtf Version 0.1 Build 26163
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26163
  LzmaF86Compress Version 0.2 Build 26163
 *PatchPcdValue.exe Version 0.10 Build 26199
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
  Split Version 1.0 Build Build 26163
 *TargetTool.exe Version 0.01 Build 26199
  TianoCompress Version 0.1 Build 26163
 *Trim.exe Version 0.10 Build 26199
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26163
  VolInfo Version 1.0 Build Build 26163
 *build.exe Version 0.60 Build 26199

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/23/2018 3:12:34AM Engine version = 5900.7806
  1/23/2018 3:12:34AM AntiVirus DAT version = 8782.0
  1/23/2018 3:12:34AM Number of detection signatures in EXTRA.DAT = None
  1/23/2018 3:12:34AM Names of detection signatures in EXTRA.DAT = None
  1/23/2018 3:12:34AM Scan Started On-Demand Scan
  1/23/2018 3:12:45AM Scan Summary
  1/23/2018 3:12:45AM Processes scanned : 0
  1/23/2018 3:12:45AM Processes detected : 0
  1/23/2018 3:12:45AM Processes cleaned : 0
  1/23/2018 3:12:45AM Boot sectors scanned : 2
  1/23/2018 3:12:45AM Boot sectors detected: 0
  1/23/2018 3:12:45AM Boot sectors cleaned : 0
  1/23/2018 3:12:45AM Files scanned : 66
  1/23/2018 3:12:45AM Files with detections: 0
  1/23/2018 3:12:45AM File detections : 0
  1/23/2018 3:12:45AM Files cleaned : 0
  1/23/2018 3:12:45AM Files deleted : 0
  1/23/2018 3:12:45AM Files not scanned : 0
  1/23/2018 3:12:45AM Scan Summary (Registry Scanning)
  1/23/2018 3:12:45AM Keys scanned : 0
  1/23/2018 3:12:45AM Keys detected : 0
  1/23/2018 3:12:45AM Keys cleaned : 0
  1/23/2018 3:12:45AM Keys deleted : 0
  1/23/2018 3:12:45AM Run time : 0:00:12
  1/23/2018 3:12:45AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26184:HEAD Source
------------------------------------------------------------------------  r26184 | edk2buildsystem | 2018-01-21 02:05:33 -0800 (Sun, 21 Jan 2018) | 12 lines
  BaseTools: Optimizing DscDefaultValue process in BuildReport
  DscDefaultValue from Dsc file has been parsed by ValueExpressionEx
  when Dsc file parse, so only DscDefaultValue from FDF file need
  ValueExpressionEx parse
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a676a24656546a7fc722868fb75cd178c003056a)

------------------------------------------------------------------------  r26195 | edk2buildsystem | 2018-01-23 02:05:57 -0800 (Tue, 23 Jan 2018) | 9 lines
  BaseTools: Add "processing meta-data" string back
  Previous build tool will display "processing meta-data ..." to let user
  know the progress. this Patch add this string back.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e74cea4c7b2ea013a4b08f22c0a4e7a4ad6e69bb)

------------------------------------------------------------------------  r26196 | edk2buildsystem | 2018-01-23 02:06:02 -0800 (Tue, 23 Jan 2018) | 9 lines
  BaseTools: Enhance binary file in [Binaries] section use relative path
  Enhance the binary file in Asbuilt inf file [Binaries] section use
  relative path.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5e2c0ecd0bff48fb960ada1d138cbc382d4c1934)

------------------------------------------------------------------------  r26197 | edk2buildsystem | 2018-01-23 02:06:07 -0800 (Tue, 23 Jan 2018) | 8 lines
  BaseTools: update SKUID value to support both integer and Hex number
  This patch updated Skuid value to support both integer and hex value.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e6b10112b3ee661595f81aec7e1948bb4e8e0153)

------------------------------------------------------------------------  r26198 | edk2buildsystem | 2018-01-23 02:06:12 -0800 (Tue, 23 Jan 2018) | 9 lines
  BaseTools: Add DefaultStore section format Check
  This patch add DefaultStore section format Check and it use same logic
  with SKUID section.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 767ddbe87416afe001d4176f5d73e74f5f10f16b)

------------------------------------------------------------------------