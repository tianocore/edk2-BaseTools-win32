Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22854

This directory contains the Win32 binaries.

Build Date:       Fri, 21 Oct 2016 09:30:49 Pacific Daylight Time
Last Changed Rev: 22852

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################

** ALL TOOLS WERE REBUILT **
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22854
  BootSectImage Version 1.0 Build Build 22854
  Ecc.exe Version 1.0 Build Build 22854
  EfiLdrImage Version 1.0 Build Build 22854
  EfiRom Version 0.1 Build 22854
  GenBootSector Version 0.2 Build 22854
  GenCrc32 Version 0.2 Build 22854
  GenDepex.exe Version 0.04 Build 22854
  GenFds.exe 1.0 Build 22854
  GenFfs Version 0.1 Build 22854
  GenFv Version 0.1 Build 22854
  GenFw Version 0.2 Build 22854
  GenPage Version 0.2 Build 22854
  GenPatchPcdTable.exe Version 0.10 Build 22854
  GenSec Version 0.1 Build 22854
  GenVtf Version 0.1 Build 22854
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 22854
  LzmaF86Compress Version 0.2 Build 22854
  PatchPcdValue.exe Version 0.10 Build 22854
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 22854
  TargetTool.exe Version 0.01 Build 22854
  TianoCompress Version 0.1 Build 22854
  Trim.exe Version 0.10 Build 22854
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22854
  VolInfo Version 1.0 Build Build 22854
  build.exe Version 0.60 Build 22854

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/21/2016 9:30:51AM Engine version = 5700.7163
  10/21/2016 9:30:51AM AntiVirus DAT version = 8325.0
  10/21/2016 9:30:51AM Number of detection signatures in EXTRA.DAT = None
  10/21/2016 9:30:51AM Names of detection signatures in EXTRA.DAT = None
  10/21/2016 9:30:51AM Scan Started On-Demand Scan
  10/21/2016 9:31:01AM Scan Summary
  10/21/2016 9:31:01AM Processes scanned : 0
  10/21/2016 9:31:01AM Processes detected : 0
  10/21/2016 9:31:01AM Processes cleaned : 0
  10/21/2016 9:31:01AM Boot sectors scanned : 2
  10/21/2016 9:31:01AM Boot sectors detected: 0
  10/21/2016 9:31:01AM Boot sectors cleaned : 0
  10/21/2016 9:31:01AM Files scanned : 77
  10/21/2016 9:31:01AM Files with detections: 0
  10/21/2016 9:31:01AM File detections : 0
  10/21/2016 9:31:01AM Files cleaned : 0
  10/21/2016 9:31:01AM Files deleted : 0
  10/21/2016 9:31:01AM Files not scanned : 0
  10/21/2016 9:31:01AM Scan Summary (Registry Scanning)
  10/21/2016 9:31:01AM Keys scanned : 0
  10/21/2016 9:31:01AM Keys detected : 0
  10/21/2016 9:31:01AM Keys cleaned : 0
  10/21/2016 9:31:01AM Keys deleted : 0
  10/21/2016 9:31:01AM Run time : 0:00:11
  10/21/2016 9:31:01AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22845:HEAD Source
------------------------------------------------------------------------  r22852 | edk2buildsystem | 2016-10-21 02:07:45 -0700 (Fri, 21 Oct 2016) | 9 lines
  BaseTools VS Makefile: Use /MT in replace of /MD to remove specific dll
  /MD option will introduce the specific version dll dependency. It will cause
  the compiled C tools not work on some system.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit c4260115f0fcf23d538dc0ac90443ee954c30c6d)

------------------------------------------------------------------------
"Rebuilding
