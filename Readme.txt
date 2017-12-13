Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25927

This directory contains the Win32 binaries.

Build Date:       Wed, 13 Dec 2017 03:12:22 Pacific Standard Time
Last Changed Rev: 25922

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25927
  BootSectImage Version 1.0 Build Build 25855
  Brotli Version 0.5.2 Build 25855
  Brotli Version 0.5.2 Build 25855
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25855
  EfiRom Version 0.1 Build 25855
  GenBootSector Version 0.2 Build 25855
  GenCrc32 Version 0.2 Build 25855
 *GenDepex.exe Version 0.04 Build 25927
 *GenFds.exe 1.0 Build 25927
  GenFfs Version 0.1 Build 25855
  GenFv Version 0.1 Build 25855
  GenFw Version 0.2 Build 25855
  GenPage Version 0.2 Build 25855
 *GenPatchPcdTable.exe Version 0.10 Build 25927
  GenSec Version 0.1 Build 25855
  GenVtf Version 0.1 Build 25855
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25855
  LzmaF86Compress Version 0.2 Build 25855
 *PatchPcdValue.exe Version 0.10 Build 25927
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25855
 *TargetTool.exe Version 0.01 Build 25927
  TianoCompress Version 0.1 Build 25855
 *Trim.exe Version 0.10 Build 25927
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25855
  VolInfo Version 1.0 Build Build 25855
 *build.exe Version 0.60 Build 25927

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/13/2017 3:12:23AM Engine version = 5900.7806
  12/13/2017 3:12:23AM AntiVirus DAT version = 8743.0
  12/13/2017 3:12:23AM Number of detection signatures in EXTRA.DAT = None
  12/13/2017 3:12:23AM Names of detection signatures in EXTRA.DAT = None
  12/13/2017 3:12:23AM Scan Started On-Demand Scan
  12/13/2017 3:12:32AM Scan Summary
  12/13/2017 3:12:32AM Processes scanned : 0
  12/13/2017 3:12:32AM Processes detected : 0
  12/13/2017 3:12:32AM Processes cleaned : 0
  12/13/2017 3:12:32AM Boot sectors scanned : 2
  12/13/2017 3:12:32AM Boot sectors detected: 0
  12/13/2017 3:12:32AM Boot sectors cleaned : 0
  12/13/2017 3:12:32AM Files scanned : 64
  12/13/2017 3:12:32AM Files with detections: 0
  12/13/2017 3:12:32AM File detections : 0
  12/13/2017 3:12:32AM Files cleaned : 0
  12/13/2017 3:12:32AM Files deleted : 0
  12/13/2017 3:12:32AM Files not scanned : 0
  12/13/2017 3:12:32AM Scan Summary (Registry Scanning)
  12/13/2017 3:12:32AM Keys scanned : 0
  12/13/2017 3:12:32AM Keys detected : 0
  12/13/2017 3:12:32AM Keys cleaned : 0
  12/13/2017 3:12:32AM Keys deleted : 0
  12/13/2017 3:12:32AM Run time : 0:00:09
  12/13/2017 3:12:32AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25882:HEAD Source
------------------------------------------------------------------------  r25882 | edk2buildsystem | 2017-12-10 02:05:24 -0800 (Sun, 10 Dec 2017) | 10 lines
  BaseTools: Add object_files.lst as dependency of lib target
  Seems object_files.lst is not added as dependency of lib target, this
  patch update BaseTools to generate Makefile with this dependency.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1c62af9ec1086b9e3066b25bfd6bee6d03186c0f)

------------------------------------------------------------------------  r25896 | edk2buildsystem | 2017-12-12 14:05:49 -0800 (Tue, 12 Dec 2017) | 10 lines
  BaseTools: Update BrotliCompress script to handle the different input format
  After this update, BrotliCompress can support below styles.
  BrotliCompress -e InputFile -o OutputFile
  BrotliCompress -e -o OutputFile InputFile
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 83e901a507804bf27b8e6c8c2ec7c8f16555b495)

------------------------------------------------------------------------  r25919 | edk2buildsystem | 2017-12-13 02:07:48 -0800 (Wed, 13 Dec 2017) | 10 lines
  BaseTools: Fix the incorrect indent introduced by 37de70
  The incorrect indent introduced by 37de70, it cause PEIM in sub FV
  image can't be rebased. Then it block some platform can't boot.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 0385efa00bc32bc60bbd023ba301022615cf215b)

------------------------------------------------------------------------  r25920 | edk2buildsystem | 2017-12-13 02:07:53 -0800 (Wed, 13 Dec 2017) | 11 lines
  BaseTools: Not cache the .efi file location into build option
  We don't need cache the .efi file location into build option, otherwise
  when we change the --binary-destination location, it would cause the
  hash value is different.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5381ff634203a087fdba81b17c34e3d9b637b406)

------------------------------------------------------------------------  r25921 | edk2buildsystem | 2017-12-13 02:07:58 -0800 (Wed, 13 Dec 2017) | 14 lines
  BaseTools: back up the binary files when hash value is same
  V2: change to use InfBuildData but not ModuleAutoGen
  We meet the case that first build with --hash option, then build it
  again with --hash and --binary-destination option, since the hash value
  is same, tool will not build the driver again, it cause the binary
  files are not backed up.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 83397f95f99b0884b27764f8ed13615a500e8fd7)

------------------------------------------------------------------------  r25922 | edk2buildsystem | 2017-12-13 02:08:03 -0800 (Wed, 13 Dec 2017) | 10 lines
  BaseTools: enable hash value check for single module build
  This patch enables hash value check for single module build to decide
  whether we can skip to build this module.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 19bf8314dc0187e1ccde0ccbd82b876722b8319e)

------------------------------------------------------------------------