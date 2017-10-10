Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25478

This directory contains the Win32 binaries.

Build Date:       Tue, 10 Oct 2017 03:11:52 Pacific Daylight Time
Last Changed Rev: 25475

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25450
  BootSectImage Version 1.0 Build Build 25453
  Brotli Version 0.5.2 Build 25453
  Brotli Version 0.5.2 Build 25453
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25453
  EfiRom Version 0.1 Build 25453
  GenBootSector Version 0.2 Build 25453
  GenCrc32 Version 0.2 Build 25453
  GenDepex.exe Version 0.04 Build 25450
  GenFds.exe 1.0 Build 25453
  GenFfs Version 0.1 Build 25453
  GenFv Version 0.1 Build 25453
  GenFw Version 0.2 Build 25453
  GenPage Version 0.2 Build 25453
  GenPatchPcdTable.exe Version 0.10 Build 25450
  GenSec Version 0.1 Build 25453
  GenVtf Version 0.1 Build 25453
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25453
  LzmaF86Compress Version 0.2 Build 25453
  PatchPcdValue.exe Version 0.10 Build 25450
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25453
  TargetTool.exe Version 0.01 Build 25450
  TianoCompress Version 0.1 Build 25453
  Trim.exe Version 0.10 Build 25450
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25453
  VolInfo Version 1.0 Build Build 25453
 *build.exe Version 0.60 Build 25478

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/10/2017 3:11:53AM Engine version = 5900.7806
  10/10/2017 3:11:53AM AntiVirus DAT version = 8679.0
  10/10/2017 3:11:53AM Number of detection signatures in EXTRA.DAT = None
  10/10/2017 3:11:53AM Names of detection signatures in EXTRA.DAT = None
  10/10/2017 3:11:53AM Scan Started On-Demand Scan
  10/10/2017 3:12:03AM Scan Summary
  10/10/2017 3:12:03AM Processes scanned : 0
  10/10/2017 3:12:03AM Processes detected : 0
  10/10/2017 3:12:03AM Processes cleaned : 0
  10/10/2017 3:12:03AM Boot sectors scanned : 2
  10/10/2017 3:12:03AM Boot sectors detected: 0
  10/10/2017 3:12:03AM Boot sectors cleaned : 0
  10/10/2017 3:12:03AM Files scanned : 64
  10/10/2017 3:12:03AM Files with detections: 0
  10/10/2017 3:12:03AM File detections : 0
  10/10/2017 3:12:03AM Files cleaned : 0
  10/10/2017 3:12:03AM Files deleted : 0
  10/10/2017 3:12:03AM Files not scanned : 0
  10/10/2017 3:12:03AM Scan Summary (Registry Scanning)
  10/10/2017 3:12:03AM Keys scanned : 0
  10/10/2017 3:12:03AM Keys detected : 0
  10/10/2017 3:12:03AM Keys cleaned : 0
  10/10/2017 3:12:03AM Keys deleted : 0
  10/10/2017 3:12:03AM Run time : 0:00:10
  10/10/2017 3:12:03AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25453:HEAD Source
------------------------------------------------------------------------  r25453 | edk2buildsystem | 2017-10-03 02:05:24 -0700 (Tue, 03 Oct 2017) | 11 lines
  BaseTools: PI 1.6 to support FV extended header contain FV used size
  Per PI 1.6 we added an FV Extended Header entry that would contain the
  size of the FV that was in use.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9425b34925d0cf1b96aaf2c316d3299df9780252)

------------------------------------------------------------------------  r25475 | edk2buildsystem | 2017-10-10 02:05:27 -0700 (Tue, 10 Oct 2017) | 11 lines
  BaseTools: Fix a bug to use module's Name attribute as compare
  Fix a bug to use module's Name attribute as compare for single module
  build. ModuleFile.File can't be used to compare INF file, because it
  is the relative path.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit fbe538450fb5327110f3b01d038e356e590dd93a)

------------------------------------------------------------------------