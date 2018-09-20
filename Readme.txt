Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 27924

This directory contains the Win32 binaries.

Build Date:       Thu, 20 Sep 2018 09:13:58 Pacific Daylight Time
Last Changed Rev: 27923

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.14 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
ERROR : This tool is missing --version option: BPDG.exe
  BootSectImage Version 1.0 Build Build 27752
  Brotli Version 0.5.2 Build 27191
  Brotli Version 0.5.2 Build 27191
  DevicePath Version 0.1 Build 27752
  Ecc.exe Version 1.0 Build Build 27306
  EfiLdrImage Version 1.0 Build Build 27752
  EfiRom Version 0.1 Build 27752
  GenBootSector Version 0.2 Build 27752
  GenCrc32 Version 0.2 Build 27752
  GenDepex.exe Version 0.04 Build 27752
ERROR : This tool is missing --version option: GenFds.exe
  GenFfs Version 0.1 Build 27752
  GenFv Version 0.1 Build 27752
  GenFw Version 0.2 Build 27752
  GenPage Version 0.2 Build 27752
  GenPatchPcdTable.exe Version 0.10 Build 27752
  GenSec Version 0.1 Build 27752
  GenVtf Version 0.1 Build 27752
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 27752
  LzmaF86Compress Version 0.2 Build 27752
  PatchPcdValue.exe Version 0.10 Build 27752
  Pkcs7Sign Version 0.9 Build 27752
  Rsa2048Sha256GenerateKeys Version 0.9 Build 27752
  Rsa2048Sha256Sign Version 0.9 Build 27752
  Split Version 1.0 Build Build 27191
  TargetTool.exe Version 0.01 Build 27752
  TianoCompress Version 0.1 Build 27752
  Trim.exe Version 0.10 Build 27752
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 27752
  VfrCompile version  2.01 (UEFI 2.4) Build Build 27752
  VolInfo Version 1.0 Build Build 27752
  build.exe Version 0.60 Build 27752

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  9/20/2018 9:14:00AM Engine version = 5900.7806
  9/20/2018 9:14:00AM AntiVirus DAT version = 9021.0
  9/20/2018 9:14:00AM Number of detection signatures in EXTRA.DAT = None
  9/20/2018 9:14:00AM Names of detection signatures in EXTRA.DAT = None
  9/20/2018 9:14:00AM Scan Started On-Demand Scan
  9/20/2018 9:14:10AM Scan Summary
  9/20/2018 9:14:10AM Processes scanned : 0
  9/20/2018 9:14:10AM Processes detected : 0
  9/20/2018 9:14:10AM Processes cleaned : 0
  9/20/2018 9:14:10AM Boot sectors scanned : 2
  9/20/2018 9:14:10AM Boot sectors detected: 0
  9/20/2018 9:14:10AM Boot sectors cleaned : 0
  9/20/2018 9:14:10AM Files scanned : 66
  9/20/2018 9:14:10AM Files with detections: 0
  9/20/2018 9:14:10AM File detections : 0
  9/20/2018 9:14:10AM Files cleaned : 0
  9/20/2018 9:14:10AM Files deleted : 0
  9/20/2018 9:14:10AM Files not scanned : 0
  9/20/2018 9:14:10AM Scan Summary (Registry Scanning)
  9/20/2018 9:14:10AM Keys scanned : 0
  9/20/2018 9:14:10AM Keys detected : 0
  9/20/2018 9:14:10AM Keys cleaned : 0
  9/20/2018 9:14:10AM Keys deleted : 0
  9/20/2018 9:14:10AM Run time : 0:00:11
  9/20/2018 9:14:10AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 27752:HEAD Source
------------------------------------------------------------------------  r27753 | edk2buildsystem | 2018-08-21 02:05:58 -0700 (Tue, 21 Aug 2018) | 15 lines
  BaseTools: Fix regression issue by b23414f6540d
  V2: Renaming function DepexExpressionTokenList to  DepexExpressionDict
  instead of changing the callers
  Fix regression issue by b23414f6540d4f336b6f00b44681911d469f9a04
  AttributeError: 'ModuleAutoGen' object has no attribute
  'DepexExpressionDict'
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 6cf6fed02408b5f3ba39de46cbc971b9dda3639b)

------------------------------------------------------------------------  r27789 | edk2buildsystem | 2018-08-22 14:05:31 -0700 (Wed, 22 Aug 2018) | 39 lines
  BaseTools/VfrCompile: honor EXTRA_LDFLAGS
  In commit 81502cee20ac ("BaseTools/Source/C: take EXTRA_LDFLAGS from the
  caller", 2018-08-16), I missed that "VfrCompile/GNUmakefile" does not use
  BUILD_LFLAGS in the APPLICATION linking rule, unlike "app.makefile" does.
  Instead, "VfrCompile/GNUmakefile" uses the (undefined) LFLAGS macro.
  Therefore commit 81502cee20ac did not cover the linking step of
  VfrCompile.
  Thankfully, the structure of the linking rules is the same, between
  "app.makefile" and "VfrCompile/GNUmakefile". Rename the undefined LFLAGS
  macro in "VfrCompile/GNUmakefile" to VFR_LFLAGS (for consistency with
  VFR_CXXFLAGS), and set it to EXTRA_LDFLAGS.
  As a result, we have:
  | compilation                    | linking

-----------+--------------------------------+----------------------  VfrCompile | VFR_CXXFLAGS =                 | VFR_LFLAGS =
  | BUILD_OPTFLAGS =               | EXTRA_LDFLAGS
  | '-O2' + EXTRA_OPTFLAGS         |

-----------+--------------------------------+----------------------  other apps | BUILD_CFLAGS/BUILD_CXXFLAGS =  | BUILD_LFLAGS =
  | [...] + BUILD_OPTFLAGS =       | [...] + EXTRA_LDFLAGS
  | [...] + '-O2' + EXTRA_OPTFLAGS |
  This table shows
  - that the VfrCompile compilation and linking flags are always a subset of
  the corresponding flags used by the other apps,
  - and that the EXTRA flags are always at the end.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Ref: https://bugzilla.redhat.com/show_bug.cgi?id=1540244
  Fixes: 81502cee20ac4046f08bb4aec754c7091c8808dc
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit aa4e0df1f0c7ffdff07d7e382c9da89cbe207cdb)

------------------------------------------------------------------------  r27790 | edk2buildsystem | 2018-08-23 02:05:41 -0700 (Thu, 23 Aug 2018) | 11 lines
  BaseTools: Update Makefile for ECC tool
  V2: Add --target-name to specify the file name to create
  Because Ecc.py was renamed to EccMain.py
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c1260801fdfb89c91878984dfbc3c5a125696886)

------------------------------------------------------------------------  r27791 | edk2buildsystem | 2018-08-23 02:05:56 -0700 (Thu, 23 Aug 2018) | 12 lines
  BaseTools: Modify class OrderedListDict
  class OrderedListDict(OrderedDict, defaultdict) will
  encounter multiple bases have instance lay-out
  conflict error on python3
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit abb8e6e97a72c53b1a5110cfdf2795d63acdadbc)

------------------------------------------------------------------------  r27792 | edk2buildsystem | 2018-08-23 02:06:09 -0700 (Thu, 23 Aug 2018) | 10 lines
  BaseTools: remove cmp due to deprecated in python3
  remove cmp due to deprecated in python3
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 87010d3d02547c81f1add57a4e2ef0483c65fddf)

------------------------------------------------------------------------  r27793 | edk2buildsystem | 2018-08-23 02:06:30 -0700 (Thu, 23 Aug 2018) | 11 lines
  BaseTools: Use hashlib instead of md5
  Use from hashlib import md5 instead of import md5
  due to md5 deprecated in python3
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit fcb1af1b69f8c491824aaa589c7693fa6e731e0b)

------------------------------------------------------------------------  r27823 | edk2buildsystem | 2018-08-28 02:05:59 -0700 (Tue, 28 Aug 2018) | 11 lines
  BaseTools: Add check only VOID* type Pcd need the maxsize info
  Add check for the datum type keyword "VOID*", only the VOID* type
  Pcd need the additional maxsize info.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zhiju.Fan <zhijux.fan@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit f2cc33d84949b711193aed145254f3b71dbfea57)

------------------------------------------------------------------------  r27824 | edk2buildsystem | 2018-08-28 02:06:07 -0700 (Tue, 28 Aug 2018) | 9 lines
  BaseTools: Fix one expression bug to support ~ operate
  current use (0x41>=~0x0&0x41|0x0) as Pcd value cause build failure
  because the ~ is not correctly recognized.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f25cd80e4d823fa6f7d970d9f0ddb935327446ba)

------------------------------------------------------------------------  r27825 | edk2buildsystem | 2018-08-29 02:05:33 -0700 (Wed, 29 Aug 2018) | 10 lines
  BaseTools: AutoGen.py remove unused import
  AutoGen does not use anything defined in BuildClassObject
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0fa0e56ee002cf369f7f4a1076eac52f813e03f0)

------------------------------------------------------------------------  r27832 | edk2buildsystem | 2018-08-30 02:06:57 -0700 (Thu, 30 Aug 2018) | 11 lines
  BaseTools: Create and use a shared value for 'MSFT' from DataType
  I see lots of 'MSFT' throughout code and this can reduce them.
  Cc: Bob Feng <Bob.c.Feng@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 94c04559374df0d1cecea32114df7be6d5931db9)

------------------------------------------------------------------------  r27837 | edk2buildsystem | 2018-08-30 14:05:32 -0700 (Thu, 30 Aug 2018) | 15 lines
  BaseTools: include variable namespace GUIDs of HII PCDs in Guid.xref
  [PcdsDynamicHii]
  gFooTokenSpaceGuid.PcdBar|L"Variable"|gVarNameSpaceGuid|0x0|FALSE|NV,BS
  This patch add the variable namespace GUIDs in "Guid.xref" that are
  used with dynamic HII PCDs.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=452
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zhiju.Fan <zhijux.fan@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0fece18d6df83cede91a4c8644c2278e63794a62)

------------------------------------------------------------------------  r27838 | edk2buildsystem | 2018-08-30 14:05:43 -0700 (Thu, 30 Aug 2018) | 12 lines
  BaseTools: Refactor to remove functionally equivalent functions
  IsSupportedArch and IsBinaryModule return the same value under the same
  curcimstances.  Remove newer one with fewer callers and send them to the
  other function.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit f5f4667dae711a7e34c75a4cd8f7a683c732a566)

------------------------------------------------------------------------  r27839 | edk2buildsystem | 2018-08-30 14:05:52 -0700 (Thu, 30 Aug 2018) | 10 lines
  BaseTools: minimize assignment processing
  Reverse the checking and only assign once to each variable.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a77e5bcac54d2e2437d7deaec9af5362c9220037)

------------------------------------------------------------------------  r27840 | edk2buildsystem | 2018-08-31 02:05:42 -0700 (Fri, 31 Aug 2018) | 11 lines
  BaseTools: Clarify a DSC parsing error about PCDs
  This error needs the information about which DEC files were searched.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Lee Hamel <lee.m.hamel@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 209d095968c4c87418e547261f62966bce34b443)

------------------------------------------------------------------------  r27852 | edk2buildsystem | 2018-09-03 02:06:14 -0700 (Mon, 03 Sep 2018) | 13 lines
  BaseTools: Check pcd DefaultValue and SkuId EBNF.
  1. When assign dynamic hii pcd value in dsc file,
  missed the DefaultValue, build should be fail.
  2. Check the EBNF of SkuId.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: ZhiqiangX Zhao <zhiqiangx.zhao@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Bob Feng <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 24bd035c904fae1868bb15dc00cfa2e197cc5809)

------------------------------------------------------------------------  r27853 | edk2buildsystem | 2018-09-03 02:06:23 -0700 (Mon, 03 Sep 2018) | 10 lines
  BaseTools: Dynamic Pcd value override from command line.
  Fixed the pcd value override issue when Dynamic Pcd is from
  command line but is not list in Dsc file.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 7c193787623f89d161255e37d80bc2907690ab37)

------------------------------------------------------------------------  r27854 | edk2buildsystem | 2018-09-03 02:06:36 -0700 (Mon, 03 Sep 2018) | 11 lines
  BaseTools: Fixed the PcdValue trailing zero issue.
  1. Not append trailing zero for PcdValue
  2. make sure the point to Variable Name in PCD
  DataBase 2 bytes aligned.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 4cf022f2f11fc3cd12ab5dd24e5ae74f541bac48)

------------------------------------------------------------------------  r27860 | edk2buildsystem | 2018-09-05 02:05:33 -0700 (Wed, 05 Sep 2018) | 13 lines
  BaseTools: Extend the keyword "!include"/"!if" to case-insensitive
  Extend the keyword "!include", "!if", etc to case-insensitive.
  Current DSC parser already support it, while FDF parser only support
  the lower case, so this patch add the support for FDF parser.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=1111
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zhiju.Fan <zhijux.fan@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 865d7f7b0158f3fb4b3fb187aae4b323a705a8ed)

------------------------------------------------------------------------  r27864 | edk2buildsystem | 2018-09-06 02:06:21 -0700 (Thu, 06 Sep 2018) | 13 lines
  BaseTools: Fix a bug about list the PCD in "not used" section
  Defined a pcd in Ovmf.dec and used that pcd in AcpiPlatformDxe.inf,
  then assign a value to that pcd from DSC, then build Ovmf platform
  successfully. But this Pcd was wrongly listed into not used section
  in the report.txt file.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zhiju.Fan <zhijux.fan@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ac4578af364916a8848453ad0f719e872b8782ec)

------------------------------------------------------------------------  r27865 | edk2buildsystem | 2018-09-06 02:06:33 -0700 (Thu, 06 Sep 2018) | 11 lines
  BaseTools: Report more clear error message for PCD used in expression
  Only the FeatureFlag type or FixedAtBuild type can be used in the
  expression.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zhiju.Fan <zhijux.fan@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit fa6e2804de6a7c9b108afcba4b03714b13f4a113)

------------------------------------------------------------------------  r27875 | edk2buildsystem | 2018-09-07 02:05:34 -0700 (Fri, 07 Sep 2018) | 12 lines
  BaseTools: refactor to remove duplicate functions
  Update GenFdsGlobalVariable GetAlignment to support G.
  replace use of local function in Region with updated shared function.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Bob C Feng <bob.c.feng@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7bf1eb6ef8ae6ccffca6fc8f36b132be704c0b1b)

------------------------------------------------------------------------  r27876 | edk2buildsystem | 2018-09-07 02:05:53 -0700 (Fri, 07 Sep 2018) | 8 lines
  BaseTools/GenFds: remove function without callers
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7761cee050e706544bfee70f1c6ca894be0b1a2a)

------------------------------------------------------------------------  r27893 | edk2buildsystem | 2018-09-11 14:05:50 -0700 (Tue, 11 Sep 2018) | 8 lines
  BaseTools/GenFds: delete unused file
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1ad635b283812283e8db457ba4809d5d38433f17)

------------------------------------------------------------------------  r27895 | edk2buildsystem | 2018-09-12 02:06:32 -0700 (Wed, 12 Sep 2018) | 11 lines
  BaseTools: Report error for incorrect hex value format
  The case is user use 0x1} as a hex value for Pcd, it directly cause
  tool report traceback info. This patch add more error info.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zhiju.Fan <zhijux.fan@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b62cbfb787e1ac594fce618a1a9c86cabc63d54b)

------------------------------------------------------------------------  r27896 | edk2buildsystem | 2018-09-12 02:06:52 -0700 (Wed, 12 Sep 2018) | 11 lines
  BaseTools: Structure Pcd value override incorrect.
  This patch is going to fix the issue that
  The Pcd field value is override incorrectly when there
  is no Pcd overall value assignment in Dsc file.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 71127ce88392d2a0392cb0cb90eaa0245da14f05)

------------------------------------------------------------------------  r27897 | edk2buildsystem | 2018-09-12 02:07:12 -0700 (Wed, 12 Sep 2018) | 12 lines
  BaseTools: Involve Dec default value to calculate Maxsize
  Involve Dec default value to calculate Maxsize for structure PCD
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Jaben Carsey <jaben.carsey@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit cfed8a37ec3cf974e4eaaa298da6704133b00019)

------------------------------------------------------------------------  r27898 | edk2buildsystem | 2018-09-12 02:07:30 -0700 (Wed, 12 Sep 2018) | 13 lines
  BaseTools: Check PcdNvStoreDefaultValueBuffer.
  Build tool should report warning if a platform
  defines [DefaultStores] but forgets to defined
  PcdNvStoreDefaultValueBuffer as PcdsDynamicExVpd in dsc file.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: ZhiqiangX Zhao <zhiqiangx.zhao@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Bob Feng <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit ced8685838bd5a9b091fdc537c494e36450b05f5)

------------------------------------------------------------------------  r27899 | edk2buildsystem | 2018-09-12 02:07:47 -0700 (Wed, 12 Sep 2018) | 12 lines
  BaseTools: Correct DXE_PCD_DATABASE_INIT.
  Add the handle of PCD_DATABASE_INIT and PCD_DATABASE_UNINIT
  for Boolean type pcd.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: ZhiqiangX Zhao <zhiqiangx.zhao@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Bob Feng <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 4c6fda33c8aafd76cad7631e5da955b916313436)

------------------------------------------------------------------------  r27900 | edk2buildsystem | 2018-09-12 02:08:07 -0700 (Wed, 12 Sep 2018) | 13 lines
  BaseTools: SKU inheritance.
  If the SkuB's parent SkuA is not in SKUID_IDENTIFIER, then
  make SkuB inherit from SkuA as if the SKUID_INDENTIFIER
  is ALL.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: ZhiqiangX Zhao <zhiqiangx.zhao@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Bob Feng <bob.c.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 84a52d4d030185a44f2d8736142c6f0b19c6e9b1)

------------------------------------------------------------------------  r27902 | edk2buildsystem | 2018-09-12 02:08:56 -0700 (Wed, 12 Sep 2018) | 20 lines
  BaseTools: Support multi thread build Basetool on Windows
  Add NmakeSubdirs.py to replace NmakeSubdirs.bat in VS Makefile. This script will
  invoke nmake in multi thread mode. It can save more than half time of BaseTools
  C clean build.
  GCC make supports multiple thread in make phase. So, GNUmakefile doesn't need apply
  this script.
  single task or job=1:
  just single thread and invoke subprocess,subprocess will use
  system.stdout to print output.
  multi task:
  thread number is logic cpu count.All subprocess output will pass to
  python script by PIPE and then script print it to system.stdout.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Dongao Guo<dongao.guo@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Test-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 4c0d19e5bf50c0edc33914a1d3e8b69943d5473f)

------------------------------------------------------------------------  r27903 | edk2buildsystem | 2018-09-12 02:09:11 -0700 (Wed, 12 Sep 2018) | 11 lines
  BaseTools: Fix the RaiseError variable issue caused by 855698fb69f
  The bug is that it cause the RaiseError always be set to TRUE even we
  call the function with FALSE parameter.
  Cc: Hess Chen <hesheng.chen@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Hess Chen <hesheng.chen@intel.com>
  (cherry picked from commit 4423f0bc613b5451feaa546c3f330ad625d65638)

------------------------------------------------------------------------  r27906 | edk2buildsystem | 2018-09-13 02:06:33 -0700 (Thu, 13 Sep 2018) | 12 lines
  BaseTools\GenFds: remove extra content
  remove uncalled functions
  remove extra blank lines
  remove commented out code
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit eb2afe08cec34cf1e2a9e6f39c6adc9c66b2498a)

------------------------------------------------------------------------  r27907 | edk2buildsystem | 2018-09-13 02:06:52 -0700 (Thu, 13 Sep 2018) | 11 lines
  BaseTools: Align the boolean type PCD value's display in the report
  This patch align the boolean type PCD value's display in the build
  report. Original it may display 0x0, also may use 0 for the same PCD.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zhiju.Fan <zhijux.fan@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7c41b8135de692ea45334747b73936ea6804622f)

------------------------------------------------------------------------  r27914 | edk2buildsystem | 2018-09-14 02:06:46 -0700 (Fri, 14 Sep 2018) | 9 lines
  BaseTools: Check GUID C structure format
  GUID C format must conform to {8,4,4,{2,2,2,2,2,2,2,2}}
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  (cherry picked from commit 85e5d3cf6b32127977d0d4ef293f4b07daa23747)

------------------------------------------------------------------------  r27923 | edk2buildsystem | 2018-09-18 02:05:58 -0700 (Tue, 18 Sep 2018) | 12 lines
  BaseTools: Fix a bug for Unused PCDs section display in the report
  Fix a regression issue caused by ac4578af364, when there doesn't exist
  not used PCD, it also display the not used Pcd section in the report.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=1170
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zhiju.Fan <zhijux.fan@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ae57950fc878618083bca435fa4bc00d4bec97c1)

------------------------------------------------------------------------