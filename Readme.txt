Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18444

This directory contains the Win32 binaries.

Build Date:       Fri, 11 Sep 2015 03:19:16 Pacific Daylight Time
Last Changed Rev: 18443

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
 *GenFw Version 0.2 Build 18444
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
  9/11/2015 3:19:17AM Engine version = 5700.7163
  9/11/2015 3:19:17AM AntiVirus DAT version = 7920.0
  9/11/2015 3:19:17AM Number of detection signatures in EXTRA.DAT = 6
  9/11/2015 3:19:17AM Names of detection signatures in EXTRA.DAT = Generic BackDoor.u (ED) GenericR-ECJ (ED) RDN/Generic BackDoor (ED)
  9/11/2015 3:19:17AM Scan Started On-Demand Scan
  9/11/2015 3:19:22AM Scan Summary
  9/11/2015 3:19:22AM Processes scanned : 0
  9/11/2015 3:19:22AM Processes detected : 0
  9/11/2015 3:19:22AM Processes cleaned : 0
  9/11/2015 3:19:22AM Boot sectors scanned : 1
  9/11/2015 3:19:22AM Boot sectors detected: 0
  9/11/2015 3:19:22AM Boot sectors cleaned : 0
  9/11/2015 3:19:22AM Files scanned : 55
  9/11/2015 3:19:22AM Files with detections: 0
  9/11/2015 3:19:22AM File detections : 0
  9/11/2015 3:19:22AM Files cleaned : 0
  9/11/2015 3:19:22AM Files deleted : 0
  9/11/2015 3:19:22AM Files not scanned : 0
  9/11/2015 3:19:22AM Scan Summary (Registry Scanning)
  9/11/2015 3:19:22AM Keys scanned : 0
  9/11/2015 3:19:22AM Keys detected : 0
  9/11/2015 3:19:22AM Keys cleaned : 0
  9/11/2015 3:19:22AM Keys deleted : 0
  9/11/2015 3:19:22AM Run time : 0:00:05
  9/11/2015 3:19:22AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18361:HEAD Source
------------------------------------------------------------------------  r18443 | abiesheuvel | 2015-09-11 00:07:06 -0700 (Fri, 11 Sep 2015) | 11 lines
  BaseTools/GenFw: align RVA of debug
  SVN commit r18077 ("BaseTools/GenFw: move .debug contents to .data to
  save space") removed the separate .debug section after moving its
  contents into .text or .data. However, this change does not take into
  account that some of these contents need to appear at a 32-bit aligned
  offset. So align the debug data RVA to 32 bits.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------