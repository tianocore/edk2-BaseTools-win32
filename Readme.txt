Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24194

This directory contains the Win32 binaries.

Build Date:       Sat, 25 Mar 2017 03:11:27 Pacific Daylight Time
Last Changed Rev: 24194

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 24194
  BootSectImage Version 1.0 Build Build 23431
  Ecc.exe Version 1.0 Build Build 24086
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 24194
 *GenFds.exe 1.0 Build 24194
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 24194
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 24194
  Pkcs7Sign Version 0.9 Build 24154
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24154
  Rsa2048Sha256Sign Version 0.9 Build 24154
  Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 24194
  TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 24194
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24130
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 24061
 *build.exe Version 0.60 Build 24194

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/25/2017 3:11:28AM Engine version = 5700.7163
  3/25/2017 3:11:28AM AntiVirus DAT version = 8477.0
  3/25/2017 3:11:28AM Number of detection signatures in EXTRA.DAT = None
  3/25/2017 3:11:28AM Names of detection signatures in EXTRA.DAT = None
  3/25/2017 3:11:28AM Scan Started On-Demand Scan
  3/25/2017 3:11:39AM Scan Summary
  3/25/2017 3:11:39AM Processes scanned : 0
  3/25/2017 3:11:39AM Processes detected : 0
  3/25/2017 3:11:39AM Processes cleaned : 0
  3/25/2017 3:11:39AM Boot sectors scanned : 2
  3/25/2017 3:11:39AM Boot sectors detected: 0
  3/25/2017 3:11:39AM Boot sectors cleaned : 0
  3/25/2017 3:11:39AM Files scanned : 62
  3/25/2017 3:11:39AM Files with detections: 0
  3/25/2017 3:11:39AM File detections : 0
  3/25/2017 3:11:39AM Files cleaned : 0
  3/25/2017 3:11:39AM Files deleted : 0
  3/25/2017 3:11:39AM Files not scanned : 0
  3/25/2017 3:11:39AM Scan Summary (Registry Scanning)
  3/25/2017 3:11:39AM Keys scanned : 0
  3/25/2017 3:11:39AM Keys detected : 0
  3/25/2017 3:11:39AM Keys cleaned : 0
  3/25/2017 3:11:39AM Keys deleted : 0
  3/25/2017 3:11:39AM Run time : 0:00:11
  3/25/2017 3:11:39AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24154:HEAD Source
------------------------------------------------------------------------  r24154 | edk2buildsystem | 2017-03-18 02:05:36 -0700 (Sat, 18 Mar 2017) | 11 lines
  BaseTools: GenFds get the Size info for FV image in the FD region
  When the FV size is specify in the FD region, Tool generate the FV file
  may not use the correct size.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=387
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 135ae8c873bb18600b8474524453c9ecc6eeed16)

------------------------------------------------------------------------  r24194 | edk2buildsystem | 2017-03-25 02:05:29 -0700 (Sat, 25 Mar 2017) | 54 lines
  BaseTools: Skip module AutoGen by comparing timestamp.
  [Introduction]
  The BaseTool Build.py AutoGen parse INF meta-file and generate
  AutoGen.c/AutoGen.h/makefile. When we only change .c .h code, the
  AutoGen might be not necessary, but Build.py spend a lot of time on it.
  There's a -u flag to skip all module's AutoGen. In my environment, it save
  35%~50% of time in rebuild a ROM.
  However, if user change one .INF meta-file, then -u flag is not available.
  [Idea]
  AutoGen can compare meta-file's timestamp and decide if the module's
  AutoGen can be skipped. With this, when a module's INF is changed, we
  only run this module's AutoGen, we don't need to run other module's.
  [Implementation]
  In the end of a module's AutoGen, we create a AutoGenTimeStamp.
  The file save a file list that related to this module's AutoGen.
  In other word, the file list in AutoGenTimeStamp is INPUT files of
  module AutoGen, AutoGenTimeStamp file is OUTPUT.
  During rebuild, we compare time stamp between INPUT and OUTPUT, and
  decide if we can skip it.
  Below is the Input/Output of a module's AutoGen.
  [Input]
  1. All the DSC/DEC/FDF used by the platform.
  2. Macro and PCD defined by Build Options such as "build -D AAA=TRUE
  --pcd BbbPcd=0".
  3. INF file of a module.
  4. Source files of a module, list in [Sources] section of INF.
  5. All the library link by the module.
  6. All the .h files included by the module's sources.
  [Output]
  AutoGen.c/AutoGen.h/makefile/AutoGenTimeStamp
  [Testing]
  This patch save my build time. When I make a change without touching
  DSC/DEC/FDF, it is absolutely much faster than original rebuild,
  35%~50% time saving in my environment
  (compare to original tool rebuild time).
  If I change any DSC/DEC/FDF, there's no performance improve, because it
  can't skip any module's AutoGen.
  Please note that if your environment will generate DSC/FDF during prebuild,
  it will not skip any AutoGen because of DSC timestamp is changed. This will
  require prebuild script not to update metafile when content is not changed.
  (cherry picked from commit c17956e0eedce299ac253ac40238ce90a5e623e0)

------------------------------------------------------------------------