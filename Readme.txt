Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 16555

This directory contains the Win32 binaries.

Build Date:       Tue, 23 Dec 2014 03:08:41 Pacific Standard Time
Last Changed Rev: 16550

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 16487
  BootSectImage Version 0.1 Build 16164
  EfiLdrImage Version 0.1 Build 16164
  EfiRom Version 0.1 Build 16164
  GenBootSector Version 0.2 Build 16164
  GenCrc32 Version 0.2 Build 16164
  GenDepex.exe Version 0.04 Build 16487
  GenFds.exe 1.0 Build 16487
  GenFfs Version 0.1 Build 16164
  GenFv Version 0.1 Build 16164
  GenFw Version 0.2 Build 16304
  GenPage Version 0.2 Build 16164
  GenPatchPcdTable.exe Version 0.10 Build 16487
  GenSec Version 0.1 Build 16164
  GenVtf Version 0.1 Build 16164
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 16164
  LzmaF86Compress Version 0.2 Build 16164
  PatchPcdValue.exe Version 0.10 Build 16487
  Rsa2048Sha256GenerateKeys Version 0.9 Build 16164
  Rsa2048Sha256Sign Version 0.9 Build 16164
  Split Version 0.1 Build 16164
  TargetTool.exe Version 0.01 Build 16487
  TianoCompress Version 0.1 Build 16164
  Trim.exe Version 0.10 Build 16487
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 16455
 *VfrCompile version  2.00 (UEFI 2.4) Build 16555
  VolInfo Version 0.83 Build 16164, Sep 24 2014
 *build.exe Version 0.60 Build 16555

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1247
  12/23/2014 3:08:43AM Engine version = 5600.1067
  12/23/2014 3:08:43AM AntiVirus DAT version = 7659.0
  12/23/2014 3:08:43AM Number of detection signatures in EXTRA.DAT = None
  12/23/2014 3:08:43AM Names of detection signatures in EXTRA.DAT = None
  12/23/2014 3:08:43AM Scan Started On-Demand Scan
  12/23/2014 3:08:55AM Scan Summary
  12/23/2014 3:08:55AM Processes scanned : 0
  12/23/2014 3:08:55AM Processes detected : 0
  12/23/2014 3:08:55AM Processes cleaned : 0
  12/23/2014 3:08:55AM Boot sectors scanned : 2
  12/23/2014 3:08:55AM Boot sectors detected: 0
  12/23/2014 3:08:55AM Boot sectors cleaned : 0
  12/23/2014 3:08:55AM Files scanned : 54
  12/23/2014 3:08:55AM Files with detections: 0
  12/23/2014 3:08:55AM File detections : 0
  12/23/2014 3:08:55AM Files cleaned : 0
  12/23/2014 3:08:55AM Files deleted : 0
  12/23/2014 3:08:55AM Files not scanned : 0
  12/23/2014 3:08:55AM Scan Summary (Registry Scanning)
  12/23/2014 3:08:55AM Keys scanned : 0
  12/23/2014 3:08:55AM Keys detected : 0
  12/23/2014 3:08:55AM Keys cleaned : 0
  12/23/2014 3:08:55AM Keys deleted : 0
  12/23/2014 3:08:55AM Run time : 0:00:12
  12/23/2014 3:08:55AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 16487:HEAD Source
------------------------------------------------------------------------  r16487 | hchen30 | 2014-12-08 22:41:58 -0800 (Mon, 08 Dec 2014) | 10 lines
  BaseTools/ECC: Fix some issues of ECC tool
  Add support for the usage which is defined in the above line for a Protocol/Ppi/Guid
  Add support for “!ERROR”
  Ignore issue of parsing a macro
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r16544 | ydong10 | 2014-12-21 18:21:53 -0800 (Sun, 21 Dec 2014) | 6 lines
  Fixed VfrCompile crash on efivarstore statement.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Aaron Pop <aaronp@ami.com>
  Reviewed-by: Eric Dong <eric.dong@intel.com>

------------------------------------------------------------------------  r16550 | yingke | 2014-12-22 21:48:31 -0800 (Mon, 22 Dec 2014) | 5 lines
  Fix ‘build run’ doesn’t work for NT32 X64 build.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Cinnamon Shia <cinnamon.shia@hp.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------