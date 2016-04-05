Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20461

This directory contains the Win32 binaries.

Build Date:       Tue, 05 Apr 2016 03:33:08 Pacific Daylight Time
Last Changed Rev: 20458

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20461
  BootSectImage Version 1.0 Build Build 20182
 *Ecc.exe Version 1.0 Build Build 20461
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20461
 *GenFds.exe 1.0 Build 20461
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20461
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20461
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20331
  Rsa2048Sha256Sign Version 0.9 Build 20331
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20461
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20461
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20331
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20182
 *build.exe Version 0.60 Build 20461

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/5/2016 3:33:09AM Engine version = 5700.7163
  4/5/2016 3:33:09AM AntiVirus DAT version = 8125.0
  4/5/2016 3:33:09AM Number of detection signatures in EXTRA.DAT = None
  4/5/2016 3:33:09AM Names of detection signatures in EXTRA.DAT = None
  4/5/2016 3:33:09AM Scan Started On-Demand Scan
  4/5/2016 3:33:11AM Scan Summary
  4/5/2016 3:33:11AM Processes scanned : 0
  4/5/2016 3:33:11AM Processes detected : 0
  4/5/2016 3:33:11AM Processes cleaned : 0
  4/5/2016 3:33:11AM Boot sectors scanned : 1
  4/5/2016 3:33:11AM Boot sectors detected: 0
  4/5/2016 3:33:11AM Boot sectors cleaned : 0
  4/5/2016 3:33:11AM Files scanned : 55
  4/5/2016 3:33:11AM Files with detections: 0
  4/5/2016 3:33:11AM File detections : 0
  4/5/2016 3:33:11AM Files cleaned : 0
  4/5/2016 3:33:11AM Files deleted : 0
  4/5/2016 3:33:11AM Files not scanned : 0
  4/5/2016 3:33:11AM Scan Summary (Registry Scanning)
  4/5/2016 3:33:11AM Keys scanned : 0
  4/5/2016 3:33:11AM Keys detected : 0
  4/5/2016 3:33:11AM Keys cleaned : 0
  4/5/2016 3:33:11AM Keys deleted : 0
  4/5/2016 3:33:11AM Run time : 0:00:02
  4/5/2016 3:33:11AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20454:HEAD Source
------------------------------------------------------------------------  r20458 | edk2buildsystem | 2016-04-05 02:27:25 -0700 (Tue, 05 Apr 2016) | 11 lines
  BaseTools/GenFds: Fix the bug for wrong alignment generate for RAW file
  When do the multiple raw file support feature, it cause the regression
  that the raw file section alignment value was wrongly overridden by the
  single raw file. this patch: 1) fix the wrong overridden bug. 2) remove
  the duplicate code for combine multiple raw file into one.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit cfaaf99bdd412139ca7b9724e678429b2f2fb45f)

------------------------------------------------------------------------