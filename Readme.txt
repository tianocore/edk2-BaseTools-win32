Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22308

This directory contains the Win32 binaries.

Build Date:       Mon, 08 Aug 2016 03:11:47 Pacific Daylight Time
Last Changed Rev: 22307

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22308
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
 *GenDepex.exe Version 0.04 Build 22308
 *GenFds.exe 1.0 Build 22308
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 20909
 *GenFw Version 0.2 Build 22308
  GenPage Version 0.2 Build 20909
 *GenPatchPcdTable.exe Version 0.10 Build 22308
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
 *PatchPcdValue.exe Version 0.10 Build 22308
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
 *TargetTool.exe Version 0.01 Build 22308
  TianoCompress Version 0.1 Build 20909
 *Trim.exe Version 0.10 Build 22308
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22280
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 22308
  VolInfo Version 1.0 Build Build 20909
 *build.exe Version 0.60 Build 22308

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/8/2016 3:11:48AM Engine version = 5700.7163
  8/8/2016 3:11:48AM AntiVirus DAT version = 8250.0
  8/8/2016 3:11:48AM Number of detection signatures in EXTRA.DAT = None
  8/8/2016 3:11:48AM Names of detection signatures in EXTRA.DAT = None
  8/8/2016 3:11:48AM Scan Started On-Demand Scan
  8/8/2016 3:11:51AM Scan Summary
  8/8/2016 3:11:51AM Processes scanned : 0
  8/8/2016 3:11:51AM Processes detected : 0
  8/8/2016 3:11:51AM Processes cleaned : 0
  8/8/2016 3:11:51AM Boot sectors scanned : 1
  8/8/2016 3:11:51AM Boot sectors detected: 0
  8/8/2016 3:11:51AM Boot sectors cleaned : 0
  8/8/2016 3:11:51AM Files scanned : 57
  8/8/2016 3:11:51AM Files with detections: 0
  8/8/2016 3:11:51AM File detections : 0
  8/8/2016 3:11:51AM Files cleaned : 0
  8/8/2016 3:11:51AM Files deleted : 0
  8/8/2016 3:11:51AM Files not scanned : 0
  8/8/2016 3:11:51AM Scan Summary (Registry Scanning)
  8/8/2016 3:11:51AM Keys scanned : 0
  8/8/2016 3:11:51AM Keys detected : 0
  8/8/2016 3:11:51AM Keys cleaned : 0
  8/8/2016 3:11:51AM Keys deleted : 0
  8/8/2016 3:11:51AM Run time : 0:00:03
  8/8/2016 3:11:51AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22280:HEAD Source
------------------------------------------------------------------------  r22286 | edk2buildsystem | 2016-08-08 02:06:08 -0700 (Mon, 08 Aug 2016) | 11 lines
  BaseTools: Allow string token identifier to use lower case letters
  This patch is to align the code behavior with UNI spec that string token
  identifier can use upper case and lower case letters.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Felix <Felixp@ami.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c3915fa586c98ec68da3b464218651480e1324b6)

------------------------------------------------------------------------  r22287 | edk2buildsystem | 2016-08-08 02:06:14 -0700 (Mon, 08 Aug 2016) | 10 lines
  BaseTools: Fix the bug when use FILE_GUID override the module in DSC
  In last commit 2502b73, it doesn't cover the case that in the DSC file
  use FILE_GUID to override the module.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 622b17582e7928d6938ab421848313c3976a368a)

------------------------------------------------------------------------  r22305 | edk2buildsystem | 2016-08-08 02:07:41 -0700 (Mon, 08 Aug 2016) | 13 lines
  BaseTool/VfrCompile: Add missing question opcode
  The function CheckQuestionOpCode is to check whether the opcode
  is question opcode, but it misses two question opcodes:
  'EFI_IFR_REF_OP' and 'EFI_IFR_RESET_BUTTON'. Now add them.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Eric Dong <eric.dong@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit bec3a18108cf5839f3fb1f451c55e1b2afcbc747)

------------------------------------------------------------------------  r22306 | edk2buildsystem | 2016-08-08 02:07:47 -0700 (Mon, 08 Aug 2016) | 17 lines
  BaseTools/VfrCompile: Add two new option for VfrCompile
  1.--autodefault option
  VfrCompile will generate default opcodes for questions if some
  default are missing.
  2 --checkdefault option
  VfrCompile will check whether every question has no default or
  has all default. If not, will generate an error to let user know
  the question misses default.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Eric Dong <eric.dong@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 74bbe31b8d485da26ec7ffad5e78b8384a9eb9a5)

------------------------------------------------------------------------  r22307 | edk2buildsystem | 2016-08-08 02:07:53 -0700 (Mon, 08 Aug 2016) | 24 lines
  BaseTools X64: fold PLT relocations into simple relative references
  For X64/GCC, we use position independent code with hidden visibility
  to inform the compiler that symbol references are never resolved at
  runtime, which removes the need for PLTs and GOTs. However, in some
  cases, GCC has been reported to still emit PLT based relocations, which
  we need to handle in the ELF to PE/COFF perform by GenFw.
  Unlike GOT based relocations, which are non-trivial to handle since the
  indirections in the code can not be fixed up easily (although relocation
  types exist for X64 that annotate relocation targets as suitable for
  relaxation), PLT relocations simply point to jump targets, and we can
  relax such relocations by resolving them using the symbol directly rather
  than via a PLT entry that does nothing more than tail call the function
  we already know it is going to call (since all symbol references are
  resolved in the same module).
  So handle R_X86_64_PLT32 as a R_X86_64_PC32 relocation.
  Suggested-by: Steven Shi <steven.shi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c9f297559be5fd60aefda24b18e77a4208c8dede)

------------------------------------------------------------------------