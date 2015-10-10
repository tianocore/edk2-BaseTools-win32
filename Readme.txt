Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18600

This directory contains the Win32 binaries.

Build Date:       Sat, 10 Oct 2015 03:20:58 Pacific Daylight Time
Last Changed Rev: 18600

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18584
 *BootSectImage Version 0.1 Build 18600
  Ecc.exe Version 0.01 Build 18595
 *EfiLdrImage Version 0.1 Build 18600
 *EfiRom Version 0.1 Build 18600
 *GenBootSector Version 0.2 Build 18600
 *GenCrc32 Version 0.2 Build 18600
  GenDepex.exe Version 0.04 Build 18584
  GenFds.exe 1.0 Build 18584
 *GenFfs Version 0.1 Build 18600
 *GenFv Version 0.1 Build 18600
 *GenFw Version 0.2 Build 18600
 *GenPage Version 0.2 Build 18600
  GenPatchPcdTable.exe Version 0.10 Build 18584
 *GenSec Version 0.1 Build 18600
 *GenVtf Version 0.1 Build 18600
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 18600
  LzmaF86Compress Version 0.2 Build 18600
  PatchPcdValue.exe Version 0.10 Build 18584
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
 *Split Version 0.1 Build 18600
  TargetTool.exe Version 0.01 Build 18584
 *TianoCompress Version 0.1 Build 18600
  Trim.exe Version 0.10 Build 18584
 *UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 18600
 *VfrCompile version  2.00 (UEFI 2.4) Build 18600
 *VolInfo Version 0.83 Build 18600, Oct 10 2015
  build.exe Version 0.60 Build 18584

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/10/2015 3:21:00AM Engine version = 5700.7163
  10/10/2015 3:21:00AM AntiVirus DAT version = 7949.0
  10/10/2015 3:21:00AM Number of detection signatures in EXTRA.DAT = 3
  10/10/2015 3:21:00AM Names of detection signatures in EXTRA.DAT = GenericR-ECJ (ED) RDN/Generic BackDoor (ED)
  10/10/2015 3:21:00AM Scan Started On-Demand Scan
  10/10/2015 3:21:18AM Scan Summary
  10/10/2015 3:21:18AM Processes scanned : 0
  10/10/2015 3:21:18AM Processes detected : 0
  10/10/2015 3:21:18AM Processes cleaned : 0
  10/10/2015 3:21:18AM Boot sectors scanned : 2
  10/10/2015 3:21:18AM Boot sectors detected: 0
  10/10/2015 3:21:18AM Boot sectors cleaned : 0
  10/10/2015 3:21:18AM Files scanned : 71
  10/10/2015 3:21:18AM Files with detections: 0
  10/10/2015 3:21:18AM File detections : 0
  10/10/2015 3:21:18AM Files cleaned : 0
  10/10/2015 3:21:18AM Files deleted : 0
  10/10/2015 3:21:18AM Files not scanned : 0
  10/10/2015 3:21:18AM Scan Summary (Registry Scanning)
  10/10/2015 3:21:18AM Keys scanned : 0
  10/10/2015 3:21:18AM Keys detected : 0
  10/10/2015 3:21:18AM Keys cleaned : 0
  10/10/2015 3:21:18AM Keys deleted : 0
  10/10/2015 3:21:18AM Run time : 0:00:19
  10/10/2015 3:21:18AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18595:HEAD Source
------------------------------------------------------------------------  r18596 | abiesheuvel | 2015-10-09 11:55:28 -0700 (Fri, 09 Oct 2015) | 11 lines
  BaseTools/PeCoffLoader: fix handling of ARM MOVW/MOVT instruction relocs
  The handling of ARM MOVW/MOVT relocations sets the FixupData twice (once
  incorrectly), but fails to advance the *FixupData pointer afterwards.
  This is not actually a problem, since the fixup data is never used but
  let's fix it anyway in case anyone reuses this code.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Leif Lindholm <leif.lindholm@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r18600 | hchen30 | 2015-10-09 22:46:00 -0700 (Fri, 09 Oct 2015) | 5 lines
  BaseTool/UPT: Fix two wrong imports for UPT
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------