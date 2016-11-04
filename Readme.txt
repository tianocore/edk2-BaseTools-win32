Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23090

This directory contains the Win32 binaries.

Build Date:       Fri, 04 Nov 2016 03:11:21 Pacific Daylight Time
Last Changed Rev: 23090

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23090
  BootSectImage Version 1.0 Build Build 22854
  Ecc.exe Version 1.0 Build Build 22854
  EfiLdrImage Version 1.0 Build Build 22854
  EfiRom Version 0.1 Build 22854
  GenBootSector Version 0.2 Build 22854
  GenCrc32 Version 0.2 Build 22854
 *GenDepex.exe Version 0.04 Build 23090
 *GenFds.exe 1.0 Build 23090
  GenFfs Version 0.1 Build 22854
  GenFv Version 0.1 Build 22854
  GenFw Version 0.2 Build 22854
  GenPage Version 0.2 Build 22854
 *GenPatchPcdTable.exe Version 0.10 Build 23090
  GenSec Version 0.1 Build 22854
  GenVtf Version 0.1 Build 22854
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23086
  LzmaF86Compress Version 0.2 Build 23086
 *PatchPcdValue.exe Version 0.10 Build 23090
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 22854
 *TargetTool.exe Version 0.01 Build 23090
  TianoCompress Version 0.1 Build 22854
 *Trim.exe Version 0.10 Build 23090
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22854
  VolInfo Version 1.0 Build Build 22854
 *build.exe Version 0.60 Build 23090

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/4/2016 3:11:23AM Engine version = 5700.7163
  11/4/2016 3:11:23AM AntiVirus DAT version = 8338.0
  11/4/2016 3:11:23AM Number of detection signatures in EXTRA.DAT = None
  11/4/2016 3:11:23AM Names of detection signatures in EXTRA.DAT = None
  11/4/2016 3:11:23AM Scan Started On-Demand Scan
  11/4/2016 3:11:33AM Scan Summary
  11/4/2016 3:11:33AM Processes scanned : 0
  11/4/2016 3:11:33AM Processes detected : 0
  11/4/2016 3:11:33AM Processes cleaned : 0
  11/4/2016 3:11:33AM Boot sectors scanned : 2
  11/4/2016 3:11:33AM Boot sectors detected: 0
  11/4/2016 3:11:33AM Boot sectors cleaned : 0
  11/4/2016 3:11:33AM Files scanned : 62
  11/4/2016 3:11:33AM Files with detections: 0
  11/4/2016 3:11:33AM File detections : 0
  11/4/2016 3:11:33AM Files cleaned : 0
  11/4/2016 3:11:33AM Files deleted : 0
  11/4/2016 3:11:33AM Files not scanned : 0
  11/4/2016 3:11:33AM Scan Summary (Registry Scanning)
  11/4/2016 3:11:33AM Keys scanned : 0
  11/4/2016 3:11:33AM Keys detected : 0
  11/4/2016 3:11:33AM Keys cleaned : 0
  11/4/2016 3:11:33AM Keys deleted : 0
  11/4/2016 3:11:33AM Run time : 0:00:10
  11/4/2016 3:11:33AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23086:HEAD Source
------------------------------------------------------------------------  r23086 | edk2buildsystem | 2016-11-03 02:06:50 -0700 (Thu, 03 Nov 2016) | 15 lines
  BaseTool/Pkcs7: Add TestRoot.cer.
  We add this binary data file for TestRoot.cer.
  So that a platform may include this default file in FDF,
  to check if the platform is using default test key,
  or different production key.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Michael D Kinney <michael.d.kinney@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Jiewen Yao <jiewen.yao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Michael D Kinney <michael.d.kinney@intel.com>
  (cherry picked from commit e9d0933d45e51027836f570427141fd2e3a7dfbd)

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

------------------------------------------------------------------------