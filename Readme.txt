Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25825

This directory contains the Win32 binaries.

Build Date:       Wed, 06 Dec 2017 03:12:20 Pacific Standard Time
Last Changed Rev: 25824

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25818
  BootSectImage Version 1.0 Build Build 25453
  Brotli Version 0.5.2 Build 25453
  Brotli Version 0.5.2 Build 25453
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25453
  EfiRom Version 0.1 Build 25453
  GenBootSector Version 0.2 Build 25453
  GenCrc32 Version 0.2 Build 25453
  GenDepex.exe Version 0.04 Build 25818
  GenFds.exe 1.0 Build 25818
  GenFfs Version 0.1 Build 25818
  GenFv Version 0.1 Build 25453
  GenFw Version 0.2 Build 25453
  GenPage Version 0.2 Build 25453
  GenPatchPcdTable.exe Version 0.10 Build 25818
 *GenSec Version 0.1 Build 25825
  GenVtf Version 0.1 Build 25453
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25453
  LzmaF86Compress Version 0.2 Build 25453
  PatchPcdValue.exe Version 0.10 Build 25818
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25453
  TargetTool.exe Version 0.01 Build 25818
  TianoCompress Version 0.1 Build 25453
  Trim.exe Version 0.10 Build 25818
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25614
  VolInfo Version 1.0 Build Build 25453
  build.exe Version 0.60 Build 25818

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/6/2017 3:12:22AM Engine version = 5900.7806
  12/6/2017 3:12:22AM AntiVirus DAT version = 8736.0
  12/6/2017 3:12:22AM Number of detection signatures in EXTRA.DAT = None
  12/6/2017 3:12:22AM Names of detection signatures in EXTRA.DAT = None
  12/6/2017 3:12:22AM Scan Started On-Demand Scan
  12/6/2017 3:12:29AM Scan Summary
  12/6/2017 3:12:29AM Processes scanned : 0
  12/6/2017 3:12:29AM Processes detected : 0
  12/6/2017 3:12:29AM Processes cleaned : 0
  12/6/2017 3:12:29AM Boot sectors scanned : 2
  12/6/2017 3:12:29AM Boot sectors detected: 0
  12/6/2017 3:12:29AM Boot sectors cleaned : 0
  12/6/2017 3:12:29AM Files scanned : 64
  12/6/2017 3:12:29AM Files with detections: 0
  12/6/2017 3:12:29AM File detections : 0
  12/6/2017 3:12:29AM Files cleaned : 0
  12/6/2017 3:12:29AM Files deleted : 0
  12/6/2017 3:12:29AM Files not scanned : 0
  12/6/2017 3:12:29AM Scan Summary (Registry Scanning)
  12/6/2017 3:12:29AM Keys scanned : 0
  12/6/2017 3:12:29AM Keys detected : 0
  12/6/2017 3:12:29AM Keys cleaned : 0
  12/6/2017 3:12:29AM Keys deleted : 0
  12/6/2017 3:12:29AM Run time : 0:00:07
  12/6/2017 3:12:29AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25818:HEAD Source
------------------------------------------------------------------------  r25824 | edk2buildsystem | 2017-12-06 02:05:37 -0800 (Wed, 06 Dec 2017) | 15 lines
  BaseTools: Fix GenSec GCC make failure
  It is a regression bug introduced by the patch b37b108, it cause GenSec
  make failure on GCC Env.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Leif Lindholm <leif.lindholm@linaro.org>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Tested-by: Leif Lindholm <leif.lindholm@linaro.org>
  Tested-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Leif Lindholm <leif.lindholm@linaro.org>
  Reviewed-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1e6e6e188e01fa08f653706076a6465e0fcb0441)

------------------------------------------------------------------------