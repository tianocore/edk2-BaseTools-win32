Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22465

This directory contains the Win32 binaries.

Build Date:       Tue, 23 Aug 2016 03:11:02 Pacific Daylight Time
Last Changed Rev: 22463

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
 *GenFds.exe 1.0 Build 22465
  GenFfs Version 0.1 Build 22449
  GenFv Version 0.1 Build 22449
  GenFw Version 0.2 Build 22449
  GenPage Version 0.2 Build 22449
  GenPatchPcdTable.exe Version 0.10 Build 22444
  GenSec Version 0.1 Build 22449
  GenVtf Version 0.1 Build 22449
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 22449
  LzmaF86Compress Version 0.2 Build 22449
  PatchPcdValue.exe Version 0.10 Build 22444
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
  8/23/2016 3:11:03AM Engine version = 5700.7163
  8/23/2016 3:11:03AM AntiVirus DAT version = 8265.0
  8/23/2016 3:11:03AM Number of detection signatures in EXTRA.DAT = None
  8/23/2016 3:11:03AM Names of detection signatures in EXTRA.DAT = None
  8/23/2016 3:11:03AM Scan Started On-Demand Scan
  8/23/2016 3:11:05AM Scan Summary
  8/23/2016 3:11:05AM Processes scanned : 0
  8/23/2016 3:11:05AM Processes detected : 0
  8/23/2016 3:11:05AM Processes cleaned : 0
  8/23/2016 3:11:05AM Boot sectors scanned : 1
  8/23/2016 3:11:05AM Boot sectors detected: 0
  8/23/2016 3:11:05AM Boot sectors cleaned : 0
  8/23/2016 3:11:05AM Files scanned : 62
  8/23/2016 3:11:05AM Files with detections: 0
  8/23/2016 3:11:05AM File detections : 0
  8/23/2016 3:11:05AM Files cleaned : 0
  8/23/2016 3:11:05AM Files deleted : 0
  8/23/2016 3:11:05AM Files not scanned : 0
  8/23/2016 3:11:05AM Scan Summary (Registry Scanning)
  8/23/2016 3:11:05AM Keys scanned : 0
  8/23/2016 3:11:05AM Keys detected : 0
  8/23/2016 3:11:05AM Keys cleaned : 0
  8/23/2016 3:11:05AM Keys deleted : 0
  8/23/2016 3:11:05AM Run time : 0:00:02
  8/23/2016 3:11:05AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22449:HEAD Source
------------------------------------------------------------------------  r22449 | edk2buildsystem | 2016-08-22 02:05:54 -0700 (Mon, 22 Aug 2016) | 15 lines
  BaseTools PeCoffLib: Fix the issue to get RelocationsStripped from TE image
  If PE image has no relocation section, and has not set RELOCS_STRIPPED,
  after it is converted to TE image, GenFw will set its relocation section
  VirtualAddress to non-zero address, and keep Size value as Zero. MdePkg
  BasePeCoffLib applied this rule to get RelocationsStripped attribute. But,
  it is missing in BaseTools BasePeCoffLib.
  Cc: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Tested-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  (cherry picked from commit 8866d337ea9eba258e942585b172d57d39376e70)

------------------------------------------------------------------------  r22459 | edk2buildsystem | 2016-08-23 02:06:08 -0700 (Tue, 23 Aug 2016) | 10 lines
  BaseTools: add capsule image header for auth FMP capsule file
  in last commit 91ae29, it missed to add the
  EFI_FIRMWARE_MANAGEMENT_CAPSULE_IMAGE_HEADER for the auth FMP capsule.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a07901418affc8d357ad319c6dec993cc00d6915)

------------------------------------------------------------------------  r22460 | edk2buildsystem | 2016-08-23 02:06:13 -0700 (Tue, 23 Aug 2016) | 11 lines
  BaseTools: update BinaryFiles.txt file to add Pkcs7Sign Tool
  add Pkcs7Sign.exe and related pem file into BinaryFiles.txt for build
  server to automatically build the binary win32 files.
  Cc: Liming Gao <liming.gao@intel.com>
  CC: Erik Bjorge <erik.c.bjorge@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Erik Bjorge <erik.c.bjorge@intel.com>
  (cherry picked from commit 759be99db5d0d4d5b2eb73e110c701e83bdee7ab)

------------------------------------------------------------------------  r22462 | edk2buildsystem | 2016-08-23 02:06:23 -0700 (Tue, 23 Aug 2016) | 9 lines
  BaseTools GNU Makefile: Add the missing rules for cpp source file
  Cc: Giri P Mudusuru <giri.p.mudusuru@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Giri P Mudusuru <giri.p.mudusuru@intel.com>
  (cherry picked from commit 00588512dc05929ff5a9a52830724bee16f72c40)

------------------------------------------------------------------------  r22463 | edk2buildsystem | 2016-08-23 02:06:28 -0700 (Tue, 23 Aug 2016) | 11 lines
  BaseTools GnuMakefile: Update GCC Flags to the specific one with BUILD_ prefix
  To avoid the conflict with the default GCC flag name, BUILD_ prefix is added.
  Cc: Giri P Mudusuru <giri.p.mudusuru@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Giri P Mudusuru <giri.p.mudusuru@intel.com>
  (cherry picked from commit a61331e8b78ba264f0ccd011b6dc5b9e809730a5)

------------------------------------------------------------------------