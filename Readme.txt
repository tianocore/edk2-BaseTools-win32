Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17419

This directory contains the Win32 binaries.

Build Date:       Tue, 12 May 2015 03:07:04 Pacific Daylight Time
Last Changed Rev: 17416

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17419
  BootSectImage Version 0.1 Build 17385
  Ecc.exe Version 0.01 Build 17164
  EfiLdrImage Version 0.1 Build 17385
  EfiRom Version 0.1 Build 17385
  GenBootSector Version 0.2 Build 17385
  GenCrc32 Version 0.2 Build 17385
 *GenDepex.exe Version 0.04 Build 17419
 *GenFds.exe 1.0 Build 17419
  GenFfs Version 0.1 Build 17385
  GenFv Version 0.1 Build 17385
  GenFw Version 0.2 Build 17385
  GenPage Version 0.2 Build 17385
 *GenPatchPcdTable.exe Version 0.10 Build 17419
  GenSec Version 0.1 Build 17385
  GenVtf Version 0.1 Build 17385
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 17385
  LzmaF86Compress Version 0.2 Build 17385
 *PatchPcdValue.exe Version 0.10 Build 17419
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17164
  Rsa2048Sha256Sign Version 0.9 Build 17164
  Split Version 0.1 Build 17385
 *TargetTool.exe Version 0.01 Build 17419
  TianoCompress Version 0.1 Build 17385
 *Trim.exe Version 0.10 Build 17419
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 17164
  VfrCompile version  2.00 (UEFI 2.4) Build 17385
  VolInfo Version 0.83 Build 17385, May  9 2015
 *build.exe Version 0.60 Build 17419

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1263
  5/12/2015 3:07:06AM Engine version = 5700.7163
  5/12/2015 3:07:06AM AntiVirus DAT version = 7798.0
  5/12/2015 3:07:06AM Number of detection signatures in EXTRA.DAT = None
  5/12/2015 3:07:06AM Names of detection signatures in EXTRA.DAT = None
  5/12/2015 3:07:07AM Scan Started On-Demand Scan
  5/12/2015 3:07:58AM Scan Summary
  5/12/2015 3:07:58AM Processes scanned : 0
  5/12/2015 3:07:58AM Processes detected : 0
  5/12/2015 3:07:58AM Processes cleaned : 0
  5/12/2015 3:07:58AM Boot sectors scanned : 1
  5/12/2015 3:07:58AM Boot sectors detected: 0
  5/12/2015 3:07:58AM Boot sectors cleaned : 0
  5/12/2015 3:07:58AM Files scanned : 56
  5/12/2015 3:07:58AM Files with detections: 0
  5/12/2015 3:07:58AM File detections : 0
  5/12/2015 3:07:58AM Files cleaned : 0
  5/12/2015 3:07:58AM Files deleted : 0
  5/12/2015 3:07:58AM Files not scanned : 0
  5/12/2015 3:07:58AM Scan Summary (Registry Scanning)
  5/12/2015 3:07:58AM Keys scanned : 0
  5/12/2015 3:07:58AM Keys detected : 0
  5/12/2015 3:07:58AM Keys cleaned : 0
  5/12/2015 3:07:58AM Keys deleted : 0
  5/12/2015 3:07:58AM Run time : 0:00:53
  5/12/2015 3:07:58AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17385:HEAD Source
------------------------------------------------------------------------  r17416 | bobfeng | 2015-05-11 17:58:20 -0700 (Mon, 11 May 2015) | 8 lines
  BaseTools/Build: The PCD value in uninitialized data range should be natural aligned.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: "Bob Feng" <bob.c.feng@intel.com>
  Reviewed-by: "Liu, Yingke D" <yingke.d.liu@intel.com>
  Tested-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>

------------------------------------------------------------------------