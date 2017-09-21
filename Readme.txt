Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25386

This directory contains the Win32 binaries.

Build Date:       Thu, 21 Sep 2017 03:12:51 Pacific Daylight Time
Last Changed Rev: 25382

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25366
 *BootSectImage Version 1.0 Build Build 25386
 *Brotli Version 0.5.2 Build 25386
  Brotli Version 0.5.2 Build 25386
  Ecc.exe Version 1.0 Build Build 24602
 *EfiLdrImage Version 1.0 Build Build 25386
 *EfiRom Version 0.1 Build 25386
 *GenBootSector Version 0.2 Build 25386
 *GenCrc32 Version 0.2 Build 25386
  GenDepex.exe Version 0.04 Build 25366
  GenFds.exe 1.0 Build 25366
 *GenFfs Version 0.1 Build 25386
 *GenFv Version 0.1 Build 25386
 *GenFw Version 0.2 Build 25386
 *GenPage Version 0.2 Build 25386
  GenPatchPcdTable.exe Version 0.10 Build 25366
 *GenSec Version 0.1 Build 25386
 *GenVtf Version 0.1 Build 25386
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 25386
  LzmaF86Compress Version 0.2 Build 25386
  PatchPcdValue.exe Version 0.10 Build 25366
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
 *Split Version 1.0 Build Build 25386
  TargetTool.exe Version 0.01 Build 25366
 *TianoCompress Version 0.1 Build 25386
  Trim.exe Version 0.10 Build 25366
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 25386
 *VolInfo Version 1.0 Build Build 25386
  build.exe Version 0.60 Build 25366

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  9/21/2017 3:12:52AM Engine version = 5900.7806
  9/21/2017 3:12:52AM AntiVirus DAT version = 8660.0
  9/21/2017 3:12:52AM Number of detection signatures in EXTRA.DAT = None
  9/21/2017 3:12:52AM Names of detection signatures in EXTRA.DAT = None
  9/21/2017 3:12:52AM Scan Started On-Demand Scan
  9/21/2017 3:13:15AM Scan Summary
  9/21/2017 3:13:15AM Processes scanned : 0
  9/21/2017 3:13:15AM Processes detected : 0
  9/21/2017 3:13:15AM Processes cleaned : 0
  9/21/2017 3:13:15AM Boot sectors scanned : 2
  9/21/2017 3:13:15AM Boot sectors detected: 0
  9/21/2017 3:13:15AM Boot sectors cleaned : 0
  9/21/2017 3:13:15AM Files scanned : 80
  9/21/2017 3:13:15AM Files with detections: 0
  9/21/2017 3:13:15AM File detections : 0
  9/21/2017 3:13:15AM Files cleaned : 0
  9/21/2017 3:13:15AM Files deleted : 0
  9/21/2017 3:13:15AM Files not scanned : 0
  9/21/2017 3:13:15AM Scan Summary (Registry Scanning)
  9/21/2017 3:13:15AM Keys scanned : 0
  9/21/2017 3:13:15AM Keys detected : 0
  9/21/2017 3:13:15AM Keys cleaned : 0
  9/21/2017 3:13:15AM Keys deleted : 0
  9/21/2017 3:13:15AM Run time : 0:00:23
  9/21/2017 3:13:15AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25366:HEAD Source
------------------------------------------------------------------------  r25366 | edk2buildsystem | 2017-09-19 02:06:21 -0700 (Tue, 19 Sep 2017) | 13 lines
  BaseTools: Fix a bug to correct SourceFileList
  We met a case that use two microcode files in the Microcode.inf file,
  one is .mcb file, another is .txt file. then it cause build failure
  because the SourceFileList include the .txt file's output file, while
  this output file is still not be generated, so it cause
  GetFileDependency report failure.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a3a4737051010a94832f7bceaa1fa414d7259da0)

------------------------------------------------------------------------  r25381 | edk2buildsystem | 2017-09-21 02:05:55 -0700 (Thu, 21 Sep 2017) | 13 lines
  BaseTool/VfrCompile: Support Union type in VFR
  https://bugzilla.tianocore.org/show_bug.cgi?id=603
  Update VfrCompiler to parse the UNION type in vfr file
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Eric Dong <eric.dong@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 2b7f3d4a6bb7e024b3c45f328bdd635f878387f7)

------------------------------------------------------------------------  r25382 | edk2buildsystem | 2017-09-21 02:06:08 -0700 (Thu, 21 Sep 2017) | 16 lines
  BaseTool/VfrCompiler: Support Bit fields in EFI/Buffer VarStore
  REF: https://bugzilla.tianocore.org/show_bug.cgi?id=545
  Enhance VfrCompiler to parse following case:
  1. EFI/Buffer VarStore can contain bit fields in their structure.
  2. For question Oneof/Checkbox/numeric, their storage can be
  bit fields of an EFI VarStore/Buffer VarStore.
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Eric Dong <eric.dong@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 42c808d4cbc66605777dad18d800708f2c06f0c4)

------------------------------------------------------------------------