Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23211

This directory contains the Win32 binaries.

Build Date:       Wed, 09 Nov 2016 03:11:57 Pacific Standard Time
Last Changed Rev: 23207

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23090
 *BootSectImage Version 1.0 Build Build 23211
  Ecc.exe Version 1.0 Build Build 22854
 *EfiLdrImage Version 1.0 Build Build 23211
 *EfiRom Version 0.1 Build 23211
 *GenBootSector Version 0.2 Build 23211
 *GenCrc32 Version 0.2 Build 23211
  GenDepex.exe Version 0.04 Build 23090
  GenFds.exe 1.0 Build 23090
 *GenFfs Version 0.1 Build 23211
 *GenFv Version 0.1 Build 23211
 *GenFw Version 0.2 Build 23211
 *GenPage Version 0.2 Build 23211
  GenPatchPcdTable.exe Version 0.10 Build 23095
 *GenSec Version 0.1 Build 23211
 *GenVtf Version 0.1 Build 23211
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 23211
  LzmaF86Compress Version 0.2 Build 23211
  PatchPcdValue.exe Version 0.10 Build 23090
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
 *Split Version 1.0 Build Build 23211
  TargetTool.exe Version 0.01 Build 23090
 *TianoCompress Version 0.1 Build 23211
  Trim.exe Version 0.10 Build 23090
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 23211
 *VolInfo Version 1.0 Build Build 23211
  build.exe Version 0.60 Build 23095

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/9/2016 3:11:58AM Engine version = 5700.7163
  11/9/2016 3:11:58AM AntiVirus DAT version = 8343.0
  11/9/2016 3:11:58AM Number of detection signatures in EXTRA.DAT = None
  11/9/2016 3:11:58AM Names of detection signatures in EXTRA.DAT = None
  11/9/2016 3:11:59AM Scan Started On-Demand Scan
  11/9/2016 3:12:02AM Scan Summary
  11/9/2016 3:12:02AM Processes scanned : 0
  11/9/2016 3:12:02AM Processes detected : 0
  11/9/2016 3:12:02AM Processes cleaned : 0
  11/9/2016 3:12:02AM Boot sectors scanned : 1
  11/9/2016 3:12:02AM Boot sectors detected: 0
  11/9/2016 3:12:02AM Boot sectors cleaned : 0
  11/9/2016 3:12:02AM Files scanned : 77
  11/9/2016 3:12:02AM Files with detections: 0
  11/9/2016 3:12:02AM File detections : 0
  11/9/2016 3:12:02AM Files cleaned : 0
  11/9/2016 3:12:02AM Files deleted : 0
  11/9/2016 3:12:02AM Files not scanned : 0
  11/9/2016 3:12:02AM Scan Summary (Registry Scanning)
  11/9/2016 3:12:02AM Keys scanned : 0
  11/9/2016 3:12:02AM Keys detected : 0
  11/9/2016 3:12:02AM Keys cleaned : 0
  11/9/2016 3:12:02AM Keys deleted : 0
  11/9/2016 3:12:02AM Run time : 0:00:04
  11/9/2016 3:12:02AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23152:HEAD Source
------------------------------------------------------------------------  r23152 | edk2buildsystem | 2016-11-08 02:11:27 -0800 (Tue, 08 Nov 2016) | 16 lines
  BaseTools/VfrCompile/Pccts: Make assignment operator not returning void
  The assignment operators for class ANTLRTokenPtr return void in current
  code.
  This commit makes them return the reference to the object just like
  primitive types do.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Dandan Bi <dandan.bi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit fef15ecd20dd8db5bf0c33b00908fc59491dba8a)

------------------------------------------------------------------------  r23207 | edk2buildsystem | 2016-11-09 02:06:20 -0800 (Wed, 09 Nov 2016) | 11 lines
  BaseTools/PeCoffLib: Check 'RelocDir' before finding relocation block
  To match the code logics in MdePkg/Library/BasePeCoffLib, add checks for
  'RelocDir' before finding the relocation block.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 49d8f534cc4280fa3f393dec5093b23b0c759c2c)

------------------------------------------------------------------------