Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 19148

This directory contains the Win32 binaries.

Build Date:       Mon, 07 Dec 2015 14:28:42 Pacific Standard Time
Last Changed Rev: 19143

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 19148
 *BootSectImage Version 0.1 Build 19148
  Ecc.exe Version 0.01 Build 18595
 *EfiLdrImage Version 0.1 Build 19148
 *EfiRom Version 0.1 Build 19148
 *GenBootSector Version 0.2 Build 19148
 *GenCrc32 Version 0.2 Build 19148
 *GenDepex.exe Version 0.04 Build 19148
 *GenFds.exe 1.0 Build 19148
 *GenFfs Version 0.1 Build 19148
 *GenFv Version 0.1 Build 19148
 *GenFw Version 0.2 Build 19148
 *GenPage Version 0.2 Build 19148
 *GenPatchPcdTable.exe Version 0.10 Build 19148
 *GenSec Version 0.1 Build 19148
 *GenVtf Version 0.1 Build 19148
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 19148
  LzmaF86Compress Version 0.2 Build 19148
 *PatchPcdValue.exe Version 0.10 Build 19148
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
 *Split Version 0.1 Build 19148
 *TargetTool.exe Version 0.01 Build 19148
 *TianoCompress Version 0.1 Build 19148
 *Trim.exe Version 0.10 Build 19148
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 18900
 *VfrCompile version  2.00 (UEFI 2.4) Build 19148
 *VolInfo Version 0.83 Build 19148, Dec  7 2015
 *build.exe Version 0.60 Build 19148

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/7/2015 2:28:43PM Engine version = 5700.7163
  12/7/2015 2:28:43PM AntiVirus DAT version = 8007.0
  12/7/2015 2:28:43PM Number of detection signatures in EXTRA.DAT = None
  12/7/2015 2:28:43PM Names of detection signatures in EXTRA.DAT = None
  12/7/2015 2:28:43PM Scan Started On-Demand Scan
  12/7/2015 2:28:46PM Scan Summary
  12/7/2015 2:28:46PM Processes scanned : 0
  12/7/2015 2:28:46PM Processes detected : 0
  12/7/2015 2:28:46PM Processes cleaned : 0
  12/7/2015 2:28:46PM Boot sectors scanned : 1
  12/7/2015 2:28:46PM Boot sectors detected: 0
  12/7/2015 2:28:46PM Boot sectors cleaned : 0
  12/7/2015 2:28:46PM Files scanned : 71
  12/7/2015 2:28:46PM Files with detections: 0
  12/7/2015 2:28:46PM File detections : 0
  12/7/2015 2:28:46PM Files cleaned : 0
  12/7/2015 2:28:46PM Files deleted : 0
  12/7/2015 2:28:46PM Files not scanned : 0
  12/7/2015 2:28:46PM Scan Summary (Registry Scanning)
  12/7/2015 2:28:46PM Keys scanned : 0
  12/7/2015 2:28:46PM Keys detected : 0
  12/7/2015 2:28:46PM Keys cleaned : 0
  12/7/2015 2:28:46PM Keys deleted : 0
  12/7/2015 2:28:46PM Run time : 0:00:03
  12/7/2015 2:28:46PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 19084:HEAD Source
------------------------------------------------------------------------  r19136 | yzhu52 | 2015-12-07 00:27:53 -0800 (Mon, 07 Dec 2015) | 9 lines
  BaseTools: Add support for INF statement in FD region
  FD region today can be file or data, but not a patched image.Add support
  for an INF statement in an FD region, so the binary from the INF can be
  patched prior to being added to the FD region.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r19137 | yzhu52 | 2015-12-07 00:29:10 -0800 (Mon, 07 Dec 2015) | 9 lines
  BaseTools: Enhance GenFv Tool to report error message
  When two vtf files in one FV image, no FV file can be generated, but it
  report the stack trace info. so we enhance the tool to report error
  message directly but not the stack trace info.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r19138 | yzhu52 | 2015-12-07 01:01:44 -0800 (Mon, 07 Dec 2015) | 4 lines
  Revert the change in r19137.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>

------------------------------------------------------------------------  r19139 | yzhu52 | 2015-12-07 01:03:35 -0800 (Mon, 07 Dec 2015) | 9 lines
  BaseTools: Fix a bug in the VPD report generation
  Changed the if condition to check whether current Region is FD VPD region
  to fix a bug in the VPD report generation.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r19141 | yzhu52 | 2015-12-07 01:04:39 -0800 (Mon, 07 Dec 2015) | 10 lines
  BaseTools: Enhance GenFv Tool to report error message
  When two vtf files in one FV image, no FV file can be generated, but it
  report the stack trace info. so we enhance the tool to report error
  message directly but not the stack trace info.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r19142 | yzhu52 | 2015-12-07 01:08:05 -0800 (Mon, 07 Dec 2015) | 10 lines
  BaseTools: Fix a bug when apply patches to SEC use the FILE_GUID override
  Fix a bug when applying patches to SEC modules that use the FILE_GUID
  override. Since a temp dir is used when FILE_GUID override is used, the
  INF file path comparisons fail. The fix is to capture the real INF file
  path comparisons instead of using the temp dir path to the INF.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r19143 | yzhu52 | 2015-12-07 01:09:31 -0800 (Mon, 07 Dec 2015) | 10 lines
  BaseTools: process the files by the priority in BUILDRULEORDER
  By the BUILDRULEORDER feature to process files listed in INF [Sources]
  sections in priority order, if a filename is listed with multiple
  extensions, the tools will use only the file that matches the first
  extension in the space separated list.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------