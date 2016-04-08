Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20523

This directory contains the Win32 binaries.

Build Date:       Fri, 08 Apr 2016 03:33:14 Pacific Daylight Time
Last Changed Rev: 20498

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20523
  BootSectImage Version 1.0 Build Build 20182
 *Ecc.exe Version 1.0 Build Build 20523
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20523
 *GenFds.exe 1.0 Build 20523
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20523
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20523
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20476
  Rsa2048Sha256Sign Version 0.9 Build 20476
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20523
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20523
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20476
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20182
 *build.exe Version 0.60 Build 20523

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/8/2016 3:33:15AM Engine version = 5700.7163
  4/8/2016 3:33:15AM AntiVirus DAT version = 8128.0
  4/8/2016 3:33:15AM Number of detection signatures in EXTRA.DAT = None
  4/8/2016 3:33:15AM Names of detection signatures in EXTRA.DAT = None
  4/8/2016 3:33:15AM Scan Started On-Demand Scan
  4/8/2016 3:33:17AM Scan Summary
  4/8/2016 3:33:17AM Processes scanned : 0
  4/8/2016 3:33:17AM Processes detected : 0
  4/8/2016 3:33:17AM Processes cleaned : 0
  4/8/2016 3:33:17AM Boot sectors scanned : 1
  4/8/2016 3:33:17AM Boot sectors detected: 0
  4/8/2016 3:33:17AM Boot sectors cleaned : 0
  4/8/2016 3:33:17AM Files scanned : 55
  4/8/2016 3:33:17AM Files with detections: 0
  4/8/2016 3:33:17AM File detections : 0
  4/8/2016 3:33:17AM Files cleaned : 0
  4/8/2016 3:33:17AM Files deleted : 0
  4/8/2016 3:33:17AM Files not scanned : 0
  4/8/2016 3:33:17AM Scan Summary (Registry Scanning)
  4/8/2016 3:33:17AM Keys scanned : 0
  4/8/2016 3:33:17AM Keys detected : 0
  4/8/2016 3:33:17AM Keys cleaned : 0
  4/8/2016 3:33:17AM Keys deleted : 0
  4/8/2016 3:33:17AM Run time : 0:00:02
  4/8/2016 3:33:17AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20476:HEAD Source
------------------------------------------------------------------------  r20497 | jljusten | 2016-04-07 09:42:05 -0700 (Thu, 07 Apr 2016) | 9 lines
  BaseTools: Enhance --Pcd which override by build option
  This patch 1) enhance the help info for --pcd to use " but not '.
  2) Add the condition statements for build option Pcd type check.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d7cd335681d6b1b5791b4e8ef4e311f39469a8c0)

------------------------------------------------------------------------  r20498 | jljusten | 2016-04-07 09:42:46 -0700 (Thu, 07 Apr 2016) | 26 lines
  BaseTools: Add support to merge Prebuild and Postbuild into build Process
  This feature is enhance build tool to incorporate execution of prebuild
  and postbuild.
  1.Prebuild script
  a.DEFINE PREBUILD in DSC [Defines] section
  b.Build command -D PREBUILD to override the one in DSC [Defines] section
  1)If PREBUILD is a file, then this file will be used as prebuild script.
  2)If PREBUILD is empty, then prebuild script will be disabled.
  3)If PREBUILD is not defined in [Defines] section and not passed in on
  command line, then prebuild script is also disabled.
  2.Prebuild option
  a.All options of build tool
  b.TARGET, ARCH and TOOL_CHAIN_TAG value, Those value will be from
  target.txt file if they are not in build command line.
  c.Additional options following prebuild definition. Quotes are needed
  when these additional options are present.
  d.Quotes would also be required if the path to the prebuild command
  contains space or special characters.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f0dc69e61bf2316dcf7cc75eb7e4ba374a5b2832)

------------------------------------------------------------------------