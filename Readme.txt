Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20182

This directory contains the Win32 binaries.

Build Date:       Thu, 10 Mar 2016 03:32:24 Pacific Standard Time
Last Changed Rev: 20180

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20182
 *BootSectImage Version 1.0 Build Build 20182
 *Ecc.exe Version 1.0 Build Build 20182
 *EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20182
 *GenFds.exe 1.0 Build 20182
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 19914
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20182
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20182
  Rsa2048Sha256GenerateKeys Version 0.9 Build 19914
  Rsa2048Sha256Sign Version 0.9 Build 19914
 *Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20182
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20182
 *UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20182
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
 *VolInfo Version 1.0 Build Build 20182
 *build.exe Version 0.60 Build 20182

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  3/10/2016 3:32:26AM Engine version = 5700.7163
  3/10/2016 3:32:26AM AntiVirus DAT version = 8098.0
  3/10/2016 3:32:26AM Number of detection signatures in EXTRA.DAT = None
  3/10/2016 3:32:26AM Names of detection signatures in EXTRA.DAT = None
  3/10/2016 3:32:26AM Scan Started On-Demand Scan
  3/10/2016 3:32:27AM Scan Summary
  3/10/2016 3:32:27AM Processes scanned : 0
  3/10/2016 3:32:27AM Processes detected : 0
  3/10/2016 3:32:27AM Processes cleaned : 0
  3/10/2016 3:32:27AM Boot sectors scanned : 1
  3/10/2016 3:32:27AM Boot sectors detected: 0
  3/10/2016 3:32:27AM Boot sectors cleaned : 0
  3/10/2016 3:32:27AM Files scanned : 60
  3/10/2016 3:32:27AM Files with detections: 0
  3/10/2016 3:32:27AM File detections : 0
  3/10/2016 3:32:27AM Files cleaned : 0
  3/10/2016 3:32:27AM Files deleted : 0
  3/10/2016 3:32:27AM Files not scanned : 0
  3/10/2016 3:32:27AM Scan Summary (Registry Scanning)
  3/10/2016 3:32:27AM Keys scanned : 0
  3/10/2016 3:32:27AM Keys detected : 0
  3/10/2016 3:32:27AM Keys cleaned : 0
  3/10/2016 3:32:27AM Keys deleted : 0
  3/10/2016 3:32:27AM Run time : 0:00:02
  3/10/2016 3:32:27AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20172:HEAD Source
------------------------------------------------------------------------  r20179 | edk2buildsystem | 2016-03-10 02:26:32 -0800 (Thu, 10 Mar 2016) | 6 lines
  BaseTools: Change source files to DOS format.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 452582852dc3654ce51e0c6072aaf752d1b0e3ed)

------------------------------------------------------------------------  r20180 | edk2buildsystem | 2016-03-10 02:26:38 -0800 (Thu, 10 Mar 2016) | 10 lines
  BaseTools: report warning if VOID* PCD with {} value is not 8-byte aligned
  For VOID* Pcd with {} value, If platform developer wants to put in a
  specific hex offset value that is not 8-byte aligned for VOID * then we
  allow it with a warning message.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 815ada26cb7069d1121153c4e661e796c9e1da25)

------------------------------------------------------------------------