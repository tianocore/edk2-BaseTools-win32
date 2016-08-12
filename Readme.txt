Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22367

This directory contains the Win32 binaries.

Build Date:       Fri, 12 Aug 2016 03:11:17 Pacific Daylight Time
Last Changed Rev: 22360

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
  GenFv Version 0.1 Build 20909
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
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 22367
  VolInfo Version 1.0 Build Build 20909
  build.exe Version 0.60 Build 22308

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/12/2016 3:11:18AM Engine version = 5700.7163
  8/12/2016 3:11:18AM AntiVirus DAT version = 8254.0
  8/12/2016 3:11:18AM Number of detection signatures in EXTRA.DAT = None
  8/12/2016 3:11:18AM Names of detection signatures in EXTRA.DAT = None
  8/12/2016 3:11:18AM Scan Started On-Demand Scan
  8/12/2016 3:11:21AM Scan Summary
  8/12/2016 3:11:21AM Processes scanned : 0
  8/12/2016 3:11:21AM Processes detected : 0
  8/12/2016 3:11:21AM Processes cleaned : 0
  8/12/2016 3:11:21AM Boot sectors scanned : 1
  8/12/2016 3:11:21AM Boot sectors detected: 0
  8/12/2016 3:11:21AM Boot sectors cleaned : 0
  8/12/2016 3:11:21AM Files scanned : 55
  8/12/2016 3:11:21AM Files with detections: 0
  8/12/2016 3:11:21AM File detections : 0
  8/12/2016 3:11:21AM Files cleaned : 0
  8/12/2016 3:11:21AM Files deleted : 0
  8/12/2016 3:11:21AM Files not scanned : 0
  8/12/2016 3:11:21AM Scan Summary (Registry Scanning)
  8/12/2016 3:11:21AM Keys scanned : 0
  8/12/2016 3:11:21AM Keys detected : 0
  8/12/2016 3:11:21AM Keys cleaned : 0
  8/12/2016 3:11:21AM Keys deleted : 0
  8/12/2016 3:11:21AM Run time : 0:00:03
  8/12/2016 3:11:21AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22316:HEAD Source
------------------------------------------------------------------------  r22360 | edk2buildsystem | 2016-08-12 02:05:49 -0700 (Fri, 12 Aug 2016) | 11 lines
  BaseTool/VfrCompile: Remove reset button opcode in CheckQuestionOpCode
  "EFI_IFR_RESET_BUTTON_OP" is a statement, not a question,
  so remove it from function CheckQuestionOpCode.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Eric Dong <eric.dong@intel.com>
  (cherry picked from commit 753cf34e29c52bb45d25eb0580e04145f19cd83d)

------------------------------------------------------------------------