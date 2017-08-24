Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25145

This directory contains the Win32 binaries.

Build Date:       Thu, 24 Aug 2017 03:11:48 Pacific Daylight Time
Last Changed Rev: 25145

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25091
  BootSectImage Version 1.0 Build Build 25090
  Brotli Version 0.5.2 Build 25090
  Brotli Version 0.5.2 Build 25090
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25090
  EfiRom Version 0.1 Build 25090
  GenBootSector Version 0.2 Build 25090
  GenCrc32 Version 0.2 Build 25090
  GenDepex.exe Version 0.04 Build 25091
  GenFds.exe 1.0 Build 25091
  GenFfs Version 0.1 Build 25090
  GenFv Version 0.1 Build 25090
 *GenFw Version 0.2 Build 25145
  GenPage Version 0.2 Build 25090
  GenPatchPcdTable.exe Version 0.10 Build 25091
  GenSec Version 0.1 Build 25090
  GenVtf Version 0.1 Build 25090
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25090
  LzmaF86Compress Version 0.2 Build 25090
  PatchPcdValue.exe Version 0.10 Build 25091
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25090
  TargetTool.exe Version 0.01 Build 25091
  TianoCompress Version 0.1 Build 25090
  Trim.exe Version 0.10 Build 25091
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25102
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25090
  VolInfo Version 1.0 Build Build 25090
  build.exe Version 0.60 Build 25091

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/24/2017 3:11:50AM Engine version = 5800.7501
  8/24/2017 3:11:50AM AntiVirus DAT version = 8632.0
  8/24/2017 3:11:50AM Number of detection signatures in EXTRA.DAT = None
  8/24/2017 3:11:50AM Names of detection signatures in EXTRA.DAT = None
  8/24/2017 3:11:50AM Scan Started On-Demand Scan
  8/24/2017 3:12:03AM Scan Summary
  8/24/2017 3:12:03AM Processes scanned : 0
  8/24/2017 3:12:03AM Processes detected : 0
  8/24/2017 3:12:03AM Processes cleaned : 0
  8/24/2017 3:12:03AM Boot sectors scanned : 2
  8/24/2017 3:12:03AM Boot sectors detected: 0
  8/24/2017 3:12:03AM Boot sectors cleaned : 0
  8/24/2017 3:12:03AM Files scanned : 64
  8/24/2017 3:12:03AM Files with detections: 0
  8/24/2017 3:12:03AM File detections : 0
  8/24/2017 3:12:03AM Files cleaned : 0
  8/24/2017 3:12:03AM Files deleted : 0
  8/24/2017 3:12:03AM Files not scanned : 0
  8/24/2017 3:12:03AM Scan Summary (Registry Scanning)
  8/24/2017 3:12:03AM Keys scanned : 0
  8/24/2017 3:12:03AM Keys detected : 0
  8/24/2017 3:12:03AM Keys cleaned : 0
  8/24/2017 3:12:03AM Keys deleted : 0
  8/24/2017 3:12:03AM Run time : 0:00:14
  8/24/2017 3:12:03AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25102:HEAD Source
------------------------------------------------------------------------  r25145 | edk2buildsystem | 2017-08-24 02:05:24 -0700 (Thu, 24 Aug 2017) | 13 lines
  BaseTools: Roll back GenFw Change to keep unknown field in RSDS debug entry
  https://lists.01.org/pipermail/edk2-devel/2017-August/013488.html
  These fields are actually a GUID and DWORD respectively: the GUID identifies
  the PDB to make it possible to verify that a given PDB matches the PE file,
  and the DWORD is the "age" of the PDB which is simply a helper value that is
  incremented by 1 by the linker every time the file is remade. Wiping the
  GUID will cause PDB parsers (such as the MS DIA SDK that IDA and most other
  tools use) to treat the PDB as a mismatch and refuse to load it.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 279c01ce13739f0fd8ec3e7652299f6873fc14a9)

------------------------------------------------------------------------