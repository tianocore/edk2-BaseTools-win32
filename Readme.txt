Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 20165, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 19610

This directory contains the Win32 binaries.

Build Date:       Wed, 06 Jan 2016 14:28:56 Pacific Standard Time
Last Changed Rev: 19604

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
 *GenBootSector Version 0.2 Build 19610
  GenCrc32 Version 0.2 Build 19148
  GenDepex.exe Version 0.04 Build 19174
  GenFds.exe 1.0 Build 19333
  GenFfs Version 0.1 Build 19148
 *GenFv Version 0.1 Build 19610
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
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 19580
  VfrCompile version  2.00 (UEFI 2.4) Build 19148
  VolInfo Version 0.83 Build 19148, Dec  7 2015
  build.exe Version 0.60 Build 19174

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/6/2016 2:28:58PM Engine version = 5700.7163
  1/6/2016 2:28:58PM AntiVirus DAT version = 8035.0
  1/6/2016 2:28:58PM Number of detection signatures in EXTRA.DAT = None
  1/6/2016 2:28:58PM Names of detection signatures in EXTRA.DAT = None
  1/6/2016 2:28:58PM Scan Started On-Demand Scan
  1/6/2016 2:29:08PM Scan Summary
  1/6/2016 2:29:08PM Processes scanned : 0
  1/6/2016 2:29:08PM Processes detected : 0
  1/6/2016 2:29:08PM Processes cleaned : 0
  1/6/2016 2:29:08PM Boot sectors scanned : 2
  1/6/2016 2:29:08PM Boot sectors detected: 0
  1/6/2016 2:29:08PM Boot sectors cleaned : 0
  1/6/2016 2:29:08PM Files scanned : 56
  1/6/2016 2:29:08PM Files with detections: 0
  1/6/2016 2:29:08PM File detections : 0
  1/6/2016 2:29:08PM Files cleaned : 0
  1/6/2016 2:29:08PM Files deleted : 0
  1/6/2016 2:29:08PM Files not scanned : 0
  1/6/2016 2:29:08PM Scan Summary (Registry Scanning)
  1/6/2016 2:29:08PM Keys scanned : 0
  1/6/2016 2:29:08PM Keys detected : 0
  1/6/2016 2:29:08PM Keys cleaned : 0
  1/6/2016 2:29:08PM Keys deleted : 0
  1/6/2016 2:29:08PM Run time : 0:00:10
  1/6/2016 2:29:08PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 19580:HEAD Source
------------------------------------------------------------------------  r19604 | hwu1225 | 2016-01-05 17:13:35 -0800 (Tue, 05 Jan 2016) | 5 lines
  BaseTools: Fix 'caculate' typos
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------