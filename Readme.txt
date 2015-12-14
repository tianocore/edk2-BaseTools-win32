Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 19244

This directory contains the Win32 binaries.

Build Date:       Mon, 14 Dec 2015 14:28:08 Pacific Standard Time
Last Changed Rev: 19238

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 19174
  BootSectImage Version 0.1 Build 19148
  Ecc.exe Version 0.01 Build 18595
  EfiLdrImage Version 0.1 Build 19148
  EfiRom Version 0.1 Build 19148
  GenBootSector Version 0.2 Build 19148
  GenCrc32 Version 0.2 Build 19148
  GenDepex.exe Version 0.04 Build 19174
  GenFds.exe 1.0 Build 19174
  GenFfs Version 0.1 Build 19148
  GenFv Version 0.1 Build 19148
 *GenFw Version 0.2 Build 19244
  GenPage Version 0.2 Build 19148
  GenPatchPcdTable.exe Version 0.10 Build 19174
  GenSec Version 0.1 Build 19148
  GenVtf Version 0.1 Build 19148
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 19148
  LzmaF86Compress Version 0.2 Build 19148
  PatchPcdValue.exe Version 0.10 Build 19174
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 19148
  TargetTool.exe Version 0.01 Build 19174
  TianoCompress Version 0.1 Build 19148
  Trim.exe Version 0.10 Build 19174
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 18900
  VfrCompile version  2.00 (UEFI 2.4) Build 19148
  VolInfo Version 0.83 Build 19148, Dec  7 2015
  build.exe Version 0.60 Build 19174

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/14/2015 2:28:09PM Engine version = 5700.7163
  12/14/2015 2:28:09PM AntiVirus DAT version = 8014.0
  12/14/2015 2:28:09PM Number of detection signatures in EXTRA.DAT = None
  12/14/2015 2:28:09PM Names of detection signatures in EXTRA.DAT = None
  12/14/2015 2:28:09PM Scan Started On-Demand Scan
  12/14/2015 2:28:22PM Scan Summary
  12/14/2015 2:28:22PM Processes scanned : 0
  12/14/2015 2:28:22PM Processes detected : 0
  12/14/2015 2:28:22PM Processes cleaned : 0
  12/14/2015 2:28:22PM Boot sectors scanned : 1
  12/14/2015 2:28:22PM Boot sectors detected: 0
  12/14/2015 2:28:22PM Boot sectors cleaned : 0
  12/14/2015 2:28:22PM Files scanned : 55
  12/14/2015 2:28:22PM Files with detections: 0
  12/14/2015 2:28:22PM File detections : 0
  12/14/2015 2:28:22PM Files cleaned : 0
  12/14/2015 2:28:22PM Files deleted : 0
  12/14/2015 2:28:22PM Files not scanned : 0
  12/14/2015 2:28:22PM Scan Summary (Registry Scanning)
  12/14/2015 2:28:22PM Keys scanned : 0
  12/14/2015 2:28:22PM Keys detected : 0
  12/14/2015 2:28:22PM Keys cleaned : 0
  12/14/2015 2:28:22PM Keys deleted : 0
  12/14/2015 2:28:22PM Run time : 0:00:13
  12/14/2015 2:28:22PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 19174:HEAD Source
------------------------------------------------------------------------  r19236 | abiesheuvel | 2015-12-13 23:56:02 -0800 (Sun, 13 Dec 2015) | 30 lines
  BaseTools/GenFw RVCT: fix relocation processing of PT_DYNAMIC sections
  Unlike GNU ld, which can be instructed to emit symbol based static
  relocations into fully linked binaries using the --emit-relocs command
  line switch, the RVCT armlink tool can only emit dynamic relocations
  into the PT_DYNAMIC segment.
  This has two consequences
  . we can only identify absolute relocations, so there is no way to fix
  up relative relocations between sections, or check their validity in
  the PE/COFF layout
  . the r_offset fields of the PT_DYNAMIC DT_REL entries are relative
  either to the base of the image or to any of its segments but *not* to
  the base of the input section that contains the location they refer
  to, and converting them to PE/COFF image offsets is non-trivial unless
  the sections are laid out in the same way in the ELF and PE/COFF
  versions of the binary.
  There is really only one way to deal with this, and that is to require
  that the ELF and PE/COFF versions of the binary are identical in memory.
  So enforce that in the code.
  Also, fix the utterly broken relocation fixup code that dereferences
  ELF32_R_SYM(r_info) both as a 1-based program header index and a 0-based
  section header index. If this code ever produced working binaries, it
  was purely by chance.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r19238 | hchen30 | 2015-12-14 00:08:21 -0800 (Mon, 14 Dec 2015) | 7 lines
  BaseTools/Ecc: Fix a bug to report fake issue
  Fix a bug to ignore the lib ins defined in [components] section but also listed in SkipDir
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>

------------------------------------------------------------------------