Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18320

This directory contains the Win32 binaries.

Build Date:       Wed, 26 Aug 2015 03:18:54 Pacific Daylight Time
Last Changed Rev: 18318

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18320
  BootSectImage Version 0.1 Build 18276
  Ecc.exe Version 0.01 Build 17712
  EfiLdrImage Version 0.1 Build 18276
  EfiRom Version 0.1 Build 18276
  GenBootSector Version 0.2 Build 18276
  GenCrc32 Version 0.2 Build 18276
 *GenDepex.exe Version 0.04 Build 18320
 *GenFds.exe 1.0 Build 18320
  GenFfs Version 0.1 Build 18276
  GenFv Version 0.1 Build 18276
  GenFw Version 0.2 Build 18276
  GenPage Version 0.2 Build 18276
 *GenPatchPcdTable.exe Version 0.10 Build 18320
  GenSec Version 0.1 Build 18276
  GenVtf Version 0.1 Build 18276
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 18276
  LzmaF86Compress Version 0.2 Build 18276
 *PatchPcdValue.exe Version 0.10 Build 18320
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 18276
 *TargetTool.exe Version 0.01 Build 18320
  TianoCompress Version 0.1 Build 18276
 *Trim.exe Version 0.10 Build 18320
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17927
  VfrCompile version  2.00 (UEFI 2.4) Build 18276
  VolInfo Version 0.83 Build 18276, Aug 24 2015
 *build.exe Version 0.60 Build 18320

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/26/2015 3:18:56AM Engine version = 5700.7163
  8/26/2015 3:18:56AM AntiVirus DAT version = 7903.0
  8/26/2015 3:18:56AM Number of detection signatures in EXTRA.DAT = None
  8/26/2015 3:18:56AM Names of detection signatures in EXTRA.DAT = None
  8/26/2015 3:18:56AM Scan Started On-Demand Scan
  8/26/2015 3:19:02AM Scan Summary
  8/26/2015 3:19:02AM Processes scanned : 0
  8/26/2015 3:19:02AM Processes detected : 0
  8/26/2015 3:19:02AM Processes cleaned : 0
  8/26/2015 3:19:02AM Boot sectors scanned : 2
  8/26/2015 3:19:02AM Boot sectors detected: 0
  8/26/2015 3:19:02AM Boot sectors cleaned : 0
  8/26/2015 3:19:02AM Files scanned : 55
  8/26/2015 3:19:02AM Files with detections: 0
  8/26/2015 3:19:02AM File detections : 0
  8/26/2015 3:19:02AM Files cleaned : 0
  8/26/2015 3:19:02AM Files deleted : 0
  8/26/2015 3:19:02AM Files not scanned : 0
  8/26/2015 3:19:02AM Scan Summary (Registry Scanning)
  8/26/2015 3:19:02AM Keys scanned : 0
  8/26/2015 3:19:02AM Keys detected : 0
  8/26/2015 3:19:02AM Keys cleaned : 0
  8/26/2015 3:19:02AM Keys deleted : 0
  8/26/2015 3:19:02AM Run time : 0:00:07
  8/26/2015 3:19:02AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18276:HEAD Source
------------------------------------------------------------------------  r18317 | yingke | 2015-08-25 23:28:59 -0700 (Tue, 25 Aug 2015) | 6 lines
  BaseTools: Nested !include support in DSC and FDF files
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Cecil Sheng <cecil.sheng@hp.com>
  Reviewed-by: Samer El-Haj-Mahmoud <elhaj@hp.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------  r18318 | lgao4 | 2015-08-25 23:33:31 -0700 (Tue, 25 Aug 2015) | 9 lines
  BaseTools: Fix the missing depex file in GenFds
  If FDF FfsRule describes |.depex for depex file on source build, it may
  be missed in the generated FD image. GenFds tool needs to check the
  output file list and find the matched one.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------