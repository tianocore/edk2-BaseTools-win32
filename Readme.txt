Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 16833

This directory contains the Win32 binaries.

Build Date:       Wed, 11 Feb 2015 03:10:27 Pacific Standard Time
Last Changed Rev: 16831

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 16814
  BootSectImage Version 0.1 Build 16164
  EfiLdrImage Version 0.1 Build 16164
  EfiRom Version 0.1 Build 16164
  GenBootSector Version 0.2 Build 16164
  GenCrc32 Version 0.2 Build 16164
  GenDepex.exe Version 0.04 Build 16814
  GenFds.exe 1.0 Build 16814
  GenFfs Version 0.1 Build 16164
  GenFv Version 0.1 Build 16164
 *GenFw Version 0.2 Build 16833
  GenPage Version 0.2 Build 16164
  GenPatchPcdTable.exe Version 0.10 Build 16814
  GenSec Version 0.1 Build 16164
  GenVtf Version 0.1 Build 16164
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 16164
  LzmaF86Compress Version 0.2 Build 16164
  PatchPcdValue.exe Version 0.10 Build 16814
  Rsa2048Sha256GenerateKeys Version 0.9 Build 16164
  Rsa2048Sha256Sign Version 0.9 Build 16164
  Split Version 0.1 Build 16164
  TargetTool.exe Version 0.01 Build 16814
  TianoCompress Version 0.1 Build 16164
  Trim.exe Version 0.10 Build 16814
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 16455
  VfrCompile version  2.00 (UEFI 2.4) Build 16591
  VolInfo Version 0.83 Build 16164, Sep 24 2014
  build.exe Version 0.60 Build 16814

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1247
  2/11/2015 3:10:29AM Engine version = 5700.7163
  2/11/2015 3:10:29AM AntiVirus DAT version = 7708.0
  2/11/2015 3:10:29AM Number of detection signatures in EXTRA.DAT = None
  2/11/2015 3:10:29AM Names of detection signatures in EXTRA.DAT = None
  2/11/2015 3:10:29AM Scan Started On-Demand Scan
  2/11/2015 3:13:30AM Scan Summary
  2/11/2015 3:13:30AM Processes scanned : 0
  2/11/2015 3:13:30AM Processes detected : 0
  2/11/2015 3:13:30AM Processes cleaned : 0
  2/11/2015 3:13:30AM Boot sectors scanned : 1
  2/11/2015 3:13:30AM Boot sectors detected: 0
  2/11/2015 3:13:30AM Boot sectors cleaned : 0
  2/11/2015 3:13:30AM Files scanned : 48
  2/11/2015 3:13:30AM Files with detections: 0
  2/11/2015 3:13:30AM File detections : 0
  2/11/2015 3:13:30AM Files cleaned : 0
  2/11/2015 3:13:30AM Files deleted : 0
  2/11/2015 3:13:30AM Files not scanned : 0
  2/11/2015 3:13:30AM Scan Summary (Registry Scanning)
  2/11/2015 3:13:30AM Keys scanned : 0
  2/11/2015 3:13:30AM Keys detected : 0
  2/11/2015 3:13:30AM Keys cleaned : 0
  2/11/2015 3:13:30AM Keys deleted : 0
  2/11/2015 3:13:30AM Run time : 0:03:01
  2/11/2015 3:13:30AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 16814:HEAD Source
------------------------------------------------------------------------  r16831 | lgao4 | 2015-02-11 00:20:17 -0800 (Wed, 11 Feb 2015) | 7 lines
  BaseTools/GenFw: Set the PE/COFF attribute BaseOfData with the address of the first '.data' section
  Before this change the alignment of the first data section was not taken into account.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Erik Bjorge <erik.c.bjorge@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------