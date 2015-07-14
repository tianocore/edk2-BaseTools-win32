Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17942

This directory contains the Win32 binaries.

Build Date:       Tue, 14 Jul 2015 03:17:32 Pacific Daylight Time
Last Changed Rev: 17942

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17823
 *BootSectImage Version 0.1 Build 17942
  Ecc.exe Version 0.01 Build 17712
 *EfiLdrImage Version 0.1 Build 17942
 *EfiRom Version 0.1 Build 17942
 *GenBootSector Version 0.2 Build 17942
 *GenCrc32 Version 0.2 Build 17942
  GenDepex.exe Version 0.04 Build 17823
  GenFds.exe 1.0 Build 17823
 *GenFfs Version 0.1 Build 17942
 *GenFv Version 0.1 Build 17942
 *GenFw Version 0.2 Build 17942
 *GenPage Version 0.2 Build 17942
  GenPatchPcdTable.exe Version 0.10 Build 17823
 *GenSec Version 0.1 Build 17942
 *GenVtf Version 0.1 Build 17942
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 17942
  LzmaF86Compress Version 0.2 Build 17942
  PatchPcdValue.exe Version 0.10 Build 17823
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
 *Split Version 0.1 Build 17942
  TargetTool.exe Version 0.01 Build 17823
 *TianoCompress Version 0.1 Build 17942
  Trim.exe Version 0.10 Build 17823
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17927
 *VfrCompile version  2.00 (UEFI 2.4) Build 17942
 *VolInfo Version 0.83 Build 17942, Jul 14 2015
  build.exe Version 0.60 Build 17823

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  7/14/2015 3:17:34AM Engine version = 5700.7163
  7/14/2015 3:17:34AM AntiVirus DAT version = 7861.0
  7/14/2015 3:17:34AM Number of detection signatures in EXTRA.DAT = None
  7/14/2015 3:17:34AM Names of detection signatures in EXTRA.DAT = None
  7/14/2015 3:17:34AM Scan Started On-Demand Scan
  7/14/2015 3:17:38AM Scan Summary
  7/14/2015 3:17:38AM Processes scanned : 0
  7/14/2015 3:17:38AM Processes detected : 0
  7/14/2015 3:17:38AM Processes cleaned : 0
  7/14/2015 3:17:38AM Boot sectors scanned : 1
  7/14/2015 3:17:38AM Boot sectors detected: 0
  7/14/2015 3:17:38AM Boot sectors cleaned : 0
  7/14/2015 3:17:38AM Files scanned : 70
  7/14/2015 3:17:38AM Files with detections: 0
  7/14/2015 3:17:38AM File detections : 0
  7/14/2015 3:17:38AM Files cleaned : 0
  7/14/2015 3:17:38AM Files deleted : 0
  7/14/2015 3:17:38AM Files not scanned : 0
  7/14/2015 3:17:38AM Scan Summary (Registry Scanning)
  7/14/2015 3:17:38AM Keys scanned : 0
  7/14/2015 3:17:38AM Keys detected : 0
  7/14/2015 3:17:38AM Keys cleaned : 0
  7/14/2015 3:17:38AM Keys deleted : 0
  7/14/2015 3:17:38AM Run time : 0:00:04
  7/14/2015 3:17:38AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17927:HEAD Source
------------------------------------------------------------------------  r17942 | abiesheuvel | 2015-07-14 01:15:28 -0700 (Tue, 14 Jul 2015) | 11 lines
  BaseTools/PeCoffLib: handle EFI_IMAGE_REL_BASED_DIR64 in generic code
  Relocations of type EFI_IMAGE_REL_BASED_DIR64 are handled in exactly
  the same way on all 64-bit machine types (IPF, X64 and AARCH64).
  So move the handling of this type to the generic part of the relocation
  routine PeCoffLoaderRelocateImage ().
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>

------------------------------------------------------------------------