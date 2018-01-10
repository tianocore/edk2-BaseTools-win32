Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26116

This directory contains the Win32 binaries.

Build Date:       Wed, 10 Jan 2018 03:13:16 Pacific Standard Time
Last Changed Rev: 26113

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26116
  BootSectImage Version 1.0 Build Build 26075
  Brotli Version 0.5.2 Build 26075
  Brotli Version 0.5.2 Build 26075
  DevicePath Version 0.1 Build 26075
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 26075
  EfiRom Version 0.1 Build 26075
  GenBootSector Version 0.2 Build 26075
  GenCrc32 Version 0.2 Build 26075
 *GenDepex.exe Version 0.04 Build 26116
 *GenFds.exe 1.0 Build 26116
  GenFfs Version 0.1 Build 26075
  GenFv Version 0.1 Build 26075
  GenFw Version 0.2 Build 26075
  GenPage Version 0.2 Build 26075
 *GenPatchPcdTable.exe Version 0.10 Build 26116
  GenSec Version 0.1 Build 26075
  GenVtf Version 0.1 Build 26075
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26075
  LzmaF86Compress Version 0.2 Build 26075
 *PatchPcdValue.exe Version 0.10 Build 26116
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 26075
 *TargetTool.exe Version 0.01 Build 26116
  TianoCompress Version 0.1 Build 26075
 *Trim.exe Version 0.10 Build 26116
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26075
  VolInfo Version 1.0 Build Build 26075
 *build.exe Version 0.60 Build 26116

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/10/2018 3:13:17AM Engine version = 5900.7806
  1/10/2018 3:13:17AM AntiVirus DAT version = 8769.0
  1/10/2018 3:13:17AM Number of detection signatures in EXTRA.DAT = None
  1/10/2018 3:13:17AM Names of detection signatures in EXTRA.DAT = None
  1/10/2018 3:13:17AM Scan Started On-Demand Scan
  1/10/2018 3:13:24AM Scan Summary
  1/10/2018 3:13:24AM Processes scanned : 0
  1/10/2018 3:13:24AM Processes detected : 0
  1/10/2018 3:13:24AM Processes cleaned : 0
  1/10/2018 3:13:24AM Boot sectors scanned : 2
  1/10/2018 3:13:24AM Boot sectors detected: 0
  1/10/2018 3:13:24AM Boot sectors cleaned : 0
  1/10/2018 3:13:24AM Files scanned : 65
  1/10/2018 3:13:24AM Files with detections: 0
  1/10/2018 3:13:24AM File detections : 0
  1/10/2018 3:13:24AM Files cleaned : 0
  1/10/2018 3:13:24AM Files deleted : 0
  1/10/2018 3:13:24AM Files not scanned : 0
  1/10/2018 3:13:24AM Scan Summary (Registry Scanning)
  1/10/2018 3:13:24AM Keys scanned : 0
  1/10/2018 3:13:24AM Keys detected : 0
  1/10/2018 3:13:24AM Keys cleaned : 0
  1/10/2018 3:13:24AM Keys deleted : 0
  1/10/2018 3:13:24AM Run time : 0:00:07
  1/10/2018 3:13:24AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26098:HEAD Source
------------------------------------------------------------------------  r26098 | edk2buildsystem | 2018-01-09 02:05:58 -0800 (Tue, 09 Jan 2018) | 8 lines
  BaseTools: Add back the cc71d8 version's fix
  The version cc71d8's fix was washed out by structure pcd report patch.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 643e8e4bd40807c5b01eba8561b753df37ac1a91)

------------------------------------------------------------------------  r26113 | edk2buildsystem | 2018-01-10 02:07:00 -0800 (Wed, 10 Jan 2018) | 11 lines
  BaseTools: Correct Target Path in CodaTargetList replace Path
  Target Path in CodaTargetList is DebugDir path, correct replace
  path with DebugDir
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit c7c5a6c4f7f58cff4329fa69426cd2aef724c026)

------------------------------------------------------------------------