Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26221

This directory contains the Win32 binaries.

Build Date:       Fri, 26 Jan 2018 03:12:28 Pacific Standard Time
Last Changed Rev: 26218

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26221
  BootSectImage Version 1.0 Build Build 26212
  Brotli Version 0.5.2 Build 26212
  Brotli Version 0.5.2 Build 26212
  DevicePath Version 0.1 Build 26212
  Ecc.exe Version 1.0 Build Build 26163
  EfiLdrImage Version 1.0 Build Build 26212
  EfiRom Version 0.1 Build 26212
  GenBootSector Version 0.2 Build 26212
  GenCrc32 Version 0.2 Build 26212
 *GenDepex.exe Version 0.04 Build 26221
 *GenFds.exe 1.0 Build 26221
  GenFfs Version 0.1 Build 26212
  GenFv Version 0.1 Build 26212
  GenFw Version 0.2 Build 26212
  GenPage Version 0.2 Build 26212
 *GenPatchPcdTable.exe Version 0.10 Build 26221
  GenSec Version 0.1 Build 26212
  GenVtf Version 0.1 Build 26212
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26212
  LzmaF86Compress Version 0.2 Build 26212
 *PatchPcdValue.exe Version 0.10 Build 26221
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
  Split Version 1.0 Build Build 26212
 *TargetTool.exe Version 0.01 Build 26221
  TianoCompress Version 0.1 Build 26212
 *Trim.exe Version 0.10 Build 26221
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26212
  VolInfo Version 1.0 Build Build 26212
 *build.exe Version 0.60 Build 26221

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/26/2018 3:12:30AM Engine version = 5900.7806
  1/26/2018 3:12:30AM AntiVirus DAT version = 8785.0
  1/26/2018 3:12:30AM Number of detection signatures in EXTRA.DAT = None
  1/26/2018 3:12:30AM Names of detection signatures in EXTRA.DAT = None
  1/26/2018 3:12:30AM Scan Started On-Demand Scan
  1/26/2018 3:12:40AM Scan Summary
  1/26/2018 3:12:40AM Processes scanned : 0
  1/26/2018 3:12:40AM Processes detected : 0
  1/26/2018 3:12:40AM Processes cleaned : 0
  1/26/2018 3:12:40AM Boot sectors scanned : 2
  1/26/2018 3:12:40AM Boot sectors detected: 0
  1/26/2018 3:12:40AM Boot sectors cleaned : 0
  1/26/2018 3:12:40AM Files scanned : 66
  1/26/2018 3:12:40AM Files with detections: 0
  1/26/2018 3:12:40AM File detections : 0
  1/26/2018 3:12:40AM Files cleaned : 0
  1/26/2018 3:12:40AM Files deleted : 0
  1/26/2018 3:12:40AM Files not scanned : 0
  1/26/2018 3:12:40AM Scan Summary (Registry Scanning)
  1/26/2018 3:12:40AM Keys scanned : 0
  1/26/2018 3:12:40AM Keys detected : 0
  1/26/2018 3:12:40AM Keys cleaned : 0
  1/26/2018 3:12:40AM Keys deleted : 0
  1/26/2018 3:12:40AM Run time : 0:00:11
  1/26/2018 3:12:40AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26212:HEAD Source
------------------------------------------------------------------------  r26213 | edk2buildsystem | 2018-01-25 14:05:36 -0800 (Thu, 25 Jan 2018) | 7 lines
  BaseTool: Combine the HiiPcd value if they link to same Variable
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e6bf3cfd50c1f4f6c6d4648ee89c950094d85727)

------------------------------------------------------------------------  r26214 | edk2buildsystem | 2018-01-25 14:05:42 -0800 (Thu, 25 Jan 2018) | 7 lines
  BaseTools: Add comments for the Structure Pcd definition in PcdValueInit.c file
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 6a103440806c33c0aaa401cd443dc786d259397e)

------------------------------------------------------------------------  r26215 | edk2buildsystem | 2018-01-26 02:05:35 -0800 (Fri, 26 Jan 2018) | 9 lines
  BaseTools: Fixed build failure for the PCD value initialization.
  A pcd is initialized under one SKU but is uninitialized under another SKU.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 841d86fe406ed6cf504c62b6838876a65cf8f7a0)

------------------------------------------------------------------------  r26216 | edk2buildsystem | 2018-01-26 02:05:42 -0800 (Fri, 26 Jan 2018) | 10 lines
  BaseTools: Fixed some small issues
  1. The structure pcd default value should use the default value under sku.
  2. Incorrect VpdOffset value for those un-used in module Vpd
  3. Add a checkpoint for Structure Pcd Name
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 8e011d83bbd7006919c00917fbdfaf7a60edae21)

------------------------------------------------------------------------  r26217 | edk2buildsystem | 2018-01-26 02:05:47 -0800 (Fri, 26 Jan 2018) | 10 lines
  BaseTool: Fixed the StructurePcd incorrect value.
  If user not set Structure overall value in Dsc,
  Structure Pcd value would be incorrect.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9904222db0affb82d2aa0004dda35c3c66b74234)

------------------------------------------------------------------------  r26218 | edk2buildsystem | 2018-01-26 02:05:52 -0800 (Fri, 26 Jan 2018) | 8 lines
  BaseTools: Fixed incorrect VPD size.
  The VPD size is incorrect if that VPD is not used in Module.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Feng Bob C <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e827d21da1c21aea0e1cdc9b896aacf988a5bacd)

------------------------------------------------------------------------