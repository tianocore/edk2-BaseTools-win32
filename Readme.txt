Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26416

This directory contains the Win32 binaries.

Build Date:       Mon, 26 Feb 2018 03:13:14 Pacific Standard Time
Last Changed Rev: 26413

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.14 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26416
 *BootSectImage Version 1.0 Build Build 26416
 *Brotli Version 0.5.2 Build 26416
  Brotli Version 0.5.2 Build 26416
  DevicePath Version 0.1 Build 26263
  Ecc.exe Version 1.0 Build Build 26237
 *EfiLdrImage Version 1.0 Build Build 26416
 *EfiRom Version 0.1 Build 26416
  GenBootSector Version 0.2 Build 26263
  GenCrc32 Version 0.2 Build 26263
 *GenDepex.exe Version 0.04 Build 26416
 *GenFds.exe 1.0 Build 26416
  GenFfs Version 0.1 Build 26263
  GenFv Version 0.1 Build 26263
  GenFw Version 0.2 Build 26263
  GenPage Version 0.2 Build 26263
 *GenPatchPcdTable.exe Version 0.10 Build 26416
  GenSec Version 0.1 Build 26263
  GenVtf Version 0.1 Build 26263
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26263
  LzmaF86Compress Version 0.2 Build 26263
 *PatchPcdValue.exe Version 0.10 Build 26416
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
  Split Version 1.0 Build Build 26263
 *TargetTool.exe Version 0.01 Build 26416
  TianoCompress Version 0.1 Build 26263
 *Trim.exe Version 0.10 Build 26416
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26263
  VolInfo Version 1.0 Build Build 26263
 *build.exe Version 0.60 Build 26416

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/26/2018 3:13:15AM Engine version = 5900.7806
  2/26/2018 3:13:15AM AntiVirus DAT version = 8815.0
  2/26/2018 3:13:15AM Number of detection signatures in EXTRA.DAT = None
  2/26/2018 3:13:15AM Names of detection signatures in EXTRA.DAT = None
  2/26/2018 3:13:15AM Scan Started On-Demand Scan
  2/26/2018 3:13:30AM Scan Summary
  2/26/2018 3:13:30AM Processes scanned : 0
  2/26/2018 3:13:30AM Processes detected : 0
  2/26/2018 3:13:30AM Processes cleaned : 0
  2/26/2018 3:13:30AM Boot sectors scanned : 2
  2/26/2018 3:13:30AM Boot sectors detected: 0
  2/26/2018 3:13:30AM Boot sectors cleaned : 0
  2/26/2018 3:13:30AM Files scanned : 70
  2/26/2018 3:13:30AM Files with detections: 0
  2/26/2018 3:13:30AM File detections : 0
  2/26/2018 3:13:30AM Files cleaned : 0
  2/26/2018 3:13:30AM Files deleted : 0
  2/26/2018 3:13:30AM Files not scanned : 0
  2/26/2018 3:13:30AM Scan Summary (Registry Scanning)
  2/26/2018 3:13:30AM Keys scanned : 0
  2/26/2018 3:13:30AM Keys detected : 0
  2/26/2018 3:13:30AM Keys cleaned : 0
  2/26/2018 3:13:30AM Keys deleted : 0
  2/26/2018 3:13:30AM Run time : 0:00:15
  2/26/2018 3:13:30AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26405:HEAD Source
------------------------------------------------------------------------  r26408 | edk2buildsystem | 2018-02-25 02:05:28 -0800 (Sun, 25 Feb 2018) | 16 lines
  BaseTools/Expression: Use 2nd passes on PCD values
  Use 2 passes when evaluating PCD values to discover
  all the LABEL() operators and compute the byte offset
  of each LABEL().  The 2nd pass then has the information
  to replace the OFFSET_OF() operator with the computed
  byte offset.  The 2 passes allows OFFSET_OF() to be used
  before a LABEL() is declared.
  fixes:https://bugzilla.tianocore.org/show_bug.cgi?id=880
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 8bd72d7c05ff820ee7826809a033fda9b007d18f)

------------------------------------------------------------------------  r26409 | edk2buildsystem | 2018-02-25 02:05:35 -0800 (Sun, 25 Feb 2018) | 11 lines
  BaseTools: Update ValueExpressionEx for flexible PCD
  1. Byte  array number should less than 0xFF.
  2. Add SplitPcdValueString for PCD split
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 3be421e98756efc6d355b45e632c5c7b19b35b9e)

------------------------------------------------------------------------  r26410 | edk2buildsystem | 2018-02-25 02:05:42 -0800 (Sun, 25 Feb 2018) | 10 lines
  BaseTools: Add *B Flag for the field that from command line
  For structure PCD, the field value may override in the command line,
  so in the report when we print the field info we add *B Flag for those
  field.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f440f7e3caba12c0649c9ce15c33c7ec7aa2a4e8)

------------------------------------------------------------------------  r26412 | edk2buildsystem | 2018-02-26 02:05:42 -0800 (Mon, 26 Feb 2018) | 6 lines
  BaseTools: Add the missing basic definition in C BaseType.h
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 3e44e9f534ddacc7f334aff31ba0a591445f2aaf)

------------------------------------------------------------------------  r26413 | edk2buildsystem | 2018-02-26 02:05:49 -0800 (Mon, 26 Feb 2018) | 6 lines
  BaseTools GenFv: Update error message to describe PE image alignment
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 3c3277f21e4b4ebbb4988893d2edcfe8f8406348)

------------------------------------------------------------------------