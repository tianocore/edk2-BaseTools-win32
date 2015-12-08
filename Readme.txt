Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 19174

This directory contains the Win32 binaries.

Build Date:       Tue, 08 Dec 2015 14:30:35 Pacific Standard Time
Last Changed Rev: 19150

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 19174
  BootSectImage Version 0.1 Build 19148
  Ecc.exe Version 0.01 Build 18595
  EfiLdrImage Version 0.1 Build 19148
  EfiRom Version 0.1 Build 19148
  GenBootSector Version 0.2 Build 19148
  GenCrc32 Version 0.2 Build 19148
 *GenDepex.exe Version 0.04 Build 19174
 *GenFds.exe 1.0 Build 19174
  GenFfs Version 0.1 Build 19148
  GenFv Version 0.1 Build 19148
  GenFw Version 0.2 Build 19148
  GenPage Version 0.2 Build 19148
 *GenPatchPcdTable.exe Version 0.10 Build 19174
  GenSec Version 0.1 Build 19148
  GenVtf Version 0.1 Build 19148
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 19148
  LzmaF86Compress Version 0.2 Build 19148
 *PatchPcdValue.exe Version 0.10 Build 19174
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 19148
 *TargetTool.exe Version 0.01 Build 19174
  TianoCompress Version 0.1 Build 19148
 *Trim.exe Version 0.10 Build 19174
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 18900
  VfrCompile version  2.00 (UEFI 2.4) Build 19148
  VolInfo Version 0.83 Build 19148, Dec  7 2015
 *build.exe Version 0.60 Build 19174

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/8/2015 2:30:36PM Engine version = 5700.7163
  12/8/2015 2:30:36PM AntiVirus DAT version = 8008.0
  12/8/2015 2:30:36PM Number of detection signatures in EXTRA.DAT = None
  12/8/2015 2:30:36PM Names of detection signatures in EXTRA.DAT = None
  12/8/2015 2:30:36PM Scan Started On-Demand Scan
  12/8/2015 2:30:46PM Scan Summary
  12/8/2015 2:30:46PM Processes scanned : 0
  12/8/2015 2:30:46PM Processes detected : 0
  12/8/2015 2:30:46PM Processes cleaned : 0
  12/8/2015 2:30:46PM Boot sectors scanned : 2
  12/8/2015 2:30:46PM Boot sectors detected: 0
  12/8/2015 2:30:46PM Boot sectors cleaned : 0
  12/8/2015 2:30:46PM Files scanned : 55
  12/8/2015 2:30:46PM Files with detections: 0
  12/8/2015 2:30:46PM File detections : 0
  12/8/2015 2:30:46PM Files cleaned : 0
  12/8/2015 2:30:46PM Files deleted : 0
  12/8/2015 2:30:46PM Files not scanned : 0
  12/8/2015 2:30:46PM Scan Summary (Registry Scanning)
  12/8/2015 2:30:46PM Keys scanned : 0
  12/8/2015 2:30:46PM Keys detected : 0
  12/8/2015 2:30:46PM Keys cleaned : 0
  12/8/2015 2:30:46PM Keys deleted : 0
  12/8/2015 2:30:46PM Run time : 0:00:10
  12/8/2015 2:30:46PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 19148:HEAD Source
------------------------------------------------------------------------  r19150 | yzhu52 | 2015-12-07 19:06:41 -0800 (Mon, 07 Dec 2015) | 4 lines
  Revert the change in r19143 for BUILDRULEORDER.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>

------------------------------------------------------------------------