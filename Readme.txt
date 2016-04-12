Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20553

This directory contains the Win32 binaries.

Build Date:       Tue, 12 Apr 2016 03:10:35 Pacific Daylight Time
Last Changed Rev: 20552

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20528
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
  GenDepex.exe Version 0.04 Build 20528
  GenFds.exe 1.0 Build 20528
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
  GenPatchPcdTable.exe Version 0.10 Build 20528
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
  PatchPcdValue.exe Version 0.10 Build 20528
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20182
  TargetTool.exe Version 0.01 Build 20528
  TianoCompress Version 0.1 Build 19914
  Trim.exe Version 0.10 Build 20528
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20528
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
 *VolInfo Version 1.0 Build Build 20553
 *build.exe Version 0.60 Build 20553

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/12/2016 3:10:36AM Engine version = 5700.7163
  4/12/2016 3:10:36AM AntiVirus DAT version = 8132.0
  4/12/2016 3:10:36AM Number of detection signatures in EXTRA.DAT = None
  4/12/2016 3:10:36AM Names of detection signatures in EXTRA.DAT = None
  4/12/2016 3:10:36AM Scan Started On-Demand Scan
  4/12/2016 3:10:39AM Scan Summary
  4/12/2016 3:10:39AM Processes scanned : 0
  4/12/2016 3:10:39AM Processes detected : 0
  4/12/2016 3:10:39AM Processes cleaned : 0
  4/12/2016 3:10:39AM Boot sectors scanned : 1
  4/12/2016 3:10:39AM Boot sectors detected: 0
  4/12/2016 3:10:39AM Boot sectors cleaned : 0
  4/12/2016 3:10:39AM Files scanned : 56
  4/12/2016 3:10:39AM Files with detections: 0
  4/12/2016 3:10:39AM File detections : 0
  4/12/2016 3:10:39AM Files cleaned : 0
  4/12/2016 3:10:39AM Files deleted : 0
  4/12/2016 3:10:39AM Files not scanned : 0
  4/12/2016 3:10:39AM Scan Summary (Registry Scanning)
  4/12/2016 3:10:39AM Keys scanned : 0
  4/12/2016 3:10:39AM Keys detected : 0
  4/12/2016 3:10:39AM Keys cleaned : 0
  4/12/2016 3:10:39AM Keys deleted : 0
  4/12/2016 3:10:39AM Run time : 0:00:03
  4/12/2016 3:10:39AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20528:HEAD Source
------------------------------------------------------------------------  r20551 | edk2buildsystem | 2016-04-12 02:27:27 -0700 (Tue, 12 Apr 2016) | 10 lines
  BaseTools/VolInfo: generate HASH value for each PE image
  VolInfo Tool add new option --hash to use openssl to generate hash value
  for each PE image. If the image base address is not zero, we will rebase
  its base address to zero before generate hash value.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9947f5769f457c6efd4e917da0bddd702a82de69)

------------------------------------------------------------------------  r20552 | edk2buildsystem | 2016-04-12 02:27:32 -0700 (Tue, 12 Apr 2016) | 9 lines
  BaseTools: generate hash value in build report for each output EFI image
  Build report add new report type 'HASH' to include the hash value for
  each output EFI image.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit eca5be7a7d813c78fbeed14736776a774a72cd45)

------------------------------------------------------------------------