Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 19579

This directory contains the Win32 binaries.

Build Date:       Wed, 30 Dec 2015 14:28:38 Pacific Standard Time
Last Changed Rev: 19576

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 19174
  BootSectImage Version 0.1 Build 19148
  Ecc.exe Version 0.01 Build 18595
  EfiLdrImage Version 0.1 Build 19148
  EfiRom Version 0.1 Build 19148
  GenBootSector Version 0.2 Build 19148
  GenCrc32 Version 0.2 Build 19148
  GenDepex.exe Version 0.04 Build 19174
  GenFds.exe 1.0 Build 19333
  GenFfs Version 0.1 Build 19148
  GenFv Version 0.1 Build 19148
  GenFw Version 0.2 Build 19244
  GenPage Version 0.2 Build 19148
  GenPatchPcdTable.exe Version 0.10 Build 19174
  GenSec Version 0.1 Build 19148
  GenVtf Version 0.1 Build 19148
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 19148
  LzmaF86Compress Version 0.2 Build 19148
  PatchPcdValue.exe Version 0.10 Build 19174
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 19148
  TargetTool.exe Version 0.01 Build 19174
  TianoCompress Version 0.1 Build 19148
  Trim.exe Version 0.10 Build 19174
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 18900
  VfrCompile version  2.00 (UEFI 2.4) Build 19148
  VolInfo Version 0.83 Build 19148, Dec  7 2015
  build.exe Version 0.60 Build 19174

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/30/2015 2:28:40PM Engine version = 5700.7163
  12/30/2015 2:28:40PM AntiVirus DAT version = 8029.0
  12/30/2015 2:28:40PM Number of detection signatures in EXTRA.DAT = None
  12/30/2015 2:28:40PM Names of detection signatures in EXTRA.DAT = None
  12/30/2015 2:28:40PM Scan Started On-Demand Scan
  12/30/2015 2:28:52PM Scan Summary
  12/30/2015 2:28:52PM Processes scanned : 0
  12/30/2015 2:28:52PM Processes detected : 0
  12/30/2015 2:28:52PM Processes cleaned : 0
  12/30/2015 2:28:52PM Boot sectors scanned : 2
  12/30/2015 2:28:52PM Boot sectors detected: 0
  12/30/2015 2:28:52PM Boot sectors cleaned : 0
  12/30/2015 2:28:52PM Files scanned : 54
  12/30/2015 2:28:52PM Files with detections: 0
  12/30/2015 2:28:52PM File detections : 0
  12/30/2015 2:28:52PM Files cleaned : 0
  12/30/2015 2:28:52PM Files deleted : 0
  12/30/2015 2:28:52PM Files not scanned : 0
  12/30/2015 2:28:52PM Scan Summary (Registry Scanning)
  12/30/2015 2:28:52PM Keys scanned : 0
  12/30/2015 2:28:52PM Keys detected : 0
  12/30/2015 2:28:52PM Keys cleaned : 0
  12/30/2015 2:28:52PM Keys deleted : 0
  12/30/2015 2:28:52PM Run time : 0:00:13
  12/30/2015 2:28:52PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 19333:HEAD Source
------------------------------------------------------------------------  r19501 | lhauch | 2015-12-23 10:30:20 -0800 (Wed, 23 Dec 2015) | 7 lines
  BaseTools: Fix Makefile to correctly break during a build failure
  Updated the Makefile so that nmake will correctly fail if the cxfreeze command fails to complete successfully.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Larry Hauch <larry.hauch@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>

------------------------------------------------------------------------  r19575 | hchen30 | 2015-12-29 18:22:02 -0800 (Tue, 29 Dec 2015) | 5 lines
  BaseTool/ECC: Add UTF-8 support on ECC tool
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>

------------------------------------------------------------------------  r19576 | hchen30 | 2015-12-29 18:22:30 -0800 (Tue, 29 Dec 2015) | 5 lines
  BaseTool/UPT: Fix a typo issue
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>

------------------------------------------------------------------------