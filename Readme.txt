Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23633

This directory contains the Win32 binaries.

Build Date:       Fri, 23 Dec 2016 03:11:35 Pacific Standard Time
Last Changed Rev: 23633

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23459
  BootSectImage Version 1.0 Build Build 23431
  Ecc.exe Version 1.0 Build Build 22854
  EfiLdrImage Version 1.0 Build Build 23431
  EfiRom Version 0.1 Build 23431
  GenBootSector Version 0.2 Build 23431
  GenCrc32 Version 0.2 Build 23431
  GenDepex.exe Version 0.04 Build 23459
  GenFds.exe 1.0 Build 23459
  GenFfs Version 0.1 Build 23431
  GenFv Version 0.1 Build 23431
  GenFw Version 0.2 Build 23431
  GenPage Version 0.2 Build 23431
  GenPatchPcdTable.exe Version 0.10 Build 23459
  GenSec Version 0.1 Build 23431
  GenVtf Version 0.1 Build 23431
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 23431
  LzmaF86Compress Version 0.2 Build 23431
  PatchPcdValue.exe Version 0.10 Build 23459
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 23431
  TargetTool.exe Version 0.01 Build 23459
  TianoCompress Version 0.1 Build 23431
  Trim.exe Version 0.10 Build 23459
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 23633
  VolInfo Version 1.0 Build Build 23468
  build.exe Version 0.60 Build 23459

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/23/2016 3:11:37AM Engine version = 5700.7163
  12/23/2016 3:11:37AM AntiVirus DAT version = 8387.0
  12/23/2016 3:11:37AM Number of detection signatures in EXTRA.DAT = None
  12/23/2016 3:11:37AM Names of detection signatures in EXTRA.DAT = None
  12/23/2016 3:11:37AM Scan Started On-Demand Scan
  12/23/2016 3:11:47AM Scan Summary
  12/23/2016 3:11:47AM Processes scanned : 0
  12/23/2016 3:11:47AM Processes detected : 0
  12/23/2016 3:11:47AM Processes cleaned : 0
  12/23/2016 3:11:47AM Boot sectors scanned : 2
  12/23/2016 3:11:47AM Boot sectors detected: 0
  12/23/2016 3:11:47AM Boot sectors cleaned : 0
  12/23/2016 3:11:47AM Files scanned : 62
  12/23/2016 3:11:47AM Files with detections: 0
  12/23/2016 3:11:47AM File detections : 0
  12/23/2016 3:11:47AM Files cleaned : 0
  12/23/2016 3:11:47AM Files deleted : 0
  12/23/2016 3:11:47AM Files not scanned : 0
  12/23/2016 3:11:47AM Scan Summary (Registry Scanning)
  12/23/2016 3:11:47AM Keys scanned : 0
  12/23/2016 3:11:47AM Keys detected : 0
  12/23/2016 3:11:47AM Keys cleaned : 0
  12/23/2016 3:11:47AM Keys deleted : 0
  12/23/2016 3:11:47AM Run time : 0:00:10
  12/23/2016 3:11:47AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23606:HEAD Source
------------------------------------------------------------------------  r23633 | edk2buildsystem | 2016-12-23 02:05:55 -0800 (Fri, 23 Dec 2016) | 8 lines
  BaseTools/Pccts: Resolve GCC sting format mismatch build warning
  https://bugzilla.tianocore.org/show_bug.cgi?id=282
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 0a64f49fde09928b6061543b08e6da195e2abfbd)

------------------------------------------------------------------------