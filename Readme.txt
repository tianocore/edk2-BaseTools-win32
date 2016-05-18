Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20909

This directory contains the Win32 binaries.

Build Date:       Wed, 18 May 2016 03:12:07 Pacific Daylight Time
Last Changed Rev: 20907

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20909
 *BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
 *EfiLdrImage Version 1.0 Build Build 20909
 *EfiRom Version 0.1 Build 20909
 *GenBootSector Version 0.2 Build 20909
 *GenCrc32 Version 0.2 Build 20909
 *GenDepex.exe Version 0.04 Build 20909
 *GenFds.exe 1.0 Build 20909
 *GenFfs Version 0.1 Build 20909
 *GenFv Version 0.1 Build 20909
 *GenFw Version 0.2 Build 20909
 *GenPage Version 0.2 Build 20909
 *GenPatchPcdTable.exe Version 0.10 Build 20909
 *GenSec Version 0.1 Build 20909
 *GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
 *PatchPcdValue.exe Version 0.10 Build 20909
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
 *Split Version 1.0 Build Build 20909
 *TargetTool.exe Version 0.01 Build 20909
 *TianoCompress Version 0.1 Build 20909
 *Trim.exe Version 0.10 Build 20909
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 20909
 *VolInfo Version 1.0 Build Build 20909
 *build.exe Version 0.60 Build 20909

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/18/2016 3:12:08AM Engine version = 5700.7163
  5/18/2016 3:12:08AM AntiVirus DAT version = 8168.0
  5/18/2016 3:12:08AM Number of detection signatures in EXTRA.DAT = 1
  5/18/2016 3:12:08AM Names of detection signatures in EXTRA.DAT = W97M/Downloader.bdj (ED)
  5/18/2016 3:12:08AM Scan Started On-Demand Scan
  5/18/2016 3:12:10AM Scan Summary
  5/18/2016 3:12:10AM Processes scanned : 0
  5/18/2016 3:12:10AM Processes detected : 0
  5/18/2016 3:12:10AM Processes cleaned : 0
  5/18/2016 3:12:10AM Boot sectors scanned : 1
  5/18/2016 3:12:10AM Boot sectors detected: 0
  5/18/2016 3:12:10AM Boot sectors cleaned : 0
  5/18/2016 3:12:10AM Files scanned : 71
  5/18/2016 3:12:10AM Files with detections: 0
  5/18/2016 3:12:10AM File detections : 0
  5/18/2016 3:12:10AM Files cleaned : 0
  5/18/2016 3:12:10AM Files deleted : 0
  5/18/2016 3:12:10AM Files not scanned : 0
  5/18/2016 3:12:10AM Scan Summary (Registry Scanning)
  5/18/2016 3:12:10AM Keys scanned : 0
  5/18/2016 3:12:10AM Keys detected : 0
  5/18/2016 3:12:10AM Keys cleaned : 0
  5/18/2016 3:12:10AM Keys deleted : 0
  5/18/2016 3:12:10AM Run time : 0:00:03
  5/18/2016 3:12:10AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20882:HEAD Source
------------------------------------------------------------------------  r20882 | edk2buildsystem | 2016-05-16 02:06:15 -0700 (Mon, 16 May 2016) | 12 lines
  BaseTools: Add HII definitions from UEFI 2.6
  Add HII definitions from UEFI 2.6 for HII Image Variability and PNG
  Blocks
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Samer El-Haj-Mahmoud <elhaj@hpe.com>
  Reviewed-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7b1fe7acdca15be49a9421156b799ed7394f7bac)

------------------------------------------------------------------------  r20902 | edk2buildsystem | 2016-05-18 02:05:35 -0700 (Wed, 18 May 2016) | 15 lines
  BaseTools: support private package definition
  EDKII build spec and DEC spec updated to support private package
  definition.
  If GUID, Protocol or PPI is listed in a DEC file, where the  Private
  modifier is used in the section tag ([Guids.common.Private] for example),
  only modules within the package are permitted to use the GUID, Protocol
  or PPI. If a module or library instance outside of the package attempts
  to use the item, the build must fail with an appropriate error message.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c28d2e1047816164ffec552e4a3375122cbcc6b6)

------------------------------------------------------------------------  r20907 | edk2buildsystem | 2016-05-18 02:05:59 -0700 (Wed, 18 May 2016) | 11 lines
  BaseTools: Eliminate two shift-negative-value in FvLib.c
  clang 3.8 flags -Wshift-negative-value warning, which turns fatal due to
  use of -Werror.
  Fixes: https://github.com/tianocore/edk2/issues/49
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Zenith432 <zenith432@users.sourceforge.net>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d3bb711834acd3eda35a07d0be7911bc3dbb9e6f)

------------------------------------------------------------------------