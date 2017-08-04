Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25038

This directory contains the Win32 binaries.

Build Date:       Fri, 04 Aug 2017 03:12:04 Pacific Daylight Time
Last Changed Rev: 25037

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24913
  BootSectImage Version 1.0 Build Build 23431
  Brotli Version 0.5.2 Build 24577
  Brotli Version 0.5.2 Build 24577
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 24994
  EfiRom Version 0.1 Build 24994
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 24994
  GenDepex.exe Version 0.04 Build 24913
  GenFds.exe 1.0 Build 24913
  GenFfs Version 0.1 Build 24994
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24909
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 24913
  GenSec Version 0.1 Build 24994
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 24913
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 24994
  TargetTool.exe Version 0.01 Build 24913
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 24913
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 25038
  VolInfo Version 1.0 Build Build 24507
  build.exe Version 0.60 Build 24994

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/4/2017 3:12:05AM Engine version = 5800.7501
  8/4/2017 3:12:05AM AntiVirus DAT version = 8611.0
  8/4/2017 3:12:05AM Number of detection signatures in EXTRA.DAT = None
  8/4/2017 3:12:05AM Names of detection signatures in EXTRA.DAT = None
  8/4/2017 3:12:05AM Scan Started On-Demand Scan
  8/4/2017 3:12:27AM Scan Summary
  8/4/2017 3:12:27AM Processes scanned : 0
  8/4/2017 3:12:27AM Processes detected : 0
  8/4/2017 3:12:27AM Processes cleaned : 0
  8/4/2017 3:12:27AM Boot sectors scanned : 2
  8/4/2017 3:12:27AM Boot sectors detected: 0
  8/4/2017 3:12:27AM Boot sectors cleaned : 0
  8/4/2017 3:12:27AM Files scanned : 64
  8/4/2017 3:12:27AM Files with detections: 0
  8/4/2017 3:12:27AM File detections : 0
  8/4/2017 3:12:27AM Files cleaned : 0
  8/4/2017 3:12:27AM Files deleted : 0
  8/4/2017 3:12:27AM Files not scanned : 0
  8/4/2017 3:12:27AM Scan Summary (Registry Scanning)
  8/4/2017 3:12:27AM Keys scanned : 0
  8/4/2017 3:12:27AM Keys detected : 0
  8/4/2017 3:12:27AM Keys cleaned : 0
  8/4/2017 3:12:27AM Keys deleted : 0
  8/4/2017 3:12:27AM Run time : 0:00:22
  8/4/2017 3:12:27AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24994:HEAD Source
------------------------------------------------------------------------  r24994 | edk2buildsystem | 2017-08-01 02:06:06 -0700 (Tue, 01 Aug 2017) | 8 lines
  BaseTools/GenCrc32: Fix a bug to hand empty file for decode
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=535
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 997b2c543751cb4a3473270c1a7016ade311f01b)

------------------------------------------------------------------------  r25036 | edk2buildsystem | 2017-08-04 02:06:35 -0700 (Fri, 04 Aug 2017) | 14 lines
  BaseTools/VfrCompile: Fix segmentation fault issues
  REF: https://bugzilla.tianocore.org/show_bug.cgi?id=532
  (1) Add NULL check before using a pointer.
  (2) Use "%s" format string in DebugError function to
  avoid crash caused by incorrect input.
  Cc: Bo Chen <chenbo@pdx.edu>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Eric Dong <eric.dong@intel.com>
  (cherry picked from commit 8c1e13d327e6c0409435edaa89b909fbdef49232)

------------------------------------------------------------------------  r25037 | edk2buildsystem | 2017-08-04 02:06:40 -0700 (Fri, 04 Aug 2017) | 14 lines
  BaseTools/VfrCompile: Remove the MAX_PATH limitation
  REF: https://bugzilla.tianocore.org/show_bug.cgi?id=579
  Since we have already used LongFilePath() to convert
  file path, so we can remove the MAX_PATH limitation.
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Daniel Díaz <daniel.diaz@linaro.org>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Eric Dong <eric.dong@intel.com>
  (cherry picked from commit ba78032bc8c9f74a4c4cc4917a3284a51840ec70)

------------------------------------------------------------------------