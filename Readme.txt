Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20849

This directory contains the Win32 binaries.

Build Date:       Thu, 12 May 2016 03:11:23 Pacific Daylight Time
Last Changed Rev: 20835

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20849
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20849
 *GenFds.exe 1.0 Build 20849
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 20600
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20849
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20849
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20849
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20849
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20600
 *build.exe Version 0.60 Build 20849

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/12/2016 3:11:25AM Engine version = 5700.7163
  5/12/2016 3:11:25AM AntiVirus DAT version = 8162.0
  5/12/2016 3:11:25AM Number of detection signatures in EXTRA.DAT = None
  5/12/2016 3:11:25AM Names of detection signatures in EXTRA.DAT = None
  5/12/2016 3:11:25AM Scan Started On-Demand Scan
  5/12/2016 3:11:29AM Scan Summary
  5/12/2016 3:11:29AM Processes scanned : 0
  5/12/2016 3:11:29AM Processes detected : 0
  5/12/2016 3:11:29AM Processes cleaned : 0
  5/12/2016 3:11:29AM Boot sectors scanned : 2
  5/12/2016 3:11:29AM Boot sectors detected: 0
  5/12/2016 3:11:29AM Boot sectors cleaned : 0
  5/12/2016 3:11:29AM Files scanned : 55
  5/12/2016 3:11:29AM Files with detections: 0
  5/12/2016 3:11:29AM File detections : 0
  5/12/2016 3:11:29AM Files cleaned : 0
  5/12/2016 3:11:29AM Files deleted : 0
  5/12/2016 3:11:29AM Files not scanned : 0
  5/12/2016 3:11:29AM Scan Summary (Registry Scanning)
  5/12/2016 3:11:29AM Keys scanned : 0
  5/12/2016 3:11:29AM Keys detected : 0
  5/12/2016 3:11:29AM Keys cleaned : 0
  5/12/2016 3:11:29AM Keys deleted : 0
  5/12/2016 3:11:29AM Run time : 0:00:05
  5/12/2016 3:11:29AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20795:HEAD Source
------------------------------------------------------------------------  r20833 | edk2buildsystem | 2016-05-11 11:17:02 -0700 (Wed, 11 May 2016) | 10 lines
  BaseTools: fix a bug for uni file \x####\ format handling
  It should start from the last '\x' position + 1 to find next '\x'
  character.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit ad319b9307aaf37ffaf27890ae03dcbfd12087ce)

------------------------------------------------------------------------  r20835 | edk2buildsystem | 2016-05-11 11:33:23 -0700 (Wed, 11 May 2016) | 9 lines
  BaseTools: Fix bug in GenFds to handle FV image alignment
  Cover the case that .fv file in the [Binaries] section.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 321151fedb3013fe3a588ee7a4fe6639ceb29c7e)

------------------------------------------------------------------------