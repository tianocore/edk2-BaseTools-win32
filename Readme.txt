Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26419

This directory contains the Win32 binaries.

Build Date:       Tue, 27 Feb 2018 10:58:30 Pacific Standard Time
Last Changed Rev: 26419

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.14 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26419
  BootSectImage Version 1.0 Build Build 26416
  Brotli Version 0.5.2 Build 26416
  Brotli Version 0.5.2 Build 26416
  DevicePath Version 0.1 Build 26263
  Ecc.exe Version 1.0 Build Build 26237
  EfiLdrImage Version 1.0 Build Build 26416
  EfiRom Version 0.1 Build 26416
  GenBootSector Version 0.2 Build 26263
  GenCrc32 Version 0.2 Build 26263
 *GenDepex.exe Version 0.04 Build 26419
 *GenFds.exe 1.0 Build 26419
  GenFfs Version 0.1 Build 26263
 *GenFv Version 0.1 Build 26419
  GenFw Version 0.2 Build 26263
  GenPage Version 0.2 Build 26263
 *GenPatchPcdTable.exe Version 0.10 Build 26419
  GenSec Version 0.1 Build 26263
  GenVtf Version 0.1 Build 26263
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26263
  LzmaF86Compress Version 0.2 Build 26263
 *PatchPcdValue.exe Version 0.10 Build 26419
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
  Split Version 1.0 Build Build 26263
 *TargetTool.exe Version 0.01 Build 26419
  TianoCompress Version 0.1 Build 26263
 *Trim.exe Version 0.10 Build 26419
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26263
  VolInfo Version 1.0 Build Build 26263
 *build.exe Version 0.60 Build 26419

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/27/2018 10:58:31AM Engine version = 5900.7806
  2/27/2018 10:58:31AM AntiVirus DAT version = 8816.0
  2/27/2018 10:58:31AM Number of detection signatures in EXTRA.DAT = None
  2/27/2018 10:58:31AM Names of detection signatures in EXTRA.DAT = None
  2/27/2018 10:58:31AM Scan Started On-Demand Scan
  2/27/2018 10:58:44AM Scan Summary
  2/27/2018 10:58:44AM Processes scanned : 0
  2/27/2018 10:58:44AM Processes detected : 0
  2/27/2018 10:58:44AM Processes cleaned : 0
  2/27/2018 10:58:44AM Boot sectors scanned : 2
  2/27/2018 10:58:44AM Boot sectors detected: 0
  2/27/2018 10:58:44AM Boot sectors cleaned : 0
  2/27/2018 10:58:44AM Files scanned : 67
  2/27/2018 10:58:44AM Files with detections: 0
  2/27/2018 10:58:44AM File detections : 0
  2/27/2018 10:58:44AM Files cleaned : 0
  2/27/2018 10:58:44AM Files deleted : 0
  2/27/2018 10:58:44AM Files not scanned : 0
  2/27/2018 10:58:44AM Scan Summary (Registry Scanning)
  2/27/2018 10:58:44AM Keys scanned : 0
  2/27/2018 10:58:44AM Keys detected : 0
  2/27/2018 10:58:44AM Keys cleaned : 0
  2/27/2018 10:58:44AM Keys deleted : 0
  2/27/2018 10:58:44AM Run time : 0:00:13
  2/27/2018 10:58:44AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26416:HEAD Source
------------------------------------------------------------------------  r26419 | edk2buildsystem | 2018-02-27 02:05:45 -0800 (Tue, 27 Feb 2018) | 9 lines
  BaseTools:Override the MAKE_FLAGS by BuildOptions in DSC
  The issue that *_*_*_MAKE_FLAGS doesn't work in DSC [BuildOptions]
  section. It means MAKE flags can't be set in platform DSC file.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 02a908fc6d93a7971990d5fa8cd4efe023d14e43)

------------------------------------------------------------------------