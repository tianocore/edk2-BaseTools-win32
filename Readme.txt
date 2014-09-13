Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 16103

This directory contains the Win32 binaries.

Build Date:       Sat, 13 Sep 2014 03:01:34 Pacific Daylight Time
Last Changed Rev: 16103

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 16068
  BootSectImage Version 0.1 Build 16068
  EfiLdrImage Version 0.1 Build 16068
  EfiRom Version 0.1 Build 16068
  GenBootSector Version 0.2 Build 16068
  GenCrc32 Version 0.2 Build 16068
  GenDepex.exe Version 0.04 Build 16068
 *GenFds.exe 1.0 Build 16103
  GenFfs Version 0.1 Build 16068
  GenFv Version 0.1 Build 16068
  GenFw Version 0.2 Build 16068
  GenPage Version 0.2 Build 16068
  GenPatchPcdTable.exe Version 0.10 Build 16068
  GenSec Version 0.1 Build 16068
  GenVtf Version 0.1 Build 16068
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 16068
  LzmaF86Compress Version 0.2 Build 16068
  PatchPcdValue.exe Version 0.10 Build 16068
  Rsa2048Sha256GenerateKeys Version 0.9 Build 16068
  Rsa2048Sha256Sign Version 0.9 Build 16068
  Split Version 0.1 Build 16068
  TargetTool.exe Version 0.01 Build 16068
  TianoCompress Version 0.1 Build 16068
  Trim.exe Version 0.10 Build 16068
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 16068
  VfrCompile version  2.00 (UEFI 2.4) Build 16068
  VolInfo Version 0.83 Build 16068, Sep  9 2014
  build.exe Version 0.51 Build 16068

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.975
  9/13/2014 3:01:35AM Engine version = 5400.1158
  9/13/2014 3:01:35AM AntiVirus DAT version = 7559.0
  9/13/2014 3:01:35AM Number of detection signatures in EXTRA.DAT = None
  9/13/2014 3:01:35AM Names of detection signatures in EXTRA.DAT = None
  9/13/2014 3:01:35AM Scan Started On-Demand Scan
  9/13/2014 3:01:42AM Scan Summary
  9/13/2014 3:01:42AM Processes scanned : 0
  9/13/2014 3:01:42AM Processes detected : 0
  9/13/2014 3:01:42AM Processes cleaned : 0
  9/13/2014 3:01:42AM Boot sectors scanned : 2
  9/13/2014 3:01:42AM Boot sectors detected: 0
  9/13/2014 3:01:42AM Boot sectors cleaned : 0
  9/13/2014 3:01:42AM Files scanned : 69
  9/13/2014 3:01:42AM Files with detections: 0
  9/13/2014 3:01:42AM File detections : 0
  9/13/2014 3:01:42AM Files cleaned : 0
  9/13/2014 3:01:42AM Files deleted : 0
  9/13/2014 3:01:42AM Files not scanned : 0
  9/13/2014 3:01:42AM Scan Summary (Registry Scanning)
  9/13/2014 3:01:42AM Keys scanned : 0
  9/13/2014 3:01:42AM Keys detected : 0
  9/13/2014 3:01:42AM Keys cleaned : 0
  9/13/2014 3:01:42AM Keys deleted : 0
  9/13/2014 3:01:42AM Scan Summary (Cookie Scanning)
  9/13/2014 3:01:42AM Cookies scanned : 0
  9/13/2014 3:01:42AM Cookies detected : 0
  9/13/2014 3:01:42AM Cookies cleaned : 0
  9/13/2014 3:01:42AM Cookies deleted : 0
  9/13/2014 3:01:42AM Run time : 0:00:08
  9/13/2014 3:01:42AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 16068:HEAD Source
------------------------------------------------------------------------  r16094 | yingke | 2014-09-10 23:44:17 -0700 (Wed, 10 Sep 2014) | 9 lines
  Add support for ${s_*} and ${d_*} macros for in FDF file for the INF files, and for each statement in the build rules.
  The following keywords are supported:
  "src", "s_path", "s_dir", "s_name", "s_base", "s_ext", "dst", "d_path", "d_name", "d_base", "d_ext"
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Abner Chang <abner.chang@hp.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Larry Hauch <larry.hauch@intel.com>

------------------------------------------------------------------------  r16099 | yingke | 2014-09-11 23:57:22 -0700 (Thu, 11 Sep 2014) | 12 lines
  BaseTools: Fix the regression issue after enbaling s_* an d_* macros in FDF.
  Add the missing 'MacroDict' field in FfsInfStatement.
  The issue is that BaseTools/Source/Python/GenFds/FfsInfStatement.py", line 448, in __ExtendMacro__
  String = GenFdsGlobalVariable.MacroExtend(String, self.MacroDict)
  AttributeError: OptRomInfStatement instance has no attribute 'MacroDict'
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r16101 | bobfeng | 2014-09-12 01:46:30 -0700 (Fri, 12 Sep 2014) | 5 lines
  This patch is going to fix the issue of the mis-match between the index of Platform DynamicPcd list and Dynamic Pcd generated token number.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Feng, Bob C <bob.c.feng@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------  r16103 | lhauch | 2014-09-12 15:59:04 -0700 (Fri, 12 Sep 2014) | 9 lines
  The current Makefile only checks the primary python file, such as build.py and does not check other files in tool’s directory tree.
  This modification adds all of the other files within the tool’s directory tree that would be a cause to rebuild the tool.
  The format in the Makefile for listing these other files was selected to allow the nightly build script to detect changes in the additional files.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: lhauch <larry.hauch@intel.com>
  Reviewed-by: Gao, Liming <liming.gao@intel.com>

------------------------------------------------------------------------