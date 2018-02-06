Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26279

This directory contains the Win32 binaries.

Build Date:       Tue, 06 Feb 2018 03:12:28 Pacific Standard Time
Last Changed Rev: 26275

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26279
  BootSectImage Version 1.0 Build Build 26263
  Brotli Version 0.5.2 Build 26263
  Brotli Version 0.5.2 Build 26263
  DevicePath Version 0.1 Build 26263
  Ecc.exe Version 1.0 Build Build 26237
  EfiLdrImage Version 1.0 Build Build 26263
  EfiRom Version 0.1 Build 26263
  GenBootSector Version 0.2 Build 26263
  GenCrc32 Version 0.2 Build 26263
 *GenDepex.exe Version 0.04 Build 26279
 *GenFds.exe 1.0 Build 26279
  GenFfs Version 0.1 Build 26263
  GenFv Version 0.1 Build 26263
  GenFw Version 0.2 Build 26263
  GenPage Version 0.2 Build 26263
 *GenPatchPcdTable.exe Version 0.10 Build 26279
  GenSec Version 0.1 Build 26263
  GenVtf Version 0.1 Build 26263
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26263
  LzmaF86Compress Version 0.2 Build 26263
 *PatchPcdValue.exe Version 0.10 Build 26279
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
  Split Version 1.0 Build Build 26263
 *TargetTool.exe Version 0.01 Build 26279
  TianoCompress Version 0.1 Build 26263
 *Trim.exe Version 0.10 Build 26279
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26263
  VolInfo Version 1.0 Build Build 26263
 *build.exe Version 0.60 Build 26279

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/6/2018 3:12:30AM Engine version = 5900.7806
  2/6/2018 3:12:30AM AntiVirus DAT version = 8796.0
  2/6/2018 3:12:30AM Number of detection signatures in EXTRA.DAT = None
  2/6/2018 3:12:30AM Names of detection signatures in EXTRA.DAT = None
  2/6/2018 3:12:30AM Scan Started On-Demand Scan
  2/6/2018 3:12:41AM Scan Summary
  2/6/2018 3:12:41AM Processes scanned : 0
  2/6/2018 3:12:41AM Processes detected : 0
  2/6/2018 3:12:41AM Processes cleaned : 0
  2/6/2018 3:12:41AM Boot sectors scanned : 2
  2/6/2018 3:12:41AM Boot sectors detected: 0
  2/6/2018 3:12:41AM Boot sectors cleaned : 0
  2/6/2018 3:12:41AM Files scanned : 66
  2/6/2018 3:12:41AM Files with detections: 0
  2/6/2018 3:12:41AM File detections : 0
  2/6/2018 3:12:41AM Files cleaned : 0
  2/6/2018 3:12:41AM Files deleted : 0
  2/6/2018 3:12:41AM Files not scanned : 0
  2/6/2018 3:12:41AM Scan Summary (Registry Scanning)
  2/6/2018 3:12:41AM Keys scanned : 0
  2/6/2018 3:12:41AM Keys detected : 0
  2/6/2018 3:12:41AM Keys cleaned : 0
  2/6/2018 3:12:41AM Keys deleted : 0
  2/6/2018 3:12:41AM Run time : 0:00:11
  2/6/2018 3:12:41AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26266:HEAD Source
------------------------------------------------------------------------  r26266 | edk2buildsystem | 2018-02-04 02:06:16 -0800 (Sun, 04 Feb 2018) | 19 lines
  BaseTools: Update Expression.py for VOID* to support L'a' and 'a'
  Original VOID* type support L"string" and "string" format, now we also
  add support for single quote string that without null terminator.
  Type VOID* support L'a' and 'a', the value transfer to c style value.
  L'a' --> {0x61, 0x00}
  L'ab' --> {0x61, 0x00, 0x62, 0x00}
  'a'  --> {0x61}
  'ab' --> {0x61, 0x62}
  when the value is L'' or '' that not include any character, tool will
  report error.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0e6b86731e5792a2fe89b595268a817f0cd989cc)

------------------------------------------------------------------------  r26273 | edk2buildsystem | 2018-02-06 02:05:49 -0800 (Tue, 06 Feb 2018) | 8 lines
  BaseTools GNUmakefile: Move HOST_ARCH detection into common makefile
  With this change, enter single tool directory, make can pass.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1eac82c878f5f65e2cd4eb6a6553dbddeb739c12)

------------------------------------------------------------------------  r26274 | edk2buildsystem | 2018-02-06 02:06:01 -0800 (Tue, 06 Feb 2018) | 7 lines
  BaseTools GNUmakefile: Remove HOST_ARCH in every tool Makefile
  HOST_ARCH has been moved into the common header.makefile
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d16e777ac564557f805db05a0110874797b65ceb)

------------------------------------------------------------------------  r26275 | edk2buildsystem | 2018-02-06 02:06:09 -0800 (Tue, 06 Feb 2018) | 9 lines
  BaseTools: enhance error check for DatumType format
  Add a check for DatumType format, eg: VOID *, original Tool will crash
  but no detail error message which cause confusion to user.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e0db09cd1cd35a1e2ae627e305d903652555aef2)

------------------------------------------------------------------------