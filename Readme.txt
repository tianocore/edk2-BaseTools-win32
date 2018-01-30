Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26237

This directory contains the Win32 binaries.

Build Date:       Tue, 30 Jan 2018 03:12:05 Pacific Standard Time
Last Changed Rev: 26234

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26221
  BootSectImage Version 1.0 Build Build 26212
  Brotli Version 0.5.2 Build 26212
  Brotli Version 0.5.2 Build 26212
  DevicePath Version 0.1 Build 26212
 *Ecc.exe Version 1.0 Build Build 26237
  EfiLdrImage Version 1.0 Build Build 26212
  EfiRom Version 0.1 Build 26212
  GenBootSector Version 0.2 Build 26212
  GenCrc32 Version 0.2 Build 26212
  GenDepex.exe Version 0.04 Build 26221
  GenFds.exe 1.0 Build 26221
  GenFfs Version 0.1 Build 26212
  GenFv Version 0.1 Build 26212
  GenFw Version 0.2 Build 26212
  GenPage Version 0.2 Build 26212
  GenPatchPcdTable.exe Version 0.10 Build 26221
  GenSec Version 0.1 Build 26212
  GenVtf Version 0.1 Build 26212
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26212
  LzmaF86Compress Version 0.2 Build 26212
  PatchPcdValue.exe Version 0.10 Build 26221
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26163
  Split Version 1.0 Build Build 26212
  TargetTool.exe Version 0.01 Build 26221
  TianoCompress Version 0.1 Build 26212
  Trim.exe Version 0.10 Build 26221
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26163
  VfrCompile version  2.01 (UEFI 2.4) Build Build 26212
  VolInfo Version 1.0 Build Build 26212
 *build.exe Version 0.60 Build 26237

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/30/2018 3:12:07AM Engine version = 5900.7806
  1/30/2018 3:12:07AM AntiVirus DAT version = 8789.0
  1/30/2018 3:12:07AM Number of detection signatures in EXTRA.DAT = None
  1/30/2018 3:12:07AM Names of detection signatures in EXTRA.DAT = None
  1/30/2018 3:12:07AM Scan Started On-Demand Scan
  1/30/2018 3:12:20AM Scan Summary
  1/30/2018 3:12:20AM Processes scanned : 0
  1/30/2018 3:12:20AM Processes detected : 0
  1/30/2018 3:12:20AM Processes cleaned : 0
  1/30/2018 3:12:20AM Boot sectors scanned : 2
  1/30/2018 3:12:20AM Boot sectors detected: 0
  1/30/2018 3:12:20AM Boot sectors cleaned : 0
  1/30/2018 3:12:20AM Files scanned : 66
  1/30/2018 3:12:20AM Files with detections: 0
  1/30/2018 3:12:20AM File detections : 0
  1/30/2018 3:12:20AM Files cleaned : 0
  1/30/2018 3:12:20AM Files deleted : 0
  1/30/2018 3:12:20AM Files not scanned : 0
  1/30/2018 3:12:20AM Scan Summary (Registry Scanning)
  1/30/2018 3:12:20AM Keys scanned : 0
  1/30/2018 3:12:20AM Keys detected : 0
  1/30/2018 3:12:20AM Keys cleaned : 0
  1/30/2018 3:12:20AM Keys deleted : 0
  1/30/2018 3:12:20AM Run time : 0:00:14
  1/30/2018 3:12:20AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26221:HEAD Source
------------------------------------------------------------------------  r26234 | edk2buildsystem | 2018-01-30 02:05:39 -0800 (Tue, 30 Jan 2018) | 11 lines
  BaseTools: Fix indentation in CParser.py file
  Mixing usage of spaces and tabs may confuse the python
  compiler/interpreter.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Gary Lin <glin@suse.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 877251b4212dedaabefbc3ef6cd637a5b2740d47)

------------------------------------------------------------------------