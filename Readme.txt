Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 16562

This directory contains the Win32 binaries.

Build Date:       Tue, 30 Dec 2014 03:09:11 Pacific Standard Time
Last Changed Rev: 16561

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
 *VfrCompile version  2.00 (UEFI 2.4) Build 16562
  VolInfo Version 0.83 Build 16164, Sep 24 2014
  build.exe Version 0.60 Build 16555

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1247
  12/30/2014 3:09:14AM Engine version = 5600.1067
  12/30/2014 3:09:14AM AntiVirus DAT version = 7666.0
  12/30/2014 3:09:14AM Number of detection signatures in EXTRA.DAT = None
  12/30/2014 3:09:14AM Names of detection signatures in EXTRA.DAT = None
  12/30/2014 3:09:14AM Scan Started On-Demand Scan
  12/30/2014 3:09:26AM Scan Summary
  12/30/2014 3:09:26AM Processes scanned : 0
  12/30/2014 3:09:26AM Processes detected : 0
  12/30/2014 3:09:26AM Processes cleaned : 0
  12/30/2014 3:09:26AM Boot sectors scanned : 2
  12/30/2014 3:09:26AM Boot sectors detected: 0
  12/30/2014 3:09:26AM Boot sectors cleaned : 0
  12/30/2014 3:09:26AM Files scanned : 48
  12/30/2014 3:09:26AM Files with detections: 0
  12/30/2014 3:09:26AM File detections : 0
  12/30/2014 3:09:26AM Files cleaned : 0
  12/30/2014 3:09:26AM Files deleted : 0
  12/30/2014 3:09:26AM Files not scanned : 0
  12/30/2014 3:09:26AM Scan Summary (Registry Scanning)
  12/30/2014 3:09:26AM Keys scanned : 0
  12/30/2014 3:09:26AM Keys detected : 0
  12/30/2014 3:09:26AM Keys cleaned : 0
  12/30/2014 3:09:26AM Keys deleted : 0
  12/30/2014 3:09:26AM Run time : 0:00:12
  12/30/2014 3:09:26AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 16555:HEAD Source
------------------------------------------------------------------------  r16561 | ydong10 | 2014-12-29 19:03:37 -0800 (Mon, 29 Dec 2014) | 4 lines
  Rollback change 16544.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Eric Dong <eric.dong@intel.com>

------------------------------------------------------------------------