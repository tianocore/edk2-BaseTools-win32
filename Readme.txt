Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20882

This directory contains the Win32 binaries.

Build Date:       Mon, 16 May 2016 03:12:09 Pacific Daylight Time
Last Changed Rev: 20882

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20882
 *BootSectImage Version 1.0 Build Build 20882
  Ecc.exe Version 1.0 Build Build 20528
 *EfiLdrImage Version 1.0 Build Build 20882
 *EfiRom Version 0.1 Build 20882
 *GenBootSector Version 0.2 Build 20882
 *GenCrc32 Version 0.2 Build 20882
 *GenDepex.exe Version 0.04 Build 20882
 *GenFds.exe 1.0 Build 20882
 *GenFfs Version 0.1 Build 20882
 *GenFv Version 0.1 Build 20882
 *GenFw Version 0.2 Build 20882
 *GenPage Version 0.2 Build 20882
 *GenPatchPcdTable.exe Version 0.10 Build 20882
 *GenSec Version 0.1 Build 20882
 *GenVtf Version 0.1 Build 20882
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 20882
  LzmaF86Compress Version 0.2 Build 20882
 *PatchPcdValue.exe Version 0.10 Build 20882
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
 *Split Version 1.0 Build Build 20882
 *TargetTool.exe Version 0.01 Build 20882
 *TianoCompress Version 0.1 Build 20882
 *Trim.exe Version 0.10 Build 20882
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 20882
 *VolInfo Version 1.0 Build Build 20882
 *build.exe Version 0.60 Build 20882

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/16/2016 3:12:11AM Engine version = 5700.7163
  5/16/2016 3:12:11AM AntiVirus DAT version = 8166.0
  5/16/2016 3:12:11AM Number of detection signatures in EXTRA.DAT = None
  5/16/2016 3:12:11AM Names of detection signatures in EXTRA.DAT = None
  5/16/2016 3:12:11AM Scan Started On-Demand Scan
  5/16/2016 3:12:13AM Scan Summary
  5/16/2016 3:12:13AM Processes scanned : 0
  5/16/2016 3:12:13AM Processes detected : 0
  5/16/2016 3:12:13AM Processes cleaned : 0
  5/16/2016 3:12:13AM Boot sectors scanned : 1
  5/16/2016 3:12:13AM Boot sectors detected: 0
  5/16/2016 3:12:13AM Boot sectors cleaned : 0
  5/16/2016 3:12:13AM Files scanned : 71
  5/16/2016 3:12:13AM Files with detections: 0
  5/16/2016 3:12:13AM File detections : 0
  5/16/2016 3:12:13AM Files cleaned : 0
  5/16/2016 3:12:13AM Files deleted : 0
  5/16/2016 3:12:13AM Files not scanned : 0
  5/16/2016 3:12:13AM Scan Summary (Registry Scanning)
  5/16/2016 3:12:13AM Keys scanned : 0
  5/16/2016 3:12:13AM Keys detected : 0
  5/16/2016 3:12:13AM Keys cleaned : 0
  5/16/2016 3:12:13AM Keys deleted : 0
  5/16/2016 3:12:13AM Run time : 0:00:02
  5/16/2016 3:12:13AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20849:HEAD Source
------------------------------------------------------------------------  r20874 | edk2buildsystem | 2016-05-16 02:05:39 -0700 (Mon, 16 May 2016) | 12 lines
  BaseTools: Fix bug to not mix comment into Asbuilt inf Depex section
  in the generated Asbuilt inf would include the driver's complete
  dependency expression, and it would be wrote as comment format. Original
  bug is mix the depex expression with real comment in the depex section.
  this patch is ignore the real comment, and list the depex expression.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 518aebe2f7ab2ca7376f450a07439b5741e65503)

------------------------------------------------------------------------  r20875 | edk2buildsystem | 2016-05-16 02:05:43 -0700 (Mon, 16 May 2016) | 14 lines
  BaseTools/GenFds: enhance INF built arch filter
  The bug is use FILE_GUID override to build the same module more than
  once, GenFds report warning "xxx NOT found in DSC file; Is it really
  a binary module?". The root cause is the module path with FILE_GUID
  overridden has the file name FILE_GUIDmodule.inf, then
  PlatformDataBase.Modules use FILE_GUIDmodule.inf as key which cause
  __GetPlatformArchList__ return empty.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 4ce415e55d93a9ae9fa1fbd6b40080877ae5f23b)

------------------------------------------------------------------------  r20876 | edk2buildsystem | 2016-05-16 02:05:48 -0700 (Mon, 16 May 2016) | 11 lines
  BaseTools/GenFw: enhance to use Magic Field to identify the image
  Original use the File Header Machine Field to identify
  EFI_IMAGE_OPTIONAL_HEADER32 or EFI_IMAGE_OPTIONAL_HEADER64, it cannot
  correctly handle EBC arch PE32 image.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 849e54aa6400b220fad8af32d3d329117e0ceac8)

------------------------------------------------------------------------  r20882 | edk2buildsystem | 2016-05-16 02:06:15 -0700 (Mon, 16 May 2016) | 12 lines
  BaseTools: Add HII definitions from UEFI 2.6
  Add HII definitions from UEFI 2.6 for HII Image Variability and PNG
  Blocks
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Samer El-Haj-Mahmoud <elhaj@hpe.com>
  Reviewed-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7b1fe7acdca15be49a9421156b799ed7394f7bac)

------------------------------------------------------------------------