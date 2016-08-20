Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22444

This directory contains the Win32 binaries.

Build Date:       Sat, 20 Aug 2016 03:11:04 Pacific Daylight Time
Last Changed Rev: 22444

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22444
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
  GenDepex.exe Version 0.04 Build 22444
  GenFds.exe 1.0 Build 22444
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 22370
  GenFw Version 0.2 Build 22308
  GenPage Version 0.2 Build 20909
  GenPatchPcdTable.exe Version 0.10 Build 22444
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
  PatchPcdValue.exe Version 0.10 Build 22444
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
 *Rsa2048Sha256Sign Version 0.9 Build 22444
  Split Version 1.0 Build Build 20909
  TargetTool.exe Version 0.01 Build 22444
  TianoCompress Version 0.1 Build 20909
  Trim.exe Version 0.10 Build 22444
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22316
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22367
  VolInfo Version 1.0 Build Build 20909
  build.exe Version 0.60 Build 22444

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/20/2016 3:11:05AM Engine version = 5700.7163
  8/20/2016 3:11:05AM AntiVirus DAT version = 8262.0
  8/20/2016 3:11:05AM Number of detection signatures in EXTRA.DAT = None
  8/20/2016 3:11:05AM Names of detection signatures in EXTRA.DAT = None
  8/20/2016 3:11:05AM Scan Started On-Demand Scan
  8/20/2016 3:11:15AM Scan Summary
  8/20/2016 3:11:15AM Processes scanned : 0
  8/20/2016 3:11:15AM Processes detected : 0
  8/20/2016 3:11:15AM Processes cleaned : 0
  8/20/2016 3:11:15AM Boot sectors scanned : 2
  8/20/2016 3:11:15AM Boot sectors detected: 0
  8/20/2016 3:11:15AM Boot sectors cleaned : 0
  8/20/2016 3:11:15AM Files scanned : 55
  8/20/2016 3:11:15AM Files with detections: 0
  8/20/2016 3:11:15AM File detections : 0
  8/20/2016 3:11:15AM Files cleaned : 0
  8/20/2016 3:11:15AM Files deleted : 0
  8/20/2016 3:11:15AM Files not scanned : 0
  8/20/2016 3:11:15AM Scan Summary (Registry Scanning)
  8/20/2016 3:11:15AM Keys scanned : 0
  8/20/2016 3:11:15AM Keys detected : 0
  8/20/2016 3:11:15AM Keys cleaned : 0
  8/20/2016 3:11:15AM Keys deleted : 0
  8/20/2016 3:11:15AM Run time : 0:00:10
  8/20/2016 3:11:15AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22444:HEAD Source
------------------------------------------------------------------------  r22444 | edk2buildsystem | 2016-08-19 02:06:39 -0700 (Fri, 19 Aug 2016) | 13 lines
  BaseTools: Fix a bug use 'COMMON' as CodeBase in BuildOptions section
  Current BaseTools query the BuildOptions not cover the case that use
  'COMMON' as CodeBase, while DSC spec allow this usage. This Patch add
  support for such 'common.DXE_RUNTIME_DRIVER' as the Scope2 in the query
  Condition.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Kurt Kennett <Kurt.Kennett@microsoft.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 35dc964bf1eab3f0725389811d2316b1331d6cee)

------------------------------------------------------------------------