Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20172

This directory contains the Win32 binaries.

Build Date:       Wed, 09 Mar 2016 03:31:54 Pacific Standard Time
Last Changed Rev: 20171

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20172
  BootSectImage Version 1.0 Build Build 19914
  Ecc.exe Version 1.0 Build Build 19914
  EfiLdrImage Version 1.0 Build Build 19914
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20172
 *GenFds.exe 1.0 Build 20172
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 19914
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20172
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20172
  Rsa2048Sha256GenerateKeys Version 0.9 Build 19914
  Rsa2048Sha256Sign Version 0.9 Build 19914
  Split Version 1.0 Build Build 19914
 *TargetTool.exe Version 0.01 Build 20172
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20172
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 19914
  VfrCompile version  2.01 (UEFI 2.4) Build Build 19914
  VolInfo Version 1.0 Build Build 19914
 *build.exe Version 0.60 Build 20172

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/9/2016 3:31:56AM Engine version = 5700.7163
  3/9/2016 3:31:56AM AntiVirus DAT version = 8098.0
  3/9/2016 3:31:56AM Number of detection signatures in EXTRA.DAT = None
  3/9/2016 3:31:56AM Names of detection signatures in EXTRA.DAT = None
  3/9/2016 3:31:56AM Scan Started On-Demand Scan
  3/9/2016 3:31:57AM Scan Summary
  3/9/2016 3:31:57AM Processes scanned : 0
  3/9/2016 3:31:57AM Processes detected : 0
  3/9/2016 3:31:57AM Processes cleaned : 0
  3/9/2016 3:31:57AM Boot sectors scanned : 1
  3/9/2016 3:31:57AM Boot sectors detected: 0
  3/9/2016 3:31:57AM Boot sectors cleaned : 0
  3/9/2016 3:31:57AM Files scanned : 55
  3/9/2016 3:31:57AM Files with detections: 0
  3/9/2016 3:31:57AM File detections : 0
  3/9/2016 3:31:57AM Files cleaned : 0
  3/9/2016 3:31:57AM Files deleted : 0
  3/9/2016 3:31:57AM Files not scanned : 0
  3/9/2016 3:31:57AM Scan Summary (Registry Scanning)
  3/9/2016 3:31:57AM Keys scanned : 0
  3/9/2016 3:31:57AM Keys detected : 0
  3/9/2016 3:31:57AM Keys cleaned : 0
  3/9/2016 3:31:57AM Keys deleted : 0
  3/9/2016 3:31:57AM Run time : 0:00:02
  3/9/2016 3:31:57AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20119:HEAD Source
------------------------------------------------------------------------  r20171 | edk2buildsystem | 2016-03-09 02:26:03 -0800 (Wed, 09 Mar 2016) | 13 lines
  BaseTools: Add Multiple Workspaces support for custom Makefiles.
  This patch makes sure the MODULE_DIR variable points to the correct
  location when multiple workspaces are used. Currently, it is
  always prefixed with $(WORKSPACE), which only works as long as the
  package is in the Workspace.
  Code modules were not effected because the required paths were valid,
  but for custom Makefiles, the MODULE_DIR variable is used.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Marvin Haeuser <Marvin.Haeuser@outlook.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 01e418d652bb3a7cbacc82d74fab1cc5260d0e1f)

------------------------------------------------------------------------