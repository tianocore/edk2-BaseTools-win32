Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18337

This directory contains the Win32 binaries.

Build Date:       Thu, 27 Aug 2015 03:18:47 Pacific Daylight Time
Last Changed Rev: 18336

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18320
  BootSectImage Version 0.1 Build 18276
  Ecc.exe Version 0.01 Build 17712
  EfiLdrImage Version 0.1 Build 18276
  EfiRom Version 0.1 Build 18276
  GenBootSector Version 0.2 Build 18276
  GenCrc32 Version 0.2 Build 18276
  GenDepex.exe Version 0.04 Build 18320
  GenFds.exe 1.0 Build 18320
  GenFfs Version 0.1 Build 18276
  GenFv Version 0.1 Build 18276
  GenFw Version 0.2 Build 18276
  GenPage Version 0.2 Build 18276
  GenPatchPcdTable.exe Version 0.10 Build 18320
  GenSec Version 0.1 Build 18276
  GenVtf Version 0.1 Build 18276
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 18276
  LzmaF86Compress Version 0.2 Build 18276
  PatchPcdValue.exe Version 0.10 Build 18320
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 18276
  TargetTool.exe Version 0.01 Build 18320
  TianoCompress Version 0.1 Build 18276
  Trim.exe Version 0.10 Build 18320
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17927
 *VfrCompile version  2.00 (UEFI 2.4) Build 18337
  VolInfo Version 0.83 Build 18276, Aug 24 2015
  build.exe Version 0.60 Build 18320

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/27/2015 3:18:48AM Engine version = 5700.7163
  8/27/2015 3:18:48AM AntiVirus DAT version = 7905.0
  8/27/2015 3:18:48AM Number of detection signatures in EXTRA.DAT = None
  8/27/2015 3:18:48AM Names of detection signatures in EXTRA.DAT = None
  8/27/2015 3:18:48AM Scan Started On-Demand Scan
  8/27/2015 3:19:03AM Scan Summary
  8/27/2015 3:19:03AM Processes scanned : 0
  8/27/2015 3:19:03AM Processes detected : 0
  8/27/2015 3:19:03AM Processes cleaned : 0
  8/27/2015 3:19:03AM Boot sectors scanned : 1
  8/27/2015 3:19:03AM Boot sectors detected: 0
  8/27/2015 3:19:03AM Boot sectors cleaned : 0
  8/27/2015 3:19:03AM Files scanned : 55
  8/27/2015 3:19:03AM Files with detections: 0
  8/27/2015 3:19:03AM File detections : 0
  8/27/2015 3:19:03AM Files cleaned : 0
  8/27/2015 3:19:03AM Files deleted : 0
  8/27/2015 3:19:03AM Files not scanned : 0
  8/27/2015 3:19:03AM Scan Summary (Registry Scanning)
  8/27/2015 3:19:03AM Keys scanned : 0
  8/27/2015 3:19:03AM Keys detected : 0
  8/27/2015 3:19:03AM Keys cleaned : 0
  8/27/2015 3:19:03AM Keys deleted : 0
  8/27/2015 3:19:03AM Run time : 0:00:15
  8/27/2015 3:19:03AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18320:HEAD Source
------------------------------------------------------------------------  r18336 | dandanbi | 2015-08-27 01:19:40 -0700 (Thu, 27 Aug 2015) | 5 lines
  BaseTools:To generate string default type correctly in VfrCompiler
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------