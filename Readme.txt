Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25171

This directory contains the Win32 binaries.

Build Date:       Sat, 26 Aug 2017 03:11:39 Pacific Daylight Time
Last Changed Rev: 25171

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
 *EfiRom Version 0.1 Build 25171
  GenBootSector Version 0.2 Build 25090
  GenCrc32 Version 0.2 Build 25090
  GenDepex.exe Version 0.04 Build 25091
  GenFds.exe 1.0 Build 25091
  GenFfs Version 0.1 Build 25090
  GenFv Version 0.1 Build 25090
  GenFw Version 0.2 Build 25145
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
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25090
  VolInfo Version 1.0 Build Build 25090
  build.exe Version 0.60 Build 25091

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/26/2017 3:11:41AM Engine version = 5900.7806
  8/26/2017 3:11:41AM AntiVirus DAT version = 8634.0
  8/26/2017 3:11:41AM Number of detection signatures in EXTRA.DAT = None
  8/26/2017 3:11:41AM Names of detection signatures in EXTRA.DAT = None
  8/26/2017 3:11:41AM Scan Started On-Demand Scan
  8/26/2017 3:12:02AM Scan Summary
  8/26/2017 3:12:02AM Processes scanned : 0
  8/26/2017 3:12:02AM Processes detected : 0
  8/26/2017 3:12:02AM Processes cleaned : 0
  8/26/2017 3:12:02AM Boot sectors scanned : 2
  8/26/2017 3:12:02AM Boot sectors detected: 0
  8/26/2017 3:12:02AM Boot sectors cleaned : 0
  8/26/2017 3:12:02AM Files scanned : 64
  8/26/2017 3:12:02AM Files with detections: 0
  8/26/2017 3:12:02AM File detections : 0
  8/26/2017 3:12:02AM Files cleaned : 0
  8/26/2017 3:12:02AM Files deleted : 0
  8/26/2017 3:12:02AM Files not scanned : 0
  8/26/2017 3:12:02AM Scan Summary (Registry Scanning)
  8/26/2017 3:12:02AM Keys scanned : 0
  8/26/2017 3:12:02AM Keys detected : 0
  8/26/2017 3:12:02AM Keys cleaned : 0
  8/26/2017 3:12:02AM Keys deleted : 0
  8/26/2017 3:12:02AM Run time : 0:00:22
  8/26/2017 3:12:02AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25166:HEAD Source
------------------------------------------------------------------------  r25171 | edk2buildsystem | 2017-08-26 02:05:23 -0700 (Sat, 26 Aug 2017) | 18 lines
  BaseTools/EfiRom: Add multiple device id support
  This is a patch to implement writing and dumping of PCI 3.0 Device ID
  lists in EFI option ROMs in the EfiRom tool.
  Using this modification, multiple space-delimited device IDs can be
  specified after -i.  The first device in the list is used for the main
  PCI ROM header Device ID field and is also written in the list.  The
  list is only written when more than one device ID has been specified;
  when only one device ID is given on the command line, the EfiRom output
  should be identical to the current code.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=666
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Tomas Pilar <tpilar@solarflare.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Daniel Verkamp <daniel.verkamp@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9f3a38cdfb354a5a074312783a43b7bd21cc90e2)

------------------------------------------------------------------------