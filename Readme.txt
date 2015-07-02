Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17815

This directory contains the Win32 binaries.

Build Date:       Thu, 02 Jul 2015 03:17:04 Pacific Daylight Time
Last Changed Rev: 17801

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17815
 *BootSectImage Version 0.1 Build 17815
  Ecc.exe Version 0.01 Build 17712
 *EfiLdrImage Version 0.1 Build 17815
 *EfiRom Version 0.1 Build 17815
 *GenBootSector Version 0.2 Build 17815
 *GenCrc32 Version 0.2 Build 17815
 *GenDepex.exe Version 0.04 Build 17815
 *GenFds.exe 1.0 Build 17815
 *GenFfs Version 0.1 Build 17815
 *GenFv Version 0.1 Build 17815
 *GenFw Version 0.2 Build 17815
 *GenPage Version 0.2 Build 17815
 *GenPatchPcdTable.exe Version 0.10 Build 17815
 *GenSec Version 0.1 Build 17815
 *GenVtf Version 0.1 Build 17815
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 17815
  LzmaF86Compress Version 0.2 Build 17815
 *PatchPcdValue.exe Version 0.10 Build 17815
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17553
 *Split Version 0.1 Build 17815
 *TargetTool.exe Version 0.01 Build 17815
 *TianoCompress Version 0.1 Build 17815
 *Trim.exe Version 0.10 Build 17815
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17674
 *VfrCompile version  2.00 (UEFI 2.4) Build 17815
 *VolInfo Version 0.83 Build 17815, Jul  2 2015
 *build.exe Version 0.60 Build 17815

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1263
  7/2/2015 3:17:05AM Engine version = 5700.7163
  7/2/2015 3:17:05AM AntiVirus DAT version = 7849.0
  7/2/2015 3:17:05AM Number of detection signatures in EXTRA.DAT = None
  7/2/2015 3:17:05AM Names of detection signatures in EXTRA.DAT = None
  7/2/2015 3:17:06AM Scan Started On-Demand Scan
  7/2/2015 3:17:23AM Scan Summary
  7/2/2015 3:17:23AM Processes scanned : 0
  7/2/2015 3:17:23AM Processes detected : 0
  7/2/2015 3:17:23AM Processes cleaned : 0
  7/2/2015 3:17:23AM Boot sectors scanned : 1
  7/2/2015 3:17:23AM Boot sectors detected: 0
  7/2/2015 3:17:23AM Boot sectors cleaned : 0
  7/2/2015 3:17:23AM Files scanned : 71
  7/2/2015 3:17:23AM Files with detections: 0
  7/2/2015 3:17:23AM File detections : 0
  7/2/2015 3:17:23AM Files cleaned : 0
  7/2/2015 3:17:23AM Files deleted : 0
  7/2/2015 3:17:23AM Files not scanned : 0
  7/2/2015 3:17:23AM Scan Summary (Registry Scanning)
  7/2/2015 3:17:23AM Keys scanned : 0
  7/2/2015 3:17:23AM Keys detected : 0
  7/2/2015 3:17:23AM Keys cleaned : 0
  7/2/2015 3:17:23AM Keys deleted : 0
  7/2/2015 3:17:23AM Run time : 0:00:18
  7/2/2015 3:17:23AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17791:HEAD Source
------------------------------------------------------------------------  r17792 | lgao4 | 2015-07-01 08:21:03 -0700 (Wed, 01 Jul 2015) | 7 lines
  BaseTools: Add missing EfiPersistentMemory to EFI_MEMORY_TYPE
  To sync with the EFI_MEMROYT_TYPE definition in MdePkg
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Samer El-Haj-Mahmoud <samer.el-haj-mahmoud@hp.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r17796 | yingke | 2015-07-01 20:42:34 -0700 (Wed, 01 Jul 2015) | 7 lines
  BaseTools: Fixed BuildOptions bug.
  The BuildOptions in an INF should also follow override rule: If '==' is used, all previous options are overridden.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r17800 | hchen30 | 2015-07-01 23:02:42 -0700 (Wed, 01 Jul 2015) | 7 lines
  BaseTools/Ecc: Fix a bug to get correct member variable
  Fix a bug to get correct member variable by ignoring 'OPTIONAL' modifier
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: YangX Li <yangx.li@intel.com>

------------------------------------------------------------------------  r17801 | hchen30 | 2015-07-01 23:05:26 -0700 (Wed, 01 Jul 2015) | 7 lines
  BaseTools/Ecc: Fix a bug when checking copyright format
  Fix a bug to only checking the copyright listed in config.ini file.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: YangX Li <yangx.li@intel.com>

------------------------------------------------------------------------