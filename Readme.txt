Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18673

This directory contains the Win32 binaries.

Build Date:       Mon, 26 Oct 2015 14:26:20 Pacific Daylight Time
Last Changed Rev: 18663

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18673
  BootSectImage Version 0.1 Build 18600
  Ecc.exe Version 0.01 Build 18595
  EfiLdrImage Version 0.1 Build 18600
  EfiRom Version 0.1 Build 18600
  GenBootSector Version 0.2 Build 18600
  GenCrc32 Version 0.2 Build 18600
 *GenDepex.exe Version 0.04 Build 18673
 *GenFds.exe 1.0 Build 18673
  GenFfs Version 0.1 Build 18600
  GenFv Version 0.1 Build 18600
  GenFw Version 0.2 Build 18600
  GenPage Version 0.2 Build 18600
 *GenPatchPcdTable.exe Version 0.10 Build 18673
  GenSec Version 0.1 Build 18600
  GenVtf Version 0.1 Build 18600
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 18600
  LzmaF86Compress Version 0.2 Build 18600
 *PatchPcdValue.exe Version 0.10 Build 18673
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 18600
 *TargetTool.exe Version 0.01 Build 18673
  TianoCompress Version 0.1 Build 18600
 *Trim.exe Version 0.10 Build 18673
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 18600
  VfrCompile version  2.00 (UEFI 2.4) Build 18607
  VolInfo Version 0.83 Build 18600, Oct 10 2015
 *build.exe Version 0.60 Build 18673

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/26/2015 2:26:21PM Engine version = 5700.7163
  10/26/2015 2:26:21PM AntiVirus DAT version = 7965.0
  10/26/2015 2:26:21PM Number of detection signatures in EXTRA.DAT = 1
  10/26/2015 2:26:21PM Names of detection signatures in EXTRA.DAT = Generic PWS.o (ED)
  10/26/2015 2:26:21PM Scan Started On-Demand Scan
  10/26/2015 2:26:51PM Scan Summary
  10/26/2015 2:26:51PM Processes scanned : 0
  10/26/2015 2:26:51PM Processes detected : 0
  10/26/2015 2:26:51PM Processes cleaned : 0
  10/26/2015 2:26:51PM Boot sectors scanned : 2
  10/26/2015 2:26:51PM Boot sectors detected: 0
  10/26/2015 2:26:51PM Boot sectors cleaned : 0
  10/26/2015 2:26:51PM Files scanned : 55
  10/26/2015 2:26:51PM Files with detections: 0
  10/26/2015 2:26:51PM File detections : 0
  10/26/2015 2:26:51PM Files cleaned : 0
  10/26/2015 2:26:51PM Files deleted : 0
  10/26/2015 2:26:51PM Files not scanned : 0
  10/26/2015 2:26:51PM Scan Summary (Registry Scanning)
  10/26/2015 2:26:51PM Keys scanned : 0
  10/26/2015 2:26:51PM Keys detected : 0
  10/26/2015 2:26:51PM Keys cleaned : 0
  10/26/2015 2:26:51PM Keys deleted : 0
  10/26/2015 2:26:51PM Run time : 0:00:30
  10/26/2015 2:26:51PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18607:HEAD Source
------------------------------------------------------------------------  r18661 | yzhu52 | 2015-10-25 20:26:55 -0700 (Sun, 25 Oct 2015) | 9 lines
  BaseTools:added extern protocol/PPI/GUID definition in AutoGen for Library
  We already added the extern declaration for protocols/PPI/GUID in AutoGen.h
  file for driver, but missing this feature for the Library. so this patch
  add it.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r18663 | lgao4 | 2015-10-26 01:48:39 -0700 (Mon, 26 Oct 2015) | 8 lines
  BaseTools: Add MultipleWorkspace.py in the common dependency.
  Add new added MultipleWorkspace.py in the common dependency to freeze
  python tools for Windows.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>

------------------------------------------------------------------------