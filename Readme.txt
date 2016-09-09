Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22617

This directory contains the Win32 binaries.

Build Date:       Fri, 09 Sep 2016 03:11:08 Pacific Daylight Time
Last Changed Rev: 22617

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
 *EfiRom Version 0.1 Build 22617
  GenBootSector Version 0.2 Build 22449
  GenCrc32 Version 0.2 Build 22449
  GenDepex.exe Version 0.04 Build 22444
  GenFds.exe 1.0 Build 22489
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
  9/9/2016 3:11:10AM Engine version = 5700.7163
  9/9/2016 3:11:10AM AntiVirus DAT version = 8282.0
  9/9/2016 3:11:10AM Number of detection signatures in EXTRA.DAT = 2
  9/9/2016 3:11:10AM Names of detection signatures in EXTRA.DAT = Generic.Tra!3c09cefe0e8d (ED) Generic.Tra!5876ae4f5bf5 (ED)
  9/9/2016 3:11:10AM Scan Started On-Demand Scan
  9/9/2016 3:11:19AM Scan Summary
  9/9/2016 3:11:19AM Processes scanned : 0
  9/9/2016 3:11:19AM Processes detected : 0
  9/9/2016 3:11:19AM Processes cleaned : 0
  9/9/2016 3:11:19AM Boot sectors scanned : 2
  9/9/2016 3:11:19AM Boot sectors detected: 0
  9/9/2016 3:11:19AM Boot sectors cleaned : 0
  9/9/2016 3:11:19AM Files scanned : 62
  9/9/2016 3:11:19AM Files with detections: 0
  9/9/2016 3:11:19AM File detections : 0
  9/9/2016 3:11:19AM Files cleaned : 0
  9/9/2016 3:11:19AM Files deleted : 0
  9/9/2016 3:11:19AM Files not scanned : 0
  9/9/2016 3:11:19AM Scan Summary (Registry Scanning)
  9/9/2016 3:11:19AM Keys scanned : 0
  9/9/2016 3:11:19AM Keys detected : 0
  9/9/2016 3:11:19AM Keys cleaned : 0
  9/9/2016 3:11:19AM Keys deleted : 0
  9/9/2016 3:11:19AM Run time : 0:00:10
  9/9/2016 3:11:19AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22543:HEAD Source
------------------------------------------------------------------------  r22543 | edk2buildsystem | 2016-09-04 02:05:28 -0700 (Sun, 04 Sep 2016) | 7 lines
  BaseTools: Change source files to DOS format
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 11eaa7affb8b325b3e00bbe9e4357705ce3b2b08)

------------------------------------------------------------------------  r22598 | edk2buildsystem | 2016-09-08 02:07:36 -0700 (Thu, 08 Sep 2016) | 13 lines
  BaseTools GNU makefile: Add BUILD_CXXFLAGS to align make built-in rule
  GNU make built-in rule to Compiling C++ programs with
  ‘$(CXX) $(CPPFLAGS) $(CXXFLAGS) -c’.
  To align to it, add empty BUILD_CXXFLAGS in cpp rule.
  Cc: Giri P Mudusuru <giri.p.mudusuru@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Giri P Mudusuru <giri.p.mudusuru@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a9355bb81ad43231c978431ecf0abbe5cfb3a1fa)

------------------------------------------------------------------------  r22599 | edk2buildsystem | 2016-09-08 02:07:40 -0700 (Thu, 08 Sep 2016) | 9 lines
  BaseTools GNU makefile: remove unused .S rule
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Giri P Mudusuru <giri.p.mudusuru@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Giri P Mudusuru <giri.p.mudusuru@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b15153451c7332532cfacd90d70942c7c03809f2)

------------------------------------------------------------------------  r22600 | edk2buildsystem | 2016-09-08 02:07:45 -0700 (Thu, 08 Sep 2016) | 11 lines
  BaseTools VfrCompile GNU makefile: Replace CXX with BUILD_CXX
  The change is missing in VfrComile GNUmakefile.
  Cc: Giri P Mudusuru <giri.p.mudusuru@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Giri P Mudusuru <giri.p.mudusuru@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit fa318476e442d7e77bf960af281a9bebe86ad59b)

------------------------------------------------------------------------  r22601 | edk2buildsystem | 2016-09-08 02:07:50 -0700 (Thu, 08 Sep 2016) | 13 lines
  BaseTools VfrCompile Pccts: Update GCC Flags to the specific one with BUILD_ prefix
  This change is also applied to VfrCompile Pccts antlr and dlg tool.
  In V2, add the missing C rules.
  Cc: Giri P Mudusuru <giri.p.mudusuru@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Giri P Mudusuru <giri.p.mudusuru@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4ac14ceae076439dcea926bc47cda4e1d2779cae)

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

------------------------------------------------------------------------