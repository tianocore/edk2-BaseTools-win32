Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 24061

This directory contains the Win32 binaries.

Build Date:       Tue, 07 Mar 2017 03:11:07 Pacific Standard Time
Last Changed Rev: 24051

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23940
  BootSectImage Version 1.0 Build Build 23431
  Ecc.exe Version 1.0 Build Build 23673
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
  GenDepex.exe Version 0.04 Build 23940
  GenFds.exe 1.0 Build 23940
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
 *GenFw Version 0.2 Build 24061
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 23940
  GenSec Version 0.1 Build 23431
 *GenVtf Version 0.1 Build 24061
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 23940
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 23431
  TargetTool.exe Version 0.01 Build 23940
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 23940
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
 *VolInfo Version 1.0 Build Build 24061
  build.exe Version 0.60 Build 23940

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/7/2017 3:11:09AM Engine version = 5700.7163
  3/7/2017 3:11:09AM AntiVirus DAT version = 8459.0
  3/7/2017 3:11:09AM Number of detection signatures in EXTRA.DAT = None
  3/7/2017 3:11:09AM Names of detection signatures in EXTRA.DAT = None
  3/7/2017 3:11:09AM Scan Started On-Demand Scan
  3/7/2017 3:11:15AM Scan Summary
  3/7/2017 3:11:15AM Processes scanned : 0
  3/7/2017 3:11:15AM Processes detected : 0
  3/7/2017 3:11:15AM Processes cleaned : 0
  3/7/2017 3:11:15AM Boot sectors scanned : 2
  3/7/2017 3:11:15AM Boot sectors detected: 0
  3/7/2017 3:11:15AM Boot sectors cleaned : 0
  3/7/2017 3:11:15AM Files scanned : 64
  3/7/2017 3:11:15AM Files with detections: 0
  3/7/2017 3:11:15AM File detections : 0
  3/7/2017 3:11:15AM Files cleaned : 0
  3/7/2017 3:11:15AM Files deleted : 0
  3/7/2017 3:11:15AM Files not scanned : 0
  3/7/2017 3:11:15AM Scan Summary (Registry Scanning)
  3/7/2017 3:11:15AM Keys scanned : 0
  3/7/2017 3:11:15AM Keys detected : 0
  3/7/2017 3:11:15AM Keys cleaned : 0
  3/7/2017 3:11:15AM Keys deleted : 0
  3/7/2017 3:11:15AM Run time : 0:00:07
  3/7/2017 3:11:15AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 24003:HEAD Source
------------------------------------------------------------------------  r24018 | edk2buildsystem | 2017-03-02 02:05:28 -0800 (Thu, 02 Mar 2017) | 12 lines
  BaseTools/Source/C/Makefiles: Fix NmakeSubdirs.bat always return 0
  In batch script file NmakeSubdirs.bat, the value changes made to the
  variable 'TOOL_ERROR' within the 'setlocal...endlocal' block will not be
  reflected in the return value of the script. A value of 0 will always be
  returned. Thus, the script will not reflect the result of the 'nmake'
  command correctly when building BaseTool source codes.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a11928f3310518ab1c6fd34e8d0fdbb72de9602c)

------------------------------------------------------------------------  r24049 | edk2buildsystem | 2017-03-07 02:05:41 -0800 (Tue, 07 Mar 2017) | 17 lines
  BaseTools/GenFw: Fix VS2010/VS2012 build failure
  https://bugzilla.tianocore.org/show_bug.cgi?id=417
  The commit makes the following refinements in GenFw source codes to
  avoid VS2010/VS2012 build failure:
  1. Replaces the uses of 'bool' with 'BOOLEAN' for accordance, and remove
  the header file dependency for '<stdbool.h>'.
  2. Refines coding style for function 'GetSymName' to declare local
  variables at the beginning of the function block.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7be7b25d11a64d186060161ebc63f0ba63500a1d)

------------------------------------------------------------------------  r24050 | edk2buildsystem | 2017-03-07 02:05:47 -0800 (Tue, 07 Mar 2017) | 14 lines
  BaseTools/GenVtf: Fix VS2010/VS2012 build failure
  https://bugzilla.tianocore.org/show_bug.cgi?id=417
  The commit makes the following refinements in GenVtf source codes to
  avoid VS2010/VS2012 build failure:
  1. Refines coding style to declare local variables at the beginning of a
  code block in function 'main'.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 52757f69e9a67c27c6a5f8188c3f281dc6ac35e8)

------------------------------------------------------------------------  r24051 | edk2buildsystem | 2017-03-07 02:05:51 -0800 (Tue, 07 Mar 2017) | 14 lines
  BaseTools/VolInfo: Fix VS2010/VS2012 build failure
  https://bugzilla.tianocore.org/show_bug.cgi?id=417
  The commit makes the following refinements in VolInfo source codes to
  avoid VS2010/VS2012 build failure:
  1. Refines coding style for function 'CombinePath' to declare local
  variables at the beginning of the function block.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 8994d2f95cc77a09a37e87ad6e4e4858615c3b9e)

------------------------------------------------------------------------