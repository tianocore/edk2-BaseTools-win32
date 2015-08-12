Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18212

This directory contains the Win32 binaries.

Build Date:       Wed, 12 Aug 2015 03:17:59 Pacific Daylight Time
Last Changed Rev: 18206

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18094
  BootSectImage Version 0.1 Build 18094
  Ecc.exe Version 0.01 Build 17712
  EfiLdrImage Version 0.1 Build 18094
  EfiRom Version 0.1 Build 18094
  GenBootSector Version 0.2 Build 18094
  GenCrc32 Version 0.2 Build 18094
  GenDepex.exe Version 0.04 Build 18094
 *GenFds.exe 1.0 Build 18212
  GenFfs Version 0.1 Build 18094
  GenFv Version 0.1 Build 18094
  GenFw Version 0.2 Build 18198
  GenPage Version 0.2 Build 18094
  GenPatchPcdTable.exe Version 0.10 Build 18094
  GenSec Version 0.1 Build 18094
  GenVtf Version 0.1 Build 18094
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 18094
  LzmaF86Compress Version 0.2 Build 18094
  PatchPcdValue.exe Version 0.10 Build 18094
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 18094
  TargetTool.exe Version 0.01 Build 18094
  TianoCompress Version 0.1 Build 18094
  Trim.exe Version 0.10 Build 18182
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17927
  VfrCompile version  2.00 (UEFI 2.4) Build 18094
  VolInfo Version 0.83 Build 18094, Jul 28 2015
  build.exe Version 0.60 Build 18094

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/12/2015 3:18:00AM Engine version = 5700.7163
  8/12/2015 3:18:00AM AntiVirus DAT version = 7889.0
  8/12/2015 3:18:00AM Number of detection signatures in EXTRA.DAT = None
  8/12/2015 3:18:00AM Names of detection signatures in EXTRA.DAT = None
  8/12/2015 3:18:01AM Scan Started On-Demand Scan
  8/12/2015 3:18:03AM Scan Summary
  8/12/2015 3:18:03AM Processes scanned : 0
  8/12/2015 3:18:03AM Processes detected : 0
  8/12/2015 3:18:03AM Processes cleaned : 0
  8/12/2015 3:18:03AM Boot sectors scanned : 1
  8/12/2015 3:18:03AM Boot sectors detected: 0
  8/12/2015 3:18:03AM Boot sectors cleaned : 0
  8/12/2015 3:18:03AM Files scanned : 55
  8/12/2015 3:18:03AM Files with detections: 0
  8/12/2015 3:18:03AM File detections : 0
  8/12/2015 3:18:03AM Files cleaned : 0
  8/12/2015 3:18:03AM Files deleted : 0
  8/12/2015 3:18:03AM Files not scanned : 0
  8/12/2015 3:18:03AM Scan Summary (Registry Scanning)
  8/12/2015 3:18:03AM Keys scanned : 0
  8/12/2015 3:18:03AM Keys detected : 0
  8/12/2015 3:18:03AM Keys cleaned : 0
  8/12/2015 3:18:03AM Keys deleted : 0
  8/12/2015 3:18:03AM Run time : 0:00:03
  8/12/2015 3:18:03AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18198:HEAD Source
------------------------------------------------------------------------  r18205 | shenshushi | 2015-08-11 18:27:31 -0700 (Tue, 11 Aug 2015) | 25 lines
  BaseTools/GenFds: Fix 'NoneType' object is not iterable error.
  When adding section VERSION in FDF file, for example:
  FILE FREEFORM = PCD(gEfiIntelFrameworkModulePkgTokenSpaceGuid.PcdLogoFile) {
  SECTION RAW = MdeModulePkg/Logo/Logo.bmp
  SECTION UI = "Logo"
  SECTION VERSION = "0001"
  }
  GenFds will report the following error:
  Traceback (most recent call last):
  File "GenFds.py", line 276, in main
  File "GenFds.py", line 391, in GenFd
  File "Fd.py", line 93, in GenFd
  File "Region.py", line 106, in AddToBuffer
  File "Fv.py", line 114, in AddToBuffer
  File "FfsFileStatement.py", line 117, in GenFfs
  File "VerSection.py", line 80, in GenSection
  File "GenFdsGlobalVariable.py", line 401, in GenerateSection
  TypeError: 'NoneType' object is not iterable.
  We found in GenFdsGlobalVariable.py line 401 'list' requires a iteralbe object as parameter while the 'Input' is None.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Qiu Shumin <shumin.qiu@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r18206 | abiesheuvel | 2015-08-11 22:22:49 -0700 (Tue, 11 Aug 2015) | 9 lines
  BaseTools: add ARCH detection for AARCH64 and ARM
  Add auto detection for the ARCH variable for AARCH64 and ARM
  systems. This allows us to do a native build of the BaseTools
  without the need to set ARCH externally.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------