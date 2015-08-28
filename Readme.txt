Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18361

This directory contains the Win32 binaries.

Build Date:       Fri, 28 Aug 2015 03:18:37 Pacific Daylight Time
Last Changed Rev: 18339

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
 *GenFds.exe 1.0 Build 18361
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
  VfrCompile version  2.00 (UEFI 2.4) Build 18337
  VolInfo Version 0.83 Build 18276, Aug 24 2015
  build.exe Version 0.60 Build 18320

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/28/2015 3:18:38AM Engine version = 5700.7163
  8/28/2015 3:18:38AM AntiVirus DAT version = 7906.0
  8/28/2015 3:18:38AM Number of detection signatures in EXTRA.DAT = None
  8/28/2015 3:18:38AM Names of detection signatures in EXTRA.DAT = None
  8/28/2015 3:18:38AM Scan Started On-Demand Scan
  8/28/2015 3:18:44AM Scan Summary
  8/28/2015 3:18:44AM Processes scanned : 0
  8/28/2015 3:18:44AM Processes detected : 0
  8/28/2015 3:18:44AM Processes cleaned : 0
  8/28/2015 3:18:44AM Boot sectors scanned : 2
  8/28/2015 3:18:44AM Boot sectors detected: 0
  8/28/2015 3:18:44AM Boot sectors cleaned : 0
  8/28/2015 3:18:44AM Files scanned : 55
  8/28/2015 3:18:44AM Files with detections: 0
  8/28/2015 3:18:44AM File detections : 0
  8/28/2015 3:18:44AM Files cleaned : 0
  8/28/2015 3:18:44AM Files deleted : 0
  8/28/2015 3:18:44AM Files not scanned : 0
  8/28/2015 3:18:44AM Scan Summary (Registry Scanning)
  8/28/2015 3:18:44AM Keys scanned : 0
  8/28/2015 3:18:44AM Keys detected : 0
  8/28/2015 3:18:44AM Keys cleaned : 0
  8/28/2015 3:18:44AM Keys deleted : 0
  8/28/2015 3:18:44AM Run time : 0:00:06
  8/28/2015 3:18:44AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18337:HEAD Source
------------------------------------------------------------------------  r18339 | yingke | 2015-08-27 19:04:37 -0700 (Thu, 27 Aug 2015) | 8 lines
  BaseTools: Fixed bug for single FV generating.
  If -i is specified and this FV has no BlockSize defined,
  tool did not inherit FD's BlockSize.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------