Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17685

This directory contains the Win32 binaries.

Build Date:       Tue, 23 Jun 2015 03:16:15 Pacific Daylight Time
Last Changed Rev: 17685

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17685
  BootSectImage Version 0.1 Build 17553
  Ecc.exe Version 0.01 Build 17553
  EfiLdrImage Version 0.1 Build 17553
  EfiRom Version 0.1 Build 17553
  GenBootSector Version 0.2 Build 17553
  GenCrc32 Version 0.2 Build 17553
 *GenDepex.exe Version 0.04 Build 17685
 *GenFds.exe 1.0 Build 17685
  GenFfs Version 0.1 Build 17553
  GenFv Version 0.1 Build 17553
  GenFw Version 0.2 Build 17553
  GenPage Version 0.2 Build 17553
 *GenPatchPcdTable.exe Version 0.10 Build 17685
  GenSec Version 0.1 Build 17553
  GenVtf Version 0.1 Build 17553
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 17553
  LzmaF86Compress Version 0.2 Build 17553
 *PatchPcdValue.exe Version 0.10 Build 17685
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17553
  Split Version 0.1 Build 17553
 *TargetTool.exe Version 0.01 Build 17685
  TianoCompress Version 0.1 Build 17553
 *Trim.exe Version 0.10 Build 17685
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17674
  VfrCompile version  2.00 (UEFI 2.4) Build 17553
  VolInfo Version 0.83 Build 17553, Jun  3 2015
 *build.exe Version 0.60 Build 17685

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1263
  6/23/2015 3:16:16AM Engine version = 5700.7163
  6/23/2015 3:16:16AM AntiVirus DAT version = 7840.0
  6/23/2015 3:16:16AM Number of detection signatures in EXTRA.DAT = None
  6/23/2015 3:16:16AM Names of detection signatures in EXTRA.DAT = None
  6/23/2015 3:16:17AM Scan Started On-Demand Scan
  6/23/2015 3:16:27AM Scan Summary
  6/23/2015 3:16:27AM Processes scanned : 0
  6/23/2015 3:16:27AM Processes detected : 0
  6/23/2015 3:16:27AM Processes cleaned : 0
  6/23/2015 3:16:27AM Boot sectors scanned : 1
  6/23/2015 3:16:27AM Boot sectors detected: 0
  6/23/2015 3:16:27AM Boot sectors cleaned : 0
  6/23/2015 3:16:27AM Files scanned : 55
  6/23/2015 3:16:27AM Files with detections: 0
  6/23/2015 3:16:27AM File detections : 0
  6/23/2015 3:16:27AM Files cleaned : 0
  6/23/2015 3:16:27AM Files deleted : 0
  6/23/2015 3:16:27AM Files not scanned : 0
  6/23/2015 3:16:27AM Scan Summary (Registry Scanning)
  6/23/2015 3:16:27AM Keys scanned : 0
  6/23/2015 3:16:27AM Keys detected : 0
  6/23/2015 3:16:27AM Keys cleaned : 0
  6/23/2015 3:16:27AM Keys deleted : 0
  6/23/2015 3:16:27AM Run time : 0:00:11
  6/23/2015 3:16:27AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17674:HEAD Source
------------------------------------------------------------------------  r17678 | yingke | 2015-06-22 23:46:01 -0700 (Mon, 22 Jun 2015) | 5 lines
  BaseTools: Supported FMP capsule image.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r17679 | yingke | 2015-06-22 23:49:25 -0700 (Mon, 22 Jun 2015) | 5 lines
  BaseTools: Build report should not be generated if build failed.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r17680 | yingke | 2015-06-22 23:52:12 -0700 (Mon, 22 Jun 2015) | 7 lines
  BaseTools: Fix a bug that UNI file can't have comment after #include "file.uni"
  The 'include' regular expression cannot match spaces before or after this statement.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r17681 | yingke | 2015-06-22 23:59:45 -0700 (Mon, 22 Jun 2015) | 5 lines
  BaseTools: Fixed a bug that Build Report always uses DEC default value for VPD PCD.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r17682 | yingke | 2015-06-23 00:02:03 -0700 (Tue, 23 Jun 2015) | 7 lines
  BaseTools: The token values cannot be numeric same with different PCDs.
  Current check only compared string format of toke value.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r17685 | bobfeng | 2015-06-23 01:45:06 -0700 (Tue, 23 Jun 2015) | 5 lines
  BaseTools/Build: Add error report for incorrect syntax in DEC file.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: "Bob Feng" <bob.c.feng@intel.com>
  Reviewed-by: Laszlo Ersek <lersek@redhat.com>

------------------------------------------------------------------------