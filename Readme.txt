Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 16227

This directory contains the Win32 binaries.

Build Date:       Wed, 22 Oct 2014 03:06:00 Pacific Daylight Time
Last Changed Rev: 16226

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 16164
  BootSectImage Version 0.1 Build 16164
  EfiLdrImage Version 0.1 Build 16164
  EfiRom Version 0.1 Build 16164
  GenBootSector Version 0.2 Build 16164
  GenCrc32 Version 0.2 Build 16164
  GenDepex.exe Version 0.04 Build 16164
  GenFds.exe 1.0 Build 16164
  GenFfs Version 0.1 Build 16164
  GenFv Version 0.1 Build 16164
  GenFw Version 0.2 Build 16164
  GenPage Version 0.2 Build 16164
  GenPatchPcdTable.exe Version 0.10 Build 16164
  GenSec Version 0.1 Build 16164
  GenVtf Version 0.1 Build 16164
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 16164
  LzmaF86Compress Version 0.2 Build 16164
  PatchPcdValue.exe Version 0.10 Build 16164
  Rsa2048Sha256GenerateKeys Version 0.9 Build 16164
  Rsa2048Sha256Sign Version 0.9 Build 16164
  Split Version 0.1 Build 16164
  TargetTool.exe Version 0.01 Build 16164
  TianoCompress Version 0.1 Build 16164
  Trim.exe Version 0.10 Build 16164
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 16164
  VfrCompile version  2.00 (UEFI 2.4) Build 16164
  VolInfo Version 0.83 Build 16164, Sep 24 2014
  build.exe Version 0.60 Build 16164

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.975
  10/22/2014 3:06:01AM Engine version = 5400.1158
  10/22/2014 3:06:01AM AntiVirus DAT version = 7523.0
  10/22/2014 3:06:01AM Number of detection signatures in EXTRA.DAT = None
  10/22/2014 3:06:01AM Names of detection signatures in EXTRA.DAT = None
  10/22/2014 3:06:01AM Scan Started On-Demand Scan
  10/22/2014 3:06:07AM Scan Summary
  10/22/2014 3:06:07AM Processes scanned : 0
  10/22/2014 3:06:07AM Processes detected : 0
  10/22/2014 3:06:07AM Processes cleaned : 0
  10/22/2014 3:06:07AM Boot sectors scanned : 2
  10/22/2014 3:06:07AM Boot sectors detected: 0
  10/22/2014 3:06:07AM Boot sectors cleaned : 0
  10/22/2014 3:06:07AM Files scanned : 47
  10/22/2014 3:06:07AM Files with detections: 0
  10/22/2014 3:06:07AM File detections : 0
  10/22/2014 3:06:07AM Files cleaned : 0
  10/22/2014 3:06:07AM Files deleted : 0
  10/22/2014 3:06:07AM Files not scanned : 0
  10/22/2014 3:06:07AM Scan Summary (Registry Scanning)
  10/22/2014 3:06:07AM Keys scanned : 0
  10/22/2014 3:06:07AM Keys detected : 0
  10/22/2014 3:06:07AM Keys cleaned : 0
  10/22/2014 3:06:07AM Keys deleted : 0
  10/22/2014 3:06:07AM Scan Summary (Cookie Scanning)
  10/22/2014 3:06:07AM Cookies scanned : 0
  10/22/2014 3:06:07AM Cookies detected : 0
  10/22/2014 3:06:07AM Cookies cleaned : 0
  10/22/2014 3:06:07AM Cookies deleted : 0
  10/22/2014 3:06:07AM Run time : 0:00:07
  10/22/2014 3:06:07AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 16164:HEAD Source
------------------------------------------------------------------------  r16169 | oliviermartin | 2014-09-24 14:07:53 -0700 (Wed, 24 Sep 2014) | 10 lines
  BaseTools: Actually plug in BaseTools build on AArch64
  Support for building BaseTools on AArch64 is available in the tree, but
  not currently "plugged in". This patch adds the required snippet.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Leif Lindholm <leif.lindholm@linaro.org>
  Reviewed-by: Olivier Martin <olivier.martin@arm.com>

------------------------------------------------------------------------  r16226 | hchen30 | 2014-10-21 23:44:45 -0700 (Tue, 21 Oct 2014) | 7 lines
  BaseTools/UPT: Remove Macro Expend for UserExtension section
  Remove Macro Expend for UserExtension section
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Gao, Liming <liming.gao@intel.com>

------------------------------------------------------------------------