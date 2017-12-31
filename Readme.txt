Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26061

This directory contains the Win32 binaries.

Build Date:       Sun, 31 Dec 2017 03:14:37 Pacific Standard Time
Last Changed Rev: 26061

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26061
 *BootSectImage Version 1.0 Build Build 26061
 *Brotli Version 0.5.2 Build 26061
  Brotli Version 0.5.2 Build 26061
  Ecc.exe Version 1.0 Build Build 24602
 *EfiLdrImage Version 1.0 Build Build 26061
 *EfiRom Version 0.1 Build 26061
 *GenBootSector Version 0.2 Build 26061
 *GenCrc32 Version 0.2 Build 26061
 *GenDepex.exe Version 0.04 Build 26061
 *GenFds.exe 1.0 Build 26061
 *GenFfs Version 0.1 Build 26061
 *GenFv Version 0.1 Build 26061
 *GenFw Version 0.2 Build 26061
 *GenPage Version 0.2 Build 26061
 *GenPatchPcdTable.exe Version 0.10 Build 26061
 *GenSec Version 0.1 Build 26061
 *GenVtf Version 0.1 Build 26061
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 26061
  LzmaF86Compress Version 0.2 Build 26061
 *PatchPcdValue.exe Version 0.10 Build 26061
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
 *Split Version 1.0 Build Build 26061
 *TargetTool.exe Version 0.01 Build 26061
 *TianoCompress Version 0.1 Build 26061
 *Trim.exe Version 0.10 Build 26061
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 26061
 *VolInfo Version 1.0 Build Build 26061
 *build.exe Version 0.60 Build 26061

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/31/2017 3:14:44AM Engine version = 5900.7806
  12/31/2017 3:14:44AM AntiVirus DAT version = 8760.0
  12/31/2017 3:14:44AM Number of detection signatures in EXTRA.DAT = None
  12/31/2017 3:14:44AM Names of detection signatures in EXTRA.DAT = None
  12/31/2017 3:14:44AM Scan Started On-Demand Scan
  12/31/2017 3:15:09AM Scan Summary
  12/31/2017 3:15:09AM Processes scanned : 0
  12/31/2017 3:15:09AM Processes detected : 0
  12/31/2017 3:15:09AM Processes cleaned : 0
  12/31/2017 3:15:09AM Boot sectors scanned : 2
  12/31/2017 3:15:09AM Boot sectors detected: 0
  12/31/2017 3:15:09AM Boot sectors cleaned : 0
  12/31/2017 3:15:09AM Files scanned : 83
  12/31/2017 3:15:09AM Files with detections: 0
  12/31/2017 3:15:09AM File detections : 0
  12/31/2017 3:15:09AM Files cleaned : 0
  12/31/2017 3:15:09AM Files deleted : 0
  12/31/2017 3:15:09AM Files not scanned : 0
  12/31/2017 3:15:09AM Scan Summary (Registry Scanning)
  12/31/2017 3:15:09AM Keys scanned : 0
  12/31/2017 3:15:09AM Keys detected : 0
  12/31/2017 3:15:09AM Keys cleaned : 0
  12/31/2017 3:15:09AM Keys deleted : 0
  12/31/2017 3:15:09AM Run time : 0:00:25
  12/31/2017 3:15:09AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26060:HEAD Source
------------------------------------------------------------------------  r26060 | edk2buildsystem | 2017-12-28 19:27:28 -0800 (Thu, 28 Dec 2017) | 12 lines
  BaseTools: Fix the bug for QuarkPlatformPkg build failure
  The issue is that the string 'LPC' starts with the 'L' character and
  this is being confused with L" or L' for a Unicode string or Unicode
  character.
  Fixes:https://bugzilla.tianocore.org/show_bug.cgi?id=831
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f13f306b3b07330191ba4620e49c2a9151b8e575)

------------------------------------------------------------------------  r26061 | edk2buildsystem | 2017-12-31 02:05:31 -0800 (Sun, 31 Dec 2017) | 12 lines
  BaseTools: Add DevicePath support for PCD values
  Use C code parse device path to output hex string, and Python
  run command when PCD Value need device path parse.
  https://bugzilla.tianocore.org/show_bug.cgi?id=541
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 7dbc50bd244d95fdc1741b9cfc561f0bfd724de1)

------------------------------------------------------------------------