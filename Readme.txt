Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25091

This directory contains the Win32 binaries.

Build Date:       Sun, 13 Aug 2017 03:12:19 Pacific Daylight Time
Last Changed Rev: 25091

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25091
  BootSectImage Version 1.0 Build Build 25090
  Brotli Version 0.5.2 Build 25090
  Brotli Version 0.5.2 Build 25090
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25090
  EfiRom Version 0.1 Build 25090
  GenBootSector Version 0.2 Build 25090
  GenCrc32 Version 0.2 Build 25090
 *GenDepex.exe Version 0.04 Build 25091
 *GenFds.exe 1.0 Build 25091
  GenFfs Version 0.1 Build 25090
  GenFv Version 0.1 Build 25090
  GenFw Version 0.2 Build 25090
  GenPage Version 0.2 Build 25090
 *GenPatchPcdTable.exe Version 0.10 Build 25091
  GenSec Version 0.1 Build 25090
  GenVtf Version 0.1 Build 25090
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25090
  LzmaF86Compress Version 0.2 Build 25090
 *PatchPcdValue.exe Version 0.10 Build 25091
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25090
 *TargetTool.exe Version 0.01 Build 25091
  TianoCompress Version 0.1 Build 25090
 *Trim.exe Version 0.10 Build 25091
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25090
  VolInfo Version 1.0 Build Build 25090
 *build.exe Version 0.60 Build 25091

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/13/2017 3:12:21AM Engine version = 5800.7501
  8/13/2017 3:12:21AM AntiVirus DAT version = 8620.0
  8/13/2017 3:12:21AM Number of detection signatures in EXTRA.DAT = None
  8/13/2017 3:12:21AM Names of detection signatures in EXTRA.DAT = None
  8/13/2017 3:12:21AM Scan Started On-Demand Scan
  8/13/2017 3:13:08AM Scan Summary
  8/13/2017 3:13:08AM Processes scanned : 0
  8/13/2017 3:13:08AM Processes detected : 0
  8/13/2017 3:13:08AM Processes cleaned : 0
  8/13/2017 3:13:08AM Boot sectors scanned : 2
  8/13/2017 3:13:08AM Boot sectors detected: 0
  8/13/2017 3:13:08AM Boot sectors cleaned : 0
  8/13/2017 3:13:08AM Files scanned : 64
  8/13/2017 3:13:08AM Files with detections: 0
  8/13/2017 3:13:08AM File detections : 0
  8/13/2017 3:13:08AM Files cleaned : 0
  8/13/2017 3:13:08AM Files deleted : 0
  8/13/2017 3:13:08AM Files not scanned : 0
  8/13/2017 3:13:08AM Scan Summary (Registry Scanning)
  8/13/2017 3:13:08AM Keys scanned : 0
  8/13/2017 3:13:08AM Keys detected : 0
  8/13/2017 3:13:08AM Keys cleaned : 0
  8/13/2017 3:13:08AM Keys deleted : 0
  8/13/2017 3:13:08AM Run time : 0:00:48
  8/13/2017 3:13:08AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25090:HEAD Source
------------------------------------------------------------------------  r25090 | edk2buildsystem | 2017-08-12 02:05:36 -0700 (Sat, 12 Aug 2017) | 11 lines
  BaseTools: Don't need to add extra quotes when UI string from file
  when the UI string is read from files, we don't need to add the extra
  quotes. Otherwise, it will cause UI name has this extra quotes.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Bin Wang <binx.a.wang@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1e892df6860dc655f8e570450d74791b84de9928)

------------------------------------------------------------------------  r25091 | edk2buildsystem | 2017-08-13 02:05:23 -0700 (Sun, 13 Aug 2017) | 14 lines
  BaseTools: Support TabSpace between section tag in DEC file
  Per DEC spec, multiple section tag use <TS> to separate, and it can
  support Tab, so this patch fix the bug to use Tab.
  <TabSpace> ::= {<Tab>} {<Space>}
  <TS> ::= <TabSpace>*
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yanyan Zhang <yanyanx.zhang@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0795920568ca2efbea71be8510f6bda1e8ef3e8a)

------------------------------------------------------------------------