Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26139

This directory contains the Win32 binaries.

Build Date:       Mon, 15 Jan 2018 03:13:18 Pacific Standard Time
Last Changed Rev: 26133

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26116
 *BootSectImage Version 1.0 Build Build 26139
 *Brotli Version 0.5.2 Build 26139
  Brotli Version 0.5.2 Build 26139
 *DevicePath Version 0.1 Build 26139
  Ecc.exe Version 1.0 Build Build 24602
 *EfiLdrImage Version 1.0 Build Build 26139
 *EfiRom Version 0.1 Build 26139
 *GenBootSector Version 0.2 Build 26139
 *GenCrc32 Version 0.2 Build 26139
  GenDepex.exe Version 0.04 Build 26116
  GenFds.exe 1.0 Build 26116
 *GenFfs Version 0.1 Build 26139
 *GenFv Version 0.1 Build 26139
 *GenFw Version 0.2 Build 26139
 *GenPage Version 0.2 Build 26139
  GenPatchPcdTable.exe Version 0.10 Build 26116
 *GenSec Version 0.1 Build 26139
 *GenVtf Version 0.1 Build 26139
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 26139
  LzmaF86Compress Version 0.2 Build 26139
  PatchPcdValue.exe Version 0.10 Build 26116
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
 *Split Version 1.0 Build Build 26139
  TargetTool.exe Version 0.01 Build 26116
 *TianoCompress Version 0.1 Build 26139
  Trim.exe Version 0.10 Build 26116
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 26139
 *VolInfo Version 1.0 Build Build 26139
  build.exe Version 0.60 Build 26116

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/15/2018 3:13:19AM Engine version = 5900.7806
  1/15/2018 3:13:19AM AntiVirus DAT version = 8774.0
  1/15/2018 3:13:19AM Number of detection signatures in EXTRA.DAT = None
  1/15/2018 3:13:19AM Names of detection signatures in EXTRA.DAT = None
  1/15/2018 3:13:19AM Scan Started On-Demand Scan
  1/15/2018 3:13:33AM Scan Summary
  1/15/2018 3:13:33AM Processes scanned : 0
  1/15/2018 3:13:33AM Processes detected : 0
  1/15/2018 3:13:33AM Processes cleaned : 0
  1/15/2018 3:13:33AM Boot sectors scanned : 2
  1/15/2018 3:13:33AM Boot sectors detected: 0
  1/15/2018 3:13:33AM Boot sectors cleaned : 0
  1/15/2018 3:13:33AM Files scanned : 82
  1/15/2018 3:13:33AM Files with detections: 0
  1/15/2018 3:13:33AM File detections : 0
  1/15/2018 3:13:33AM Files cleaned : 0
  1/15/2018 3:13:33AM Files deleted : 0
  1/15/2018 3:13:33AM Files not scanned : 0
  1/15/2018 3:13:33AM Scan Summary (Registry Scanning)
  1/15/2018 3:13:33AM Keys scanned : 0
  1/15/2018 3:13:33AM Keys detected : 0
  1/15/2018 3:13:33AM Keys cleaned : 0
  1/15/2018 3:13:33AM Keys deleted : 0
  1/15/2018 3:13:33AM Run time : 0:00:14
  1/15/2018 3:13:33AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26116:HEAD Source
------------------------------------------------------------------------  r26129 | edk2buildsystem | 2018-01-15 02:05:53 -0800 (Mon, 15 Jan 2018) | 10 lines
  BaseTools/C/Common: Fix code to be more readable
  The change doesn't impact the functionality.
  Cc: Ruiyu Ni <ruiyu.ni@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 3710ec21d59cd1764a4075af419e70332d7f0a3c)

------------------------------------------------------------------------  r26130 | edk2buildsystem | 2018-01-15 02:05:58 -0800 (Mon, 15 Jan 2018) | 7 lines
  BaseTools/C/Common: Fix potential memory leak
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1f7e7e70d2aafbea9f56053280fbb2a7b17da8ed)

------------------------------------------------------------------------  r26131 | edk2buildsystem | 2018-01-15 02:06:04 -0800 (Mon, 15 Jan 2018) | 7 lines
  BaseTools/DevicePath: Fix potential memory leak
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 46cced287e3a01c19929c4a92bbb713c9c999842)

------------------------------------------------------------------------  r26132 | edk2buildsystem | 2018-01-15 02:06:09 -0800 (Mon, 15 Jan 2018) | 7 lines
  BaseTools/C/Common: Fix potential null pointer dereference
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 66329d53bde5febe55cb1e8d3352ff94d3773277)

------------------------------------------------------------------------  r26133 | edk2buildsystem | 2018-01-15 02:06:14 -0800 (Mon, 15 Jan 2018) | 7 lines
  BaseTools/DevicePath: Fix potential null pointer dereference
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e73fbac5d7f7c4ecb803991839c054a682f991d4)

------------------------------------------------------------------------