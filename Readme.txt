Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18198

This directory contains the Win32 binaries.

Build Date:       Mon, 10 Aug 2015 03:17:58 Pacific Daylight Time
Last Changed Rev: 18197

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18094
  BootSectImage Version 0.1 Build 18094
  Ecc.exe Version 0.01 Build 17712
  EfiLdrImage Version 0.1 Build 18094
  EfiRom Version 0.1 Build 18094
  GenBootSector Version 0.2 Build 18094
  GenCrc32 Version 0.2 Build 18094
  GenDepex.exe Version 0.04 Build 18094
  GenFds.exe 1.0 Build 18094
  GenFfs Version 0.1 Build 18094
  GenFv Version 0.1 Build 18094
 *GenFw Version 0.2 Build 18198
  GenPage Version 0.2 Build 18094
  GenPatchPcdTable.exe Version 0.10 Build 18094
  GenSec Version 0.1 Build 18094
  GenVtf Version 0.1 Build 18094
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 18094
  LzmaF86Compress Version 0.2 Build 18094
  PatchPcdValue.exe Version 0.10 Build 18094
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 18094
  TargetTool.exe Version 0.01 Build 18094
  TianoCompress Version 0.1 Build 18094
  Trim.exe Version 0.10 Build 18182
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17927
  VfrCompile version  2.00 (UEFI 2.4) Build 18094
  VolInfo Version 0.83 Build 18094, Jul 28 2015
  build.exe Version 0.60 Build 18094

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/10/2015 3:17:59AM Engine version = 5700.7163
  8/10/2015 3:17:59AM AntiVirus DAT version = 7888.0
  8/10/2015 3:17:59AM Number of detection signatures in EXTRA.DAT = None
  8/10/2015 3:17:59AM Names of detection signatures in EXTRA.DAT = None
  8/10/2015 3:17:59AM Scan Started On-Demand Scan
  8/10/2015 3:18:17AM Scan Summary
  8/10/2015 3:18:17AM Processes scanned : 0
  8/10/2015 3:18:17AM Processes detected : 0
  8/10/2015 3:18:17AM Processes cleaned : 0
  8/10/2015 3:18:17AM Boot sectors scanned : 2
  8/10/2015 3:18:17AM Boot sectors detected: 0
  8/10/2015 3:18:17AM Boot sectors cleaned : 0
  8/10/2015 3:18:17AM Files scanned : 55
  8/10/2015 3:18:17AM Files with detections: 0
  8/10/2015 3:18:17AM File detections : 0
  8/10/2015 3:18:17AM Files cleaned : 0
  8/10/2015 3:18:17AM Files deleted : 0
  8/10/2015 3:18:17AM Files not scanned : 0
  8/10/2015 3:18:17AM Scan Summary (Registry Scanning)
  8/10/2015 3:18:17AM Keys scanned : 0
  8/10/2015 3:18:17AM Keys detected : 0
  8/10/2015 3:18:17AM Keys cleaned : 0
  8/10/2015 3:18:17AM Keys deleted : 0
  8/10/2015 3:18:17AM Run time : 0:00:18
  8/10/2015 3:18:17AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18182:HEAD Source
------------------------------------------------------------------------  r18197 | abiesheuvel | 2015-08-10 00:55:18 -0700 (Mon, 10 Aug 2015) | 21 lines
  BaseTools/GenFw: allow AArch64 tiny and small code model relocations
  The AArch64 small C model makes extensive use of ADRP/ADD and
  ADRP/{LDR,STR} pairs to emit PC-relative symbol references with
  a +/- 4 GB range. Since the relocation pair splits the relative
  offset into a relative page offset and an absolute offset into
  a 4 KB page, we need to take extra care to ensure that the target
  of the relocation preserves its alignment relative to a 4 KB
  alignment boundary.
  Also, due to a problem with the --emit-relocs GNU ld option, where
  it does not recalculate the addends for section relative relocations,
  the only way to guarantee correct code is by requiring the relative
  section offset to be equal in the ELF and PE/COFF versions of the
  binary. This affects both the 'tiny' and 'small' GCC code models.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Leif Lindholm <leif.lindholm@linaro.org>
  Tested-by: Leif Lindholm <leif.lindholm@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------