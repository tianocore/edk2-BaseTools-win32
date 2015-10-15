Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18607

This directory contains the Win32 binaries.

Build Date:       Wed, 14 Oct 2015 18:59:28 Pacific Daylight Time
Last Changed Rev: 18606

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18584
  BootSectImage Version 0.1 Build 18600
  Ecc.exe Version 0.01 Build 18595
  EfiLdrImage Version 0.1 Build 18600
  EfiRom Version 0.1 Build 18600
  GenBootSector Version 0.2 Build 18600
  GenCrc32 Version 0.2 Build 18600
  GenDepex.exe Version 0.04 Build 18584
  GenFds.exe 1.0 Build 18584
  GenFfs Version 0.1 Build 18600
  GenFv Version 0.1 Build 18600
  GenFw Version 0.2 Build 18600
  GenPage Version 0.2 Build 18600
  GenPatchPcdTable.exe Version 0.10 Build 18584
  GenSec Version 0.1 Build 18600
  GenVtf Version 0.1 Build 18600
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 18600
  LzmaF86Compress Version 0.2 Build 18600
  PatchPcdValue.exe Version 0.10 Build 18584
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 18600
  TargetTool.exe Version 0.01 Build 18584
  TianoCompress Version 0.1 Build 18600
  Trim.exe Version 0.10 Build 18584
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 18600
 *VfrCompile version  2.00 (UEFI 2.4) Build 18607
  VolInfo Version 0.83 Build 18600, Oct 10 2015
  build.exe Version 0.60 Build 18584

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/14/2015 6:59:30PM Engine version = 5700.7163
  10/14/2015 6:59:30PM AntiVirus DAT version = 7954.0
  10/14/2015 6:59:30PM Number of detection signatures in EXTRA.DAT = 1
  10/14/2015 6:59:30PM Names of detection signatures in EXTRA.DAT = Generic PWS.o (ED)
  10/14/2015 6:59:30PM Scan Started On-Demand Scan
  10/14/2015 6:59:44PM Scan Summary
  10/14/2015 6:59:44PM Processes scanned : 0
  10/14/2015 6:59:44PM Processes detected : 0
  10/14/2015 6:59:44PM Processes cleaned : 0
  10/14/2015 6:59:44PM Boot sectors scanned : 1
  10/14/2015 6:59:44PM Boot sectors detected: 0
  10/14/2015 6:59:44PM Boot sectors cleaned : 0
  10/14/2015 6:59:44PM Files scanned : 55
  10/14/2015 6:59:44PM Files with detections: 0
  10/14/2015 6:59:44PM File detections : 0
  10/14/2015 6:59:44PM Files cleaned : 0
  10/14/2015 6:59:44PM Files deleted : 0
  10/14/2015 6:59:44PM Files not scanned : 0
  10/14/2015 6:59:44PM Scan Summary (Registry Scanning)
  10/14/2015 6:59:44PM Keys scanned : 0
  10/14/2015 6:59:44PM Keys detected : 0
  10/14/2015 6:59:44PM Keys cleaned : 0
  10/14/2015 6:59:44PM Keys deleted : 0
  10/14/2015 6:59:44PM Run time : 0:00:14
  10/14/2015 6:59:44PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18600:HEAD Source
------------------------------------------------------------------------  r18600 | hchen30 | 2015-10-09 22:46:00 -0700 (Fri, 09 Oct 2015) | 5 lines
  BaseTool/UPT: Fix two wrong imports for UPT
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r18601 | lgao4 | 2015-10-11 23:02:09 -0700 (Sun, 11 Oct 2015) | 5 lines
  BaseTools: Fixed an error reported during generating report
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r18602 | lgao4 | 2015-10-14 02:43:43 -0700 (Wed, 14 Oct 2015) | 7 lines
  BaseTools: Fix the issue to support windows root directory
  Use os.path.relpath to get the relative directory instead of directly trim it.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>

------------------------------------------------------------------------  r18606 | ydong10 | 2015-10-14 18:03:47 -0700 (Wed, 14 Oct 2015) | 7 lines
  BaseTools VfrCompiler: In order to keep consistent, add an optional ";" for condition op-code.
  Current grammar for suppressif opcode not consistent in statement and option case, this patch fixed this issue. The same case also existed for other condition opcodes.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Eric Dong <eric.dong@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------