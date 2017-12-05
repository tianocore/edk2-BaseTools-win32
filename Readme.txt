Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25818

This directory contains the Win32 binaries.

Build Date:       Tue, 05 Dec 2017 03:12:06 Pacific Standard Time
Last Changed Rev: 25816

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25818
  BootSectImage Version 1.0 Build Build 25453
  Brotli Version 0.5.2 Build 25453
  Brotli Version 0.5.2 Build 25453
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25453
  EfiRom Version 0.1 Build 25453
  GenBootSector Version 0.2 Build 25453
  GenCrc32 Version 0.2 Build 25453
 *GenDepex.exe Version 0.04 Build 25818
 *GenFds.exe 1.0 Build 25818
 *GenFfs Version 0.1 Build 25818
  GenFv Version 0.1 Build 25453
  GenFw Version 0.2 Build 25453
  GenPage Version 0.2 Build 25453
 *GenPatchPcdTable.exe Version 0.10 Build 25818
 *GenSec Version 0.1 Build 25818
  GenVtf Version 0.1 Build 25453
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25453
  LzmaF86Compress Version 0.2 Build 25453
 *PatchPcdValue.exe Version 0.10 Build 25818
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25453
 *TargetTool.exe Version 0.01 Build 25818
  TianoCompress Version 0.1 Build 25453
 *Trim.exe Version 0.10 Build 25818
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25614
  VolInfo Version 1.0 Build Build 25453
 *build.exe Version 0.60 Build 25818

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/5/2017 3:12:07AM Engine version = 5900.7806
  12/5/2017 3:12:07AM AntiVirus DAT version = 8735.0
  12/5/2017 3:12:07AM Number of detection signatures in EXTRA.DAT = None
  12/5/2017 3:12:07AM Names of detection signatures in EXTRA.DAT = None
  12/5/2017 3:12:07AM Scan Started On-Demand Scan
  12/5/2017 3:12:18AM Scan Summary
  12/5/2017 3:12:18AM Processes scanned : 0
  12/5/2017 3:12:18AM Processes detected : 0
  12/5/2017 3:12:18AM Processes cleaned : 0
  12/5/2017 3:12:18AM Boot sectors scanned : 2
  12/5/2017 3:12:18AM Boot sectors detected: 0
  12/5/2017 3:12:18AM Boot sectors cleaned : 0
  12/5/2017 3:12:18AM Files scanned : 66
  12/5/2017 3:12:18AM Files with detections: 0
  12/5/2017 3:12:18AM File detections : 0
  12/5/2017 3:12:18AM Files cleaned : 0
  12/5/2017 3:12:18AM Files deleted : 0
  12/5/2017 3:12:18AM Files not scanned : 0
  12/5/2017 3:12:18AM Scan Summary (Registry Scanning)
  12/5/2017 3:12:18AM Keys scanned : 0
  12/5/2017 3:12:18AM Keys detected : 0
  12/5/2017 3:12:18AM Keys cleaned : 0
  12/5/2017 3:12:18AM Keys deleted : 0
  12/5/2017 3:12:18AM Run time : 0:00:10
  12/5/2017 3:12:18AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25694:HEAD Source
------------------------------------------------------------------------  r25776 | edk2buildsystem | 2017-11-30 02:06:21 -0800 (Thu, 30 Nov 2017) | 11 lines
  BaseTools: Replace ARCH with HOST_ARCH in C Makefile to avoid conflict
  https://bugzilla.tianocore.org/show_bug.cgi?id=793
  ARCH is too generic. It may cause confuse of target arch or host arch.
  To be clarified, replace it with HOST_ARCH in BaseTools C Makefile.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a9f6e0a4dc6d3f4dec53bb2a11b1c0ecee455076)

------------------------------------------------------------------------  r25777 | edk2buildsystem | 2017-11-30 02:06:31 -0800 (Thu, 30 Nov 2017) | 13 lines
  BaseTools: Update BaseTools top GNUMakefile with the clear dependency
  https://bugzilla.tianocore.org/show_bug.cgi?id=786
  After GNUmakefile dependency is fixed up, it can make with -j N to enable
  multiple thread build in base tools C source and save build time.
  In my linux host machine, make -j 4 to compile BaseTools and save ~60% time.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 9e1131b70b4b6002cd1904401946ef0b22cf7d33)

------------------------------------------------------------------------  r25778 | edk2buildsystem | 2017-11-30 02:06:36 -0800 (Thu, 30 Nov 2017) | 9 lines
  BaseTools: Update C tools top GNUMakefile to adjust tool order
  Place the tool that takes much build time at the first. This can improve
  build performance when make -j N used.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 81fa5ad02821dc53fffc9e91e40f31bb4e6e34d3)

------------------------------------------------------------------------  r25813 | edk2buildsystem | 2017-12-05 02:05:35 -0800 (Tue, 05 Dec 2017) | 10 lines
  BaseTools: GenFfs support to get alignment value from SectionFile
  Update GenFfs tool to get alignment value from SectionFile when use
  the new option -n 0.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f3d8e506728e2925d64aa86a79699ecd04a167ca)

------------------------------------------------------------------------  r25814 | edk2buildsystem | 2017-12-05 02:05:40 -0800 (Tue, 05 Dec 2017) | 10 lines
  BaseTools: Update Trim to generate VfrBinOffset Binary
  Its usage is
  "Trim --Vfr-Uni-Offset -o $(OUTPUT_DIR)(+)$(MODULE_NAME)VfrOffset.sec
  --ModuleName=$(MODULE_NAME) --DebugDir=$(DEBUG_DIR)"
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 111dab620362b2f28ce48c18b1e513819e32e37f)

------------------------------------------------------------------------  r25815 | edk2buildsystem | 2017-12-05 02:05:44 -0800 (Tue, 05 Dec 2017) | 11 lines
  BaseTools: Update Gensec to set PROCESSING_REQUIRED value
  This patch add new option --dummy file, and we compare the dummpy file
  with input file to decide whether we need to set PROCESSING_REQUIRED
  value.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b37b108d92aa08cc7eed5f52feea53b0e7563068)

------------------------------------------------------------------------  r25816 | edk2buildsystem | 2017-12-05 02:05:54 -0800 (Tue, 05 Dec 2017) | 11 lines
  BaseTools: Update Makefile to support FFS file generation
  Update Makefile to support FFS file generation with new build option
  --genfds-multi-thread.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 37de70b764200718cc39a21abc491c335e3da7b3)

------------------------------------------------------------------------