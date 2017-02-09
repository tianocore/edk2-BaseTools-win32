Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23852

This directory contains the Win32 binaries.

Build Date:       Wed, 08 Feb 2017 19:09:42 Pacific Standard Time
Last Changed Rev: 23844

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23852
  BootSectImage Version 1.0 Build Build 23431
  Ecc.exe Version 1.0 Build Build 23673
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 23852
 *GenFds.exe 1.0 Build 23852
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 23431
  GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 23852
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 23431
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 23852
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 23852
  TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 23852
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23818
  VolInfo Version 1.0 Build Build 23468
 *build.exe Version 0.60 Build 23852

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/8/2017 7:09:43PM Engine version = 5700.7163
  2/8/2017 7:09:43PM AntiVirus DAT version = 8433.0
  2/8/2017 7:09:43PM Number of detection signatures in EXTRA.DAT = None
  2/8/2017 7:09:43PM Names of detection signatures in EXTRA.DAT = None
  2/8/2017 7:09:43PM Scan Started On-Demand Scan
  2/8/2017 7:09:53PM Scan Summary
  2/8/2017 7:09:53PM Processes scanned : 0
  2/8/2017 7:09:53PM Processes detected : 0
  2/8/2017 7:09:53PM Processes cleaned : 0
  2/8/2017 7:09:53PM Boot sectors scanned : 2
  2/8/2017 7:09:53PM Boot sectors detected: 0
  2/8/2017 7:09:53PM Boot sectors cleaned : 0
  2/8/2017 7:09:53PM Files scanned : 62
  2/8/2017 7:09:53PM Files with detections: 0
  2/8/2017 7:09:53PM File detections : 0
  2/8/2017 7:09:53PM Files cleaned : 0
  2/8/2017 7:09:53PM Files deleted : 0
  2/8/2017 7:09:53PM Files not scanned : 0
  2/8/2017 7:09:53PM Scan Summary (Registry Scanning)
  2/8/2017 7:09:53PM Keys scanned : 0
  2/8/2017 7:09:53PM Keys detected : 0
  2/8/2017 7:09:53PM Keys cleaned : 0
  2/8/2017 7:09:53PM Keys deleted : 0
  2/8/2017 7:09:53PM Run time : 0:00:10
  2/8/2017 7:09:53PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23818:HEAD Source
------------------------------------------------------------------------  r23844 | edk2buildsystem | 2017-02-08 19:02:25 -0800 (Wed, 08 Feb 2017) | 11 lines
  BaseTools: Fix the bug to parse the short varname in map file
  current in the map file, there have two ways for var to save its offset,
  if the varname is short, then the offset will in the same line with
  varname, otherwise, it saved in the next line.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d03c056b2946cc2f83b6d206297915dadc08f230)

------------------------------------------------------------------------