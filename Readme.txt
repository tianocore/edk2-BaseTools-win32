Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17353

This directory contains the Win32 binaries.

Build Date:       Thu, 07 May 2015 03:07:10 Pacific Daylight Time
Last Changed Rev: 17346

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17164
 *BootSectImage Version 0.1 Build 17353
  Ecc.exe Version 0.01 Build 17164
 *EfiLdrImage Version 0.1 Build 17353
 *EfiRom Version 0.1 Build 17353
 *GenBootSector Version 0.2 Build 17353
 *GenCrc32 Version 0.2 Build 17353
  GenDepex.exe Version 0.04 Build 17164
  GenFds.exe 1.0 Build 17164
 *GenFfs Version 0.1 Build 17353
 *GenFv Version 0.1 Build 17353
 *GenFw Version 0.2 Build 17353
 *GenPage Version 0.2 Build 17353
  GenPatchPcdTable.exe Version 0.10 Build 17164
 *GenSec Version 0.1 Build 17353
 *GenVtf Version 0.1 Build 17353
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 17353
  LzmaF86Compress Version 0.2 Build 17353
  PatchPcdValue.exe Version 0.10 Build 17164
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17164
  Rsa2048Sha256Sign Version 0.9 Build 17164
 *Split Version 0.1 Build 17353
  TargetTool.exe Version 0.01 Build 17164
 *TianoCompress Version 0.1 Build 17353
  Trim.exe Version 0.10 Build 17164
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 17164
 *VfrCompile version  2.00 (UEFI 2.4) Build 17353
 *VolInfo Version 0.83 Build 17353, May  7 2015
  build.exe Version 0.60 Build 17164

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1263
  5/7/2015 3:07:12AM Engine version = 5700.7163
  5/7/2015 3:07:12AM AntiVirus DAT version = 7793.0
  5/7/2015 3:07:12AM Number of detection signatures in EXTRA.DAT = None
  5/7/2015 3:07:12AM Names of detection signatures in EXTRA.DAT = None
  5/7/2015 3:07:13AM Scan Started On-Demand Scan
  5/7/2015 3:07:55AM Scan Summary
  5/7/2015 3:07:55AM Processes scanned : 0
  5/7/2015 3:07:55AM Processes detected : 0
  5/7/2015 3:07:55AM Processes cleaned : 0
  5/7/2015 3:07:55AM Boot sectors scanned : 1
  5/7/2015 3:07:55AM Boot sectors detected: 0
  5/7/2015 3:07:55AM Boot sectors cleaned : 0
  5/7/2015 3:07:55AM Files scanned : 66
  5/7/2015 3:07:55AM Files with detections: 0
  5/7/2015 3:07:55AM File detections : 0
  5/7/2015 3:07:55AM Files cleaned : 0
  5/7/2015 3:07:55AM Files deleted : 0
  5/7/2015 3:07:55AM Files not scanned : 0
  5/7/2015 3:07:55AM Scan Summary (Registry Scanning)
  5/7/2015 3:07:55AM Keys scanned : 0
  5/7/2015 3:07:55AM Keys detected : 0
  5/7/2015 3:07:55AM Keys cleaned : 0
  5/7/2015 3:07:55AM Keys deleted : 0
  5/7/2015 3:07:55AM Run time : 0:00:42
  5/7/2015 3:07:55AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17336:HEAD Source
------------------------------------------------------------------------  r17338 | ydong10 | 2015-05-06 03:38:04 -0700 (Wed, 06 May 2015) | 6 lines
  BaseTools: Enable Match2 Opcode.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Eric Dong <eric.dong@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Samer El-Haj-Mahmoud <samer.el-haj-mahmoud@hp.com>

------------------------------------------------------------------------  r17344 | ydong10 | 2015-05-06 05:29:33 -0700 (Wed, 06 May 2015) | 6 lines
  BaseTools: Enhance the check for numeric opcode with EFI_IFR_DISPLAY_INT_DEC attribute.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Eric Dong <eric.dong@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Aaron Pop <Aaron.Pop@congatec.com>

------------------------------------------------------------------------  r17346 | ydong10 | 2015-05-06 05:52:16 -0700 (Wed, 06 May 2015) | 5 lines
  BaseTools: Fix build fail issue.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Eric Dong <eric.dong@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------