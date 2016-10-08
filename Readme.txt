Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22752

This directory contains the Win32 binaries.

Build Date:       Sat, 08 Oct 2016 03:11:04 Pacific Daylight Time
Last Changed Rev: 22752

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22700
  BootSectImage Version 1.0 Build Build 22449
  Ecc.exe Version 1.0 Build Build 22700
 *EfiLdrImage Version 1.0 Build Build 22752
  EfiRom Version 0.1 Build 22617
  GenBootSector Version 0.2 Build 22449
  GenCrc32 Version 0.2 Build 22449
  GenDepex.exe Version 0.04 Build 22700
  GenFds.exe 1.0 Build 22700
  GenFfs Version 0.1 Build 22449
  GenFv Version 0.1 Build 22543
  GenFw Version 0.2 Build 22466
  GenPage Version 0.2 Build 22449
  GenPatchPcdTable.exe Version 0.10 Build 22700
  GenSec Version 0.1 Build 22449
 *GenVtf Version 0.1 Build 22752
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 22449
  LzmaF86Compress Version 0.2 Build 22449
  PatchPcdValue.exe Version 0.10 Build 22700
  Pkcs7Sign Version 0.9 Build 22543
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 22444
  Split Version 1.0 Build Build 22449
  TargetTool.exe Version 0.01 Build 22700
  TianoCompress Version 0.1 Build 22449
  Trim.exe Version 0.10 Build 22700
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22316
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22449
  VolInfo Version 1.0 Build Build 22449
  build.exe Version 0.60 Build 22731

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/8/2016 3:11:05AM Engine version = 5700.7163
  10/8/2016 3:11:05AM AntiVirus DAT version = 8311.0
  10/8/2016 3:11:05AM Number of detection signatures in EXTRA.DAT = None
  10/8/2016 3:11:05AM Names of detection signatures in EXTRA.DAT = None
  10/8/2016 3:11:05AM Scan Started On-Demand Scan
  10/8/2016 3:11:15AM Scan Summary
  10/8/2016 3:11:15AM Processes scanned : 0
  10/8/2016 3:11:15AM Processes detected : 0
  10/8/2016 3:11:15AM Processes cleaned : 0
  10/8/2016 3:11:15AM Boot sectors scanned : 2
  10/8/2016 3:11:15AM Boot sectors detected: 0
  10/8/2016 3:11:15AM Boot sectors cleaned : 0
  10/8/2016 3:11:15AM Files scanned : 63
  10/8/2016 3:11:15AM Files with detections: 0
  10/8/2016 3:11:15AM File detections : 0
  10/8/2016 3:11:15AM Files cleaned : 0
  10/8/2016 3:11:15AM Files deleted : 0
  10/8/2016 3:11:15AM Files not scanned : 0
  10/8/2016 3:11:15AM Scan Summary (Registry Scanning)
  10/8/2016 3:11:15AM Keys scanned : 0
  10/8/2016 3:11:15AM Keys detected : 0
  10/8/2016 3:11:15AM Keys cleaned : 0
  10/8/2016 3:11:15AM Keys deleted : 0
  10/8/2016 3:11:15AM Run time : 0:00:10
  10/8/2016 3:11:15AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22731:HEAD Source
------------------------------------------------------------------------  r22731 | edk2buildsystem | 2016-09-30 02:05:50 -0700 (Fri, 30 Sep 2016) | 9 lines
  BaseTools Build: Fix build break for clean target in Linux
  In Linux, Command needs to be String instead of list when Command run
  as shell with True.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ed72804638c9b240477c5235d72c3823483813b2)

------------------------------------------------------------------------  r22749 | edk2buildsystem | 2016-10-08 02:07:02 -0700 (Sat, 08 Oct 2016) | 6 lines
  BaseTools EfiLdrImage: Remove unnecessary exit (0)
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Jordan Justen <jordan.l.justen@intel.com>
  (cherry picked from commit 5277efed286d95168742fe257b11fa4578145e32)

------------------------------------------------------------------------  r22750 | edk2buildsystem | 2016-10-08 02:07:07 -0700 (Sat, 08 Oct 2016) | 8 lines
  BaseTools Makefile: Enable O2 option to replace Od for VS tool chain
  Enable O2 option to generate fast code for performance improvement.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Acked-by: Jordan Justen <jordan.l.justen@intel.com>
  (cherry picked from commit 9a1a63cf1148eeeb50d58a6982b4c45f2e83e8ab)

------------------------------------------------------------------------  r22751 | edk2buildsystem | 2016-10-08 02:07:12 -0700 (Sat, 08 Oct 2016) | 6 lines
  BaseTools GenVtf: Initialize the return point as NULL
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Jordan Justen <jordan.l.justen@intel.com>
  (cherry picked from commit c52d9f71ba179a825c12851a2b4823c1181bf55a)

------------------------------------------------------------------------  r22752 | edk2buildsystem | 2016-10-08 02:07:17 -0700 (Sat, 08 Oct 2016) | 8 lines
  BaseTools Makefile: Enable O2 option for GCC tool chain
  Enable O2 option to generate fast code for performance improvement.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Jordan Justen <jordan.l.justen@intel.com>
  (cherry picked from commit 202726b3ceb33576ac6feb778e48bd851bfe171e)

------------------------------------------------------------------------