Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26352

This directory contains the Win32 binaries.

Build Date:       Fri, 09 Feb 2018 03:12:33 Pacific Standard Time
Last Changed Rev: 26350

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26352
  BootSectImage Version 1.0 Build Build 26263
  Brotli Version 0.5.2 Build 26263
  Brotli Version 0.5.2 Build 26263
  DevicePath Version 0.1 Build 26263
  Ecc.exe Version 1.0 Build Build 26237
  EfiLdrImage Version 1.0 Build Build 26263
  EfiRom Version 0.1 Build 26263
  GenBootSector Version 0.2 Build 26263
  GenCrc32 Version 0.2 Build 26263
 *GenDepex.exe Version 0.04 Build 26352
 *GenFds.exe 1.0 Build 26352
  GenFfs Version 0.1 Build 26263
  GenFv Version 0.1 Build 26263
  GenFw Version 0.2 Build 26263
  GenPage Version 0.2 Build 26263
 *GenPatchPcdTable.exe Version 0.10 Build 26352
  GenSec Version 0.1 Build 26263
  GenVtf Version 0.1 Build 26263
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26263
  LzmaF86Compress Version 0.2 Build 26263
 *PatchPcdValue.exe Version 0.10 Build 26352
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
  Split Version 1.0 Build Build 26263
 *TargetTool.exe Version 0.01 Build 26352
  TianoCompress Version 0.1 Build 26263
 *Trim.exe Version 0.10 Build 26352
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26263
  VolInfo Version 1.0 Build Build 26263
 *build.exe Version 0.60 Build 26352

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/9/2018 3:12:34AM Engine version = 5900.7806
  2/9/2018 3:12:34AM AntiVirus DAT version = 8799.0
  2/9/2018 3:12:34AM Number of detection signatures in EXTRA.DAT = None
  2/9/2018 3:12:34AM Names of detection signatures in EXTRA.DAT = None
  2/9/2018 3:12:34AM Scan Started On-Demand Scan
  2/9/2018 3:12:45AM Scan Summary
  2/9/2018 3:12:45AM Processes scanned : 0
  2/9/2018 3:12:45AM Processes detected : 0
  2/9/2018 3:12:45AM Processes cleaned : 0
  2/9/2018 3:12:45AM Boot sectors scanned : 2
  2/9/2018 3:12:45AM Boot sectors detected: 0
  2/9/2018 3:12:45AM Boot sectors cleaned : 0
  2/9/2018 3:12:45AM Files scanned : 66
  2/9/2018 3:12:45AM Files with detections: 0
  2/9/2018 3:12:45AM File detections : 0
  2/9/2018 3:12:45AM Files cleaned : 0
  2/9/2018 3:12:45AM Files deleted : 0
  2/9/2018 3:12:45AM Files not scanned : 0
  2/9/2018 3:12:45AM Scan Summary (Registry Scanning)
  2/9/2018 3:12:45AM Keys scanned : 0
  2/9/2018 3:12:45AM Keys detected : 0
  2/9/2018 3:12:45AM Keys cleaned : 0
  2/9/2018 3:12:45AM Keys deleted : 0
  2/9/2018 3:12:45AM Run time : 0:00:12
  2/9/2018 3:12:45AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26326:HEAD Source
------------------------------------------------------------------------  r26329 | edk2buildsystem | 2018-02-09 02:05:54 -0800 (Fri, 09 Feb 2018) | 10 lines
  BaseTools: not specified value of MAX_CONCURRENT_THREAD_NUMBER
  when MAX_CONCURRENT_THREAD_NUMBER is not specified, tool will
  automatically detect number of processor threads.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=775
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 2052cb675f1fdbc77f916422fdf5c2da29741169)

------------------------------------------------------------------------  r26330 | edk2buildsystem | 2018-02-09 02:06:02 -0800 (Fri, 09 Feb 2018) | 12 lines
  BaseTools: Update Expression.py for string comparison and MACRO replace issue
  1. Fix string comparison incorrect issue, we expected "ABC" is greater than
  "AAD" since the second char 'B' is greater than 'A'.
  2. fix MACRO not replace issue.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 9efe8d604049b1d2f320ae5c40cd925d6504bceb)

------------------------------------------------------------------------  r26350 | edk2buildsystem | 2018-02-09 02:07:58 -0800 (Fri, 09 Feb 2018) | 11 lines
  BaseTool: correct the generate compress section process
  First generate a dummy file with section alignment,
  then compress the dummy file to generate the compress file
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit ce2818e418020a9cf84f6712cbda4075b0652809)

------------------------------------------------------------------------