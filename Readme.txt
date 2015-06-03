Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17553

This directory contains the Win32 binaries.

Build Date:       Wed, 03 Jun 2015 09:06:42 Pacific Daylight Time
Last Changed Rev: 17514

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Not available
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################

** ALL TOOLS WERE REBUILT **
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17553
  BootSectImage Version 0.1 Build 17553
  Ecc.exe Version 0.01 Build 17553
  EfiLdrImage Version 0.1 Build 17553
  EfiRom Version 0.1 Build 17553
  GenBootSector Version 0.2 Build 17553
  GenCrc32 Version 0.2 Build 17553
  GenDepex.exe Version 0.04 Build 17553
  GenFds.exe 1.0 Build 17553
  GenFfs Version 0.1 Build 17553
  GenFv Version 0.1 Build 17553
  GenFw Version 0.2 Build 17553
  GenPage Version 0.2 Build 17553
  GenPatchPcdTable.exe Version 0.10 Build 17553
  GenSec Version 0.1 Build 17553
  GenVtf Version 0.1 Build 17553
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 17553
  LzmaF86Compress Version 0.2 Build 17553
  PatchPcdValue.exe Version 0.10 Build 17553
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17553
  Split Version 0.1 Build 17553
  TargetTool.exe Version 0.01 Build 17553
  TianoCompress Version 0.1 Build 17553
  Trim.exe Version 0.10 Build 17553
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 17553
  VfrCompile version  2.00 (UEFI 2.4) Build 17553
  VolInfo Version 0.83 Build 17553, Jun  3 2015
  build.exe Version 0.60 Build 17553

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1263
  6/3/2015 9:06:44AM Engine version = 5700.7163
  6/3/2015 9:06:44AM AntiVirus DAT version = 7820.0
  6/3/2015 9:06:44AM Number of detection signatures in EXTRA.DAT = None
  6/3/2015 9:06:44AM Names of detection signatures in EXTRA.DAT = None
  6/3/2015 9:06:45AM Scan Started On-Demand Scan
  6/3/2015 9:07:10AM Scan Summary
  6/3/2015 9:07:10AM Processes scanned : 0
  6/3/2015 9:07:10AM Processes detected : 0
  6/3/2015 9:07:10AM Processes cleaned : 0
  6/3/2015 9:07:10AM Boot sectors scanned : 1
  6/3/2015 9:07:10AM Boot sectors detected: 0
  6/3/2015 9:07:10AM Boot sectors cleaned : 0
  6/3/2015 9:07:10AM Files scanned : 70
  6/3/2015 9:07:10AM Files with detections: 0
  6/3/2015 9:07:10AM File detections : 0
  6/3/2015 9:07:10AM Files cleaned : 0
  6/3/2015 9:07:10AM Files deleted : 0
  6/3/2015 9:07:10AM Files not scanned : 0
  6/3/2015 9:07:10AM Scan Summary (Registry Scanning)
  6/3/2015 9:07:10AM Keys scanned : 0
  6/3/2015 9:07:10AM Keys detected : 0
  6/3/2015 9:07:10AM Keys cleaned : 0
  6/3/2015 9:07:10AM Keys deleted : 0
  6/3/2015 9:07:10AM Run time : 0:00:27
  6/3/2015 9:07:10AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17514:HEAD Source
------------------------------------------------------------------------  r17514 | ydong10 | 2015-05-26 19:25:48 -0700 (Tue, 26 May 2015) | 6 lines
  BaseTools: Add reconnect request flag for question.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Eric Dong <eric.dong@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------
Force Rebuilding tools after resolving issue with SVN password
