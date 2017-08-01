Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24994

This directory contains the Win32 binaries.

Build Date:       Tue, 01 Aug 2017 03:11:55 Pacific Daylight Time
Last Changed Rev: 24994

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
 *EfiLdrImage Version 1.0 Build Build 24994
 *EfiRom Version 0.1 Build 24994
  GenBootSector Version 0.2 Build 23431
 *GenCrc32 Version 0.2 Build 24994
  GenDepex.exe Version 0.04 Build 24913
  GenFds.exe 1.0 Build 24913
 *GenFfs Version 0.1 Build 24994
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24909
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 24913
 *GenSec Version 0.1 Build 24994
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 24913
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
 *Split Version 1.0 Build Build 24994
  TargetTool.exe Version 0.01 Build 24913
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 24913
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24507
 *build.exe Version 0.60 Build 24994

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/1/2017 3:11:56AM Engine version = 5800.7501
  8/1/2017 3:11:56AM AntiVirus DAT version = 8608.0
  8/1/2017 3:11:56AM Number of detection signatures in EXTRA.DAT = None
  8/1/2017 3:11:56AM Names of detection signatures in EXTRA.DAT = None
  8/1/2017 3:11:57AM Scan Started On-Demand Scan
  8/1/2017 3:12:18AM Scan Summary
  8/1/2017 3:12:18AM Processes scanned : 0
  8/1/2017 3:12:18AM Processes detected : 0
  8/1/2017 3:12:18AM Processes cleaned : 0
  8/1/2017 3:12:18AM Boot sectors scanned : 2
  8/1/2017 3:12:18AM Boot sectors detected: 0
  8/1/2017 3:12:18AM Boot sectors cleaned : 0
  8/1/2017 3:12:18AM Files scanned : 70
  8/1/2017 3:12:18AM Files with detections: 0
  8/1/2017 3:12:18AM File detections : 0
  8/1/2017 3:12:18AM Files cleaned : 0
  8/1/2017 3:12:18AM Files deleted : 0
  8/1/2017 3:12:18AM Files not scanned : 0
  8/1/2017 3:12:18AM Scan Summary (Registry Scanning)
  8/1/2017 3:12:18AM Keys scanned : 0
  8/1/2017 3:12:18AM Keys detected : 0
  8/1/2017 3:12:18AM Keys cleaned : 0
  8/1/2017 3:12:18AM Keys deleted : 0
  8/1/2017 3:12:18AM Run time : 0:00:22
  8/1/2017 3:12:18AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24968:HEAD Source
------------------------------------------------------------------------  r24988 | edk2buildsystem | 2017-08-01 02:05:35 -0700 (Tue, 01 Aug 2017) | 11 lines
  BaseTools: Fix the bug to correctly check Pcd type that in FDF file
  We set Pcd value in FDF and used this Pcd as PatchableInModule type in
  module, it cause build report generate failure. because we incorrectly
  set the Pcd type during check whether the Pcd is used.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c65df5d9a14331d2b6d583359f1cf88c3b710d34)

------------------------------------------------------------------------  r24989 | edk2buildsystem | 2017-08-01 02:05:44 -0700 (Tue, 01 Aug 2017) | 8 lines
  BaseTools/Split: Fix the segmentation fault in GetSplitValue()
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=538
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 15face06f400283e227aa814bf3180ccd19328a3)

------------------------------------------------------------------------  r24990 | edk2buildsystem | 2017-08-01 02:05:49 -0700 (Tue, 01 Aug 2017) | 8 lines
  BaseTools/GenSec: Fix a segmentation fault in main()
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=537
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 67f3d09924b0fedf36833d11e599c609d319d0ea)

------------------------------------------------------------------------  r24991 | edk2buildsystem | 2017-08-01 02:05:54 -0700 (Tue, 01 Aug 2017) | 8 lines
  BaseTools/GenFfs: Fix a segmentation fault from vsprintf()/vfprintf()
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=536
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 13d79c2976205ffc2ec380e87163b39ada96bc03)

------------------------------------------------------------------------  r24992 | edk2buildsystem | 2017-08-01 02:05:57 -0700 (Tue, 01 Aug 2017) | 8 lines
  BaseTools/EfiRom: Fix a segmentation fault from vsprintf()/vfprintf()
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=534
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit ef6cd66ae46c7d90be6ffdf3f8ed092738292336)

------------------------------------------------------------------------  r24993 | edk2buildsystem | 2017-08-01 02:06:02 -0700 (Tue, 01 Aug 2017) | 8 lines
  BaseTools/EfiLdrImage: Fix a segmentation fault from vfprintf()
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=533
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b5bd6387d225dfef9a693982cabccd37fcdd1fb7)

------------------------------------------------------------------------  r24994 | edk2buildsystem | 2017-08-01 02:06:06 -0700 (Tue, 01 Aug 2017) | 8 lines
  BaseTools/GenCrc32: Fix a bug to hand empty file for decode
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=535
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 997b2c543751cb4a3473270c1a7016ade311f01b)

------------------------------------------------------------------------