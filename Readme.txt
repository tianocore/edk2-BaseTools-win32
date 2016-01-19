Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 20165, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 19691

This directory contains the Win32 binaries.

Build Date:       Tue, 19 Jan 2016 14:35:39 Pacific Standard Time
Last Changed Rev: 19686

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 19691
  BootSectImage Version 0.1 Build 19148
  Ecc.exe Version 0.01 Build 18595
  EfiLdrImage Version 0.1 Build 19148
  EfiRom Version 0.1 Build 19148
  GenBootSector Version 0.2 Build 19610
  GenCrc32 Version 0.2 Build 19148
 *GenDepex.exe Version 0.04 Build 19691
 *GenFds.exe 1.0 Build 19691
  GenFfs Version 0.1 Build 19148
  GenFv Version 0.1 Build 19610
  GenFw Version 0.2 Build 19244
  GenPage Version 0.2 Build 19148
 *GenPatchPcdTable.exe Version 0.10 Build 19691
  GenSec Version 0.1 Build 19148
  GenVtf Version 0.1 Build 19148
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 19148
  LzmaF86Compress Version 0.2 Build 19148
 *PatchPcdValue.exe Version 0.10 Build 19691
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 19148
 *TargetTool.exe Version 0.01 Build 19691
  TianoCompress Version 0.1 Build 19148
 *Trim.exe Version 0.10 Build 19691
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 19580
  VfrCompile version  2.00 (UEFI 2.4) Build 19148
  VolInfo Version 0.83 Build 19148, Dec  7 2015
 *build.exe Version 0.60 Build 19691

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/19/2016 2:35:40PM Engine version = 5700.7163
  1/19/2016 2:35:40PM AntiVirus DAT version = 8048.0
  1/19/2016 2:35:40PM Number of detection signatures in EXTRA.DAT = None
  1/19/2016 2:35:40PM Names of detection signatures in EXTRA.DAT = None
  1/19/2016 2:35:40PM Scan Started On-Demand Scan
  1/19/2016 2:35:50PM Scan Summary
  1/19/2016 2:35:50PM Processes scanned : 0
  1/19/2016 2:35:50PM Processes detected : 0
  1/19/2016 2:35:50PM Processes cleaned : 0
  1/19/2016 2:35:50PM Boot sectors scanned : 2
  1/19/2016 2:35:50PM Boot sectors detected: 0
  1/19/2016 2:35:50PM Boot sectors cleaned : 0
  1/19/2016 2:35:50PM Files scanned : 55
  1/19/2016 2:35:50PM Files with detections: 0
  1/19/2016 2:35:50PM File detections : 0
  1/19/2016 2:35:50PM Files cleaned : 0
  1/19/2016 2:35:50PM Files deleted : 0
  1/19/2016 2:35:50PM Files not scanned : 0
  1/19/2016 2:35:50PM Scan Summary (Registry Scanning)
  1/19/2016 2:35:50PM Keys scanned : 0
  1/19/2016 2:35:50PM Keys detected : 0
  1/19/2016 2:35:50PM Keys cleaned : 0
  1/19/2016 2:35:50PM Keys deleted : 0
  1/19/2016 2:35:50PM Run time : 0:00:10
  1/19/2016 2:35:50PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 19661:HEAD Source
------------------------------------------------------------------------  r19686 | yzhu52 | 2016-01-19 04:58:52 -0800 (Tue, 19 Jan 2016) | 10 lines
  BaseTools: process the files by the priority in BUILDRULEORDER
  By the BUILDRULEORDER feature to process files listed in INF [Sources]
  sections in priority order, if a filename is listed with multiple
  extensions, the tools will use only the file that matches the first
  extension in the space separated list.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------