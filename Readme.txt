Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18063

This directory contains the Win32 binaries.

Build Date:       Sun, 26 Jul 2015 03:18:26 Pacific Daylight Time
Last Changed Rev: 18058

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18063
 *BootSectImage Version 0.1 Build 18063
  Ecc.exe Version 0.01 Build 17712
 *EfiLdrImage Version 0.1 Build 18063
 *EfiRom Version 0.1 Build 18063
 *GenBootSector Version 0.2 Build 18063
 *GenCrc32 Version 0.2 Build 18063
 *GenDepex.exe Version 0.04 Build 18063
 *GenFds.exe 1.0 Build 18063
 *GenFfs Version 0.1 Build 18063
 *GenFv Version 0.1 Build 18063
 *GenFw Version 0.2 Build 18063
 *GenPage Version 0.2 Build 18063
 *GenPatchPcdTable.exe Version 0.10 Build 18063
 *GenSec Version 0.1 Build 18063
 *GenVtf Version 0.1 Build 18063
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 18063
  LzmaF86Compress Version 0.2 Build 18063
 *PatchPcdValue.exe Version 0.10 Build 18063
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
 *Split Version 0.1 Build 18063
 *TargetTool.exe Version 0.01 Build 18063
 *TianoCompress Version 0.1 Build 18063
 *Trim.exe Version 0.10 Build 18063
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17927
 *VfrCompile version  2.00 (UEFI 2.4) Build 18063
 *VolInfo Version 0.83 Build 18063, Jul 26 2015
 *build.exe Version 0.60 Build 18063

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  7/26/2015 3:18:28AM Engine version = 5700.7163
  7/26/2015 3:18:28AM AntiVirus DAT version = 7873.0
  7/26/2015 3:18:28AM Number of detection signatures in EXTRA.DAT = None
  7/26/2015 3:18:28AM Names of detection signatures in EXTRA.DAT = None
  7/26/2015 3:18:28AM Scan Started On-Demand Scan
  7/26/2015 3:18:35AM Scan Summary
  7/26/2015 3:18:35AM Processes scanned : 0
  7/26/2015 3:18:35AM Processes detected : 0
  7/26/2015 3:18:35AM Processes cleaned : 0
  7/26/2015 3:18:35AM Boot sectors scanned : 2
  7/26/2015 3:18:35AM Boot sectors detected: 0
  7/26/2015 3:18:35AM Boot sectors cleaned : 0
  7/26/2015 3:18:35AM Files scanned : 71
  7/26/2015 3:18:35AM Files with detections: 0
  7/26/2015 3:18:35AM File detections : 0
  7/26/2015 3:18:35AM Files cleaned : 0
  7/26/2015 3:18:35AM Files deleted : 0
  7/26/2015 3:18:35AM Files not scanned : 0
  7/26/2015 3:18:35AM Scan Summary (Registry Scanning)
  7/26/2015 3:18:35AM Keys scanned : 0
  7/26/2015 3:18:35AM Keys detected : 0
  7/26/2015 3:18:35AM Keys cleaned : 0
  7/26/2015 3:18:35AM Keys deleted : 0
  7/26/2015 3:18:35AM Run time : 0:00:08
  7/26/2015 3:18:35AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17942:HEAD Source
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

------------------------------------------------------------------------  r18016 | jljusten | 2015-07-26 00:36:57 -0700 (Sun, 26 Jul 2015) | 8 lines
  BaseTools: Fixed incorrect alignment bug.
  The alignment in rule section is shared by modules to generate FFS,
  it should not be modified by certain module.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r18047 | jljusten | 2015-07-26 01:03:15 -0700 (Sun, 26 Jul 2015) | 9 lines
  BaseTools/Common: fix heap overrun in ReadMemoryFileLine ()
  ReadMemoryFileLine () appends a NULL character to the string
  it returns, but it failed to account for it in the allocation.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>

------------------------------------------------------------------------  r18058 | jljusten | 2015-07-26 01:04:10 -0700 (Sun, 26 Jul 2015) | 16 lines
  BaseTools: Make AutoGen.h array declaration match AutoGen.c definition
  When a quoted string is used as initialization data in a DEC file PCD
  entry, the PCD data type in that entry must be VOID*. The created
  AutoGen.c defines the PCD data as UINT8[] or UINT16[], depending on
  the string type. The created AutoGen.h, however, declares the PCD data
  as VOID*. For a standard compile/link, this works because AutoGen.c
  doesn't include AutoGen.h. But when GCC LTO is used, the link time
  code generation detects the mismatch and the build fails. This
  change makes the AutoGen.h PCD data declaration match the AutoGen.c
  definition.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Scott Duplichan <scott@notabs.org>
  Reviewed-by: Yingke Liu <yingke.d.liu@intel.com>
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>

------------------------------------------------------------------------