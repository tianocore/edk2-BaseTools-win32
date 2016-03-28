Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20407

This directory contains the Win32 binaries.

Build Date:       Mon, 28 Mar 2016 03:32:27 Pacific Daylight Time
Last Changed Rev: 20407

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20357
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20331
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
  GenDepex.exe Version 0.04 Build 20357
 *GenFds.exe 1.0 Build 20407
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
  GenPatchPcdTable.exe Version 0.10 Build 20357
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
  PatchPcdValue.exe Version 0.10 Build 20357
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20331
  Rsa2048Sha256Sign Version 0.9 Build 20331
  Split Version 1.0 Build Build 20182
  TargetTool.exe Version 0.01 Build 20357
  TianoCompress Version 0.1 Build 19914
  Trim.exe Version 0.10 Build 20357
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20331
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20182
  build.exe Version 0.60 Build 20357

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/28/2016 3:32:28AM Engine version = 5700.7163
  3/28/2016 3:32:28AM AntiVirus DAT version = 8117.0
  3/28/2016 3:32:28AM Number of detection signatures in EXTRA.DAT = None
  3/28/2016 3:32:28AM Names of detection signatures in EXTRA.DAT = None
  3/28/2016 3:32:28AM Scan Started On-Demand Scan
  3/28/2016 3:32:30AM Scan Summary
  3/28/2016 3:32:30AM Processes scanned : 0
  3/28/2016 3:32:30AM Processes detected : 0
  3/28/2016 3:32:30AM Processes cleaned : 0
  3/28/2016 3:32:30AM Boot sectors scanned : 1
  3/28/2016 3:32:30AM Boot sectors detected: 0
  3/28/2016 3:32:30AM Boot sectors cleaned : 0
  3/28/2016 3:32:30AM Files scanned : 55
  3/28/2016 3:32:30AM Files with detections: 0
  3/28/2016 3:32:30AM File detections : 0
  3/28/2016 3:32:30AM Files cleaned : 0
  3/28/2016 3:32:30AM Files deleted : 0
  3/28/2016 3:32:30AM Files not scanned : 0
  3/28/2016 3:32:30AM Scan Summary (Registry Scanning)
  3/28/2016 3:32:30AM Keys scanned : 0
  3/28/2016 3:32:30AM Keys detected : 0
  3/28/2016 3:32:30AM Keys cleaned : 0
  3/28/2016 3:32:30AM Keys deleted : 0
  3/28/2016 3:32:30AM Run time : 0:00:02
  3/28/2016 3:32:30AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20406:HEAD Source
------------------------------------------------------------------------  r20406 | edk2buildsystem | 2016-03-27 02:26:52 -0700 (Sun, 27 Mar 2016) | 11 lines
  BaseTools: generate alignment when the FV content come from the filesystem
  when the FV contents come from the filesystem instead of from a named FDF
  section, the build tool missed to generate alignment for this FV. The fix
  is get the alignment value from FV header and use this value to generate
  alignment.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 877c0a93be4317f5715347359cc78d41f4654748)

------------------------------------------------------------------------  r20407 | edk2buildsystem | 2016-03-28 02:26:47 -0700 (Mon, 28 Mar 2016) | 9 lines
  BaseTools: Remove the unnecessary check for RAW File
  Because the __VerifyFile function already checked whether the file is
  valid.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 4fa7b3301ef31f2787b9d0bde6694203a67b3ff2)

------------------------------------------------------------------------