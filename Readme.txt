Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 20165, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 19857

This directory contains the Win32 binaries.

Build Date:       Wed, 17 Feb 2016 13:36:07 Pacific Standard Time
Last Changed Rev: 19857

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 19857
 *BootSectImage Version 1.0 Build Build 19857
 *Ecc.exe Version 1.0 Build Build 19857
 *EfiLdrImage Version 1.0 Build Build 19857
  EfiRom Version 0.1 Build 19148
  GenBootSector Version 0.2 Build 19610
  GenCrc32 Version 0.2 Build 19148
  GenDepex.exe Version 0.04 Build 19775
  GenFds.exe 1.0 Build 19775
  GenFfs Version 0.1 Build 19148
  GenFv Version 0.1 Build 19610
 *GenFw Version 0.2 Build 19857
  GenPage Version 0.2 Build 19148
  GenPatchPcdTable.exe Version 0.10 Build 19775
  GenSec Version 0.1 Build 19148
  GenVtf Version 0.1 Build 19775
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 19775
  LzmaF86Compress Version 0.2 Build 19775
  PatchPcdValue.exe Version 0.10 Build 19775
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
 *Split Version 1.0 Build Build 19857
  TargetTool.exe Version 0.01 Build 19775
  TianoCompress Version 0.1 Build 19148
  Trim.exe Version 0.10 Build 19775
 *UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 19857
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 19857
 *VolInfo Version 1.0 Build Build 19857
  build.exe Version 0.60 Build 19775

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/17/2016 1:36:09PM Engine version = 5700.7163
  2/17/2016 1:36:09PM AntiVirus DAT version = 8077.0
  2/17/2016 1:36:09PM Number of detection signatures in EXTRA.DAT = None
  2/17/2016 1:36:09PM Names of detection signatures in EXTRA.DAT = None
  2/17/2016 1:36:09PM Scan Started On-Demand Scan
  2/17/2016 1:36:22PM Scan Summary
  2/17/2016 1:36:22PM Processes scanned : 0
  2/17/2016 1:36:22PM Processes detected : 0
  2/17/2016 1:36:22PM Processes cleaned : 0
  2/17/2016 1:36:22PM Boot sectors scanned : 1
  2/17/2016 1:36:22PM Boot sectors detected: 0
  2/17/2016 1:36:22PM Boot sectors cleaned : 0
  2/17/2016 1:36:22PM Files scanned : 61
  2/17/2016 1:36:22PM Files with detections: 0
  2/17/2016 1:36:22PM File detections : 0
  2/17/2016 1:36:22PM Files cleaned : 0
  2/17/2016 1:36:22PM Files deleted : 0
  2/17/2016 1:36:22PM Files not scanned : 0
  2/17/2016 1:36:22PM Scan Summary (Registry Scanning)
  2/17/2016 1:36:22PM Keys scanned : 0
  2/17/2016 1:36:22PM Keys detected : 0
  2/17/2016 1:36:22PM Keys cleaned : 0
  2/17/2016 1:36:22PM Keys deleted : 0
  2/17/2016 1:36:22PM Run time : 0:00:14
  2/17/2016 1:36:22PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 19775:HEAD Source
------------------------------------------------------------------------  r19835 | edk2buildsystem | 2016-02-16 09:40:04 -0800 (Tue, 16 Feb 2016) | 17 lines
  BaseTools/GenFw AARCH64: add support for relative data relocations
  This adds support to the ELF to PE/COFF conversion performed by GenFw for
  the AArch64 ELF relocation types R_AARCH64_PREL64, R_AARCH64_PREL32 and
  R_AARCH64_PREL16. Since we already require the ELF and PE/COFF section
  layouts to be identical in order to support other relative relocation
  types, this is simply a matter of whitelisting these new relocation types
  in the same way.
  While we're at it, clean up the code a bit, and add a comment explaining
  why these relocations are ignored in WriteRelocations64 ().
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Leif Lindholm <leif.lindholm@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 0b6249f5902f85a9c1a438878b27f8d7ef960a41)

------------------------------------------------------------------------  r19841 | edk2buildsystem | 2016-02-16 09:41:15 -0800 (Tue, 16 Feb 2016) | 13 lines
  BaseTools-Source: Update displayed version information
  Standardize the --version and --help text command-line options
  Updated tools to correctly display the Build number when using command-line
  option --version and exit successfully after termination.
  Ecc was also updated to print informational messages after the options are
  parsed.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Larry Hauch <larry.hauch@intel.com>
  Reviewed-by: Erik Bjorge <erik.c.bjorge@intel.com>
  (cherry picked from commit fbf2338143952da2c63241e51379504a15aa3ea9)

------------------------------------------------------------------------  r19855 | jljusten | 2016-02-17 10:34:12 -0800 (Wed, 17 Feb 2016) | 12 lines
  BaseTools/GenFw: Exit with error when header lookup fails
  This patch revises GetPhdrByIndex and GetShdrByIndex to cause GenFw to
  exit with an error message when a section header lookup fails.  The
  current behavior of those functions in such circumstances is to return
  NULL, which can cause GenFw to subsequently fault when it attempts to
  dereference the null pointer.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Michael LeMay <michael.lemay@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 17751c5fa473fd4f830007590d59e8d15a2d2935)

------------------------------------------------------------------------  r19856 | jljusten | 2016-02-17 10:34:16 -0800 (Wed, 17 Feb 2016) | 20 lines
  BaseTools/GenFw: Enhance error message for bad symbol definitions
  This patch expands the error message that is output when GenFw
  encounters a bad symbol definition or an unsupported symbol type.  It
  displays the symbol name, the symbol address, and a message that
  describes both possibilities (bad symbol definition or unsupported
  symbol type).  It also provides two examples of unsupported symbol
  types.
  Furthermore, this patch revises the conditional for detecting bad
  symbol definitions to eliminate a redundant test (a Sym->st_shndx
  value of SHN_ABS should certainly be greater than mEhdr->e_shnum) and
  to change another test from 'Sym->st_shndx > mEhdr->e_shnum' to
  'Sym->st_shndx >= mEhdr->e_shnum' for consistency with the test in
  GetShdrByIndex.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Michael LeMay <michael.lemay@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 621bb723a4e00cb93e8a94c6126de4976dde1d9e)

------------------------------------------------------------------------  r19857 | jljusten | 2016-02-17 10:34:22 -0800 (Wed, 17 Feb 2016) | 13 lines
  BaseTools/GenFw: Correct datatypes in diagnostic messages and check for string termination
  This patch revises multiple diagnostic messages to use correct
  datatypes.  It also checks that a symbol name that is about to be used
  in a diagnostic message is terminated by a null character within the
  contents of the string table section so that the print routine does
  not read past the end of the string table section contents when
  reading the symbol name.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Michael LeMay <michael.lemay@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ea3e924a0c91e2dd7fbb5e2f79899367222f27eb)

------------------------------------------------------------------------