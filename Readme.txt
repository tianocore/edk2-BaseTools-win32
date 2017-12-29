Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26060

This directory contains the Win32 binaries.

Build Date:       Thu, 28 Dec 2017 19:31:17 Pacific Standard Time
Last Changed Rev: 26060

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26060
  BootSectImage Version 1.0 Build Build 26005
  Brotli Version 0.5.2 Build 26005
  Brotli Version 0.5.2 Build 26005
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 26005
  EfiRom Version 0.1 Build 26005
  GenBootSector Version 0.2 Build 26005
  GenCrc32 Version 0.2 Build 26005
 *GenDepex.exe Version 0.04 Build 26060
 *GenFds.exe 1.0 Build 26060
  GenFfs Version 0.1 Build 26005
  GenFv Version 0.1 Build 26005
  GenFw Version 0.2 Build 26005
  GenPage Version 0.2 Build 26005
 *GenPatchPcdTable.exe Version 0.10 Build 26060
  GenSec Version 0.1 Build 26005
  GenVtf Version 0.1 Build 26005
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26005
  LzmaF86Compress Version 0.2 Build 26005
 *PatchPcdValue.exe Version 0.10 Build 26060
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 26005
 *TargetTool.exe Version 0.01 Build 26060
  TianoCompress Version 0.1 Build 26005
 *Trim.exe Version 0.10 Build 26060
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26005
  VolInfo Version 1.0 Build Build 26005
 *build.exe Version 0.60 Build 26060

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/28/2017 7:31:18PM Engine version = 5900.7806
  12/28/2017 7:31:18PM AntiVirus DAT version = 8758.0
  12/28/2017 7:31:18PM Number of detection signatures in EXTRA.DAT = None
  12/28/2017 7:31:18PM Names of detection signatures in EXTRA.DAT = None
  12/28/2017 7:31:19PM Scan Started On-Demand Scan
  12/28/2017 7:31:28PM Scan Summary
  12/28/2017 7:31:28PM Processes scanned : 0
  12/28/2017 7:31:28PM Processes detected : 0
  12/28/2017 7:31:28PM Processes cleaned : 0
  12/28/2017 7:31:28PM Boot sectors scanned : 2
  12/28/2017 7:31:28PM Boot sectors detected: 0
  12/28/2017 7:31:28PM Boot sectors cleaned : 0
  12/28/2017 7:31:28PM Files scanned : 64
  12/28/2017 7:31:28PM Files with detections: 0
  12/28/2017 7:31:28PM File detections : 0
  12/28/2017 7:31:28PM Files cleaned : 0
  12/28/2017 7:31:28PM Files deleted : 0
  12/28/2017 7:31:28PM Files not scanned : 0
  12/28/2017 7:31:28PM Scan Summary (Registry Scanning)
  12/28/2017 7:31:28PM Keys scanned : 0
  12/28/2017 7:31:28PM Keys detected : 0
  12/28/2017 7:31:28PM Keys cleaned : 0
  12/28/2017 7:31:28PM Keys deleted : 0
  12/28/2017 7:31:28PM Run time : 0:00:10
  12/28/2017 7:31:28PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26048:HEAD Source
------------------------------------------------------------------------  r26059 | edk2buildsystem | 2017-12-28 19:27:22 -0800 (Thu, 28 Dec 2017) | 11 lines
  BaseTools: Fix a bug for different FV use same FILE statement Guid
  We meet a case that different FV use same FILE statement Guid, but the
  FILE content is different. current we use the Guid value as Ffs file
  dir which cause the ffs file will be override. This patch use Guid
  value and Fv name as ffs dir for FILE statement.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a743986df89b60ae49e970cdb81fac4575e87342)

------------------------------------------------------------------------  r26060 | edk2buildsystem | 2017-12-28 19:27:28 -0800 (Thu, 28 Dec 2017) | 12 lines
  BaseTools: Fix the bug for QuarkPlatformPkg build failure
  The issue is that the string 'LPC' starts with the 'L' character and
  this is being confused with L" or L' for a Unicode string or Unicode
  character.
  Fixes:https://bugzilla.tianocore.org/show_bug.cgi?id=831
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f13f306b3b07330191ba4620e49c2a9151b8e575)

------------------------------------------------------------------------