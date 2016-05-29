Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 21006

This directory contains the Win32 binaries.

Build Date:       Sun, 29 May 2016 03:11:23 Pacific Daylight Time
Last Changed Rev: 20996

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 21006
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
 *GenDepex.exe Version 0.04 Build 21006
 *GenFds.exe 1.0 Build 21006
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 20909
  GenFw Version 0.2 Build 20909
  GenPage Version 0.2 Build 20909
 *GenPatchPcdTable.exe Version 0.10 Build 21006
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
 *PatchPcdValue.exe Version 0.10 Build 21006
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
 *TargetTool.exe Version 0.01 Build 21006
  TianoCompress Version 0.1 Build 20909
 *Trim.exe Version 0.10 Build 21006
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20909
  VolInfo Version 1.0 Build Build 20909
 *build.exe Version 0.60 Build 21006

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/29/2016 3:11:24AM Engine version = 5700.7163
  5/29/2016 3:11:24AM AntiVirus DAT version = 8179.0
  5/29/2016 3:11:24AM Number of detection signatures in EXTRA.DAT = 1
  5/29/2016 3:11:24AM Names of detection signatures in EXTRA.DAT = W97M/Downloader.bdj (ED)
  5/29/2016 3:11:24AM Scan Started On-Demand Scan
  5/29/2016 3:11:27AM Scan Summary
  5/29/2016 3:11:27AM Processes scanned : 0
  5/29/2016 3:11:27AM Processes detected : 0
  5/29/2016 3:11:27AM Processes cleaned : 0
  5/29/2016 3:11:27AM Boot sectors scanned : 1
  5/29/2016 3:11:27AM Boot sectors detected: 0
  5/29/2016 3:11:27AM Boot sectors cleaned : 0
  5/29/2016 3:11:27AM Files scanned : 55
  5/29/2016 3:11:27AM Files with detections: 0
  5/29/2016 3:11:27AM File detections : 0
  5/29/2016 3:11:27AM Files cleaned : 0
  5/29/2016 3:11:27AM Files deleted : 0
  5/29/2016 3:11:27AM Files not scanned : 0
  5/29/2016 3:11:27AM Scan Summary (Registry Scanning)
  5/29/2016 3:11:27AM Keys scanned : 0
  5/29/2016 3:11:27AM Keys detected : 0
  5/29/2016 3:11:27AM Keys cleaned : 0
  5/29/2016 3:11:27AM Keys deleted : 0
  5/29/2016 3:11:27AM Run time : 0:00:03
  5/29/2016 3:11:27AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20993:HEAD Source
------------------------------------------------------------------------  r20996 | edk2buildsystem | 2016-05-27 09:16:28 -0700 (Fri, 27 May 2016) | 8 lines
  BaseTools: Fix bad macro expansion during tools_def.txt parsing
  this is something I missed in 8ac46e4
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Michael Zimmermann <sigmaepsilon92@gmail.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 6608330d76d50746aeba63a032d85a5389164a54)

------------------------------------------------------------------------