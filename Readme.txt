Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 20165, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 19775

This directory contains the Win32 binaries.

Build Date:       Fri, 29 Jan 2016 14:30:49 Pacific Standard Time
Last Changed Rev: 19768

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 19775
  BootSectImage Version 0.1 Build 19148
  Ecc.exe Version 0.01 Build 18595
  EfiLdrImage Version 0.1 Build 19148
  EfiRom Version 0.1 Build 19148
  GenBootSector Version 0.2 Build 19610
  GenCrc32 Version 0.2 Build 19148
 *GenDepex.exe Version 0.04 Build 19775
 *GenFds.exe 1.0 Build 19775
  GenFfs Version 0.1 Build 19148
  GenFv Version 0.1 Build 19610
 *GenFw Version 0.2 Build 19775
  GenPage Version 0.2 Build 19148
 *GenPatchPcdTable.exe Version 0.10 Build 19775
  GenSec Version 0.1 Build 19148
 *GenVtf Version 0.1 Build 19775
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 19775
  LzmaF86Compress Version 0.2 Build 19775
 *PatchPcdValue.exe Version 0.10 Build 19775
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 19148
 *TargetTool.exe Version 0.01 Build 19775
  TianoCompress Version 0.1 Build 19148
 *Trim.exe Version 0.10 Build 19775
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 19580
 *VfrCompile version  2.00 (UEFI 2.4) Build 19775
  VolInfo Version 0.83 Build 19148, Dec  7 2015
 *build.exe Version 0.60 Build 19775

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/29/2016 2:30:51PM Engine version = 5700.7163
  1/29/2016 2:30:51PM AntiVirus DAT version = 8059.0
  1/29/2016 2:30:51PM Number of detection signatures in EXTRA.DAT = None
  1/29/2016 2:30:51PM Names of detection signatures in EXTRA.DAT = None
  1/29/2016 2:30:51PM Scan Started On-Demand Scan
  1/29/2016 2:30:59PM Scan Summary
  1/29/2016 2:30:59PM Processes scanned : 0
  1/29/2016 2:30:59PM Processes detected : 0
  1/29/2016 2:30:59PM Processes cleaned : 0
  1/29/2016 2:30:59PM Boot sectors scanned : 2
  1/29/2016 2:30:59PM Boot sectors detected: 0
  1/29/2016 2:30:59PM Boot sectors cleaned : 0
  1/29/2016 2:30:59PM Files scanned : 59
  1/29/2016 2:30:59PM Files with detections: 0
  1/29/2016 2:30:59PM File detections : 0
  1/29/2016 2:30:59PM Files cleaned : 0
  1/29/2016 2:30:59PM Files deleted : 0
  1/29/2016 2:30:59PM Files not scanned : 0
  1/29/2016 2:30:59PM Scan Summary (Registry Scanning)
  1/29/2016 2:30:59PM Keys scanned : 0
  1/29/2016 2:30:59PM Keys detected : 0
  1/29/2016 2:30:59PM Keys cleaned : 0
  1/29/2016 2:30:59PM Keys deleted : 0
  1/29/2016 2:30:59PM Run time : 0:00:09
  1/29/2016 2:30:59PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 19749:HEAD Source
------------------------------------------------------------------------  r19765 | yzhu52 | 2016-01-28 20:44:54 -0800 (Thu, 28 Jan 2016) | 8 lines
  BaseTools: Fix a bug for VpdOffset calculate
  The VpdOffset value in the DSC both support integer and Hex value, so we
  fix the bug to support both format.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r19766 | yzhu52 | 2016-01-28 20:46:47 -0800 (Thu, 28 Jan 2016) | 8 lines
  BaseTools: Fix the bug for VOID* Patchable PCD declaration in Library
  VOID* Patchable PCD in Library has the different declaration from the
  one in Driver, this issue that will cause GCC LTO build failure.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r19767 | yzhu52 | 2016-01-28 20:48:55 -0800 (Thu, 28 Jan 2016) | 11 lines
  BaseTools:Incremental build not work if VPD values in DSC changed by -D
  If a -D flag is passed into build that selects different lines in
  [PcdsDynamicExVpd], then build does not see any changes to the timestamp
  of the DSC file and the VPD tool is not used to regenerate the VPD
  region based in the statements that are active. so we changed the detect
  condition and use SaveFileOnChange function to generate VPD.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r19768 | yzhu52 | 2016-01-28 20:54:37 -0800 (Thu, 28 Jan 2016) | 9 lines
  BaseTools: Update BaseTools to pass VS2015 compiler
  Fix some errors to pass VS2015 compiler.
  1. warning C4456: declaration of xxx hides previous local declaration
  2. warning C4005: 'UINT8_MAX': macro redefinition
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------