Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18552

This directory contains the Win32 binaries.

Build Date:       Fri, 25 Sep 2015 03:19:45 Pacific Daylight Time
Last Changed Rev: 18540

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18320
  BootSectImage Version 0.1 Build 18276
  Ecc.exe Version 0.01 Build 17712
  EfiLdrImage Version 0.1 Build 18276
  EfiRom Version 0.1 Build 18276
  GenBootSector Version 0.2 Build 18276
  GenCrc32 Version 0.2 Build 18276
  GenDepex.exe Version 0.04 Build 18320
  GenFds.exe 1.0 Build 18361
  GenFfs Version 0.1 Build 18276
  GenFv Version 0.1 Build 18276
 *GenFw Version 0.2 Build 18552
  GenPage Version 0.2 Build 18276
  GenPatchPcdTable.exe Version 0.10 Build 18320
  GenSec Version 0.1 Build 18276
  GenVtf Version 0.1 Build 18276
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 18276
  LzmaF86Compress Version 0.2 Build 18276
  PatchPcdValue.exe Version 0.10 Build 18320
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 18276
  TargetTool.exe Version 0.01 Build 18320
  TianoCompress Version 0.1 Build 18276
  Trim.exe Version 0.10 Build 18320
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17927
  VfrCompile version  2.00 (UEFI 2.4) Build 18337
  VolInfo Version 0.83 Build 18276, Aug 24 2015
  build.exe Version 0.60 Build 18320

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  9/25/2015 3:19:46AM Engine version = 5700.7163
  9/25/2015 3:19:46AM AntiVirus DAT version = 7934.0
  9/25/2015 3:19:46AM Number of detection signatures in EXTRA.DAT = 3
  9/25/2015 3:19:46AM Names of detection signatures in EXTRA.DAT = GenericR-ECJ (ED) RDN/Generic BackDoor (ED)
  9/25/2015 3:19:46AM Scan Started On-Demand Scan
  9/25/2015 3:19:49AM Scan Summary
  9/25/2015 3:19:49AM Processes scanned : 0
  9/25/2015 3:19:49AM Processes detected : 0
  9/25/2015 3:19:49AM Processes cleaned : 0
  9/25/2015 3:19:49AM Boot sectors scanned : 1
  9/25/2015 3:19:49AM Boot sectors detected: 0
  9/25/2015 3:19:49AM Boot sectors cleaned : 0
  9/25/2015 3:19:49AM Files scanned : 55
  9/25/2015 3:19:49AM Files with detections: 0
  9/25/2015 3:19:49AM File detections : 0
  9/25/2015 3:19:49AM Files cleaned : 0
  9/25/2015 3:19:49AM Files deleted : 0
  9/25/2015 3:19:49AM Files not scanned : 0
  9/25/2015 3:19:49AM Scan Summary (Registry Scanning)
  9/25/2015 3:19:49AM Keys scanned : 0
  9/25/2015 3:19:49AM Keys detected : 0
  9/25/2015 3:19:49AM Keys cleaned : 0
  9/25/2015 3:19:49AM Keys deleted : 0
  9/25/2015 3:19:49AM Run time : 0:00:03
  9/25/2015 3:19:49AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18444:HEAD Source
------------------------------------------------------------------------  r18446 | hchen30 | 2015-09-14 00:12:29 -0700 (Mon, 14 Sep 2015) | 8 lines
  BaseTools/Ecc: Remove checkpoint for STATIC modifier
  1. Fix a bug of removing the checkpoint for STATIC modifier
  2. Fix a bug of parsing CONST variable
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: YangX Li <yangx.li@intel.com>

------------------------------------------------------------------------  r18539 | abiesheuvel | 2015-09-24 12:35:10 -0700 (Thu, 24 Sep 2015) | 9 lines
  BaseTools/GenFw: remove ARM and RVCT references from ELF64 code
  ARM and RVCT apply to 32-bit code only, so remove any references
  to them (including the workaround for the linker) from the 64-bit
  version of ElfConvert.c
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Leif Lindholm <leif.lindholm@linaro.org>

------------------------------------------------------------------------  r18540 | abiesheuvel | 2015-09-24 12:35:16 -0700 (Thu, 24 Sep 2015) | 15 lines
  BaseTools/GenFw: disable RVCT linker size optimization
  Disable the RVCT size optimization that may put sections at an offset
  that is not aligned to their own alignment, by adding the --no_legacyalign
  switch to the RVCT linker command line. This is necessary since such sections
  cannot be correctly converted into PE/COFF sections without padding them at
  the front, which defeats the purpose of the optimization anyway.
  With the optimization gone, we can also remove the special case for ARM in
  GenFw that could result in corrupt PE/COFF images to be emitted. Instead,
  sections whose base address is not aligned correctly are outright rejected.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Leif Lindholm <leif.lindholm@linaro.org>

------------------------------------------------------------------------