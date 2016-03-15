Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20288

This directory contains the Win32 binaries.

Build Date:       Tue, 15 Mar 2016 12:55:40 Pacific Daylight Time
Last Changed Rev: 20281

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20288
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20182
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20288
 *GenFds.exe 1.0 Build 20288
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20288
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20288
  Rsa2048Sha256GenerateKeys Version 0.9 Build 19914
  Rsa2048Sha256Sign Version 0.9 Build 19914
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20288
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20288
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20212
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20182
 *build.exe Version 0.60 Build 20288

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/15/2016 12:55:41PM Engine version = 5700.7163
  3/15/2016 12:55:41PM AntiVirus DAT version = 8105.0
  3/15/2016 12:55:41PM Number of detection signatures in EXTRA.DAT = None
  3/15/2016 12:55:41PM Names of detection signatures in EXTRA.DAT = None
  3/15/2016 12:55:41PM Scan Started On-Demand Scan
  3/15/2016 12:55:43PM Scan Summary
  3/15/2016 12:55:43PM Processes scanned : 0
  3/15/2016 12:55:43PM Processes detected : 0
  3/15/2016 12:55:43PM Processes cleaned : 0
  3/15/2016 12:55:43PM Boot sectors scanned : 1
  3/15/2016 12:55:43PM Boot sectors detected: 0
  3/15/2016 12:55:43PM Boot sectors cleaned : 0
  3/15/2016 12:55:43PM Files scanned : 55
  3/15/2016 12:55:43PM Files with detections: 0
  3/15/2016 12:55:43PM File detections : 0
  3/15/2016 12:55:43PM Files cleaned : 0
  3/15/2016 12:55:43PM Files deleted : 0
  3/15/2016 12:55:43PM Files not scanned : 0
  3/15/2016 12:55:43PM Scan Summary (Registry Scanning)
  3/15/2016 12:55:43PM Keys scanned : 0
  3/15/2016 12:55:43PM Keys detected : 0
  3/15/2016 12:55:43PM Keys cleaned : 0
  3/15/2016 12:55:43PM Keys deleted : 0
  3/15/2016 12:55:43PM Run time : 0:00:02
  3/15/2016 12:55:43PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20274:HEAD Source
------------------------------------------------------------------------  r20280 | edk2buildsystem | 2016-03-15 02:26:39 -0700 (Tue, 15 Mar 2016) | 10 lines
  BaseTools: Add two macros into AutoGenObject macro dict
  Add DEST_DIR_OUTPUT and DEST_DIR_DEBUG into AutoGenObject macro dict.
  Because some module (eg: BaseUefiCpuLib) may use this macro in the make
  file.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit df1e1b63d4c54e1ed5ea0b697ac3fba903c28009)

------------------------------------------------------------------------  r20281 | edk2buildsystem | 2016-03-15 02:26:43 -0700 (Tue, 15 Mar 2016) | 11 lines
  BaseTools: Support recent versions of cx_freeze.
  This patch fixes the assumed invalid command to start recent versions
  of cx_freeze on Windows, which are python and not Windows
  executables. To launch them correctly, the '$(PYTHON_HOME)\python'
  prefix has been added, so that Python can interpret the tool.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Marvin Haeuser <Marvin.Haeuser@outlook.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 89a811538e24fd598b9267b888c4ab4c2556dae2)

------------------------------------------------------------------------