Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20274

This directory contains the Win32 binaries.

Build Date:       Mon, 14 Mar 2016 15:09:53 Pacific Daylight Time
Last Changed Rev: 20234

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20274
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20182
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
  GenDepex.exe Version 0.04 Build 20182
  GenFds.exe 1.0 Build 20208
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
  GenPatchPcdTable.exe Version 0.10 Build 20182
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
  PatchPcdValue.exe Version 0.10 Build 20182
  Rsa2048Sha256GenerateKeys Version 0.9 Build 19914
  Rsa2048Sha256Sign Version 0.9 Build 19914
  Split Version 1.0 Build Build 20182
  TargetTool.exe Version 0.01 Build 20182
  TianoCompress Version 0.1 Build 19914
  Trim.exe Version 0.10 Build 20208
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20212
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20182
  build.exe Version 0.60 Build 20208

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/14/2016 3:09:54PM Engine version = 5700.7163
  3/14/2016 3:09:54PM AntiVirus DAT version = 8098.0
  3/14/2016 3:09:54PM Number of detection signatures in EXTRA.DAT = None
  3/14/2016 3:09:54PM Names of detection signatures in EXTRA.DAT = None
  3/14/2016 3:09:54PM Scan Started On-Demand Scan
  3/14/2016 3:09:59PM Scan Summary
  3/14/2016 3:09:59PM Processes scanned : 0
  3/14/2016 3:09:59PM Processes detected : 0
  3/14/2016 3:09:59PM Processes cleaned : 0
  3/14/2016 3:09:59PM Boot sectors scanned : 2
  3/14/2016 3:09:59PM Boot sectors detected: 0
  3/14/2016 3:09:59PM Boot sectors cleaned : 0
  3/14/2016 3:09:59PM Files scanned : 55
  3/14/2016 3:09:59PM Files with detections: 0
  3/14/2016 3:09:59PM File detections : 0
  3/14/2016 3:09:59PM Files cleaned : 0
  3/14/2016 3:09:59PM Files deleted : 0
  3/14/2016 3:09:59PM Files not scanned : 0
  3/14/2016 3:09:59PM Scan Summary (Registry Scanning)
  3/14/2016 3:09:59PM Keys scanned : 0
  3/14/2016 3:09:59PM Keys detected : 0
  3/14/2016 3:09:59PM Keys cleaned : 0
  3/14/2016 3:09:59PM Keys deleted : 0
  3/14/2016 3:09:59PM Run time : 0:00:05
  3/14/2016 3:09:59PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20212:HEAD Source
------------------------------------------------------------------------  r20234 | edk2buildsystem | 2016-03-14 10:21:00 -0700 (Mon, 14 Mar 2016) | 10 lines
  BaseTools/BPDG: Fix the bug to get the PCD Size
  The original bug is only consider int format of PcdSize, but forgot the
  Hex format. The fix is use the already exist variable PCD.PcdBinSize
  which done to translate PCD size cover both format.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 53c1329529e47a7da3a0bb5169b5fe0b44f4307e)

------------------------------------------------------------------------