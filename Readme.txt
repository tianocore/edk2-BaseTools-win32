Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 16400

This directory contains the Win32 binaries.

Build Date:       Tue, 18 Nov 2014 03:07:28 Pacific Standard Time
Last Changed Rev: 16400

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 16400
  BootSectImage Version 0.1 Build 16164
  EfiLdrImage Version 0.1 Build 16164
  EfiRom Version 0.1 Build 16164
  GenBootSector Version 0.2 Build 16164
  GenCrc32 Version 0.2 Build 16164
 *GenDepex.exe Version 0.04 Build 16400
 *GenFds.exe 1.0 Build 16400
  GenFfs Version 0.1 Build 16164
  GenFv Version 0.1 Build 16164
  GenFw Version 0.2 Build 16304
  GenPage Version 0.2 Build 16164
 *GenPatchPcdTable.exe Version 0.10 Build 16400
  GenSec Version 0.1 Build 16164
  GenVtf Version 0.1 Build 16164
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 16164
  LzmaF86Compress Version 0.2 Build 16164
 *PatchPcdValue.exe Version 0.10 Build 16400
  Rsa2048Sha256GenerateKeys Version 0.9 Build 16164
  Rsa2048Sha256Sign Version 0.9 Build 16164
  Split Version 0.1 Build 16164
 *TargetTool.exe Version 0.01 Build 16400
  TianoCompress Version 0.1 Build 16164
 *Trim.exe Version 0.10 Build 16400
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 16229
  VfrCompile version  2.00 (UEFI 2.4) Build 16164
  VolInfo Version 0.83 Build 16164, Sep 24 2014
 *build.exe Version 0.60 Build 16400

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1247
  11/18/2014 3:07:30AM Engine version = 5600.1067
  11/18/2014 3:07:30AM AntiVirus DAT version = 7624.0
  11/18/2014 3:07:30AM Number of detection signatures in EXTRA.DAT = None
  11/18/2014 3:07:30AM Names of detection signatures in EXTRA.DAT = None
  11/18/2014 3:07:30AM Scan Started On-Demand Scan
  11/18/2014 3:07:37AM Scan Summary
  11/18/2014 3:07:37AM Processes scanned : 0
  11/18/2014 3:07:37AM Processes detected : 0
  11/18/2014 3:07:37AM Processes cleaned : 0
  11/18/2014 3:07:37AM Boot sectors scanned : 1
  11/18/2014 3:07:37AM Boot sectors detected: 0
  11/18/2014 3:07:37AM Boot sectors cleaned : 0
  11/18/2014 3:07:37AM Files scanned : 53
  11/18/2014 3:07:37AM Files with detections: 0
  11/18/2014 3:07:37AM File detections : 0
  11/18/2014 3:07:37AM Files cleaned : 0
  11/18/2014 3:07:37AM Files deleted : 0
  11/18/2014 3:07:37AM Files not scanned : 0
  11/18/2014 3:07:37AM Scan Summary (Registry Scanning)
  11/18/2014 3:07:37AM Keys scanned : 0
  11/18/2014 3:07:37AM Keys detected : 0
  11/18/2014 3:07:37AM Keys cleaned : 0
  11/18/2014 3:07:37AM Keys deleted : 0
  11/18/2014 3:07:37AM Run time : 0:00:07
  11/18/2014 3:07:37AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 16340:HEAD Source
------------------------------------------------------------------------  r16400 | lgao4 | 2014-11-17 18:38:20 -0800 (Mon, 17 Nov 2014) | 25 lines
  BaseTools: Modify gcc 4.8 and 4.9 tool chain definition to support building from Windows.
  Here is a new patch that adds Windows support for both gcc 4.8.x and gcc 4.9.x.
  This time testing is more thorough: boot testing using Duet for all 4 combinations of
  IA32/X64 and gcc 4.8.2 and gcc 4.9.1 passes. A Windows hosted gcc 4.8.2 has been added here:
  http://sourceforge.net/projects/edk2developertoolsforwindows/
  The environment variable settings for Windows look like:
  set UEFI_BUILD_TOOLS=%cd%\tools
  set NASM_PREFIX=%UEFI_BUILD_TOOLS%\nasm211\
  set GCC48_BIN=%UEFI_BUILD_TOOLS%\gcc482-x86\bin\
  set GCC48_DLL=%UEFI_BUILD_TOOLS%\gcc482-x86\dll\;%GCC48_BIN%
  set GCC48_ARM_PREFIX=%UEFI_BUILD_TOOLS%\gcc482-arm\bin\
  set GCC48_AARCH64_PREFIX=%UEFI_BUILD_TOOLS%\gcc482-aarch64\bin\
  set GCC49_BIN=%UEFI_BUILD_TOOLS%\gcc491-x86\bin\
  set GCC49_DLL=%UEFI_BUILD_TOOLS%\gcc491-x86\dll\;%GCC49_BIN%
  set GCC49_ARM_PREFIX=%UEFI_BUILD_TOOLS%\gcc491-arm\bin\
  set GCC49_AARCH64_PREFIX=%UEFI_BUILD_TOOLS%\gcc491-aarch64\bin\
  No change is needed for building from Linux.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Scott Duplichan <scott@notabs.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------