Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22650

This directory contains the Win32 binaries.

Build Date:       Thu, 15 Sep 2016 03:11:01 Pacific Daylight Time
Last Changed Rev: 22650

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
  EfiRom Version 0.1 Build 22617
  GenBootSector Version 0.2 Build 22449
  GenCrc32 Version 0.2 Build 22449
  GenDepex.exe Version 0.04 Build 22444
 *GenFds.exe 1.0 Build 22650
  GenFfs Version 0.1 Build 22449
  GenFv Version 0.1 Build 22543
  GenFw Version 0.2 Build 22466
  GenPage Version 0.2 Build 22449
  GenPatchPcdTable.exe Version 0.10 Build 22444
  GenSec Version 0.1 Build 22449
  GenVtf Version 0.1 Build 22449
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 22449
  LzmaF86Compress Version 0.2 Build 22449
  PatchPcdValue.exe Version 0.10 Build 22444
  Pkcs7Sign Version 0.9 Build 22543
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
  9/15/2016 3:11:03AM Engine version = 5700.7163
  9/15/2016 3:11:03AM AntiVirus DAT version = 8288.0
  9/15/2016 3:11:03AM Number of detection signatures in EXTRA.DAT = 2
  9/15/2016 3:11:03AM Names of detection signatures in EXTRA.DAT = Generic.Tra!3c09cefe0e8d (ED) Generic.Tra!5876ae4f5bf5 (ED)
  9/15/2016 3:11:03AM Scan Started On-Demand Scan
  9/15/2016 3:11:06AM Scan Summary
  9/15/2016 3:11:06AM Processes scanned : 0
  9/15/2016 3:11:06AM Processes detected : 0
  9/15/2016 3:11:06AM Processes cleaned : 0
  9/15/2016 3:11:06AM Boot sectors scanned : 2
  9/15/2016 3:11:06AM Boot sectors detected: 0
  9/15/2016 3:11:06AM Boot sectors cleaned : 0
  9/15/2016 3:11:06AM Files scanned : 62
  9/15/2016 3:11:06AM Files with detections: 0
  9/15/2016 3:11:06AM File detections : 0
  9/15/2016 3:11:06AM Files cleaned : 0
  9/15/2016 3:11:06AM Files deleted : 0
  9/15/2016 3:11:06AM Files not scanned : 0
  9/15/2016 3:11:06AM Scan Summary (Registry Scanning)
  9/15/2016 3:11:06AM Keys scanned : 0
  9/15/2016 3:11:06AM Keys detected : 0
  9/15/2016 3:11:06AM Keys cleaned : 0
  9/15/2016 3:11:06AM Keys deleted : 0
  9/15/2016 3:11:06AM Run time : 0:00:04
  9/15/2016 3:11:06AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22617:HEAD Source
------------------------------------------------------------------------  r22617 | edk2buildsystem | 2016-09-09 02:05:32 -0700 (Fri, 09 Sep 2016) | 24 lines
  BaseTools/EfiRom: supply missing machine type lookup strings
  "EfiRom --dump" does not recognize the 0x8664 machine type:
  >   EFI ROM header contents
  >     EFI Signature          0x0EF1
  >     Compression Type       0x0001 (compressed)
  >     Machine type           0x8664 (unknown)
  >     Subsystem              0x000B (EFI boot service driver)
  >     EFI image offset       0x0050 (@0xF650)
  Add lookup strings for the remaining EFI_IMAGE_MACHINE_* numeric macros
  that can be found in
  "BaseTools/Source/C/Include/IndustryStandard/PeImage.h". The strings
  follow Table 12. "UEFI Image Types" from the UEFI v2.6 spec.
  Cc: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  (cherry picked from commit 2d41ea3aed4ea1935fc63df35b834e9626f896df)

------------------------------------------------------------------------  r22650 | edk2buildsystem | 2016-09-15 02:05:42 -0700 (Thu, 15 Sep 2016) | 11 lines
  BaseTools: Fix the bug to handle the read-only file
  change the 'r+b' to 'rb' for some file's open, since these files we only
  read it and no need to write. It can fix the bug that the file's attribute
  had been set to read-only.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f8db6527da8678f1480f08ba99b745279e8d104a)

------------------------------------------------------------------------