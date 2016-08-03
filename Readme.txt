Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22274

This directory contains the Win32 binaries.

Build Date:       Wed, 03 Aug 2016 03:11:25 Pacific Daylight Time
Last Changed Rev: 22251

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22274
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
 *GenDepex.exe Version 0.04 Build 22274
 *GenFds.exe 1.0 Build 22274
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 20909
  GenFw Version 0.2 Build 22237
  GenPage Version 0.2 Build 20909
 *GenPatchPcdTable.exe Version 0.10 Build 22274
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
 *PatchPcdValue.exe Version 0.10 Build 22274
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
 *TargetTool.exe Version 0.01 Build 22274
  TianoCompress Version 0.1 Build 20909
 *Trim.exe Version 0.10 Build 22274
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20909
  VolInfo Version 1.0 Build Build 20909
 *build.exe Version 0.60 Build 22274

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/3/2016 3:11:27AM Engine version = 5700.7163
  8/3/2016 3:11:27AM AntiVirus DAT version = 8245.0
  8/3/2016 3:11:27AM Number of detection signatures in EXTRA.DAT = None
  8/3/2016 3:11:27AM Names of detection signatures in EXTRA.DAT = None
  8/3/2016 3:11:27AM Scan Started On-Demand Scan
  8/3/2016 3:11:29AM Scan Summary
  8/3/2016 3:11:29AM Processes scanned : 0
  8/3/2016 3:11:29AM Processes detected : 0
  8/3/2016 3:11:29AM Processes cleaned : 0
  8/3/2016 3:11:29AM Boot sectors scanned : 1
  8/3/2016 3:11:29AM Boot sectors detected: 0
  8/3/2016 3:11:29AM Boot sectors cleaned : 0
  8/3/2016 3:11:29AM Files scanned : 55
  8/3/2016 3:11:29AM Files with detections: 0
  8/3/2016 3:11:29AM File detections : 0
  8/3/2016 3:11:29AM Files cleaned : 0
  8/3/2016 3:11:29AM Files deleted : 0
  8/3/2016 3:11:29AM Files not scanned : 0
  8/3/2016 3:11:29AM Scan Summary (Registry Scanning)
  8/3/2016 3:11:29AM Keys scanned : 0
  8/3/2016 3:11:29AM Keys detected : 0
  8/3/2016 3:11:29AM Keys cleaned : 0
  8/3/2016 3:11:29AM Keys deleted : 0
  8/3/2016 3:11:29AM Run time : 0:00:02
  8/3/2016 3:11:29AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22237:HEAD Source
------------------------------------------------------------------------  r22239 | edk2buildsystem | 2016-08-02 14:05:54 -0700 (Tue, 02 Aug 2016) | 11 lines
  BaseTools: Keep the Pcd order in the Asbuilt Inf is same with Source
  The original behavior is that in the Asbuilt inf Pcd's order is base on
  the Pcd's offset. Now we change the order to keep it is same with the Pcd
  order in the source inf file.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e5cf919889b92a5fb89638ea10cebbb3ef59b5c7)

------------------------------------------------------------------------  r22248 | edk2buildsystem | 2016-08-03 02:06:53 -0700 (Wed, 03 Aug 2016) | 10 lines
  BaseTool/UPT: Add Test Install
  Add a new function to test if a DIST file list
  one by one to see if they can meet the requirement
  of Dependency.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 6cf9903481f07859cb0013598d2d13309d4e4644)

------------------------------------------------------------------------  r22249 | edk2buildsystem | 2016-08-03 02:07:00 -0700 (Wed, 03 Aug 2016) | 12 lines
  BaseTool/Upt: Add support for Private
  Support new syntax in package DEC file as below:
  [Includes.Common.Private]
  [Ppis.Common.Private]
  [Guids.Common.Private]
  [Protocols.Common.Private]
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 645a51287e9519eb4c6d27b4e4f11d0556a624e8)

------------------------------------------------------------------------  r22250 | edk2buildsystem | 2016-08-03 02:07:06 -0700 (Wed, 03 Aug 2016) | 11 lines
  BaseTool/UPT: Not expand macro for UserExtension
  All MACRO values defined by the DEFINE statements
  n any section (except [Userextensions] sections
  other than TianoCore."ExtraFiles) of the INF or
  DEC file must be expanded before processing of the file.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0e025deac50ec0fbcfc419afb47014ad1a8e10c5)

------------------------------------------------------------------------  r22251 | edk2buildsystem | 2016-08-03 02:07:13 -0700 (Wed, 03 Aug 2016) | 9 lines
  BaseTool/Upt: Avoid UNI file name conflict
  When creating a UNI file if there is a name conflict, add an index
  from 0 to the file name
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 06eb35402e456066c86f621e566160967b7740ad)

------------------------------------------------------------------------