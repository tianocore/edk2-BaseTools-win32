Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22731

This directory contains the Win32 binaries.

Build Date:       Fri, 30 Sep 2016 03:11:05 Pacific Daylight Time
Last Changed Rev: 22731

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
  EfiLdrImage Version 1.0 Build Build 22449
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
  GenVtf Version 0.1 Build 22449
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
 *build.exe Version 0.60 Build 22731

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  9/30/2016 3:11:06AM Engine version = 5700.7163
  9/30/2016 3:11:06AM AntiVirus DAT version = 8303.0
  9/30/2016 3:11:06AM Number of detection signatures in EXTRA.DAT = None
  9/30/2016 3:11:06AM Names of detection signatures in EXTRA.DAT = None
  9/30/2016 3:11:06AM Scan Started On-Demand Scan
  9/30/2016 3:11:15AM Scan Summary
  9/30/2016 3:11:15AM Processes scanned : 0
  9/30/2016 3:11:15AM Processes detected : 0
  9/30/2016 3:11:15AM Processes cleaned : 0
  9/30/2016 3:11:15AM Boot sectors scanned : 2
  9/30/2016 3:11:15AM Boot sectors detected: 0
  9/30/2016 3:11:15AM Boot sectors cleaned : 0
  9/30/2016 3:11:15AM Files scanned : 62
  9/30/2016 3:11:15AM Files with detections: 0
  9/30/2016 3:11:15AM File detections : 0
  9/30/2016 3:11:15AM Files cleaned : 0
  9/30/2016 3:11:15AM Files deleted : 0
  9/30/2016 3:11:15AM Files not scanned : 0
  9/30/2016 3:11:15AM Scan Summary (Registry Scanning)
  9/30/2016 3:11:15AM Keys scanned : 0
  9/30/2016 3:11:15AM Keys detected : 0
  9/30/2016 3:11:15AM Keys cleaned : 0
  9/30/2016 3:11:15AM Keys deleted : 0
  9/30/2016 3:11:15AM Run time : 0:00:10
  9/30/2016 3:11:15AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22700:HEAD Source
------------------------------------------------------------------------  r22700 | edk2buildsystem | 2016-09-27 02:06:19 -0700 (Tue, 27 Sep 2016) | 12 lines
  BaseTools: List missing source python files for Ecc tool in Makefile
  Add missing python sources files that are dependent for Ecc tool in
  Makefile.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7807dea57fba6a019bb8641572e0159ffa03ad9e)

------------------------------------------------------------------------  r22729 | edk2buildsystem | 2016-09-30 02:05:41 -0700 (Fri, 30 Sep 2016) | 6 lines
  BaseTools Makefile: Missing LFAGS in app.makefile
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 2dc547da460038e180f28161a44998e1849b2f43)

------------------------------------------------------------------------  r22730 | edk2buildsystem | 2016-09-30 02:05:45 -0700 (Fri, 30 Sep 2016) | 9 lines
  BaseTools VS Makefile: Don't include ms.common in ms.app
  ms.common is included by every tool Makefile. it is not necessary to be placed
  in ms.app again.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0eb330424c194a4869b2e33f42928715a5cad34e)

------------------------------------------------------------------------  r22731 | edk2buildsystem | 2016-09-30 02:05:50 -0700 (Fri, 30 Sep 2016) | 9 lines
  BaseTools Build: Fix build break for clean target in Linux
  In Linux, Command needs to be String instead of list when Command run
  as shell with True.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ed72804638c9b240477c5235d72c3823483813b2)

------------------------------------------------------------------------