Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22237

This directory contains the Win32 binaries.

Build Date:       Tue, 02 Aug 2016 03:11:08 Pacific Daylight Time
Last Changed Rev: 22234

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22210
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
  GenDepex.exe Version 0.04 Build 22210
  GenFds.exe 1.0 Build 22210
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 20909
 *GenFw Version 0.2 Build 22237
  GenPage Version 0.2 Build 20909
  GenPatchPcdTable.exe Version 0.10 Build 22210
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
  PatchPcdValue.exe Version 0.10 Build 22210
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
  TargetTool.exe Version 0.01 Build 22210
  TianoCompress Version 0.1 Build 20909
  Trim.exe Version 0.10 Build 22210
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20909
  VolInfo Version 1.0 Build Build 20909
  build.exe Version 0.60 Build 22210

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/2/2016 3:11:10AM Engine version = 5700.7163
  8/2/2016 3:11:10AM AntiVirus DAT version = 8244.0
  8/2/2016 3:11:10AM Number of detection signatures in EXTRA.DAT = None
  8/2/2016 3:11:10AM Names of detection signatures in EXTRA.DAT = None
  8/2/2016 3:11:10AM Scan Started On-Demand Scan
  8/2/2016 3:11:12AM Scan Summary
  8/2/2016 3:11:12AM Processes scanned : 0
  8/2/2016 3:11:12AM Processes detected : 0
  8/2/2016 3:11:12AM Processes cleaned : 0
  8/2/2016 3:11:12AM Boot sectors scanned : 1
  8/2/2016 3:11:12AM Boot sectors detected: 0
  8/2/2016 3:11:12AM Boot sectors cleaned : 0
  8/2/2016 3:11:12AM Files scanned : 55
  8/2/2016 3:11:12AM Files with detections: 0
  8/2/2016 3:11:12AM File detections : 0
  8/2/2016 3:11:12AM Files cleaned : 0
  8/2/2016 3:11:12AM Files deleted : 0
  8/2/2016 3:11:12AM Files not scanned : 0
  8/2/2016 3:11:12AM Scan Summary (Registry Scanning)
  8/2/2016 3:11:12AM Keys scanned : 0
  8/2/2016 3:11:12AM Keys detected : 0
  8/2/2016 3:11:12AM Keys cleaned : 0
  8/2/2016 3:11:12AM Keys deleted : 0
  8/2/2016 3:11:12AM Run time : 0:00:02
  8/2/2016 3:11:12AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22210:HEAD Source
------------------------------------------------------------------------  r22234 | edk2buildsystem | 2016-08-02 02:06:33 -0700 (Tue, 02 Aug 2016) | 28 lines
  BaseTools/GenFw AARCH64: convert ADRP to ADR instructions if binary size allows it
  The ADRP instruction in the AArch64 ISA requires the link time and load time
  offsets of a binary to be equal modulo 4 KB. The reason is that this instruction
  always produces a multiple of 4 KB, and relies on a subsequent ADD or LDR
  instruction to set the offset into the page. The resulting symbol reference
  only produces the correct value if the symbol in question resides at that
  exact offset into the page, and so loading the binary at arbitrary offsets
  is not possible.
  Due to the various levels of padding when packing FVs into FVs into FDs, this
  alignment is very costly for XIP code, and so we would like to relax this
  alignment requirement if possible.
  Given that symbols that are sufficiently close (within 1 MB) of the reference
  can also be reached using an ADR instruction which does not suffer from this
  alignment issue, let's replace ADRP instructions with ADR after linking if
  the offset can be encoded in this instruction's immediate field. Note that
  this only makes sense if the section alignment is < 4 KB. Otherwise,
  replacing the ADRP has no benefit, considering that the subsequent ADD or
  LDR instruction is retained, and that micro-architectures are more likely
  to be optimized for ADRP/ADD pairs (i.e., via micro op fusing) than for
  ADR/ADD pairs, which are non-typical.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Leif Lindholm <leif.lindholm@linaro.org>
  (cherry picked from commit 026a82abf0bd6268d32f4559dbede00715264f74)

------------------------------------------------------------------------