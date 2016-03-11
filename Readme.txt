Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20208

This directory contains the Win32 binaries.

Build Date:       Fri, 11 Mar 2016 03:31:56 Pacific Standard Time
Last Changed Rev: 20197

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20182
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20182
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
  GenDepex.exe Version 0.04 Build 20182
 *GenFds.exe 1.0 Build 20208
  GenFfs Version 0.1 Build 19914
 *GenFv Version 0.1 Build 20208
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
 *Trim.exe Version 0.10 Build 20208
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20182
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20182
 *build.exe Version 0.60 Build 20208

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/11/2016 3:31:58AM Engine version = 5700.7163
  3/11/2016 3:31:58AM AntiVirus DAT version = 8098.0
  3/11/2016 3:31:58AM Number of detection signatures in EXTRA.DAT = None
  3/11/2016 3:31:58AM Names of detection signatures in EXTRA.DAT = None
  3/11/2016 3:31:58AM Scan Started On-Demand Scan
  3/11/2016 3:32:08AM Scan Summary
  3/11/2016 3:32:08AM Processes scanned : 0
  3/11/2016 3:32:08AM Processes detected : 0
  3/11/2016 3:32:08AM Processes cleaned : 0
  3/11/2016 3:32:08AM Boot sectors scanned : 2
  3/11/2016 3:32:08AM Boot sectors detected: 0
  3/11/2016 3:32:08AM Boot sectors cleaned : 0
  3/11/2016 3:32:08AM Files scanned : 56
  3/11/2016 3:32:08AM Files with detections: 0
  3/11/2016 3:32:08AM File detections : 0
  3/11/2016 3:32:08AM Files cleaned : 0
  3/11/2016 3:32:08AM Files deleted : 0
  3/11/2016 3:32:08AM Files not scanned : 0
  3/11/2016 3:32:08AM Scan Summary (Registry Scanning)
  3/11/2016 3:32:08AM Keys scanned : 0
  3/11/2016 3:32:08AM Keys detected : 0
  3/11/2016 3:32:08AM Keys cleaned : 0
  3/11/2016 3:32:08AM Keys deleted : 0
  3/11/2016 3:32:08AM Run time : 0:00:11
  3/11/2016 3:32:08AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20182:HEAD Source
------------------------------------------------------------------------  r20183 | edk2buildsystem | 2016-03-10 14:07:18 -0800 (Thu, 10 Mar 2016) | 10 lines
  BaseTools: Update ARM/AArch64 GenFv vector processing for encapsulated FVs
  Instead of only handling SEC Core or PEI Core instances in the outer FV,
  the GenFv tool will now recurse into FV image FFS files to look for instances
  in encapsulated FVs so the vector area can be updated appropriately.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Eugene Cohen <eugene@hp.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit eca22f362cd5f008ba2c1f1a3b4f122b206e0a1c)

------------------------------------------------------------------------  r20197 | edk2buildsystem | 2016-03-11 02:26:29 -0800 (Fri, 11 Mar 2016) | 10 lines
  BaseTools: update the mail address for stack trace info
  Update the mail address from edk2-devel@lists.sourceforge.net to
  edk2-devel@lists.01.org.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Andrew Fish <afish@apple.com>
  (cherry picked from commit 3a0f8bdef348a3afca72217d319bb1a8d8b1036a)

------------------------------------------------------------------------