Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22793

This directory contains the Win32 binaries.

Build Date:       Wed, 12 Oct 2016 03:11:06 Pacific Daylight Time
Last Changed Rev: 22789

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
  EfiLdrImage Version 1.0 Build Build 22752
  EfiRom Version 0.1 Build 22617
  GenBootSector Version 0.2 Build 22449
  GenCrc32 Version 0.2 Build 22449
  GenDepex.exe Version 0.04 Build 22700
 *GenFds.exe 1.0 Build 22793
  GenFfs Version 0.1 Build 22449
  GenFv Version 0.1 Build 22543
  GenFw Version 0.2 Build 22466
  GenPage Version 0.2 Build 22449
  GenPatchPcdTable.exe Version 0.10 Build 22700
  GenSec Version 0.1 Build 22449
  GenVtf Version 0.1 Build 22752
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
  10/12/2016 3:11:08AM Engine version = 5700.7163
  10/12/2016 3:11:08AM AntiVirus DAT version = 8315.0
  10/12/2016 3:11:08AM Number of detection signatures in EXTRA.DAT = None
  10/12/2016 3:11:08AM Names of detection signatures in EXTRA.DAT = None
  10/12/2016 3:11:08AM Scan Started On-Demand Scan
  10/12/2016 3:11:10AM Scan Summary
  10/12/2016 3:11:10AM Processes scanned : 0
  10/12/2016 3:11:10AM Processes detected : 0
  10/12/2016 3:11:10AM Processes cleaned : 0
  10/12/2016 3:11:10AM Boot sectors scanned : 1
  10/12/2016 3:11:10AM Boot sectors detected: 0
  10/12/2016 3:11:10AM Boot sectors cleaned : 0
  10/12/2016 3:11:10AM Files scanned : 62
  10/12/2016 3:11:10AM Files with detections: 0
  10/12/2016 3:11:10AM File detections : 0
  10/12/2016 3:11:10AM Files cleaned : 0
  10/12/2016 3:11:10AM Files deleted : 0
  10/12/2016 3:11:10AM Files not scanned : 0
  10/12/2016 3:11:10AM Scan Summary (Registry Scanning)
  10/12/2016 3:11:10AM Keys scanned : 0
  10/12/2016 3:11:10AM Keys detected : 0
  10/12/2016 3:11:10AM Keys cleaned : 0
  10/12/2016 3:11:10AM Keys deleted : 0
  10/12/2016 3:11:10AM Run time : 0:00:03
  10/12/2016 3:11:10AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22752:HEAD Source
------------------------------------------------------------------------  r22752 | edk2buildsystem | 2016-10-08 02:07:17 -0700 (Sat, 08 Oct 2016) | 8 lines
  BaseTools Makefile: Enable O2 option for GCC tool chain
  Enable O2 option to generate fast code for performance improvement.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Jordan Justen <jordan.l.justen@intel.com>
  (cherry picked from commit 202726b3ceb33576ac6feb778e48bd851bfe171e)

------------------------------------------------------------------------  r22789 | edk2buildsystem | 2016-10-12 02:06:59 -0700 (Wed, 12 Oct 2016) | 11 lines
  BaseTools: Extend FMP to support FV statement and FD statement
  This patch extend the <FmpFileData> to support <FvStatements> and
  <FdStatenents>, just like the normal [Capsule] section format.
  In order to fix the bug https://bugzilla.tianocore.org/show_bug.cgi?id=132
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 19e3aa7a8a8dcd661e0c2c45d139c5a6bda57dbb)

------------------------------------------------------------------------