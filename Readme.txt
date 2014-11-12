Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 16340

This directory contains the Win32 binaries.

Build Date:       Wed, 12 Nov 2014 03:07:00 Pacific Standard Time
Last Changed Rev: 16338

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 16330
  BootSectImage Version 0.1 Build 16164
  EfiLdrImage Version 0.1 Build 16164
  EfiRom Version 0.1 Build 16164
  GenBootSector Version 0.2 Build 16164
  GenCrc32 Version 0.2 Build 16164
  GenDepex.exe Version 0.04 Build 16330
  GenFds.exe 1.0 Build 16330
  GenFfs Version 0.1 Build 16164
  GenFv Version 0.1 Build 16164
  GenFw Version 0.2 Build 16304
  GenPage Version 0.2 Build 16164
  GenPatchPcdTable.exe Version 0.10 Build 16330
  GenSec Version 0.1 Build 16164
  GenVtf Version 0.1 Build 16164
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 16164
  LzmaF86Compress Version 0.2 Build 16164
  PatchPcdValue.exe Version 0.10 Build 16330
  Rsa2048Sha256GenerateKeys Version 0.9 Build 16164
  Rsa2048Sha256Sign Version 0.9 Build 16164
  Split Version 0.1 Build 16164
  TargetTool.exe Version 0.01 Build 16330
  TianoCompress Version 0.1 Build 16164
  Trim.exe Version 0.10 Build 16330
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 16229
  VfrCompile version  2.00 (UEFI 2.4) Build 16164
  VolInfo Version 0.83 Build 16164, Sep 24 2014
 *build.exe Version 0.60 Build 16340

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1247
  11/12/2014 3:07:03AM Engine version = 5600.1067
  11/12/2014 3:07:03AM AntiVirus DAT version = 7619.0
  11/12/2014 3:07:03AM Number of detection signatures in EXTRA.DAT = None
  11/12/2014 3:07:03AM Names of detection signatures in EXTRA.DAT = None
  11/12/2014 3:07:03AM Scan Started On-Demand Scan
  11/12/2014 3:07:09AM Scan Summary
  11/12/2014 3:07:09AM Processes scanned : 0
  11/12/2014 3:07:09AM Processes detected : 0
  11/12/2014 3:07:09AM Processes cleaned : 0
  11/12/2014 3:07:09AM Boot sectors scanned : 1
  11/12/2014 3:07:09AM Boot sectors detected: 0
  11/12/2014 3:07:09AM Boot sectors cleaned : 0
  11/12/2014 3:07:09AM Files scanned : 53
  11/12/2014 3:07:09AM Files with detections: 0
  11/12/2014 3:07:09AM File detections : 0
  11/12/2014 3:07:09AM Files cleaned : 0
  11/12/2014 3:07:09AM Files deleted : 0
  11/12/2014 3:07:09AM Files not scanned : 0
  11/12/2014 3:07:09AM Scan Summary (Registry Scanning)
  11/12/2014 3:07:09AM Keys scanned : 0
  11/12/2014 3:07:09AM Keys detected : 0
  11/12/2014 3:07:09AM Keys cleaned : 0
  11/12/2014 3:07:09AM Keys deleted : 0
  11/12/2014 3:07:09AM Run time : 0:00:06
  11/12/2014 3:07:09AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 16330:HEAD Source
------------------------------------------------------------------------  r16330 | yingke | 2014-11-10 23:33:50 -0800 (Mon, 10 Nov 2014) | 5 lines
  BaseTool: Support EDKII style GUID definition for VFR function.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r16338 | yingke | 2014-11-12 00:26:03 -0800 (Wed, 12 Nov 2014) | 5 lines
  BaseTools: Fix a cleanall issue.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------