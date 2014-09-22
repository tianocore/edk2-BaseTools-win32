Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 16154

This directory contains the Win32 binaries.

Build Date:       Mon, 22 Sep 2014 03:01:33 Pacific Daylight Time
Last Changed Rev: 16154

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 16114
  BootSectImage Version 0.1 Build 16068
  EfiLdrImage Version 0.1 Build 16068
  EfiRom Version 0.1 Build 16068
  GenBootSector Version 0.2 Build 16068
  GenCrc32 Version 0.2 Build 16068
  GenDepex.exe Version 0.04 Build 16114
  GenFds.exe 1.0 Build 16114
  GenFfs Version 0.1 Build 16068
  GenFv Version 0.1 Build 16068
  GenFw Version 0.2 Build 16068
  GenPage Version 0.2 Build 16068
  GenPatchPcdTable.exe Version 0.10 Build 16114
  GenSec Version 0.1 Build 16068
  GenVtf Version 0.1 Build 16068
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 16068
  LzmaF86Compress Version 0.2 Build 16068
  PatchPcdValue.exe Version 0.10 Build 16114
  Rsa2048Sha256GenerateKeys Version 0.9 Build 16068
  Rsa2048Sha256Sign Version 0.9 Build 16068
  Split Version 0.1 Build 16068
  TargetTool.exe Version 0.01 Build 16114
  TianoCompress Version 0.1 Build 16068
  Trim.exe Version 0.10 Build 16114
 *Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 16154
  VfrCompile version  2.00 (UEFI 2.4) Build 16068
  VolInfo Version 0.83 Build 16068, Sep  9 2014
  build.exe Version 0.60 Build 16114

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.975
  9/22/2014 3:01:34AM Engine version = 5400.1158
  9/22/2014 3:01:34AM AntiVirus DAT version = 7568.0
  9/22/2014 3:01:34AM Number of detection signatures in EXTRA.DAT = None
  9/22/2014 3:01:34AM Names of detection signatures in EXTRA.DAT = None
  9/22/2014 3:01:34AM Scan Started On-Demand Scan
  9/22/2014 3:01:42AM Scan Summary
  9/22/2014 3:01:42AM Processes scanned : 0
  9/22/2014 3:01:42AM Processes detected : 0
  9/22/2014 3:01:42AM Processes cleaned : 0
  9/22/2014 3:01:42AM Boot sectors scanned : 2
  9/22/2014 3:01:42AM Boot sectors detected: 0
  9/22/2014 3:01:42AM Boot sectors cleaned : 0
  9/22/2014 3:01:42AM Files scanned : 69
  9/22/2014 3:01:42AM Files with detections: 0
  9/22/2014 3:01:42AM File detections : 0
  9/22/2014 3:01:42AM Files cleaned : 0
  9/22/2014 3:01:42AM Files deleted : 0
  9/22/2014 3:01:42AM Files not scanned : 0
  9/22/2014 3:01:42AM Scan Summary (Registry Scanning)
  9/22/2014 3:01:42AM Keys scanned : 0
  9/22/2014 3:01:42AM Keys detected : 0
  9/22/2014 3:01:42AM Keys cleaned : 0
  9/22/2014 3:01:42AM Keys deleted : 0
  9/22/2014 3:01:42AM Scan Summary (Cookie Scanning)
  9/22/2014 3:01:42AM Cookies scanned : 0
  9/22/2014 3:01:42AM Cookies detected : 0
  9/22/2014 3:01:42AM Cookies cleaned : 0
  9/22/2014 3:01:42AM Cookies deleted : 0
  9/22/2014 3:01:42AM Run time : 0:00:08
  9/22/2014 3:01:42AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 16149:HEAD Source
------------------------------------------------------------------------  r16149 | hchen30 | 2014-09-18 19:04:08 -0700 (Thu, 18 Sep 2014) | 9 lines
  BaseTools/Upt: Fix several bugs
  1. Fix a bug of packaging a full path file in zip at Linux.
  2. Fix a format error of generating Hob/Event/BootMode information.
  3. Fix a bug of generating additional “GUID” subtype for “UNDEFINED” guid.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@Intel.com>

------------------------------------------------------------------------  r16153 | hchen30 | 2014-09-22 00:06:12 -0700 (Mon, 22 Sep 2014) | 8 lines
  BaseTools/Upt: Fix several bugs
  1. Fix a bug of generating additional EOL in file header.
  2. Fix a bug of format error for Defines section.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@Intel.com>

------------------------------------------------------------------------  r16154 | hchen30 | 2014-09-22 00:37:28 -0700 (Mon, 22 Sep 2014) | 7 lines
  BaseTools/ECC: Ignore duplicate check for 'NULL' library
  Update a checkpoint to ignore duplicate check for 'NULL' library
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@Intel.com>

------------------------------------------------------------------------