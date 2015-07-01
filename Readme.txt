Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17791

This directory contains the Win32 binaries.

Build Date:       Wed, 01 Jul 2015 03:16:41 Pacific Daylight Time
Last Changed Rev: 17775

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17712
 *BootSectImage Version 0.1 Build 17791
  Ecc.exe Version 0.01 Build 17712
 *EfiLdrImage Version 0.1 Build 17791
 *EfiRom Version 0.1 Build 17791
 *GenBootSector Version 0.2 Build 17791
 *GenCrc32 Version 0.2 Build 17791
  GenDepex.exe Version 0.04 Build 17712
  GenFds.exe 1.0 Build 17712
 *GenFfs Version 0.1 Build 17791
 *GenFv Version 0.1 Build 17791
 *GenFw Version 0.2 Build 17791
 *GenPage Version 0.2 Build 17791
  GenPatchPcdTable.exe Version 0.10 Build 17712
 *GenSec Version 0.1 Build 17791
 *GenVtf Version 0.1 Build 17791
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 17791
  LzmaF86Compress Version 0.2 Build 17791
  PatchPcdValue.exe Version 0.10 Build 17712
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17553
 *Split Version 0.1 Build 17791
  TargetTool.exe Version 0.01 Build 17712
 *TianoCompress Version 0.1 Build 17791
  Trim.exe Version 0.10 Build 17712
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17674
 *VfrCompile version  2.00 (UEFI 2.4) Build 17791
 *VolInfo Version 0.83 Build 17791, Jul  1 2015
  build.exe Version 0.60 Build 17712

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1263
  7/1/2015 3:16:42AM Engine version = 5700.7163
  7/1/2015 3:16:42AM AntiVirus DAT version = 7848.0
  7/1/2015 3:16:42AM Number of detection signatures in EXTRA.DAT = None
  7/1/2015 3:16:42AM Names of detection signatures in EXTRA.DAT = None
  7/1/2015 3:16:43AM Scan Started On-Demand Scan
  7/1/2015 3:16:50AM Scan Summary
  7/1/2015 3:16:50AM Processes scanned : 0
  7/1/2015 3:16:50AM Processes detected : 0
  7/1/2015 3:16:50AM Processes cleaned : 0
  7/1/2015 3:16:50AM Boot sectors scanned : 1
  7/1/2015 3:16:50AM Boot sectors detected: 0
  7/1/2015 3:16:50AM Boot sectors cleaned : 0
  7/1/2015 3:16:50AM Files scanned : 70
  7/1/2015 3:16:50AM Files with detections: 0
  7/1/2015 3:16:50AM File detections : 0
  7/1/2015 3:16:50AM Files cleaned : 0
  7/1/2015 3:16:50AM Files deleted : 0
  7/1/2015 3:16:50AM Files not scanned : 0
  7/1/2015 3:16:50AM Scan Summary (Registry Scanning)
  7/1/2015 3:16:50AM Keys scanned : 0
  7/1/2015 3:16:50AM Keys detected : 0
  7/1/2015 3:16:50AM Keys cleaned : 0
  7/1/2015 3:16:50AM Keys deleted : 0
  7/1/2015 3:16:50AM Run time : 0:00:08
  7/1/2015 3:16:50AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17712:HEAD Source
------------------------------------------------------------------------  r17727 | yingke | 2015-06-28 20:17:34 -0700 (Sun, 28 Jun 2015) | 7 lines
  BaseTools: Update GenFw to support 4K alignment.
  Get maximum section alignment from each ELF section, and this alignment is used to create PE header.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r17774 | yingke | 2015-06-30 22:14:28 -0700 (Tue, 30 Jun 2015) | 5 lines
  BaseTools: Do not create an empty file if Rsa2048Sha256Sign was failed.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r17775 | yingke | 2015-06-30 22:16:46 -0700 (Tue, 30 Jun 2015) | 5 lines
  BaseTools: Checked return value of malloc for EfiCompress.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------