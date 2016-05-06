Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20795

This directory contains the Win32 binaries.

Build Date:       Fri, 06 May 2016 03:11:19 Pacific Daylight Time
Last Changed Rev: 20767

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20795
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20795
 *GenFds.exe 1.0 Build 20795
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 20600
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20795
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20795
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20795
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20795
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20600
 *build.exe Version 0.60 Build 20795

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/6/2016 3:11:20AM Engine version = 5700.7163
  5/6/2016 3:11:20AM AntiVirus DAT version = 8156.0
  5/6/2016 3:11:20AM Number of detection signatures in EXTRA.DAT = None
  5/6/2016 3:11:20AM Names of detection signatures in EXTRA.DAT = None
  5/6/2016 3:11:20AM Scan Started On-Demand Scan
  5/6/2016 3:11:30AM Scan Summary
  5/6/2016 3:11:30AM Processes scanned : 0
  5/6/2016 3:11:30AM Processes detected : 0
  5/6/2016 3:11:30AM Processes cleaned : 0
  5/6/2016 3:11:30AM Boot sectors scanned : 2
  5/6/2016 3:11:30AM Boot sectors detected: 0
  5/6/2016 3:11:30AM Boot sectors cleaned : 0
  5/6/2016 3:11:30AM Files scanned : 55
  5/6/2016 3:11:30AM Files with detections: 0
  5/6/2016 3:11:30AM File detections : 0
  5/6/2016 3:11:30AM Files cleaned : 0
  5/6/2016 3:11:30AM Files deleted : 0
  5/6/2016 3:11:30AM Files not scanned : 0
  5/6/2016 3:11:30AM Scan Summary (Registry Scanning)
  5/6/2016 3:11:30AM Keys scanned : 0
  5/6/2016 3:11:30AM Keys detected : 0
  5/6/2016 3:11:30AM Keys cleaned : 0
  5/6/2016 3:11:30AM Keys deleted : 0
  5/6/2016 3:11:30AM Run time : 0:00:10
  5/6/2016 3:11:30AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20696:HEAD Source
------------------------------------------------------------------------  r20767 | edk2buildsystem | 2016-05-06 02:07:06 -0700 (Fri, 06 May 2016) | 10 lines
  BaseTools: Support \x####\ in UNI files to specify non-ascii characters
  UNI spec updated to allow using \x####\ to specify non-ascii characters,
  # is a hex digit.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 314e2fb1752679392e9fe386564ef04d99680a93)

------------------------------------------------------------------------