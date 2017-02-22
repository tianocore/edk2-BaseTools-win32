Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23932

This directory contains the Win32 binaries.

Build Date:       Wed, 22 Feb 2017 08:27:30 Pacific Standard Time
Last Changed Rev: 23916

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23932
  BootSectImage Version 1.0 Build Build 23431
  Ecc.exe Version 1.0 Build Build 23673
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
 *GenDepex.exe Version 0.04 Build 23932
 *GenFds.exe 1.0 Build 23932
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 23431
  GenPage Version 0.2 Build 23431
 *GenPatchPcdTable.exe Version 0.10 Build 23932
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 23431
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
 *PatchPcdValue.exe Version 0.10 Build 23932
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 23431
 *TargetTool.exe Version 0.01 Build 23932
  TianoCompress Version 0.1 Build 23431
 *Trim.exe Version 0.10 Build 23932
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 23932
  VolInfo Version 1.0 Build Build 23468
 *build.exe Version 0.60 Build 23932

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/22/2017 8:27:32AM Engine version = 5700.7163
  2/22/2017 8:27:32AM AntiVirus DAT version = 8446.0
  2/22/2017 8:27:32AM Number of detection signatures in EXTRA.DAT = None
  2/22/2017 8:27:32AM Names of detection signatures in EXTRA.DAT = None
  2/22/2017 8:27:32AM Scan Started On-Demand Scan
  2/22/2017 8:27:36AM Scan Summary
  2/22/2017 8:27:36AM Processes scanned : 0
  2/22/2017 8:27:36AM Processes detected : 0
  2/22/2017 8:27:36AM Processes cleaned : 0
  2/22/2017 8:27:36AM Boot sectors scanned : 2
  2/22/2017 8:27:36AM Boot sectors detected: 0
  2/22/2017 8:27:36AM Boot sectors cleaned : 0
  2/22/2017 8:27:36AM Files scanned : 63
  2/22/2017 8:27:36AM Files with detections: 0
  2/22/2017 8:27:36AM File detections : 0
  2/22/2017 8:27:36AM Files cleaned : 0
  2/22/2017 8:27:36AM Files deleted : 0
  2/22/2017 8:27:36AM Files not scanned : 0
  2/22/2017 8:27:36AM Scan Summary (Registry Scanning)
  2/22/2017 8:27:36AM Keys scanned : 0
  2/22/2017 8:27:36AM Keys detected : 0
  2/22/2017 8:27:36AM Keys cleaned : 0
  2/22/2017 8:27:36AM Keys deleted : 0
  2/22/2017 8:27:36AM Run time : 0:00:04
  2/22/2017 8:27:36AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23880:HEAD Source
------------------------------------------------------------------------  r23915 | edk2buildsystem | 2017-02-22 02:06:36 -0800 (Wed, 22 Feb 2017) | 11 lines
  BaseTools: add error check for Macro usage in the INF file
  Use of MACRO statements in the EDK II INF files is limited to local
  usage only; global or external macros are not permitted. This patch
  add the check for not defined macros.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit dc4c770763d05297c7de6893a1e34b76499d0b09)

------------------------------------------------------------------------  r23916 | edk2buildsystem | 2017-02-22 02:06:41 -0800 (Wed, 22 Feb 2017) | 8 lines
  VfrCompile: fix invalid comparison between pointer and integer
  This would be valid C but is not valid C++, so change the comparison to do what it has always been doing.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Paolo Bonzini <pbonzini@redhat.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit d37fa01fbbe2cf0cd8b49069a71706a33cb4a53e)

------------------------------------------------------------------------