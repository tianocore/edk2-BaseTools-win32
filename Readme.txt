Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17611

This directory contains the Win32 binaries.

Build Date:       Wed, 10 Jun 2015 03:15:35 Pacific Daylight Time
Last Changed Rev: 17608

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Not available
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17611
  BootSectImage Version 0.1 Build 17553
  Ecc.exe Version 0.01 Build 17553
  EfiLdrImage Version 0.1 Build 17553
  EfiRom Version 0.1 Build 17553
  GenBootSector Version 0.2 Build 17553
  GenCrc32 Version 0.2 Build 17553
 *GenDepex.exe Version 0.04 Build 17611
 *GenFds.exe 1.0 Build 17611
  GenFfs Version 0.1 Build 17553
  GenFv Version 0.1 Build 17553
  GenFw Version 0.2 Build 17553
  GenPage Version 0.2 Build 17553
 *GenPatchPcdTable.exe Version 0.10 Build 17611
  GenSec Version 0.1 Build 17553
  GenVtf Version 0.1 Build 17553
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 17553
  LzmaF86Compress Version 0.2 Build 17553
 *PatchPcdValue.exe Version 0.10 Build 17611
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17553
  Split Version 0.1 Build 17553
 *TargetTool.exe Version 0.01 Build 17611
  TianoCompress Version 0.1 Build 17553
 *Trim.exe Version 0.10 Build 17611
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 17553
  VfrCompile version  2.00 (UEFI 2.4) Build 17553
  VolInfo Version 0.83 Build 17553, Jun  3 2015
 *build.exe Version 0.60 Build 17611

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1247
  6/10/2015 3:15:37AM Engine version = 5700.7163
  6/10/2015 3:15:37AM AntiVirus DAT version = 7827.0
  6/10/2015 3:15:37AM Number of detection signatures in EXTRA.DAT = None
  6/10/2015 3:15:37AM Names of detection signatures in EXTRA.DAT = None
  6/10/2015 3:15:37AM Scan Started On-Demand Scan
  6/10/2015 3:16:00AM Scan Summary
  6/10/2015 3:16:00AM Processes scanned : 0
  6/10/2015 3:16:00AM Processes detected : 0
  6/10/2015 3:16:00AM Processes cleaned : 0
  6/10/2015 3:16:00AM Boot sectors scanned : 2
  6/10/2015 3:16:00AM Boot sectors detected: 0
  6/10/2015 3:16:00AM Boot sectors cleaned : 0
  6/10/2015 3:16:00AM Files scanned : 55
  6/10/2015 3:16:00AM Files with detections: 0
  6/10/2015 3:16:00AM File detections : 0
  6/10/2015 3:16:00AM Files cleaned : 0
  6/10/2015 3:16:00AM Files deleted : 0
  6/10/2015 3:16:00AM Files not scanned : 0
  6/10/2015 3:16:00AM Scan Summary (Registry Scanning)
  6/10/2015 3:16:00AM Keys scanned : 0
  6/10/2015 3:16:00AM Keys detected : 0
  6/10/2015 3:16:00AM Keys cleaned : 0
  6/10/2015 3:16:00AM Keys deleted : 0
  6/10/2015 3:16:00AM Run time : 0:00:24
  6/10/2015 3:16:00AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17553:HEAD Source
------------------------------------------------------------------------  r17573 | yingke | 2015-06-08 01:08:58 -0700 (Mon, 08 Jun 2015) | 5 lines
  BaseTools: Added extern declaration for protocols/PPI/GUID in AutoGhen.h
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r17579 | lgao4 | 2015-06-08 02:44:01 -0700 (Mon, 08 Jun 2015) | 11 lines
  BaseTools: Update GenFds to handle file type Ffs Rule
  Ffs Rule can specify a file type instead of specific file name. GenFds
  should search Binary sections of module INF file and output directory
  of the module to find all matched file with the specific file type.
  Current GenFds only considers the final output target file. This patch
  applies the above rule to match output file with the specific file type.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------  r17602 | lhauch | 2015-06-09 11:20:51 -0700 (Tue, 09 Jun 2015) | 5 lines
  Removing the msvcr71.dll - no longer required, building with VS2013.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: lhauch <larry.hauch@intel.com>
  Reviewed-by: Joe Peterson <joe.peterson@intel.com>

------------------------------------------------------------------------  r17608 | yingke | 2015-06-10 00:50:59 -0700 (Wed, 10 Jun 2015) | 7 lines
  BaseTools: Append FILE_GUID to BaseName.
  This patch makes sure the EFI file in $(BIN_DIR) is unique. If there are modules with same BaseName, the FILE_GUID is appended.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------