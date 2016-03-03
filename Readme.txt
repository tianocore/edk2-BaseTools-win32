Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 20165, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20119

This directory contains the Win32 binaries.

Build Date:       Thu, 03 Mar 2016 10:06:20 Pacific Standard Time
Last Changed Rev: 20090

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 19914
  BootSectImage Version 1.0 Build Build 19914
  Ecc.exe Version 1.0 Build Build 19914
  EfiLdrImage Version 1.0 Build Build 19914
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
  GenDepex.exe Version 0.04 Build 19914
  GenFds.exe 1.0 Build 19914
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 19914
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
  GenPatchPcdTable.exe Version 0.10 Build 19914
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
  PatchPcdValue.exe Version 0.10 Build 19914
  Rsa2048Sha256GenerateKeys Version 0.9 Build 19914
  Rsa2048Sha256Sign Version 0.9 Build 19914
  Split Version 1.0 Build Build 19914
  TargetTool.exe Version 0.01 Build 19914
  TianoCompress Version 0.1 Build 19914
  Trim.exe Version 0.10 Build 19914
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 19914
  VfrCompile version  2.01 (UEFI 2.4) Build Build 19914
  VolInfo Version 1.0 Build Build 19914
  build.exe Version 0.60 Build 19914

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/3/2016 10:06:21AM Engine version = 5700.7163
  3/3/2016 10:06:21AM AntiVirus DAT version = 8092.0
  3/3/2016 10:06:21AM Number of detection signatures in EXTRA.DAT = None
  3/3/2016 10:06:21AM Names of detection signatures in EXTRA.DAT = None
  3/3/2016 10:06:21AM Scan Started On-Demand Scan
  3/3/2016 10:06:23AM Scan Summary
  3/3/2016 10:06:23AM Processes scanned : 0
  3/3/2016 10:06:23AM Processes detected : 0
  3/3/2016 10:06:23AM Processes cleaned : 0
  3/3/2016 10:06:23AM Boot sectors scanned : 1
  3/3/2016 10:06:23AM Boot sectors detected: 0
  3/3/2016 10:06:23AM Boot sectors cleaned : 0
  3/3/2016 10:06:23AM Files scanned : 55
  3/3/2016 10:06:23AM Files with detections: 0
  3/3/2016 10:06:23AM File detections : 0
  3/3/2016 10:06:23AM Files cleaned : 0
  3/3/2016 10:06:23AM Files deleted : 0
  3/3/2016 10:06:23AM Files not scanned : 0
  3/3/2016 10:06:23AM Scan Summary (Registry Scanning)
  3/3/2016 10:06:23AM Keys scanned : 0
  3/3/2016 10:06:23AM Keys detected : 0
  3/3/2016 10:06:23AM Keys cleaned : 0
  3/3/2016 10:06:23AM Keys deleted : 0
  3/3/2016 10:06:23AM Run time : 0:00:02
  3/3/2016 10:06:23AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20059:HEAD Source
------------------------------------------------------------------------  r20090 | edk2buildsystem | 2016-03-03 09:57:55 -0800 (Thu, 03 Mar 2016) | 12 lines
  BaseTools/LZMA: fix the format issue for last patch
  There are no functional changes in this patch. fixing the format base on
  last commit.
  The only change is 1) add back the blank line, which can help we better
  compare with the original LZMA source code. 2) remove the indent of
  #ifndef and #endif.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b9da8fe0e3a1353af0f5d698f449210908bab491)

------------------------------------------------------------------------