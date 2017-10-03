Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25453

This directory contains the Win32 binaries.

Build Date:       Tue, 03 Oct 2017 03:13:05 Pacific Daylight Time
Last Changed Rev: 25453

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25450
 *BootSectImage Version 1.0 Build Build 25453
 *Brotli Version 0.5.2 Build 25453
  Brotli Version 0.5.2 Build 25453
  Ecc.exe Version 1.0 Build Build 24602
 *EfiLdrImage Version 1.0 Build Build 25453
 *EfiRom Version 0.1 Build 25453
 *GenBootSector Version 0.2 Build 25453
 *GenCrc32 Version 0.2 Build 25453
  GenDepex.exe Version 0.04 Build 25450
 *GenFds.exe 1.0 Build 25453
 *GenFfs Version 0.1 Build 25453
 *GenFv Version 0.1 Build 25453
 *GenFw Version 0.2 Build 25453
 *GenPage Version 0.2 Build 25453
  GenPatchPcdTable.exe Version 0.10 Build 25450
 *GenSec Version 0.1 Build 25453
 *GenVtf Version 0.1 Build 25453
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 25453
  LzmaF86Compress Version 0.2 Build 25453
  PatchPcdValue.exe Version 0.10 Build 25450
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
 *Split Version 1.0 Build Build 25453
  TargetTool.exe Version 0.01 Build 25450
 *TianoCompress Version 0.1 Build 25453
  Trim.exe Version 0.10 Build 25450
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 25453
 *VolInfo Version 1.0 Build Build 25453
 *build.exe Version 0.60 Build 25453

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/3/2017 3:13:06AM Engine version = 5900.7806
  10/3/2017 3:13:06AM AntiVirus DAT version = 8672.0
  10/3/2017 3:13:06AM Number of detection signatures in EXTRA.DAT = None
  10/3/2017 3:13:06AM Names of detection signatures in EXTRA.DAT = None
  10/3/2017 3:13:06AM Scan Started On-Demand Scan
  10/3/2017 3:13:28AM Scan Summary
  10/3/2017 3:13:28AM Processes scanned : 0
  10/3/2017 3:13:28AM Processes detected : 0
  10/3/2017 3:13:28AM Processes cleaned : 0
  10/3/2017 3:13:28AM Boot sectors scanned : 2
  10/3/2017 3:13:28AM Boot sectors detected: 0
  10/3/2017 3:13:28AM Boot sectors cleaned : 0
  10/3/2017 3:13:28AM Files scanned : 81
  10/3/2017 3:13:28AM Files with detections: 0
  10/3/2017 3:13:28AM File detections : 0
  10/3/2017 3:13:28AM Files cleaned : 0
  10/3/2017 3:13:28AM Files deleted : 0
  10/3/2017 3:13:28AM Files not scanned : 0
  10/3/2017 3:13:28AM Scan Summary (Registry Scanning)
  10/3/2017 3:13:28AM Keys scanned : 0
  10/3/2017 3:13:28AM Keys detected : 0
  10/3/2017 3:13:28AM Keys cleaned : 0
  10/3/2017 3:13:28AM Keys deleted : 0
  10/3/2017 3:13:28AM Run time : 0:00:22
  10/3/2017 3:13:28AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25450:HEAD Source
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

------------------------------------------------------------------------