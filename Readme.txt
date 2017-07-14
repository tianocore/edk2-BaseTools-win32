Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24939

This directory contains the Win32 binaries.

Build Date:       Fri, 14 Jul 2017 03:11:50 Pacific Daylight Time
Last Changed Rev: 24939

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24913
  BootSectImage Version 1.0 Build Build 23431
  Brotli Version 0.5.2 Build 24577
  Brotli Version 0.5.2 Build 24577
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
  GenDepex.exe Version 0.04 Build 24913
  GenFds.exe 1.0 Build 24913
  GenFfs Version 0.1 Build 24909
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24909
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 24913
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 24913
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 23431
  TargetTool.exe Version 0.01 Build 24913
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 24913
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24507
 *build.exe Version 0.60 Build 24939

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  7/14/2017 3:11:52AM Engine version = 5800.7501
  7/14/2017 3:11:52AM AntiVirus DAT version = 8590.0
  7/14/2017 3:11:52AM Number of detection signatures in EXTRA.DAT = None
  7/14/2017 3:11:52AM Names of detection signatures in EXTRA.DAT = None
  7/14/2017 3:11:52AM Scan Started On-Demand Scan
  7/14/2017 3:12:02AM Scan Summary
  7/14/2017 3:12:02AM Processes scanned : 0
  7/14/2017 3:12:02AM Processes detected : 0
  7/14/2017 3:12:02AM Processes cleaned : 0
  7/14/2017 3:12:02AM Boot sectors scanned : 2
  7/14/2017 3:12:02AM Boot sectors detected: 0
  7/14/2017 3:12:02AM Boot sectors cleaned : 0
  7/14/2017 3:12:02AM Files scanned : 64
  7/14/2017 3:12:02AM Files with detections: 0
  7/14/2017 3:12:02AM File detections : 0
  7/14/2017 3:12:02AM Files cleaned : 0
  7/14/2017 3:12:02AM Files deleted : 0
  7/14/2017 3:12:02AM Files not scanned : 0
  7/14/2017 3:12:02AM Scan Summary (Registry Scanning)
  7/14/2017 3:12:02AM Keys scanned : 0
  7/14/2017 3:12:02AM Keys detected : 0
  7/14/2017 3:12:02AM Keys cleaned : 0
  7/14/2017 3:12:02AM Keys deleted : 0
  7/14/2017 3:12:02AM Run time : 0:00:10
  7/14/2017 3:12:02AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24913:HEAD Source
------------------------------------------------------------------------  r24913 | edk2buildsystem | 2017-07-10 02:05:36 -0700 (Mon, 10 Jul 2017) | 10 lines
  BaseTools: Report Fd File Path in build log
  At the end of build, Report Fd image path in build log
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit c82fc2b555285306904c9c1ed6524a85bee8841a)

------------------------------------------------------------------------  r24939 | edk2buildsystem | 2017-07-14 02:05:21 -0700 (Fri, 14 Jul 2017) | 13 lines
  BaseTools/Build: Support python scripts in PREBUILD/POSTBUILD
  https://bugzilla.tianocore.org/show_bug.cgi?id=627
  Add shell=True in Popen() calls to support direct execution of
  python scripts
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Michael Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b926f2f2a4cd404df1d2c1dddbcd1178acc63b5e)

------------------------------------------------------------------------