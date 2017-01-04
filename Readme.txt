Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23684

This directory contains the Win32 binaries.

Build Date:       Wed, 04 Jan 2017 03:11:16 Pacific Standard Time
Last Changed Rev: 23684

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
  Ecc.exe Version 1.0 Build Build 23673
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
  GenDepex.exe Version 0.04 Build 23459
  GenFds.exe 1.0 Build 23673
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
 *build.exe Version 0.60 Build 23684

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/4/2017 3:11:17AM Engine version = 5700.7163
  1/4/2017 3:11:17AM AntiVirus DAT version = 8397.0
  1/4/2017 3:11:17AM Number of detection signatures in EXTRA.DAT = None
  1/4/2017 3:11:17AM Names of detection signatures in EXTRA.DAT = None
  1/4/2017 3:11:17AM Scan Started On-Demand Scan
  1/4/2017 3:11:27AM Scan Summary
  1/4/2017 3:11:27AM Processes scanned : 0
  1/4/2017 3:11:27AM Processes detected : 0
  1/4/2017 3:11:27AM Processes cleaned : 0
  1/4/2017 3:11:27AM Boot sectors scanned : 2
  1/4/2017 3:11:27AM Boot sectors detected: 0
  1/4/2017 3:11:27AM Boot sectors cleaned : 0
  1/4/2017 3:11:27AM Files scanned : 62
  1/4/2017 3:11:27AM Files with detections: 0
  1/4/2017 3:11:27AM File detections : 0
  1/4/2017 3:11:27AM Files cleaned : 0
  1/4/2017 3:11:27AM Files deleted : 0
  1/4/2017 3:11:27AM Files not scanned : 0
  1/4/2017 3:11:27AM Scan Summary (Registry Scanning)
  1/4/2017 3:11:27AM Keys scanned : 0
  1/4/2017 3:11:27AM Keys detected : 0
  1/4/2017 3:11:27AM Keys cleaned : 0
  1/4/2017 3:11:27AM Keys deleted : 0
  1/4/2017 3:11:27AM Run time : 0:00:10
  1/4/2017 3:11:27AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23673:HEAD Source
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

------------------------------------------------------------------------  r23684 | edk2buildsystem | 2017-01-04 02:05:58 -0800 (Wed, 04 Jan 2017) | 10 lines
  BaseTools: fix the bug for Mixed Pcd display in the report
  Fix the bug to not display the mixed PCD in the Global PCD section, and
  correct the Pcd display name.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 7cb63c870bac7a986936aeb6e70b22ebf80d4ba9)

------------------------------------------------------------------------