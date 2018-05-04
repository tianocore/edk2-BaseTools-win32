Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 27029

This directory contains the Win32 binaries.

Build Date:       Thu, 03 May 2018 17:01:36 Pacific Daylight Time
Last Changed Rev: 27019

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.14 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 27029
  BootSectImage Version 1.0 Build Build 26482
  Brotli Version 0.5.2 Build 26482
  Brotli Version 0.5.2 Build 26482
  DevicePath Version 0.1 Build 26482
 *Ecc.exe Version 1.0 Build Build 27029
  EfiLdrImage Version 1.0 Build Build 26482
  EfiRom Version 0.1 Build 26482
  GenBootSector Version 0.2 Build 26482
  GenCrc32 Version 0.2 Build 26482
 *GenDepex.exe Version 0.04 Build 27029
 *GenFds.exe 1.0 Build 27029
  GenFfs Version 0.1 Build 26482
  GenFv Version 0.1 Build 26482
  GenFw Version 0.2 Build 26482
  GenPage Version 0.2 Build 26482
 *GenPatchPcdTable.exe Version 0.10 Build 27029
  GenSec Version 0.1 Build 26914
  GenVtf Version 0.1 Build 26914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26482
  LzmaF86Compress Version 0.2 Build 26482
 *PatchPcdValue.exe Version 0.10 Build 27029
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26914
  Split Version 1.0 Build Build 26482
 *TargetTool.exe Version 0.01 Build 27029
  TianoCompress Version 0.1 Build 26482
 *Trim.exe Version 0.10 Build 27029
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26914
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 27029
  VolInfo Version 1.0 Build Build 26482
 *build.exe Version 0.60 Build 27029

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/3/2018 5:01:38PM Engine version = 5900.7806
  5/3/2018 5:01:38PM AntiVirus DAT version = 8882.0
  5/3/2018 5:01:38PM Number of detection signatures in EXTRA.DAT = None
  5/3/2018 5:01:38PM Names of detection signatures in EXTRA.DAT = None
  5/3/2018 5:01:38PM Scan Started On-Demand Scan
  5/3/2018 5:01:49PM Scan Summary
  5/3/2018 5:01:49PM Processes scanned : 0
  5/3/2018 5:01:49PM Processes detected : 0
  5/3/2018 5:01:49PM Processes cleaned : 0
  5/3/2018 5:01:49PM Boot sectors scanned : 2
  5/3/2018 5:01:49PM Boot sectors detected: 0
  5/3/2018 5:01:49PM Boot sectors cleaned : 0
  5/3/2018 5:01:49PM Files scanned : 67
  5/3/2018 5:01:49PM Files with detections: 0
  5/3/2018 5:01:49PM File detections : 0
  5/3/2018 5:01:49PM Files cleaned : 0
  5/3/2018 5:01:49PM Files deleted : 0
  5/3/2018 5:01:49PM Files not scanned : 0
  5/3/2018 5:01:49PM Scan Summary (Registry Scanning)
  5/3/2018 5:01:49PM Keys scanned : 0
  5/3/2018 5:01:49PM Keys detected : 0
  5/3/2018 5:01:49PM Keys cleaned : 0
  5/3/2018 5:01:49PM Keys deleted : 0
  5/3/2018 5:01:49PM Run time : 0:00:12
  5/3/2018 5:01:49PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 27019:HEAD Source
------------------------------------------------------------------------  r27019 | edk2buildsystem | 2018-05-02 02:21:54 -0700 (Wed, 02 May 2018) | 8 lines
  BaseTools: remove unused MigrationUtilities.py
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a079c5550d84b2e151185f4d4c4d6afaef1dcb64)

------------------------------------------------------------------------