Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25600

This directory contains the Win32 binaries.

Build Date:       Mon, 06 Nov 2017 11:32:28 Pacific Standard Time
Last Changed Rev: 10

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25600
  BootSectImage Version 1.0 Build Build 25453
  Brotli Version 0.5.2 Build 25453
  Brotli Version 0.5.2 Build 25453
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25453
  EfiRom Version 0.1 Build 25453
  GenBootSector Version 0.2 Build 25453
  GenCrc32 Version 0.2 Build 25453
 *GenDepex.exe Version 0.04 Build 25600
 *GenFds.exe 1.0 Build 25600
  GenFfs Version 0.1 Build 25453
  GenFv Version 0.1 Build 25453
  GenFw Version 0.2 Build 25453
  GenPage Version 0.2 Build 25453
 *GenPatchPcdTable.exe Version 0.10 Build 25600
  GenSec Version 0.1 Build 25453
  GenVtf Version 0.1 Build 25453
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25453
  LzmaF86Compress Version 0.2 Build 25453
 *PatchPcdValue.exe Version 0.10 Build 25600
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25453
 *TargetTool.exe Version 0.01 Build 25600
  TianoCompress Version 0.1 Build 25453
 *Trim.exe Version 0.10 Build 25600
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25453
  VolInfo Version 1.0 Build Build 25453
 *build.exe Version 0.60 Build 25600

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/6/2017 11:33:00AM Engine version = 5900.7806
  11/6/2017 11:33:00AM AntiVirus DAT version = 8703.0
  11/6/2017 11:33:00AM Number of detection signatures in EXTRA.DAT = None
  11/6/2017 11:33:00AM Names of detection signatures in EXTRA.DAT = None
  11/6/2017 11:33:00AM Scan Started On-Demand Scan
  11/6/2017 11:33:36AM Scan Summary
  11/6/2017 11:33:36AM Processes scanned : 0
  11/6/2017 11:33:36AM Processes detected : 0
  11/6/2017 11:33:36AM Processes cleaned : 0
  11/6/2017 11:33:36AM Boot sectors scanned : 2
  11/6/2017 11:33:36AM Boot sectors detected: 0
  11/6/2017 11:33:36AM Boot sectors cleaned : 0
  11/6/2017 11:33:36AM Files scanned : 64
  11/6/2017 11:33:36AM Files with detections: 0
  11/6/2017 11:33:36AM File detections : 0
  11/6/2017 11:33:36AM Files cleaned : 0
  11/6/2017 11:33:36AM Files deleted : 0
  11/6/2017 11:33:36AM Files not scanned : 0
  11/6/2017 11:33:36AM Scan Summary (Registry Scanning)
  11/6/2017 11:33:36AM Keys scanned : 0
  11/6/2017 11:33:36AM Keys detected : 0
  11/6/2017 11:33:36AM Keys cleaned : 0
  11/6/2017 11:33:36AM Keys deleted : 0
  11/6/2017 11:33:36AM Run time : 0:00:41
  11/6/2017 11:33:36AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25532:HEAD Source
------------------------------------------------------------------------  r25532 | edk2buildsystem | 2017-10-16 02:06:07 -0700 (Mon, 16 Oct 2017) | 13 lines
  BaseTools: Fix a bug Build directory should relative to WORKSPACE
  The bug is for build output files it still use mws.join function, it
  cause maybe we will get the build output files in the PACKAGES_PATH
  because mws.join will try WORKSPACE first, if the file doesn't exist
  then try PACKAGES_PATH. But for build output, we expected it should
  relative to WORKSPACE.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 97058144294759ffb64005a8543d5dd9a5bdc1fc)

------------------------------------------------------------------------  r25599 | edk2buildsystem | 2017-11-03 02:05:26 -0700 (Fri, 03 Nov 2017) | 20 lines
  BaseTools/VfrCompile: Add check to avoid using NULL pointer
  Question value are stored in one specified storage, but the Data type
  of the storage is not specified or there is no sub fields in the Data
  type sometimes, so we need to add check before using related pointers.
  Here list some NULL cases:
  (1)For an efivastore which doesn't specify a data structure or a
  data type(UINT8,UINT16...)as the storage, just has VarName and
  VarSize instead, we can not get its data type before parsing
  its VarSize.
  (2)For efivastore which just specifies the data type(UINT8,UINT16...)
  not a structure as the storage,this data type doesn't have sub-fields.
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 631ffb70ebbe78b6e3f342b7ad9ab9b75f8796ae)

------------------------------------------------------------------------  r25600 | edk2buildsystem | 2017-11-03 02:05:32 -0700 (Fri, 03 Nov 2017) | 10 lines
  BaseTools: parse map file generated by Xcode on Mac
  Add support to parse map file generated by Xcode on Mac to get
  variable offset and Patchable Pcd info in current EFI file.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 14239ee0770fdbb1d69f1e3f5f70b8df30de1895)

------------------------------------------------------------------------