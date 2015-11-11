Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18768

This directory contains the Win32 binaries.

Build Date:       Wed, 11 Nov 2015 14:27:49 Pacific Standard Time
Last Changed Rev: 18767

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18759
  BootSectImage Version 0.1 Build 18600
  Ecc.exe Version 0.01 Build 18595
  EfiLdrImage Version 0.1 Build 18600
  EfiRom Version 0.1 Build 18600
  GenBootSector Version 0.2 Build 18600
  GenCrc32 Version 0.2 Build 18600
  GenDepex.exe Version 0.04 Build 18759
  GenFds.exe 1.0 Build 18759
  GenFfs Version 0.1 Build 18600
  GenFv Version 0.1 Build 18600
 *GenFw Version 0.2 Build 18768
  GenPage Version 0.2 Build 18600
  GenPatchPcdTable.exe Version 0.10 Build 18759
  GenSec Version 0.1 Build 18600
  GenVtf Version 0.1 Build 18600
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 18600
  LzmaF86Compress Version 0.2 Build 18600
  PatchPcdValue.exe Version 0.10 Build 18759
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 18686
  TargetTool.exe Version 0.01 Build 18759
  TianoCompress Version 0.1 Build 18600
  Trim.exe Version 0.10 Build 18759
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 18600
  VfrCompile version  2.00 (UEFI 2.4) Build 18607
  VolInfo Version 0.83 Build 18600, Oct 10 2015
  build.exe Version 0.60 Build 18759

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/11/2015 2:27:51PM Engine version = 5700.7163
  11/11/2015 2:27:51PM AntiVirus DAT version = 7981.0
  11/11/2015 2:27:51PM Number of detection signatures in EXTRA.DAT = 1
  11/11/2015 2:27:51PM Names of detection signatures in EXTRA.DAT = Generic BackDoor.u (ED)
  11/11/2015 2:27:51PM Scan Started On-Demand Scan
  11/11/2015 2:27:54PM Scan Summary
  11/11/2015 2:27:54PM Processes scanned : 0
  11/11/2015 2:27:54PM Processes detected : 0
  11/11/2015 2:27:54PM Processes cleaned : 0
  11/11/2015 2:27:54PM Boot sectors scanned : 2
  11/11/2015 2:27:54PM Boot sectors detected: 0
  11/11/2015 2:27:54PM Boot sectors cleaned : 0
  11/11/2015 2:27:54PM Files scanned : 55
  11/11/2015 2:27:54PM Files with detections: 0
  11/11/2015 2:27:54PM File detections : 0
  11/11/2015 2:27:54PM Files cleaned : 0
  11/11/2015 2:27:54PM Files deleted : 0
  11/11/2015 2:27:54PM Files not scanned : 0
  11/11/2015 2:27:54PM Scan Summary (Registry Scanning)
  11/11/2015 2:27:54PM Keys scanned : 0
  11/11/2015 2:27:54PM Keys detected : 0
  11/11/2015 2:27:54PM Keys cleaned : 0
  11/11/2015 2:27:54PM Keys deleted : 0
  11/11/2015 2:27:54PM Run time : 0:00:03
  11/11/2015 2:27:54PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18759:HEAD Source
------------------------------------------------------------------------  r18767 | yzhu52 | 2015-11-10 22:30:42 -0800 (Tue, 10 Nov 2015) | 9 lines
  BaseTools/GenFw: add new option to not zero PE/COFF optional header fields
  Add new option --keepoptionalheader and that flag does not zero PE/COFF
  optional header fields including the version fields. It can support the
  case that the PE/COFF optional header would be kept.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------