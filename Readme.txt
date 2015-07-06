Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17823

This directory contains the Win32 binaries.

Build Date:       Mon, 06 Jul 2015 03:16:50 Pacific Daylight Time
Last Changed Rev: 17822

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17823
  BootSectImage Version 0.1 Build 17815
  Ecc.exe Version 0.01 Build 17712
  EfiLdrImage Version 0.1 Build 17815
  EfiRom Version 0.1 Build 17815
  GenBootSector Version 0.2 Build 17815
  GenCrc32 Version 0.2 Build 17815
 *GenDepex.exe Version 0.04 Build 17823
 *GenFds.exe 1.0 Build 17823
  GenFfs Version 0.1 Build 17815
  GenFv Version 0.1 Build 17815
  GenFw Version 0.2 Build 17815
  GenPage Version 0.2 Build 17815
 *GenPatchPcdTable.exe Version 0.10 Build 17823
  GenSec Version 0.1 Build 17815
  GenVtf Version 0.1 Build 17815
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 17815
  LzmaF86Compress Version 0.2 Build 17815
 *PatchPcdValue.exe Version 0.10 Build 17823
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 17815
 *TargetTool.exe Version 0.01 Build 17823
  TianoCompress Version 0.1 Build 17815
 *Trim.exe Version 0.10 Build 17823
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17674
  VfrCompile version  2.00 (UEFI 2.4) Build 17815
  VolInfo Version 0.83 Build 17815, Jul  2 2015
 *build.exe Version 0.60 Build 17823

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1263
  7/6/2015 3:16:51AM Engine version = 5700.7163
  7/6/2015 3:16:51AM AntiVirus DAT version = 7853.0
  7/6/2015 3:16:51AM Number of detection signatures in EXTRA.DAT = None
  7/6/2015 3:16:51AM Names of detection signatures in EXTRA.DAT = None
  7/6/2015 3:16:52AM Scan Started On-Demand Scan
  7/6/2015 3:17:12AM Scan Summary
  7/6/2015 3:17:12AM Processes scanned : 0
  7/6/2015 3:17:12AM Processes detected : 0
  7/6/2015 3:17:12AM Processes cleaned : 0
  7/6/2015 3:17:12AM Boot sectors scanned : 1
  7/6/2015 3:17:12AM Boot sectors detected: 0
  7/6/2015 3:17:12AM Boot sectors cleaned : 0
  7/6/2015 3:17:12AM Files scanned : 55
  7/6/2015 3:17:12AM Files with detections: 0
  7/6/2015 3:17:12AM File detections : 0
  7/6/2015 3:17:12AM Files cleaned : 0
  7/6/2015 3:17:12AM Files deleted : 0
  7/6/2015 3:17:12AM Files not scanned : 0
  7/6/2015 3:17:12AM Scan Summary (Registry Scanning)
  7/6/2015 3:17:12AM Keys scanned : 0
  7/6/2015 3:17:12AM Keys detected : 0
  7/6/2015 3:17:12AM Keys cleaned : 0
  7/6/2015 3:17:12AM Keys deleted : 0
  7/6/2015 3:17:12AM Run time : 0:00:21
  7/6/2015 3:17:12AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17821:HEAD Source
------------------------------------------------------------------------  r17822 | bobfeng | 2015-07-05 17:55:15 -0700 (Sun, 05 Jul 2015) | 6 lines
  BaseTools/Build: Fix the range expression evaluation error.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: "Bob Feng" <bob.c.feng@intel.com>
  Reviewed-by: "Chen, Hesheng" <hesheng.chen@intel.com>
  Reviewed-by: "Liu, Yingke D" <yingke.d.liu@intel.com>

------------------------------------------------------------------------