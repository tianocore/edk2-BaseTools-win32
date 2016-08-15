Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22370

This directory contains the Win32 binaries.

Build Date:       Mon, 15 Aug 2016 03:11:11 Pacific Daylight Time
Last Changed Rev: 22368

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22308
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
  GenDepex.exe Version 0.04 Build 22308
  GenFds.exe 1.0 Build 22308
  GenFfs Version 0.1 Build 20909
 *GenFv Version 0.1 Build 22370
  GenFw Version 0.2 Build 22308
  GenPage Version 0.2 Build 20909
  GenPatchPcdTable.exe Version 0.10 Build 22308
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
  PatchPcdValue.exe Version 0.10 Build 22308
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
  TargetTool.exe Version 0.01 Build 22308
  TianoCompress Version 0.1 Build 20909
  Trim.exe Version 0.10 Build 22308
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22316
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22367
  VolInfo Version 1.0 Build Build 20909
  build.exe Version 0.60 Build 22308

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/15/2016 3:11:12AM Engine version = 5700.7163
  8/15/2016 3:11:12AM AntiVirus DAT version = 8257.0
  8/15/2016 3:11:12AM Number of detection signatures in EXTRA.DAT = None
  8/15/2016 3:11:12AM Names of detection signatures in EXTRA.DAT = None
  8/15/2016 3:11:12AM Scan Started On-Demand Scan
  8/15/2016 3:11:19AM Scan Summary
  8/15/2016 3:11:19AM Processes scanned : 0
  8/15/2016 3:11:19AM Processes detected : 0
  8/15/2016 3:11:19AM Processes cleaned : 0
  8/15/2016 3:11:19AM Boot sectors scanned : 2
  8/15/2016 3:11:19AM Boot sectors detected: 0
  8/15/2016 3:11:19AM Boot sectors cleaned : 0
  8/15/2016 3:11:19AM Files scanned : 55
  8/15/2016 3:11:19AM Files with detections: 0
  8/15/2016 3:11:19AM File detections : 0
  8/15/2016 3:11:19AM Files cleaned : 0
  8/15/2016 3:11:19AM Files deleted : 0
  8/15/2016 3:11:19AM Files not scanned : 0
  8/15/2016 3:11:19AM Scan Summary (Registry Scanning)
  8/15/2016 3:11:19AM Keys scanned : 0
  8/15/2016 3:11:19AM Keys detected : 0
  8/15/2016 3:11:19AM Keys cleaned : 0
  8/15/2016 3:11:19AM Keys deleted : 0
  8/15/2016 3:11:19AM Run time : 0:00:07
  8/15/2016 3:11:19AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22367:HEAD Source
------------------------------------------------------------------------  r22368 | edk2buildsystem | 2016-08-14 14:05:42 -0700 (Sun, 14 Aug 2016) | 14 lines
  BaseTools/GenFv: Account for rebase of FV section containing VTF file
  Account for rebase of FV section containing VTF file on IA32/IA64.
  This supports cases where the reset vector may not be set at 0xFFFFFFF0.
  For example, FV section defined as:
  [FV.FvSecPei]
  FvBaseAddress = $(FV_BOOT_BASE)
  FvForceRebase = TRUE
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Leo Duran <leo.duran@amd.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit adb6ac256338329883e4d8fafaa8c753dba707c9)

------------------------------------------------------------------------