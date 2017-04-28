Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24507

This directory contains the Win32 binaries.

Build Date:       Fri, 28 Apr 2017 03:12:17 Pacific Daylight Time
Last Changed Rev: 24496

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24507
  BootSectImage Version 1.0 Build Build 23431
ERROR : This tool is missing --version option: Brotli.exe
ERROR : This tool is missing --version option: BrotliCompress.bat
  Ecc.exe Version 1.0 Build Build 24382
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 24507
 *GenFds.exe 1.0 Build 24507
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 24507
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 24507
 *Pkcs7Sign Version 0.9 Build 24507
 *Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
 *Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 24507
  TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 24507
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
 *VolInfo Version 1.0 Build Build 24507
 *build.exe Version 0.60 Build 24507

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/28/2017 3:12:19AM Engine version = 5700.7163
  4/28/2017 3:12:19AM AntiVirus DAT version = 8511.0
  4/28/2017 3:12:19AM Number of detection signatures in EXTRA.DAT = None
  4/28/2017 3:12:19AM Names of detection signatures in EXTRA.DAT = None
  4/28/2017 3:12:19AM Scan Started On-Demand Scan
  4/28/2017 3:12:30AM Scan Summary
  4/28/2017 3:12:30AM Processes scanned : 0
  4/28/2017 3:12:30AM Processes detected : 0
  4/28/2017 3:12:30AM Processes cleaned : 0
  4/28/2017 3:12:30AM Boot sectors scanned : 2
  4/28/2017 3:12:30AM Boot sectors detected: 0
  4/28/2017 3:12:30AM Boot sectors cleaned : 0
  4/28/2017 3:12:30AM Files scanned : 65
  4/28/2017 3:12:30AM Files with detections: 0
  4/28/2017 3:12:30AM File detections : 0
  4/28/2017 3:12:30AM Files cleaned : 0
  4/28/2017 3:12:30AM Files deleted : 0
  4/28/2017 3:12:30AM Files not scanned : 0
  4/28/2017 3:12:30AM Scan Summary (Registry Scanning)
  4/28/2017 3:12:30AM Keys scanned : 0
  4/28/2017 3:12:30AM Keys detected : 0
  4/28/2017 3:12:30AM Keys cleaned : 0
  4/28/2017 3:12:30AM Keys deleted : 0
  4/28/2017 3:12:30AM Run time : 0:00:12
  4/28/2017 3:12:30AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24411:HEAD Source
------------------------------------------------------------------------  r24491 | edk2buildsystem | 2017-04-27 14:05:27 -0700 (Thu, 27 Apr 2017) | 10 lines
  BaseTools: Fix a bug for BOOLEAN type value in Asbuilt inf
  When the PCD value is set to TRUE or FALSE, while it is not exchanged to
  its int value, it cause error in the function int(Pcd.DefaultValue, 0).
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 7ced8bb49b69cb2b443f2c357fae8c8b5b75aac6)

------------------------------------------------------------------------  r24492 | edk2buildsystem | 2017-04-27 14:05:33 -0700 (Thu, 27 Apr 2017) | 10 lines
  BaseTools: fix the typo in function name LanuchPostbuild
  The patch fix function name typo LanuchPostbuild ==> LaunchPostbuild.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Nikolai SAOUKH <nms@otdel-1.org>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 91048b0df658e47cef0ccdedc4b790e8a0f1035d)

------------------------------------------------------------------------  r24493 | edk2buildsystem | 2017-04-27 14:05:37 -0700 (Thu, 27 Apr 2017) | 9 lines
  BaseTools/VolInfo: Update OPENSSL_PATH to support space characters
  Update OPENSSL_PATH handling to support space characters in the Path.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 3337eefb49d9053cfd75028ab74dad0cd7acd045)

------------------------------------------------------------------------  r24494 | edk2buildsystem | 2017-04-27 14:05:42 -0700 (Thu, 27 Apr 2017) | 10 lines
  BaseTools: Pkcs7Sign Tool to support OPENSSL_PATH has space
  Update Pkcs7Sign Tool to support the case that OPENSSL_PATH has space
  characters.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b10515378d0a87d36207e44ca1ee02d02918f47c)

------------------------------------------------------------------------  r24495 | edk2buildsystem | 2017-04-27 14:05:47 -0700 (Thu, 27 Apr 2017) | 10 lines
  BaseTools: Rsa2048Sha256Sign Tool to support OPENSSL_PATH has space
  Update Rsa2048Sha256Sign Tool to support the case that OPENSSL_PATH has
  space characters.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a3607b263baabb360dcc67aeb26f9e80018ee3cd)

------------------------------------------------------------------------  r24496 | edk2buildsystem | 2017-04-27 14:05:51 -0700 (Thu, 27 Apr 2017) | 10 lines
  BaseTools: Rsa2048Sha256GenerateKeys to support OPENSSL_PATH has space
  Update Rsa2048Sha256GenerateKeys Tool to support the case that
  OPENSSL_PATH has space characters.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit fcdb928a82c4ed3d776d05c277d5fb30f00f2120)

------------------------------------------------------------------------