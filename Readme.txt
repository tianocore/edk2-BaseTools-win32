Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20331

This directory contains the Win32 binaries.

Build Date:       Wed, 23 Mar 2016 03:32:44 Pacific Daylight Time
Last Changed Rev: 20317

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20331
  BootSectImage Version 1.0 Build Build 20182
 *Ecc.exe Version 1.0 Build Build 20331
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20331
 *GenFds.exe 1.0 Build 20331
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20331
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20331
 *Rsa2048Sha256GenerateKeys Version 0.9 Build 20331
 *Rsa2048Sha256Sign Version 0.9 Build 20331
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20331
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20331
 *UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20331
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20182
 *build.exe Version 0.60 Build 20331

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/23/2016 3:32:45AM Engine version = 5700.7163
  3/23/2016 3:32:45AM AntiVirus DAT version = 8112.0
  3/23/2016 3:32:45AM Number of detection signatures in EXTRA.DAT = None
  3/23/2016 3:32:45AM Names of detection signatures in EXTRA.DAT = None
  3/23/2016 3:32:45AM Scan Started On-Demand Scan
  3/23/2016 3:32:53AM Scan Summary
  3/23/2016 3:32:53AM Processes scanned : 0
  3/23/2016 3:32:53AM Processes detected : 0
  3/23/2016 3:32:53AM Processes cleaned : 0
  3/23/2016 3:32:53AM Boot sectors scanned : 2
  3/23/2016 3:32:53AM Boot sectors detected: 0
  3/23/2016 3:32:53AM Boot sectors cleaned : 0
  3/23/2016 3:32:53AM Files scanned : 55
  3/23/2016 3:32:53AM Files with detections: 0
  3/23/2016 3:32:53AM File detections : 0
  3/23/2016 3:32:53AM Files cleaned : 0
  3/23/2016 3:32:53AM Files deleted : 0
  3/23/2016 3:32:53AM Files not scanned : 0
  3/23/2016 3:32:53AM Scan Summary (Registry Scanning)
  3/23/2016 3:32:53AM Keys scanned : 0
  3/23/2016 3:32:53AM Keys detected : 0
  3/23/2016 3:32:53AM Keys cleaned : 0
  3/23/2016 3:32:53AM Keys deleted : 0
  3/23/2016 3:32:53AM Run time : 0:00:08
  3/23/2016 3:32:53AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20317:HEAD Source
------------------------------------------------------------------------  r20317 | edk2buildsystem | 2016-03-22 02:27:49 -0700 (Tue, 22 Mar 2016) | 22 lines
  BaseTools: Fix nmake failure due to command-line length limitation
  NMAKE is limited to command-line length of 4096 characters. Due to the
  large number of /I directives specified on command line (one per include
  directory), the path length of WORKSPACE is multiplied by the number of
  /I directives and can exceed the limit.
  This patch:
  1. Add new build option -l, --cmd-len to set the maximum command line
  length, default value is 4096.
  2. Generate the response file only if the command line length exceed its
  maximum characters (default is 4096) when build the module. Cover
  PP_FLAGS, CC_FLAGS, VFRPP_FLAGS, APP_FLAGS, ASLPP_FLAGS, ASLCC_FLAGS and
  ASM_FLAGS.
  3. The content of the response file is combine from the FLAGS option and
  INC option.
  4. When build failure, it would print out the response file's file
  location and its content.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 725cdb8fbfb034cd73574ed9c356b0dca14ff843)

------------------------------------------------------------------------