Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20298

This directory contains the Win32 binaries.

Build Date:       Wed, 16 Mar 2016 03:32:19 Pacific Daylight Time
Last Changed Rev: 20291

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20298
  BootSectImage Version 1.0 Build Build 20182
 *Ecc.exe Version 1.0 Build Build 20298
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20298
 *GenFds.exe 1.0 Build 20298
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20298
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20298
 *Rsa2048Sha256GenerateKeys Version 0.9 Build 20298
 *Rsa2048Sha256Sign Version 0.9 Build 20298
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20298
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20298
 *UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20298
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20182
 *build.exe Version 0.60 Build 20298

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/16/2016 3:32:21AM Engine version = 5700.7163
  3/16/2016 3:32:21AM AntiVirus DAT version = 8102.0
  3/16/2016 3:32:21AM Number of detection signatures in EXTRA.DAT = None
  3/16/2016 3:32:21AM Names of detection signatures in EXTRA.DAT = None
  3/16/2016 3:32:21AM Scan Started On-Demand Scan
  3/16/2016 3:32:44AM Scan Summary
  3/16/2016 3:32:44AM Processes scanned : 0
  3/16/2016 3:32:44AM Processes detected : 0
  3/16/2016 3:32:44AM Processes cleaned : 0
  3/16/2016 3:32:44AM Boot sectors scanned : 2
  3/16/2016 3:32:44AM Boot sectors detected: 0
  3/16/2016 3:32:44AM Boot sectors cleaned : 0
  3/16/2016 3:32:44AM Files scanned : 55
  3/16/2016 3:32:44AM Files with detections: 0
  3/16/2016 3:32:44AM File detections : 0
  3/16/2016 3:32:44AM Files cleaned : 0
  3/16/2016 3:32:44AM Files deleted : 0
  3/16/2016 3:32:44AM Files not scanned : 0
  3/16/2016 3:32:44AM Scan Summary (Registry Scanning)
  3/16/2016 3:32:44AM Keys scanned : 0
  3/16/2016 3:32:44AM Keys detected : 0
  3/16/2016 3:32:44AM Keys cleaned : 0
  3/16/2016 3:32:44AM Keys deleted : 0
  3/16/2016 3:32:44AM Run time : 0:00:23
  3/16/2016 3:32:44AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20288:HEAD Source
------------------------------------------------------------------------  r20291 | edk2buildsystem | 2016-03-16 02:26:28 -0700 (Wed, 16 Mar 2016) | 21 lines
  BaseTools: add new command line option to support override PCD value
  this patch add new feature to support override PCD value on the command
  line. The value from the command line is the highest priority.
  1.Add option(--pcd) to support both PcdName and TokenSpaceGuild.PcdName
  2.For void* type PCD, use following format:
  cstring PCD: --pcd PcdName="string"
  unicodestring PCD: --pcd PcdName=L"string"
  CArray PCD: --pcd PcdName=B"{0x1, 0x2}"
  3.Build Report, use *B to show the PCD value was overridden in the
  command line.
  4.Error Condition:
  Report error if the PCD is not found
  Report error if the PcdName is found under multiple different TokenSpaceGuid
  Report error if PCD value syntax is incorrect
  Report error if void* type PCD value exceed its max size
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 763e8edf610b2ccf422986c81ee36b4733560cdb)

------------------------------------------------------------------------