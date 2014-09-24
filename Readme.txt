Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 16164

This directory contains the Win32 binaries.

Build Date:       Wed, 24 Sep 2014 00:25:26 Pacific Daylight Time
Last Changed Rev: 16160

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################

** ALL TOOLS WERE REBUILT **
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
  GenFw Version 0.2 Build 16164
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
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 16164
  VfrCompile version  2.00 (UEFI 2.4) Build 16164
  VolInfo Version 0.83 Build 16164, Sep 24 2014
  build.exe Version 0.60 Build 16164

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.975
  9/24/2014 12:25:27AM Engine version = 5400.1158
  9/24/2014 12:25:27AM AntiVirus DAT version = 7570.0
  9/24/2014 12:25:27AM Number of detection signatures in EXTRA.DAT = None
  9/24/2014 12:25:27AM Names of detection signatures in EXTRA.DAT = None
  9/24/2014 12:25:27AM Scan Started On-Demand Scan
  9/24/2014 12:25:34AM Scan Summary
  9/24/2014 12:25:34AM Processes scanned : 0
  9/24/2014 12:25:34AM Processes detected : 0
  9/24/2014 12:25:34AM Processes cleaned : 0
  9/24/2014 12:25:34AM Boot sectors scanned : 2
  9/24/2014 12:25:34AM Boot sectors detected: 0
  9/24/2014 12:25:34AM Boot sectors cleaned : 0
  9/24/2014 12:25:34AM Files scanned : 67
  9/24/2014 12:25:34AM Files with detections: 0
  9/24/2014 12:25:34AM File detections : 0
  9/24/2014 12:25:34AM Files cleaned : 0
  9/24/2014 12:25:34AM Files deleted : 0
  9/24/2014 12:25:34AM Files not scanned : 0
  9/24/2014 12:25:34AM Scan Summary (Registry Scanning)
  9/24/2014 12:25:34AM Keys scanned : 0
  9/24/2014 12:25:34AM Keys detected : 0
  9/24/2014 12:25:34AM Keys cleaned : 0
  9/24/2014 12:25:34AM Keys deleted : 0
  9/24/2014 12:25:34AM Scan Summary (Cookie Scanning)
  9/24/2014 12:25:34AM Cookies scanned : 0
  9/24/2014 12:25:34AM Cookies detected : 0
  9/24/2014 12:25:34AM Cookies cleaned : 0
  9/24/2014 12:25:34AM Cookies deleted : 0
  9/24/2014 12:25:34AM Run time : 0:00:07
  9/24/2014 12:25:34AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 16154:HEAD Source
------------------------------------------------------------------------  r16154 | hchen30 | 2014-09-22 00:37:28 -0700 (Mon, 22 Sep 2014) | 7 lines
  BaseTools/ECC: Ignore duplicate check for 'NULL' library
  Update a checkpoint to ignore duplicate check for 'NULL' library
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@Intel.com>

------------------------------------------------------------------------  r16160 | lgao4 | 2014-09-22 18:32:56 -0700 (Mon, 22 Sep 2014) | 7 lines
  BaseTools: Update nmake Makefile to handle the file path with “:\\”.
  DOS del command doesn’t handle “:\\” in the file path. This patch converts “:\\” to “:\”.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Gao, Liming <liming.gao@intel.com>
  Reviewed-by: lhauch <larry.hauch@intel.com>

------------------------------------------------------------------------
No changes to source files, build was executed for other reasons.
