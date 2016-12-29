Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23673

This directory contains the Win32 binaries.

Build Date:       Thu, 29 Dec 2016 03:11:10 Pacific Standard Time
Last Changed Rev: 23673

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23459
  BootSectImage Version 1.0 Build Build 23431
 *Ecc.exe Version 1.0 Build Build 23673
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
  GenDepex.exe Version 0.04 Build 23459
 *GenFds.exe 1.0 Build 23673
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 23431
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 23459
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 23431
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 23459
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 23431
  TargetTool.exe Version 0.01 Build 23459
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 23459
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23633
  VolInfo Version 1.0 Build Build 23468
 *build.exe Version 0.60 Build 23673

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/29/2016 3:11:12AM Engine version = 5700.7163
  12/29/2016 3:11:12AM AntiVirus DAT version = 8392.0
  12/29/2016 3:11:12AM Number of detection signatures in EXTRA.DAT = None
  12/29/2016 3:11:12AM Names of detection signatures in EXTRA.DAT = None
  12/29/2016 3:11:12AM Scan Started On-Demand Scan
  12/29/2016 3:11:26AM Scan Summary
  12/29/2016 3:11:26AM Processes scanned : 0
  12/29/2016 3:11:26AM Processes detected : 0
  12/29/2016 3:11:26AM Processes cleaned : 0
  12/29/2016 3:11:26AM Boot sectors scanned : 2
  12/29/2016 3:11:26AM Boot sectors detected: 0
  12/29/2016 3:11:26AM Boot sectors cleaned : 0
  12/29/2016 3:11:26AM Files scanned : 62
  12/29/2016 3:11:26AM Files with detections: 0
  12/29/2016 3:11:26AM File detections : 0
  12/29/2016 3:11:26AM Files cleaned : 0
  12/29/2016 3:11:26AM Files deleted : 0
  12/29/2016 3:11:26AM Files not scanned : 0
  12/29/2016 3:11:26AM Scan Summary (Registry Scanning)
  12/29/2016 3:11:26AM Keys scanned : 0
  12/29/2016 3:11:26AM Keys detected : 0
  12/29/2016 3:11:26AM Keys cleaned : 0
  12/29/2016 3:11:26AM Keys deleted : 0
  12/29/2016 3:11:26AM Run time : 0:00:15
  12/29/2016 3:11:26AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23633:HEAD Source
------------------------------------------------------------------------  r23633 | edk2buildsystem | 2016-12-23 02:05:55 -0800 (Fri, 23 Dec 2016) | 8 lines
  BaseTools/Pccts: Resolve GCC sting format mismatch build warning
  https://bugzilla.tianocore.org/show_bug.cgi?id=282
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 0a64f49fde09928b6061543b08e6da195e2abfbd)

------------------------------------------------------------------------  r23671 | edk2buildsystem | 2016-12-29 02:06:01 -0800 (Thu, 29 Dec 2016) | 8 lines
  BaseTools/Ecc: Fix the issue of not recognizing "FILE_GUID"
  Fix the issue of not recognizing "FILE_GUID"
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit f05c2e9fca28fcfb529e43af985605a362d2aa98)

------------------------------------------------------------------------  r23673 | edk2buildsystem | 2016-12-29 02:06:10 -0800 (Thu, 29 Dec 2016) | 12 lines
  BaseTools: Fix the bug for RAW file alignment value support
  Fix the bug for RAW file to support Align=32 and Align=64. Current FDF
  spec FfsAlignmentValues support this two values, while it is not the
  valid value for GenFfs. So this patch add the logic to handle it.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=248
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d2192f12b2d0b93416ff63ac73a3276a07d26c9e)

------------------------------------------------------------------------