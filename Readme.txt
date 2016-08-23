Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22466

This directory contains the Win32 binaries.

Build Date:       Tue, 23 Aug 2016 16:57:33 Pacific Daylight Time
Last Changed Rev: 22466

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22444
  BootSectImage Version 1.0 Build Build 22449
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 22449
  EfiRom Version 0.1 Build 22449
  GenBootSector Version 0.2 Build 22449
  GenCrc32 Version 0.2 Build 22449
  GenDepex.exe Version 0.04 Build 22444
  GenFds.exe 1.0 Build 22465
  GenFfs Version 0.1 Build 22449
  GenFv Version 0.1 Build 22449
 *GenFw Version 0.2 Build 22466
  GenPage Version 0.2 Build 22449
  GenPatchPcdTable.exe Version 0.10 Build 22444
  GenSec Version 0.1 Build 22449
  GenVtf Version 0.1 Build 22449
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 22449
  LzmaF86Compress Version 0.2 Build 22449
  PatchPcdValue.exe Version 0.10 Build 22444
ERROR : This tool is missing --version option: Pkcs7Sign.exe
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 22444
  Split Version 1.0 Build Build 22449
  TargetTool.exe Version 0.01 Build 22444
  TianoCompress Version 0.1 Build 22449
  Trim.exe Version 0.10 Build 22444
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22316
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22449
  VolInfo Version 1.0 Build Build 22449
  build.exe Version 0.60 Build 22444

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/23/2016 4:57:34PM Engine version = 5700.7163
  8/23/2016 4:57:34PM AntiVirus DAT version = 8266.0
  8/23/2016 4:57:34PM Number of detection signatures in EXTRA.DAT = None
  8/23/2016 4:57:34PM Names of detection signatures in EXTRA.DAT = None
  8/23/2016 4:57:34PM Scan Started On-Demand Scan
  8/23/2016 4:57:44PM Scan Summary
  8/23/2016 4:57:44PM Processes scanned : 0
  8/23/2016 4:57:44PM Processes detected : 0
  8/23/2016 4:57:44PM Processes cleaned : 0
  8/23/2016 4:57:44PM Boot sectors scanned : 2
  8/23/2016 4:57:44PM Boot sectors detected: 0
  8/23/2016 4:57:44PM Boot sectors cleaned : 0
  8/23/2016 4:57:44PM Files scanned : 62
  8/23/2016 4:57:44PM Files with detections: 0
  8/23/2016 4:57:44PM File detections : 0
  8/23/2016 4:57:44PM Files cleaned : 0
  8/23/2016 4:57:44PM Files deleted : 0
  8/23/2016 4:57:44PM Files not scanned : 0
  8/23/2016 4:57:44PM Scan Summary (Registry Scanning)
  8/23/2016 4:57:44PM Keys scanned : 0
  8/23/2016 4:57:44PM Keys detected : 0
  8/23/2016 4:57:44PM Keys cleaned : 0
  8/23/2016 4:57:44PM Keys deleted : 0
  8/23/2016 4:57:44PM Run time : 0:00:10
  8/23/2016 4:57:44PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22465:HEAD Source
------------------------------------------------------------------------  r22466 | edk2buildsystem | 2016-08-23 14:05:32 -0700 (Tue, 23 Aug 2016) | 67 lines
  BaseTools/GenFw: ignore dynamic RELA sections
  When building PIE (ET_DYN) executables, an additional RELA section is
  emitted (in addition to the per-section .rela.text and .rela.data sections)
  that is intended to be resolved at runtime by a ET_DYN compatible loader.
  At the moment, due to the fact that we don't support GOT based relocations,
  this dynamic RELA section only contains relocations that are redundant,
  i.e., each R_xxx_RELATIVE relocation it contains duplicates a R_xxx_xx64
  relocation appearing in .rela.text or .rela.data, and so we can simply
  ignore this section (and we already ignore it in practice due to the fact
  that it points to the NULL section, which has the SHF_ALLOC bit cleared).
  For example,
  Section Headers:
  [Nr] Name              Type             Address           Offset
  Size              EntSize          Flags  Link  Info  Align
  [ 0]                   NULL             0000000000000000  00000000
  0000000000000000  0000000000000000           0     0     0
  [ 1] .text             PROGBITS         0000000000000240  000000c0
  000000000000427c  0000000000000008  AX       0     0     64
  [ 2] .rela.text        RELA             0000000000000000  00009310
  0000000000001bf0  0000000000000018   I       7     1     8
  [ 3] .data             PROGBITS         00000000000044c0  00004340
  00000000000046d0  0000000000000000  WA       0     0     64
  [ 4] .rela.data        RELA             0000000000000000  0000af00
  0000000000000600  0000000000000018   I       7     3     8
  [ 5] .rela             RELA             0000000000008bc0  00008a10
  0000000000000600  0000000000000018           0     0     8
  [ 6] .shstrtab         STRTAB           0000000000000000  0000b500
  0000000000000037  0000000000000000           0     0     1
  [ 7] .symtab           SYMTAB           0000000000000000  00009010
  0000000000000210  0000000000000018           8    17     8
  [ 8] .strtab           STRTAB           0000000000000000  00009220
  00000000000000eb  0000000000000000           0     0     1
  Relocation section '.rela.data' at offset 0xaf00 contains 64 entries:
  Offset          Info           Type           Sym. Value    Sym. Name + Addend
  000000004800  000100000001 R_X86_64_64       0000000000000240 .text + 3f5b
  000000004808  000100000001 R_X86_64_64       0000000000000240 .text + 3f63
  000000004810  000100000001 R_X86_64_64       0000000000000240 .text + 3f79
  000000004818  000100000001 R_X86_64_64       0000000000000240 .text + 3f90
  000000004820  000100000001 R_X86_64_64       0000000000000240 .text + 3fa6
  ...
  Relocation section '.rela' at offset 0x8a10 contains 64 entries:
  Offset          Info           Type           Sym. Value    Sym. Name + Addend
  000000004800  000000000008 R_X86_64_RELATIVE                    419b
  000000004808  000000000008 R_X86_64_RELATIVE                    41a3
  000000004810  000000000008 R_X86_64_RELATIVE                    41b9
  000000004818  000000000008 R_X86_64_RELATIVE                    41d0
  000000004820  000000000008 R_X86_64_RELATIVE                    41e6
  000000004828  000000000008 R_X86_64_RELATIVE                    41ff
  ...
  Note that GOT based relocations result in entries that *only* appear in the
  dynamic .rela section and not in .rela.text or .rela.data. This means two
  things if we intend to add support for GOT based relocations:
  - we must check that a dynamic RELA section exists;
  - we must filter out duplicates between .rela and .rela.xxx, to prevent
  emitting duplicate fixups into the PE/COFF .reloc section.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 4962fcfa7d265824f01f74d782d5ed841ec8a72f)

------------------------------------------------------------------------