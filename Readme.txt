Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18182

This directory contains the Win32 binaries.

Build Date:       Thu, 06 Aug 2015 03:17:48 Pacific Daylight Time
Last Changed Rev: 18170

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18094
  BootSectImage Version 0.1 Build 18094
  Ecc.exe Version 0.01 Build 17712
  EfiLdrImage Version 0.1 Build 18094
  EfiRom Version 0.1 Build 18094
  GenBootSector Version 0.2 Build 18094
  GenCrc32 Version 0.2 Build 18094
  GenDepex.exe Version 0.04 Build 18094
  GenFds.exe 1.0 Build 18094
  GenFfs Version 0.1 Build 18094
  GenFv Version 0.1 Build 18094
  GenFw Version 0.2 Build 18094
  GenPage Version 0.2 Build 18094
  GenPatchPcdTable.exe Version 0.10 Build 18094
  GenSec Version 0.1 Build 18094
  GenVtf Version 0.1 Build 18094
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 18094
  LzmaF86Compress Version 0.2 Build 18094
  PatchPcdValue.exe Version 0.10 Build 18094
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 18094
  TargetTool.exe Version 0.01 Build 18094
  TianoCompress Version 0.1 Build 18094
 *Trim.exe Version 0.10 Build 18182
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17927
  VfrCompile version  2.00 (UEFI 2.4) Build 18094
  VolInfo Version 0.83 Build 18094, Jul 28 2015
  build.exe Version 0.60 Build 18094

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/6/2015 3:17:50AM Engine version = 5700.7163
  8/6/2015 3:17:50AM AntiVirus DAT version = 7884.0
  8/6/2015 3:17:50AM Number of detection signatures in EXTRA.DAT = None
  8/6/2015 3:17:50AM Names of detection signatures in EXTRA.DAT = None
  8/6/2015 3:17:50AM Scan Started On-Demand Scan
  8/6/2015 3:17:52AM Scan Summary
  8/6/2015 3:17:52AM Processes scanned : 0
  8/6/2015 3:17:52AM Processes detected : 0
  8/6/2015 3:17:52AM Processes cleaned : 0
  8/6/2015 3:17:52AM Boot sectors scanned : 1
  8/6/2015 3:17:52AM Boot sectors detected: 0
  8/6/2015 3:17:52AM Boot sectors cleaned : 0
  8/6/2015 3:17:52AM Files scanned : 55
  8/6/2015 3:17:52AM Files with detections: 0
  8/6/2015 3:17:52AM File detections : 0
  8/6/2015 3:17:52AM Files cleaned : 0
  8/6/2015 3:17:52AM Files deleted : 0
  8/6/2015 3:17:52AM Files not scanned : 0
  8/6/2015 3:17:52AM Scan Summary (Registry Scanning)
  8/6/2015 3:17:52AM Keys scanned : 0
  8/6/2015 3:17:52AM Keys detected : 0
  8/6/2015 3:17:52AM Keys cleaned : 0
  8/6/2015 3:17:52AM Keys deleted : 0
  8/6/2015 3:17:52AM Run time : 0:00:03
  8/6/2015 3:17:52AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18094:HEAD Source
------------------------------------------------------------------------  r18170 | yingke | 2015-08-06 01:05:59 -0700 (Thu, 06 Aug 2015) | 8 lines
  BaseTools/Trim: Fixed a bug that cannot trim long values
  The long value substitution must move to the front of
  HEX substitution, and updated build_rule to add --trim-long
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------