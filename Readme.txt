Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26482

This directory contains the Win32 binaries.

Build Date:       Sun, 04 Mar 2018 03:14:18 Pacific Standard Time
Last Changed Rev: 26475

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.14 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26482
 *BootSectImage Version 1.0 Build Build 26482
 *Brotli Version 0.5.2 Build 26482
  Brotli Version 0.5.2 Build 26482
 *DevicePath Version 0.1 Build 26482
  Ecc.exe Version 1.0 Build Build 26237
 *EfiLdrImage Version 1.0 Build Build 26482
 *EfiRom Version 0.1 Build 26482
 *GenBootSector Version 0.2 Build 26482
 *GenCrc32 Version 0.2 Build 26482
 *GenDepex.exe Version 0.04 Build 26482
 *GenFds.exe 1.0 Build 26482
 *GenFfs Version 0.1 Build 26482
 *GenFv Version 0.1 Build 26482
 *GenFw Version 0.2 Build 26482
 *GenPage Version 0.2 Build 26482
 *GenPatchPcdTable.exe Version 0.10 Build 26482
 *GenSec Version 0.1 Build 26482
 *GenVtf Version 0.1 Build 26482
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 26482
  LzmaF86Compress Version 0.2 Build 26482
 *PatchPcdValue.exe Version 0.10 Build 26482
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
 *Split Version 1.0 Build Build 26482
 *TargetTool.exe Version 0.01 Build 26482
 *TianoCompress Version 0.1 Build 26482
 *Trim.exe Version 0.10 Build 26482
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 26482
 *VolInfo Version 1.0 Build Build 26482
 *build.exe Version 0.60 Build 26482

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/4/2018 3:14:19AM Engine version = 5900.7806
  3/4/2018 3:14:19AM AntiVirus DAT version = 8821.0
  3/4/2018 3:14:19AM Number of detection signatures in EXTRA.DAT = None
  3/4/2018 3:14:19AM Names of detection signatures in EXTRA.DAT = None
  3/4/2018 3:14:20AM Scan Started On-Demand Scan
  3/4/2018 3:14:35AM Scan Summary
  3/4/2018 3:14:35AM Processes scanned : 0
  3/4/2018 3:14:35AM Processes detected : 0
  3/4/2018 3:14:35AM Processes cleaned : 0
  3/4/2018 3:14:35AM Boot sectors scanned : 2
  3/4/2018 3:14:35AM Boot sectors detected: 0
  3/4/2018 3:14:35AM Boot sectors cleaned : 0
  3/4/2018 3:14:35AM Files scanned : 84
  3/4/2018 3:14:35AM Files with detections: 0
  3/4/2018 3:14:35AM File detections : 0
  3/4/2018 3:14:35AM Files cleaned : 0
  3/4/2018 3:14:35AM Files deleted : 0
  3/4/2018 3:14:35AM Files not scanned : 0
  3/4/2018 3:14:35AM Scan Summary (Registry Scanning)
  3/4/2018 3:14:35AM Keys scanned : 0
  3/4/2018 3:14:35AM Keys detected : 0
  3/4/2018 3:14:35AM Keys cleaned : 0
  3/4/2018 3:14:35AM Keys deleted : 0
  3/4/2018 3:14:35AM Run time : 0:00:16
  3/4/2018 3:14:35AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26437:HEAD Source
------------------------------------------------------------------------  r26437 | edk2buildsystem | 2018-02-28 02:07:10 -0800 (Wed, 28 Feb 2018) | 9 lines
  BaseTools: Improve build performance of structure PCD value generation
  Optimized the PcdValueInit.c size by abstract the common logic in the funciton.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f3b314331ce1557d51bbd6930ca9bec01ceefdd7)

------------------------------------------------------------------------  r26443 | edk2buildsystem | 2018-03-04 02:07:12 -0800 (Sun, 04 Mar 2018) | 11 lines
  BaseTools: Enhance FV info report file path to support absolute path
  When generate build report, Tool will get the info like size, Fv Name,
  etc from the xx.Fv.txt file and add these info into the build report.
  This patch support the xx.Fv.txt to use absolute file path format since
  user may provide specified FV path.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 2157bc9c8b8be30ada11fe2e64454157d3ae528f)

------------------------------------------------------------------------  r26444 | edk2buildsystem | 2018-03-04 02:07:19 -0800 (Sun, 04 Mar 2018) | 6 lines
  BaseTools: Align WIN_CERTIFICATE_UEFI_GUID definition to MdePkg one.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a16f7f47949ebddf07d228ef3827ec8747180e48)

------------------------------------------------------------------------  r26446 | edk2buildsystem | 2018-03-04 02:07:37 -0800 (Sun, 04 Mar 2018) | 8 lines
  BaseTools: Fix the bug for single module build with GenC/GenMake
  copy the same logic from _BuildPa() function.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit cd49821608f7eb867b8351c7a0cd3ed4dd2d563d)

------------------------------------------------------------------------  r26447 | edk2buildsystem | 2018-03-04 02:07:45 -0800 (Sun, 04 Mar 2018) | 12 lines
  BaseTools: GlobalData.gConfDirectory is None when run GenFds
  When run GenFds,  GlobalData.gConfDirectory is None, On Linux
  self._ToolChainFamily default Value is "MSFT", and then
  generate the wrong PcdValueInit Makefile
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 541a3f5882d60d6241a752127acf3ef367c548e4)

------------------------------------------------------------------------  r26449 | edk2buildsystem | 2018-03-04 02:07:58 -0800 (Sun, 04 Mar 2018) | 16 lines
  BaseTools: Fix eval parse string issue
  eval argument start with " or ', but it is unicode string,
  will encounter error:
  List = list(eval(Value)) # translate escape character
  File "<string>", line 1
  'j??=????????F??
  ^
  SyntaxError: EOL while scanning string literal
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4faf13222edead307109bf8c747200ea3fb617c0)

------------------------------------------------------------------------  r26450 | edk2buildsystem | 2018-03-04 02:08:05 -0800 (Sun, 04 Mar 2018) | 11 lines
  BaseTools: Fix the bug for display incorrect *M flag in report
  The root cause is the byte array value in the driver Pcd, some bytes
  have additional space character, while the value in DSC file doesn't
  have this space, it cause the string compare return false, so we remove
  the extra space.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 6ee9c68912324b4053cfa15fd06b02af1c1c74d9)

------------------------------------------------------------------------  r26451 | edk2buildsystem | 2018-03-04 02:08:13 -0800 (Sun, 04 Mar 2018) | 10 lines
  BaseTools: report error if flag in LABEL() invalid
  Flag in LABEL() is not valid C variable name, will report error.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 5ac0a5450bb87ccefa9f847d3d5bf579cb13925e)

------------------------------------------------------------------------  r26461 | edk2buildsystem | 2018-03-04 02:09:34 -0800 (Sun, 04 Mar 2018) | 10 lines
  BaseTools: Dsc/Fdf conditional statement parse issue
  Set PCD value with --pcd argument not replace DSC/Fdf PCD value.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1fa7fdf6eada55316d7b5b45a0d116625d697fc5)

------------------------------------------------------------------------  r26463 | edk2buildsystem | 2018-03-04 02:09:53 -0800 (Sun, 04 Mar 2018) | 13 lines
  BaseTools: DSC Components section support flexible PCD
  DSC Components section support flexible PCD, and for binary driver, we
  need patch this value. Update the split char ',' not ', ' because some
  value may have space, while others may not have this space.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 0537f332c968e6c3adeefa2222b5f1aa7252b711)

------------------------------------------------------------------------  r26464 | edk2buildsystem | 2018-03-04 02:10:05 -0800 (Sun, 04 Mar 2018) | 13 lines
  BaseTools: Fixed Pcd value override issue.
  1. Handle the Pcd maxsize issue for the case
  that the length of Pcd value from CommandLine
  bigger that its maxsize
  2. The Pcd value override in commandline.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b854e2bf752940b8d4dd3a569942d9c07b5d498f)

------------------------------------------------------------------------  r26465 | edk2buildsystem | 2018-03-04 02:10:14 -0800 (Sun, 04 Mar 2018) | 10 lines
  BaseTools: Fixed build failed issue.
  Case 1. A Pcd has no default sku setting in DSC.
  Case 2. Build as Single SKU.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f832bb3466008998001c1a3247febc0abfbcab55)

------------------------------------------------------------------------  r26466 | edk2buildsystem | 2018-03-04 02:10:27 -0800 (Sun, 04 Mar 2018) | 10 lines
  BaseTools: Pcd Value override issue.
  For the case that the structure PCD has no value assignment in DSC,
  but has value assignment in command line.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1667eec6990fae902981504887546f5a4913fde0)

------------------------------------------------------------------------  r26467 | edk2buildsystem | 2018-03-04 02:10:33 -0800 (Sun, 04 Mar 2018) | 9 lines
  BaseTools: Correct Structure Pcd value in the report
  The patch "Fixed build failed issue" changed structure Pcd Object, so
  we need update build report to correct structure Pcd Value.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 24326f381f84aca925a5df3eace96a7523ce1c27)

------------------------------------------------------------------------  r26468 | edk2buildsystem | 2018-03-04 02:10:46 -0800 (Sun, 04 Mar 2018) | 10 lines
  BaseTools: Fix the bug to search Fv.txt file relative to workspace
  when the SECTION FV_IMAGE = $(XX)/XX.Fv, the Fv file should relative to
  WORKSPACE, so when we search the XX.Fv.txt file, we should search the
  path relative to workspace first.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit aebe5a36b6e960896671d3134c6b26f6735b7f53)

------------------------------------------------------------------------  r26474 | edk2buildsystem | 2018-03-04 02:13:55 -0800 (Sun, 04 Mar 2018) | 10 lines
  BaseTools: Fix bug when converting iSCSI node
  If protocol string is not specified, default TCP(0) should be used.
  Today's implementation wrongly sets to 1 for this case.
  Copy the fix solution from MdePkg Hash version e6c80aea.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c1d6749b0ed3c58b7dc771e0f857995096107f44)

------------------------------------------------------------------------  r26475 | edk2buildsystem | 2018-03-04 02:14:02 -0800 (Sun, 04 Mar 2018) | 16 lines
  BaseTools: Fix byte orders when handling 8-byte array
  Per UEFI spec, FibreEx.WWN, FibreEx.Lun, SasEx.Address, SasEx.Lun
  and iSCSI.Lun are all 8-byte array with byte #0 in the left.
  It means "0102030405060708" should be converted to:
  UINT8[8] = {01, 02, 03, 04, 05, 06, 07, 08}
  or  UINT64 = {0807060504030201}
  Today's implementation wrongly uses the reversed order.
  The patch fixes this issue by using StrHexToBytes().
  Copy this solution from MdePkg Hash version d0196be.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 27db236ac2beefc8a2de4c0df07ab47374aacfc3)

------------------------------------------------------------------------