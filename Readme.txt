Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26437

This directory contains the Win32 binaries.

Build Date:       Wed, 28 Feb 2018 03:14:14 Pacific Standard Time
Last Changed Rev: 26437

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.14 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26437
 *BootSectImage Version 1.0 Build Build 26437
 *Brotli Version 0.5.2 Build 26437
  Brotli Version 0.5.2 Build 26437
 *DevicePath Version 0.1 Build 26437
  Ecc.exe Version 1.0 Build Build 26237
 *EfiLdrImage Version 1.0 Build Build 26437
 *EfiRom Version 0.1 Build 26437
 *GenBootSector Version 0.2 Build 26437
 *GenCrc32 Version 0.2 Build 26437
 *GenDepex.exe Version 0.04 Build 26437
 *GenFds.exe 1.0 Build 26437
 *GenFfs Version 0.1 Build 26437
 *GenFv Version 0.1 Build 26437
 *GenFw Version 0.2 Build 26437
 *GenPage Version 0.2 Build 26437
 *GenPatchPcdTable.exe Version 0.10 Build 26437
 *GenSec Version 0.1 Build 26437
 *GenVtf Version 0.1 Build 26437
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 26437
  LzmaF86Compress Version 0.2 Build 26437
 *PatchPcdValue.exe Version 0.10 Build 26437
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
 *Split Version 1.0 Build Build 26437
 *TargetTool.exe Version 0.01 Build 26437
 *TianoCompress Version 0.1 Build 26437
 *Trim.exe Version 0.10 Build 26437
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 26437
 *VolInfo Version 1.0 Build Build 26437
 *build.exe Version 0.60 Build 26437

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/28/2018 3:14:15AM Engine version = 5900.7806
  2/28/2018 3:14:15AM AntiVirus DAT version = 8817.0
  2/28/2018 3:14:15AM Number of detection signatures in EXTRA.DAT = None
  2/28/2018 3:14:15AM Names of detection signatures in EXTRA.DAT = None
  2/28/2018 3:14:15AM Scan Started On-Demand Scan
  2/28/2018 3:14:28AM Scan Summary
  2/28/2018 3:14:28AM Processes scanned : 0
  2/28/2018 3:14:28AM Processes detected : 0
  2/28/2018 3:14:28AM Processes cleaned : 0
  2/28/2018 3:14:28AM Boot sectors scanned : 2
  2/28/2018 3:14:28AM Boot sectors detected: 0
  2/28/2018 3:14:28AM Boot sectors cleaned : 0
  2/28/2018 3:14:28AM Files scanned : 84
  2/28/2018 3:14:28AM Files with detections: 0
  2/28/2018 3:14:28AM File detections : 0
  2/28/2018 3:14:28AM Files cleaned : 0
  2/28/2018 3:14:28AM Files deleted : 0
  2/28/2018 3:14:28AM Files not scanned : 0
  2/28/2018 3:14:28AM Scan Summary (Registry Scanning)
  2/28/2018 3:14:28AM Keys scanned : 0
  2/28/2018 3:14:28AM Keys detected : 0
  2/28/2018 3:14:28AM Keys cleaned : 0
  2/28/2018 3:14:28AM Keys deleted : 0
  2/28/2018 3:14:28AM Run time : 0:00:13
  2/28/2018 3:14:28AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26419:HEAD Source
------------------------------------------------------------------------  r26419 | edk2buildsystem | 2018-02-27 02:05:45 -0800 (Tue, 27 Feb 2018) | 9 lines
  BaseTools:Override the MAKE_FLAGS by BuildOptions in DSC
  The issue that *_*_*_MAKE_FLAGS doesn't work in DSC [BuildOptions]
  section. It means MAKE flags can't be set in platform DSC file.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 02a908fc6d93a7971990d5fa8cd4efe023d14e43)

------------------------------------------------------------------------  r26421 | edk2buildsystem | 2018-02-27 14:05:43 -0800 (Tue, 27 Feb 2018) | 9 lines
  BaseTools: Resolve BaseTools C tool build failure
  New GUID definition is conflicted with GUID in Windows Kits guiddef.h.
  GUID definition will be defined when it is undefined.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 006c2647dc60cd7e9d32c3555a3bf7cfd890ddd6)

------------------------------------------------------------------------  r26422 | edk2buildsystem | 2018-02-27 16:39:18 -0800 (Tue, 27 Feb 2018) | 10 lines
  BaseTools: Add more error message when PcdValue is wrong
  For structure PCD, its field name is wrong and cause build failure. Its
  build error message will output to let user aware what's wrong.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Cc: Feng Bob C <bob.c.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0939fda93cbc252cd5b4ed4f026ed6ec9e07687f)

------------------------------------------------------------------------  r26423 | edk2buildsystem | 2018-02-27 16:39:26 -0800 (Tue, 27 Feb 2018) | 9 lines
  BaseTools: Update GenFw to correct DebugEntry Offset when convert XIP image
  DebugEntry FileOffset is required to be updated to the virtual address if
  the input image is converted to XIP image.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 29c50757873c431c59fa4173f9cfd5c3548a1394)

------------------------------------------------------------------------  r26426 | edk2buildsystem | 2018-02-28 02:05:46 -0800 (Wed, 28 Feb 2018) | 22 lines
  BaseTools: Fix flexible PCD single quote and double quote bugs
  1.The " and ' inside the string, must use escape character format
  (\", \')
  2.'string' and L'string' format in --pcd, it must be double quoted
  first.
  Some examples that to match --pcd format and DSC format
  --pcd                             DSC format
  L"ABC"                            L"ABC"
  "AB\\\"C"                         "AB\"C"
  "AB\\\'C"                         "AB\'C"
  L"\'AB\\\"C\'"                    L'AB\"C'
  "\'AB\\\'C\'"                     'AB\'C'
  H"{0, L\"AB\\\"B\", \'ab\\\"c\'}" {0, L"AB\"B", 'ab\"c'}
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ea927d2f3f2e34f4b26c10829f5887830cb0720e)

------------------------------------------------------------------------  r26427 | edk2buildsystem | 2018-02-28 02:05:55 -0800 (Wed, 28 Feb 2018) | 11 lines
  BaseTools: Fix report not used --pcd value incorrectly
  Argument --pcd gUefiOvmfPkgTokenSpaceGuid.test10=H"{1}",
  If the PCD is not used, report value {0x01, 0x00}, is incorrect.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 97e1ff1b913bdedcf08c0d1917d488e0097759b7)

------------------------------------------------------------------------  r26429 | edk2buildsystem | 2018-02-28 02:06:11 -0800 (Wed, 28 Feb 2018) | 11 lines
  BaseTools: Fix a bug override Pcd by DSC Components section
  The case is: define a VOID* pcd in DEC file, eg: Value is {0x1}.
  then override this PCD on DSC component section, eg: Value is
  {0x1, 0x2, 0x3}, the max size of this PCD is calculate wrong
  which cause build error.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit cdbf45ad859b1e75e055f1fd06d0c8a10452b3aa)

------------------------------------------------------------------------  r26434 | edk2buildsystem | 2018-02-28 02:06:46 -0800 (Wed, 28 Feb 2018) | 11 lines
  BaseTools: Fixed the pcd value override issue.
  1. the issue in the overriding value from command line.
  2. dec fully value < dec field assign value <
  dsc fully value < dsc field assign value
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 06140766c13fb9288a922990ffde77fca93fc71d)

------------------------------------------------------------------------  r26435 | edk2buildsystem | 2018-02-28 02:06:55 -0800 (Wed, 28 Feb 2018) | 10 lines
  BaseTools: Improve build performance of structure PCD value generation
  Add cache for building PcdValueInit.c. If PcdValueInit.c is not changed,
  it will not be regenerated.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 0a57a9782bef8ee11d8de937c149eb7ff22647c9)

------------------------------------------------------------------------  r26436 | edk2buildsystem | 2018-02-28 02:07:03 -0800 (Wed, 28 Feb 2018) | 10 lines
  BaseTool: GUID format PCD value assignment fail in Structure PCD field
  If Structure PCD field is assigned as GUID format, its data type should be
  the fixed GUID structure. No flexible check is required.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 79820e32ec96b560bc0d5cd437990f600a2ddce7)

------------------------------------------------------------------------  r26437 | edk2buildsystem | 2018-02-28 02:07:10 -0800 (Wed, 28 Feb 2018) | 9 lines
  BaseTools: Improve build performance of structure PCD value generation
  Optimized the PcdValueInit.c size by abstract the common logic in the funciton.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f3b314331ce1557d51bbd6930ca9bec01ceefdd7)

------------------------------------------------------------------------