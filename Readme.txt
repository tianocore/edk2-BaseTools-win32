Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18256

This directory contains the Win32 binaries.

Build Date:       Fri, 21 Aug 2015 03:18:37 Pacific Daylight Time
Last Changed Rev: 18256

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18256
  BootSectImage Version 0.1 Build 18094
  Ecc.exe Version 0.01 Build 17712
  EfiLdrImage Version 0.1 Build 18094
  EfiRom Version 0.1 Build 18094
  GenBootSector Version 0.2 Build 18094
  GenCrc32 Version 0.2 Build 18094
 *GenDepex.exe Version 0.04 Build 18256
 *GenFds.exe 1.0 Build 18256
  GenFfs Version 0.1 Build 18094
  GenFv Version 0.1 Build 18094
  GenFw Version 0.2 Build 18198
  GenPage Version 0.2 Build 18094
 *GenPatchPcdTable.exe Version 0.10 Build 18256
  GenSec Version 0.1 Build 18094
  GenVtf Version 0.1 Build 18094
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 18094
  LzmaF86Compress Version 0.2 Build 18094
 *PatchPcdValue.exe Version 0.10 Build 18256
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 18094
 *TargetTool.exe Version 0.01 Build 18256
  TianoCompress Version 0.1 Build 18094
 *Trim.exe Version 0.10 Build 18256
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17927
  VfrCompile version  2.00 (UEFI 2.4) Build 18094
  VolInfo Version 0.83 Build 18094, Jul 28 2015
 *build.exe Version 0.60 Build 18256

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/21/2015 3:18:39AM Engine version = 5700.7163
  8/21/2015 3:18:39AM AntiVirus DAT version = 7898.0
  8/21/2015 3:18:39AM Number of detection signatures in EXTRA.DAT = None
  8/21/2015 3:18:39AM Names of detection signatures in EXTRA.DAT = None
  8/21/2015 3:18:39AM Scan Started On-Demand Scan
  8/21/2015 3:18:44AM Scan Summary
  8/21/2015 3:18:44AM Processes scanned : 0
  8/21/2015 3:18:44AM Processes detected : 0
  8/21/2015 3:18:44AM Processes cleaned : 0
  8/21/2015 3:18:44AM Boot sectors scanned : 2
  8/21/2015 3:18:44AM Boot sectors detected: 0
  8/21/2015 3:18:44AM Boot sectors cleaned : 0
  8/21/2015 3:18:44AM Files scanned : 55
  8/21/2015 3:18:44AM Files with detections: 0
  8/21/2015 3:18:44AM File detections : 0
  8/21/2015 3:18:44AM Files cleaned : 0
  8/21/2015 3:18:44AM Files deleted : 0
  8/21/2015 3:18:44AM Files not scanned : 0
  8/21/2015 3:18:44AM Scan Summary (Registry Scanning)
  8/21/2015 3:18:44AM Keys scanned : 0
  8/21/2015 3:18:44AM Keys detected : 0
  8/21/2015 3:18:44AM Keys cleaned : 0
  8/21/2015 3:18:44AM Keys deleted : 0
  8/21/2015 3:18:44AM Run time : 0:00:05
  8/21/2015 3:18:44AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18212:HEAD Source
------------------------------------------------------------------------  r18256 | bobfeng | 2015-08-20 18:09:16 -0700 (Thu, 20 Aug 2015) | 8 lines
  BaseTools: Fix build fail when the number in validlist is long type.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: "Bob Feng" <bob.c.feng@intel.com>
  Reviewed-by: "Chen, Hesheng" <hesheng.chen@intel.com>

------------------------------------------------------------------------