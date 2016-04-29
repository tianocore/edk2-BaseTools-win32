Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20696

This directory contains the Win32 binaries.

Build Date:       Fri, 29 Apr 2016 03:11:18 Pacific Daylight Time
Last Changed Rev: 20695

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20696
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20696
 *GenFds.exe 1.0 Build 20696
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 20600
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20696
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20696
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20696
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20696
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20600
 *build.exe Version 0.60 Build 20696

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/29/2016 3:11:19AM Engine version = 5700.7163
  4/29/2016 3:11:19AM AntiVirus DAT version = 8149.0
  4/29/2016 3:11:19AM Number of detection signatures in EXTRA.DAT = None
  4/29/2016 3:11:19AM Names of detection signatures in EXTRA.DAT = None
  4/29/2016 3:11:20AM Scan Started On-Demand Scan
  4/29/2016 3:11:22AM Scan Summary
  4/29/2016 3:11:22AM Processes scanned : 0
  4/29/2016 3:11:22AM Processes detected : 0
  4/29/2016 3:11:22AM Processes cleaned : 0
  4/29/2016 3:11:22AM Boot sectors scanned : 1
  4/29/2016 3:11:22AM Boot sectors detected: 0
  4/29/2016 3:11:22AM Boot sectors cleaned : 0
  4/29/2016 3:11:22AM Files scanned : 55
  4/29/2016 3:11:22AM Files with detections: 0
  4/29/2016 3:11:22AM File detections : 0
  4/29/2016 3:11:22AM Files cleaned : 0
  4/29/2016 3:11:22AM Files deleted : 0
  4/29/2016 3:11:22AM Files not scanned : 0
  4/29/2016 3:11:22AM Scan Summary (Registry Scanning)
  4/29/2016 3:11:22AM Keys scanned : 0
  4/29/2016 3:11:22AM Keys detected : 0
  4/29/2016 3:11:22AM Keys cleaned : 0
  4/29/2016 3:11:22AM Keys deleted : 0
  4/29/2016 3:11:22AM Run time : 0:00:03
  4/29/2016 3:11:22AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20663:HEAD Source
------------------------------------------------------------------------  r20694 | edk2buildsystem | 2016-04-29 02:07:26 -0700 (Fri, 29 Apr 2016) | 10 lines
  BaseTools: fix the bug for FMP to support use Macro as path description
  Fix the bug for FMP image to support to use Macro as path description,
  eg: FILE DATA = $(OUTPUT_DIRECTORY)/$(TARGET)_$(TOOL_CHAIN_TAG)/test.efi
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 35217a337cb6d262d4a3b5165bd86ba150a6c088)

------------------------------------------------------------------------  r20695 | edk2buildsystem | 2016-04-29 02:07:30 -0700 (Fri, 29 Apr 2016) | 17 lines
  BaseTools/Build: Better DSC arch filtering
  Description:
  When building for any specific architecture, the build script today is loading
  DSC sections for other architectures not in the build. The build process should
  disregard DSC sections that are not relevant to the build.
  My previous patch only fixed issue for one section type (Components). This
  patch will handle all section types by updating the MetaFileParser class, which
  now takes a Arch argument and will filter the DSC table results as they are
  returned from the database.  The database still contains all information from
  DSCs for when builds support multiple arch's
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Thomas Palmer <thomas.palmer@hpe.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit cdd1b5e5486460ac96f44cddf1edfda25b1fdce9)

------------------------------------------------------------------------