Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23606

This directory contains the Win32 binaries.

Build Date:       Tue, 20 Dec 2016 03:11:15 Pacific Standard Time
Last Changed Rev: 23603

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23459
  BootSectImage Version 1.0 Build Build 23431
  Ecc.exe Version 1.0 Build Build 22854
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
  GenDepex.exe Version 0.04 Build 23459
  GenFds.exe 1.0 Build 23459
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 23431
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 23459
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 23431
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 23459
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 23431
  TargetTool.exe Version 0.01 Build 23459
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 23459
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 23606
  VolInfo Version 1.0 Build Build 23468
  build.exe Version 0.60 Build 23459

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/20/2016 3:11:17AM Engine version = 5700.7163
  12/20/2016 3:11:17AM AntiVirus DAT version = 8384.0
  12/20/2016 3:11:17AM Number of detection signatures in EXTRA.DAT = None
  12/20/2016 3:11:17AM Names of detection signatures in EXTRA.DAT = None
  12/20/2016 3:11:17AM Scan Started On-Demand Scan
  12/20/2016 3:11:27AM Scan Summary
  12/20/2016 3:11:27AM Processes scanned : 0
  12/20/2016 3:11:27AM Processes detected : 0
  12/20/2016 3:11:27AM Processes cleaned : 0
  12/20/2016 3:11:27AM Boot sectors scanned : 2
  12/20/2016 3:11:27AM Boot sectors detected: 0
  12/20/2016 3:11:27AM Boot sectors cleaned : 0
  12/20/2016 3:11:27AM Files scanned : 62
  12/20/2016 3:11:27AM Files with detections: 0
  12/20/2016 3:11:27AM File detections : 0
  12/20/2016 3:11:27AM Files cleaned : 0
  12/20/2016 3:11:27AM Files deleted : 0
  12/20/2016 3:11:27AM Files not scanned : 0
  12/20/2016 3:11:27AM Scan Summary (Registry Scanning)
  12/20/2016 3:11:27AM Keys scanned : 0
  12/20/2016 3:11:27AM Keys detected : 0
  12/20/2016 3:11:27AM Keys cleaned : 0
  12/20/2016 3:11:27AM Keys deleted : 0
  12/20/2016 3:11:27AM Run time : 0:00:11
  12/20/2016 3:11:27AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23468:HEAD Source
------------------------------------------------------------------------  r23600 | edk2buildsystem | 2016-12-20 02:06:37 -0800 (Tue, 20 Dec 2016) | 12 lines
  BaseTools: fix format-security build warnings
  Fix build warnings of "format not a string literal and no format
  arguments [-Wformat-security]" for BaseTools, while using "gcc version
  4.8.4 (Ubuntu 4.8.4-2ubuntu1~14.04.3)".
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Heyi Guo <heyi.guo@linaro.org>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5b26adf03a0b66b741ff05daee985888fe1d636f)

------------------------------------------------------------------------  r23601 | edk2buildsystem | 2016-12-20 02:06:42 -0800 (Tue, 20 Dec 2016) | 12 lines
  BaseTools: fix format type build warnings
  Fix build warnings of "format ?%d? expects argument of type ?int?, but
  argument 5 has type ?long unsigned int? [-Wformat=]" for BaseTools,
  while using "gcc version 4.8.4 (Ubuntu 4.8.4-2ubuntu1~14.04.3)".
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Heyi Guo <heyi.guo@linaro.org>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 8230d45bba517d78c20634425587efeb6fa14d7c)

------------------------------------------------------------------------  r23602 | edk2buildsystem | 2016-12-20 02:06:46 -0800 (Tue, 20 Dec 2016) | 12 lines
  BaseTools: fix write-strings build warnings
  Fix build warnings of "deprecated conversion from string constant to
  ?CHAR8* {aka char*}? [-Wwrite-strings]" for BaseTools, while using
  "gcc version 4.8.4 (Ubuntu 4.8.4-2ubuntu1~14.04.3)".
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Heyi Guo <heyi.guo@linaro.org>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 00de920a0339e78824cdb9015f66c5a98644e0b6)

------------------------------------------------------------------------  r23603 | edk2buildsystem | 2016-12-20 02:06:50 -0800 (Tue, 20 Dec 2016) | 10 lines
  BaseTools GCC makefile: disable unused-result warning for CPP file
  This warning has been disabled for C file. To be same, it is also disabled
  for CPP file.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4fa9134e47bfb3b7cd9348c8d44fdb029830018b)

------------------------------------------------------------------------