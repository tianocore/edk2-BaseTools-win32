Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 16304

This directory contains the Win32 binaries.

Build Date:       Thu, 06 Nov 2014 03:06:35 Pacific Standard Time
Last Changed Rev: 16302

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 16164
  BootSectImage Version 0.1 Build 16164
  EfiLdrImage Version 0.1 Build 16164
  EfiRom Version 0.1 Build 16164
  GenBootSector Version 0.2 Build 16164
  GenCrc32 Version 0.2 Build 16164
  GenDepex.exe Version 0.04 Build 16164
  GenFds.exe 1.0 Build 16164
  GenFfs Version 0.1 Build 16164
  GenFv Version 0.1 Build 16164
 *GenFw Version 0.2 Build 16304
  GenPage Version 0.2 Build 16164
  GenPatchPcdTable.exe Version 0.10 Build 16164
  GenSec Version 0.1 Build 16164
  GenVtf Version 0.1 Build 16164
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 16164
  LzmaF86Compress Version 0.2 Build 16164
  PatchPcdValue.exe Version 0.10 Build 16164
  Rsa2048Sha256GenerateKeys Version 0.9 Build 16164
  Rsa2048Sha256Sign Version 0.9 Build 16164
  Split Version 0.1 Build 16164
  TargetTool.exe Version 0.01 Build 16164
  TianoCompress Version 0.1 Build 16164
  Trim.exe Version 0.10 Build 16164
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 16229
  VfrCompile version  2.00 (UEFI 2.4) Build 16164
  VolInfo Version 0.83 Build 16164, Sep 24 2014
  build.exe Version 0.60 Build 16164

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1247
  11/6/2014 3:06:37AM Engine version = 5600.1067
  11/6/2014 3:06:37AM AntiVirus DAT version = 7613.0
  11/6/2014 3:06:37AM Number of detection signatures in EXTRA.DAT = None
  11/6/2014 3:06:37AM Names of detection signatures in EXTRA.DAT = None
  11/6/2014 3:06:37AM Scan Started On-Demand Scan
  11/6/2014 3:06:55AM Scan Summary
  11/6/2014 3:06:55AM Processes scanned : 0
  11/6/2014 3:06:55AM Processes detected : 0
  11/6/2014 3:06:55AM Processes cleaned : 0
  11/6/2014 3:06:55AM Boot sectors scanned : 2
  11/6/2014 3:06:55AM Boot sectors detected: 0
  11/6/2014 3:06:55AM Boot sectors cleaned : 0
  11/6/2014 3:06:55AM Files scanned : 48
  11/6/2014 3:06:55AM Files with detections: 0
  11/6/2014 3:06:55AM File detections : 0
  11/6/2014 3:06:55AM Files cleaned : 0
  11/6/2014 3:06:55AM Files deleted : 0
  11/6/2014 3:06:55AM Files not scanned : 0
  11/6/2014 3:06:55AM Scan Summary (Registry Scanning)
  11/6/2014 3:06:55AM Keys scanned : 0
  11/6/2014 3:06:55AM Keys detected : 0
  11/6/2014 3:06:55AM Keys cleaned : 0
  11/6/2014 3:06:55AM Keys deleted : 0
  11/6/2014 3:06:55AM Run time : 0:00:18
  11/6/2014 3:06:55AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 16229:HEAD Source
------------------------------------------------------------------------  r16302 | oliviermartin | 2014-11-05 10:56:17 -0800 (Wed, 05 Nov 2014) | 13 lines
  BaseTools/GenFw: Fixed R_AARCH64_CALL26/R_AARCH64_JUMP26 when referring to start of a section
  When R_AARCH64_CALL26/R_AARCH64_JUMP26 relocations referred to static
  functions, they sometime refer to the start of the '.text' section + addend.
  It means the addend is different of '0'.
  The non-patched code (before applying the relocation) already contains
  the correct offset.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Olivier Martin <olivier.martin@arm.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------