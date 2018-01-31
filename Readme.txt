Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26242

This directory contains the Win32 binaries.

Build Date:       Wed, 31 Jan 2018 03:12:54 Pacific Standard Time
Last Changed Rev: 26242

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26242
  BootSectImage Version 1.0 Build Build 26212
  Brotli Version 0.5.2 Build 26212
  Brotli Version 0.5.2 Build 26212
  DevicePath Version 0.1 Build 26212
  Ecc.exe Version 1.0 Build Build 26237
  EfiLdrImage Version 1.0 Build Build 26212
  EfiRom Version 0.1 Build 26212
  GenBootSector Version 0.2 Build 26212
  GenCrc32 Version 0.2 Build 26212
 *GenDepex.exe Version 0.04 Build 26242
 *GenFds.exe 1.0 Build 26242
  GenFfs Version 0.1 Build 26212
  GenFv Version 0.1 Build 26212
  GenFw Version 0.2 Build 26212
  GenPage Version 0.2 Build 26212
 *GenPatchPcdTable.exe Version 0.10 Build 26242
  GenSec Version 0.1 Build 26212
  GenVtf Version 0.1 Build 26212
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26212
  LzmaF86Compress Version 0.2 Build 26212
 *PatchPcdValue.exe Version 0.10 Build 26242
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
  Split Version 1.0 Build Build 26212
 *TargetTool.exe Version 0.01 Build 26242
  TianoCompress Version 0.1 Build 26212
 *Trim.exe Version 0.10 Build 26242
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26212
  VolInfo Version 1.0 Build Build 26212
 *build.exe Version 0.60 Build 26242

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/31/2018 3:12:55AM Engine version = 5900.7806
  1/31/2018 3:12:55AM AntiVirus DAT version = 8790.0
  1/31/2018 3:12:55AM Number of detection signatures in EXTRA.DAT = None
  1/31/2018 3:12:55AM Names of detection signatures in EXTRA.DAT = None
  1/31/2018 3:12:55AM Scan Started On-Demand Scan
  1/31/2018 3:13:09AM Scan Summary
  1/31/2018 3:13:09AM Processes scanned : 0
  1/31/2018 3:13:09AM Processes detected : 0
  1/31/2018 3:13:09AM Processes cleaned : 0
  1/31/2018 3:13:09AM Boot sectors scanned : 2
  1/31/2018 3:13:09AM Boot sectors detected: 0
  1/31/2018 3:13:09AM Boot sectors cleaned : 0
  1/31/2018 3:13:09AM Files scanned : 66
  1/31/2018 3:13:09AM Files with detections: 0
  1/31/2018 3:13:09AM File detections : 0
  1/31/2018 3:13:09AM Files cleaned : 0
  1/31/2018 3:13:09AM Files deleted : 0
  1/31/2018 3:13:09AM Files not scanned : 0
  1/31/2018 3:13:09AM Scan Summary (Registry Scanning)
  1/31/2018 3:13:09AM Keys scanned : 0
  1/31/2018 3:13:09AM Keys detected : 0
  1/31/2018 3:13:09AM Keys cleaned : 0
  1/31/2018 3:13:09AM Keys deleted : 0
  1/31/2018 3:13:09AM Run time : 0:00:14
  1/31/2018 3:13:09AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26237:HEAD Source
------------------------------------------------------------------------  r26238 | edk2buildsystem | 2018-01-30 14:05:27 -0800 (Tue, 30 Jan 2018) | 12 lines
  BaseTools: Enhance parse performance by optimize ValueExpressionEx
  Optimize ValueExpressionEx function to enhance meta-data file parse
  performance.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 35f613d96ce43c7b23cd77aab063424ec4422e0c)

------------------------------------------------------------------------  r26241 | edk2buildsystem | 2018-01-31 02:05:40 -0800 (Wed, 31 Jan 2018) | 11 lines
  BaseTools: Fix the bug to align VPD PCD based on value type
  Spec required for VOID* VPD Pcd, Ascii string use byte alignment, byte
  array use 8-byte alignment, unicode string use 2-byte alignment.
  while when the VPD pcd offset use *, the offset generated in the .map
  file not follow this rule.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 86737681af34d14dfe088d806d4a5062fdfb3f1f)

------------------------------------------------------------------------  r26242 | edk2buildsystem | 2018-01-31 02:05:46 -0800 (Wed, 31 Jan 2018) | 9 lines
  BaseTools: Update BPDG to support L'' and '' format as VPD Pcd Value
  Current Pcd value support flexible format, this patch add support for
  BPDG Tool to support L'' and '' format.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d5988a8ac9716130a323fb12bbf81c41807c7865)

------------------------------------------------------------------------