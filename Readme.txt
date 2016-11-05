Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23095

This directory contains the Win32 binaries.

Build Date:       Sat, 05 Nov 2016 03:11:07 Pacific Daylight Time
Last Changed Rev: 23094

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23090
  BootSectImage Version 1.0 Build Build 22854
  Ecc.exe Version 1.0 Build Build 22854
  EfiLdrImage Version 1.0 Build Build 22854
  EfiRom Version 0.1 Build 22854
  GenBootSector Version 0.2 Build 22854
  GenCrc32 Version 0.2 Build 22854
  GenDepex.exe Version 0.04 Build 23090
  GenFds.exe 1.0 Build 23090
  GenFfs Version 0.1 Build 22854
  GenFv Version 0.1 Build 22854
  GenFw Version 0.2 Build 22854
  GenPage Version 0.2 Build 22854
 *GenPatchPcdTable.exe Version 0.10 Build 23095
  GenSec Version 0.1 Build 22854
  GenVtf Version 0.1 Build 22854
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23086
  LzmaF86Compress Version 0.2 Build 23086
  PatchPcdValue.exe Version 0.10 Build 23090
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 22854
  TargetTool.exe Version 0.01 Build 23090
  TianoCompress Version 0.1 Build 22854
  Trim.exe Version 0.10 Build 23090
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22854
  VolInfo Version 1.0 Build Build 22854
 *build.exe Version 0.60 Build 23095

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/5/2016 3:11:08AM Engine version = 5700.7163
  11/5/2016 3:11:08AM AntiVirus DAT version = 8339.0
  11/5/2016 3:11:08AM Number of detection signatures in EXTRA.DAT = None
  11/5/2016 3:11:08AM Names of detection signatures in EXTRA.DAT = None
  11/5/2016 3:11:08AM Scan Started On-Demand Scan
  11/5/2016 3:11:18AM Scan Summary
  11/5/2016 3:11:18AM Processes scanned : 0
  11/5/2016 3:11:18AM Processes detected : 0
  11/5/2016 3:11:18AM Processes cleaned : 0
  11/5/2016 3:11:18AM Boot sectors scanned : 2
  11/5/2016 3:11:18AM Boot sectors detected: 0
  11/5/2016 3:11:18AM Boot sectors cleaned : 0
  11/5/2016 3:11:18AM Files scanned : 62
  11/5/2016 3:11:18AM Files with detections: 0
  11/5/2016 3:11:18AM File detections : 0
  11/5/2016 3:11:18AM Files cleaned : 0
  11/5/2016 3:11:18AM Files deleted : 0
  11/5/2016 3:11:18AM Files not scanned : 0
  11/5/2016 3:11:18AM Scan Summary (Registry Scanning)
  11/5/2016 3:11:18AM Keys scanned : 0
  11/5/2016 3:11:18AM Keys detected : 0
  11/5/2016 3:11:18AM Keys cleaned : 0
  11/5/2016 3:11:18AM Keys deleted : 0
  11/5/2016 3:11:18AM Run time : 0:00:10
  11/5/2016 3:11:18AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23090:HEAD Source
------------------------------------------------------------------------  r23090 | edk2buildsystem | 2016-11-04 02:05:57 -0700 (Fri, 04 Nov 2016) | 11 lines
  BaseTools: Fix the Windows GCC Build Failure with too long path
  When path is too long, build tool will wrap them into resp.txt, then call
  gcc @resp.txt. It will cause windows GCC build failure, because resp.txt
  still uses windows directory separator \. This patch change the \ to /.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 669b6cc60bf610bbee32e79ed165ca604764c169)

------------------------------------------------------------------------  r23092 | edk2buildsystem | 2016-11-04 14:05:42 -0700 (Fri, 04 Nov 2016) | 12 lines
  BaseTools/Pkcs7: Add readme.md
  Add readme.md to describe the X.509 certificate generation.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Michael D Kinney <michael.d.kinney@intel.com>
  Cc: Qin Long <qin.long@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Jiewen Yao <jiewen.yao@intel.com>
  Reviewed-by: Qin Long <qin.long@intel.com>
  (cherry picked from commit fdaf78424da45b34ef515119cd308ffa8cd43d54)

------------------------------------------------------------------------  r23094 | edk2buildsystem | 2016-11-05 02:05:44 -0700 (Sat, 05 Nov 2016) | 12 lines
  BaseTools: Add the support for character '<' and '>' in the map file
  Current the regex for the symbol in the map file doesn't support the '<'
  and '>' character, while user use Lambda Expression (C++11 feature), it
  would generate the something like @V<lambda_xxx>@ in the map file which
  cause build fail to parse the symbol in map file.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 7e7a8116640605be83528ab12837e71c6a2accae)

------------------------------------------------------------------------