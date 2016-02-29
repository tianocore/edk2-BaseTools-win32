Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 20165, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20059

This directory contains the Win32 binaries.

Build Date:       Mon, 29 Feb 2016 14:31:25 Pacific Standard Time
Last Changed Rev: 20055

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 19914
  BootSectImage Version 1.0 Build Build 19914
  Ecc.exe Version 1.0 Build Build 19914
  EfiLdrImage Version 1.0 Build Build 19914
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
  GenDepex.exe Version 0.04 Build 19914
  GenFds.exe 1.0 Build 19914
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 19914
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
  GenPatchPcdTable.exe Version 0.10 Build 19914
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 20059
  LzmaF86Compress Version 0.2 Build 20059
  PatchPcdValue.exe Version 0.10 Build 19914
  Rsa2048Sha256GenerateKeys Version 0.9 Build 19914
  Rsa2048Sha256Sign Version 0.9 Build 19914
  Split Version 1.0 Build Build 19914
  TargetTool.exe Version 0.01 Build 19914
  TianoCompress Version 0.1 Build 19914
  Trim.exe Version 0.10 Build 19914
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 19914
  VfrCompile version  2.01 (UEFI 2.4) Build Build 19914
  VolInfo Version 1.0 Build Build 19914
  build.exe Version 0.60 Build 19914

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/29/2016 2:31:26PM Engine version = 5700.7163
  2/29/2016 2:31:26PM AntiVirus DAT version = 8089.0
  2/29/2016 2:31:26PM Number of detection signatures in EXTRA.DAT = None
  2/29/2016 2:31:26PM Names of detection signatures in EXTRA.DAT = None
  2/29/2016 2:31:26PM Scan Started On-Demand Scan
  2/29/2016 2:31:28PM Scan Summary
  2/29/2016 2:31:28PM Processes scanned : 0
  2/29/2016 2:31:28PM Processes detected : 0
  2/29/2016 2:31:28PM Processes cleaned : 0
  2/29/2016 2:31:28PM Boot sectors scanned : 1
  2/29/2016 2:31:28PM Boot sectors detected: 0
  2/29/2016 2:31:28PM Boot sectors cleaned : 0
  2/29/2016 2:31:28PM Files scanned : 55
  2/29/2016 2:31:28PM Files with detections: 0
  2/29/2016 2:31:28PM File detections : 0
  2/29/2016 2:31:28PM Files cleaned : 0
  2/29/2016 2:31:28PM Files deleted : 0
  2/29/2016 2:31:28PM Files not scanned : 0
  2/29/2016 2:31:28PM Scan Summary (Registry Scanning)
  2/29/2016 2:31:28PM Keys scanned : 0
  2/29/2016 2:31:28PM Keys detected : 0
  2/29/2016 2:31:28PM Keys cleaned : 0
  2/29/2016 2:31:28PM Keys deleted : 0
  2/29/2016 2:31:28PM Run time : 0:00:02
  2/29/2016 2:31:28PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 19914:HEAD Source
------------------------------------------------------------------------  r20055 | edk2buildsystem | 2016-02-29 09:38:08 -0800 (Mon, 29 Feb 2016) | 9 lines
  BaseTools: fix LzmaCompress VS2013 make failure
  when make BaseTools by VS2013, LzmaEnc.c report warning C4127:
  conditional expression is constant, so this patch fix this issue.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b0c583cdd19cc6316cbda82cb79df4346a7db8c7)

------------------------------------------------------------------------