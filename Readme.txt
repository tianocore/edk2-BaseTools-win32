Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26182

This directory contains the Win32 binaries.

Build Date:       Fri, 19 Jan 2018 03:12:10 Pacific Standard Time
Last Changed Rev: 26177

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26163
  BootSectImage Version 1.0 Build Build 26163
  Brotli Version 0.5.2 Build 26163
  Brotli Version 0.5.2 Build 26163
  DevicePath Version 0.1 Build 26163
  Ecc.exe Version 1.0 Build Build 26163
  EfiLdrImage Version 1.0 Build Build 26163
  EfiRom Version 0.1 Build 26163
  GenBootSector Version 0.2 Build 26163
  GenCrc32 Version 0.2 Build 26163
  GenDepex.exe Version 0.04 Build 26163
  GenFds.exe 1.0 Build 26163
  GenFfs Version 0.1 Build 26163
  GenFv Version 0.1 Build 26163
  GenFw Version 0.2 Build 26163
  GenPage Version 0.2 Build 26163
  GenPatchPcdTable.exe Version 0.10 Build 26163
  GenSec Version 0.1 Build 26163
  GenVtf Version 0.1 Build 26163
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26163
  LzmaF86Compress Version 0.2 Build 26163
  PatchPcdValue.exe Version 0.10 Build 26163
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
  Split Version 1.0 Build Build 26163
  TargetTool.exe Version 0.01 Build 26163
  TianoCompress Version 0.1 Build 26163
  Trim.exe Version 0.10 Build 26163
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26163
  VolInfo Version 1.0 Build Build 26163
 *build.exe Version 0.60 Build 26182

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/19/2018 3:12:12AM Engine version = 5900.7806
  1/19/2018 3:12:12AM AntiVirus DAT version = 8778.0
  1/19/2018 3:12:12AM Number of detection signatures in EXTRA.DAT = None
  1/19/2018 3:12:12AM Names of detection signatures in EXTRA.DAT = None
  1/19/2018 3:12:12AM Scan Started On-Demand Scan
  1/19/2018 3:12:21AM Scan Summary
  1/19/2018 3:12:21AM Processes scanned : 0
  1/19/2018 3:12:21AM Processes detected : 0
  1/19/2018 3:12:21AM Processes cleaned : 0
  1/19/2018 3:12:21AM Boot sectors scanned : 2
  1/19/2018 3:12:21AM Boot sectors detected: 0
  1/19/2018 3:12:21AM Boot sectors cleaned : 0
  1/19/2018 3:12:21AM Files scanned : 66
  1/19/2018 3:12:21AM Files with detections: 0
  1/19/2018 3:12:21AM File detections : 0
  1/19/2018 3:12:21AM Files cleaned : 0
  1/19/2018 3:12:21AM Files deleted : 0
  1/19/2018 3:12:21AM Files not scanned : 0
  1/19/2018 3:12:21AM Scan Summary (Registry Scanning)
  1/19/2018 3:12:21AM Keys scanned : 0
  1/19/2018 3:12:21AM Keys detected : 0
  1/19/2018 3:12:21AM Keys cleaned : 0
  1/19/2018 3:12:21AM Keys deleted : 0
  1/19/2018 3:12:21AM Run time : 0:00:09
  1/19/2018 3:12:21AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26177:HEAD Source
------------------------------------------------------------------------  r26177 | edk2buildsystem | 2018-01-19 02:05:40 -0800 (Fri, 19 Jan 2018) | 9 lines
  BaseTools: enhance error handling for option --binary-source
  Enhance error handling for option --binary-source to report invalid
  option value. --binary-destination use same rule.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f21547ff64a58909c85ce215531345f6f8364884)

------------------------------------------------------------------------