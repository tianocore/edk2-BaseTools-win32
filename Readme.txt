Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22810

This directory contains the Win32 binaries.

Build Date:       Mon, 17 Oct 2016 03:11:04 Pacific Daylight Time
Last Changed Rev: 22810

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22700
  BootSectImage Version 1.0 Build Build 22449
  Ecc.exe Version 1.0 Build Build 22700
  EfiLdrImage Version 1.0 Build Build 22752
  EfiRom Version 0.1 Build 22617
  GenBootSector Version 0.2 Build 22449
  GenCrc32 Version 0.2 Build 22449
  GenDepex.exe Version 0.04 Build 22700
  GenFds.exe 1.0 Build 22801
  GenFfs Version 0.1 Build 22449
  GenFv Version 0.1 Build 22543
  GenFw Version 0.2 Build 22466
  GenPage Version 0.2 Build 22449
  GenPatchPcdTable.exe Version 0.10 Build 22700
  GenSec Version 0.1 Build 22449
  GenVtf Version 0.1 Build 22752
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 22449
  LzmaF86Compress Version 0.2 Build 22449
  PatchPcdValue.exe Version 0.10 Build 22700
 *Pkcs7Sign Version 0.9 Build 22810
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 22444
  Split Version 1.0 Build Build 22449
  TargetTool.exe Version 0.01 Build 22700
  TianoCompress Version 0.1 Build 22449
  Trim.exe Version 0.10 Build 22700
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22316
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22449
  VolInfo Version 1.0 Build Build 22449
  build.exe Version 0.60 Build 22731

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/17/2016 3:11:06AM Engine version = 5700.7163
  10/17/2016 3:11:06AM AntiVirus DAT version = 8320.0
  10/17/2016 3:11:06AM Number of detection signatures in EXTRA.DAT = None
  10/17/2016 3:11:06AM Names of detection signatures in EXTRA.DAT = None
  10/17/2016 3:11:06AM Scan Started On-Demand Scan
  10/17/2016 3:11:09AM Scan Summary
  10/17/2016 3:11:09AM Processes scanned : 0
  10/17/2016 3:11:09AM Processes detected : 0
  10/17/2016 3:11:09AM Processes cleaned : 0
  10/17/2016 3:11:09AM Boot sectors scanned : 1
  10/17/2016 3:11:09AM Boot sectors detected: 0
  10/17/2016 3:11:09AM Boot sectors cleaned : 0
  10/17/2016 3:11:09AM Files scanned : 62
  10/17/2016 3:11:09AM Files with detections: 0
  10/17/2016 3:11:09AM File detections : 0
  10/17/2016 3:11:09AM Files cleaned : 0
  10/17/2016 3:11:09AM Files deleted : 0
  10/17/2016 3:11:09AM Files not scanned : 0
  10/17/2016 3:11:09AM Scan Summary (Registry Scanning)
  10/17/2016 3:11:09AM Keys scanned : 0
  10/17/2016 3:11:09AM Keys detected : 0
  10/17/2016 3:11:09AM Keys cleaned : 0
  10/17/2016 3:11:09AM Keys deleted : 0
  10/17/2016 3:11:09AM Run time : 0:00:04
  10/17/2016 3:11:09AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22801:HEAD Source
------------------------------------------------------------------------  r22810 | edk2buildsystem | 2016-10-17 02:05:32 -0700 (Mon, 17 Oct 2016) | 15 lines
  BaseTools: Update sign tool to make MonotonicCount *after* Payload
  The WIN_CERTIFICATE_UEFI_GUID AuthInfo defined in the UEFI spec
  mentioned that It is a signature across the image data and the
  Monotonic Count value. After clarification, we do the signature
  calculation, we put MonotonicCount after Payload.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Jiewen Yao <jiewen.yao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Jiewen Yao <jiewen.yao@intel.com>
  Tested-by: Jiewen Yao <jiewen.yao@intel.com>
  (cherry picked from commit 245cda6641ade1f1013c2d5c9c838f2706636828)

------------------------------------------------------------------------