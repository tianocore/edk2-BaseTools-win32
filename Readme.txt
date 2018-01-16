Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26150

This directory contains the Win32 binaries.

Build Date:       Tue, 16 Jan 2018 03:11:57 Pacific Standard Time
Last Changed Rev: 26140

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26116
  BootSectImage Version 1.0 Build Build 26139
  Brotli Version 0.5.2 Build 26139
  Brotli Version 0.5.2 Build 26139
  DevicePath Version 0.1 Build 26139
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 26139
  EfiRom Version 0.1 Build 26139
  GenBootSector Version 0.2 Build 26139
  GenCrc32 Version 0.2 Build 26139
  GenDepex.exe Version 0.04 Build 26116
  GenFds.exe 1.0 Build 26116
  GenFfs Version 0.1 Build 26139
  GenFv Version 0.1 Build 26139
  GenFw Version 0.2 Build 26139
  GenPage Version 0.2 Build 26139
  GenPatchPcdTable.exe Version 0.10 Build 26116
  GenSec Version 0.1 Build 26139
  GenVtf Version 0.1 Build 26139
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26139
  LzmaF86Compress Version 0.2 Build 26139
  PatchPcdValue.exe Version 0.10 Build 26116
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 26139
  TargetTool.exe Version 0.01 Build 26116
  TianoCompress Version 0.1 Build 26139
  Trim.exe Version 0.10 Build 26116
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26139
  VolInfo Version 1.0 Build Build 26139
 *build.exe Version 0.60 Build 26150

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/16/2018 3:11:59AM Engine version = 5900.7806
  1/16/2018 3:11:59AM AntiVirus DAT version = 8775.0
  1/16/2018 3:11:59AM Number of detection signatures in EXTRA.DAT = None
  1/16/2018 3:11:59AM Names of detection signatures in EXTRA.DAT = None
  1/16/2018 3:11:59AM Scan Started On-Demand Scan
  1/16/2018 3:12:11AM Scan Summary
  1/16/2018 3:12:11AM Processes scanned : 0
  1/16/2018 3:12:11AM Processes detected : 0
  1/16/2018 3:12:11AM Processes cleaned : 0
  1/16/2018 3:12:11AM Boot sectors scanned : 2
  1/16/2018 3:12:11AM Boot sectors detected: 0
  1/16/2018 3:12:11AM Boot sectors cleaned : 0
  1/16/2018 3:12:11AM Files scanned : 66
  1/16/2018 3:12:11AM Files with detections: 0
  1/16/2018 3:12:11AM File detections : 0
  1/16/2018 3:12:11AM Files cleaned : 0
  1/16/2018 3:12:11AM Files deleted : 0
  1/16/2018 3:12:11AM Files not scanned : 0
  1/16/2018 3:12:11AM Scan Summary (Registry Scanning)
  1/16/2018 3:12:11AM Keys scanned : 0
  1/16/2018 3:12:11AM Keys detected : 0
  1/16/2018 3:12:11AM Keys cleaned : 0
  1/16/2018 3:12:11AM Keys deleted : 0
  1/16/2018 3:12:11AM Run time : 0:00:13
  1/16/2018 3:12:11AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26139:HEAD Source
------------------------------------------------------------------------  r26140 | edk2buildsystem | 2018-01-15 14:05:29 -0800 (Mon, 15 Jan 2018) | 12 lines
  BaseTools: Enable MAX_CONCURRENT_THREAD_NUMBER = 0 feature
  when set 'MAX_CONCURRENT_THREAD_NUMBER=0',  will auto-detect number of
  processor threads as MAX_CONCURRENT_THREAD_NUMBER.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=775
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 29af38b0f8f2aa7b08f61a9df38a59dbc15e9302)

------------------------------------------------------------------------