Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17336

This directory contains the Win32 binaries.

Build Date:       Wed, 06 May 2015 03:06:38 Pacific Daylight Time
Last Changed Rev: 17335

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17164
  BootSectImage Version 0.1 Build 16164
  Ecc.exe Version 0.01 Build 17164
  EfiLdrImage Version 0.1 Build 16164
  EfiRom Version 0.1 Build 16164
  GenBootSector Version 0.2 Build 16164
  GenCrc32 Version 0.2 Build 16164
  GenDepex.exe Version 0.04 Build 17164
  GenFds.exe 1.0 Build 17164
  GenFfs Version 0.1 Build 16164
  GenFv Version 0.1 Build 16164
  GenFw Version 0.2 Build 16833
  GenPage Version 0.2 Build 16164
  GenPatchPcdTable.exe Version 0.10 Build 17164
  GenSec Version 0.1 Build 16164
  GenVtf Version 0.1 Build 16164
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 16164
  LzmaF86Compress Version 0.2 Build 16164
  PatchPcdValue.exe Version 0.10 Build 17164
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17164
  Rsa2048Sha256Sign Version 0.9 Build 17164
  Split Version 0.1 Build 16164
  TargetTool.exe Version 0.01 Build 17164
  TianoCompress Version 0.1 Build 16164
  Trim.exe Version 0.10 Build 17164
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 17164
 *VfrCompile version  2.00 (UEFI 2.4) Build 17336
  VolInfo Version 0.83 Build 16164, Sep 24 2014
  build.exe Version 0.60 Build 17164

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1247
  5/6/2015 3:06:39AM Engine version = 5700.7163
  5/6/2015 3:06:39AM AntiVirus DAT version = 7791.0
  5/6/2015 3:06:39AM Number of detection signatures in EXTRA.DAT = None
  5/6/2015 3:06:39AM Names of detection signatures in EXTRA.DAT = None
  5/6/2015 3:06:39AM Scan Started On-Demand Scan
  5/6/2015 3:06:52AM Scan Summary
  5/6/2015 3:06:52AM Processes scanned : 0
  5/6/2015 3:06:52AM Processes detected : 0
  5/6/2015 3:06:52AM Processes cleaned : 0
  5/6/2015 3:06:52AM Boot sectors scanned : 2
  5/6/2015 3:06:52AM Boot sectors detected: 0
  5/6/2015 3:06:52AM Boot sectors cleaned : 0
  5/6/2015 3:06:52AM Files scanned : 51
  5/6/2015 3:06:52AM Files with detections: 0
  5/6/2015 3:06:52AM File detections : 0
  5/6/2015 3:06:52AM Files cleaned : 0
  5/6/2015 3:06:52AM Files deleted : 0
  5/6/2015 3:06:52AM Files not scanned : 0
  5/6/2015 3:06:52AM Scan Summary (Registry Scanning)
  5/6/2015 3:06:52AM Keys scanned : 0
  5/6/2015 3:06:52AM Keys detected : 0
  5/6/2015 3:06:52AM Keys cleaned : 0
  5/6/2015 3:06:52AM Keys deleted : 0
  5/6/2015 3:06:52AM Run time : 0:00:13
  5/6/2015 3:06:52AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17335:HEAD Source
------------------------------------------------------------------------  r17335 | ydong10 | 2015-05-06 02:35:14 -0700 (Wed, 06 May 2015) | 5 lines
  BaseTools: Enable buffer type value for default and oneofoption opcode.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Eric Dong <eric.dong@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------