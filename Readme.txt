Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20979

This directory contains the Win32 binaries.

Build Date:       Wed, 25 May 2016 03:11:02 Pacific Daylight Time
Last Changed Rev: 20976

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20909
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
  GenDepex.exe Version 0.04 Build 20909
 *GenFds.exe 1.0 Build 20979
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 20909
  GenFw Version 0.2 Build 20909
  GenPage Version 0.2 Build 20909
  GenPatchPcdTable.exe Version 0.10 Build 20909
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
  PatchPcdValue.exe Version 0.10 Build 20909
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
  TargetTool.exe Version 0.01 Build 20909
  TianoCompress Version 0.1 Build 20909
  Trim.exe Version 0.10 Build 20909
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20909
  VolInfo Version 1.0 Build Build 20909
  build.exe Version 0.60 Build 20964

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/25/2016 3:11:04AM Engine version = 5700.7163
  5/25/2016 3:11:04AM AntiVirus DAT version = 8175.0
  5/25/2016 3:11:04AM Number of detection signatures in EXTRA.DAT = 1
  5/25/2016 3:11:04AM Names of detection signatures in EXTRA.DAT = W97M/Downloader.bdj (ED)
  5/25/2016 3:11:04AM Scan Started On-Demand Scan
  5/25/2016 3:11:10AM Scan Summary
  5/25/2016 3:11:10AM Processes scanned : 0
  5/25/2016 3:11:10AM Processes detected : 0
  5/25/2016 3:11:10AM Processes cleaned : 0
  5/25/2016 3:11:10AM Boot sectors scanned : 2
  5/25/2016 3:11:10AM Boot sectors detected: 0
  5/25/2016 3:11:10AM Boot sectors cleaned : 0
  5/25/2016 3:11:10AM Files scanned : 55
  5/25/2016 3:11:10AM Files with detections: 0
  5/25/2016 3:11:10AM File detections : 0
  5/25/2016 3:11:10AM Files cleaned : 0
  5/25/2016 3:11:10AM Files deleted : 0
  5/25/2016 3:11:10AM Files not scanned : 0
  5/25/2016 3:11:10AM Scan Summary (Registry Scanning)
  5/25/2016 3:11:10AM Keys scanned : 0
  5/25/2016 3:11:10AM Keys detected : 0
  5/25/2016 3:11:10AM Keys cleaned : 0
  5/25/2016 3:11:10AM Keys deleted : 0
  5/25/2016 3:11:10AM Run time : 0:00:07
  5/25/2016 3:11:10AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20964:HEAD Source
------------------------------------------------------------------------  r20976 | edk2buildsystem | 2016-05-25 02:06:22 -0700 (Wed, 25 May 2016) | 16 lines
  BaseTools/GenFds: enhance to get TOOL_CHAIN_TAG and TARGET value
  when user don't set TOOL_CHAIN_TAG and TARGET by –D Flag, then GenFds
  would report failure for format:
  FILE DATA = $(OUTPUT_DIRECTORY)/$(TARGET)_$(TOOL_CHAIN_TAG)/testfile
  so this patch enhance to get the TOOL_CHAIN_TAG and TARGET value by
  following priority (high to low): 1. the Macro value set by -D Flag;
  2. Get the value by the -t/-b option. 3. get the value from target.txt
  file. Besides, this patch also remove the error checking for missing
  -t/-b option.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e4979beee9e5d334d97fd8e2c79670ad08587bc6)

------------------------------------------------------------------------