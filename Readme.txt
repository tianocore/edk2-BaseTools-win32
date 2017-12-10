Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25882

This directory contains the Win32 binaries.

Build Date:       Sun, 10 Dec 2017 03:12:42 Pacific Standard Time
Last Changed Rev: 25882

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25882
  BootSectImage Version 1.0 Build Build 25855
  Brotli Version 0.5.2 Build 25855
  Brotli Version 0.5.2 Build 25855
  Ecc.exe Version 1.0 Build Build 24602
  EfiLdrImage Version 1.0 Build Build 25855
  EfiRom Version 0.1 Build 25855
  GenBootSector Version 0.2 Build 25855
  GenCrc32 Version 0.2 Build 25855
 *GenDepex.exe Version 0.04 Build 25882
 *GenFds.exe 1.0 Build 25882
  GenFfs Version 0.1 Build 25855
  GenFv Version 0.1 Build 25855
  GenFw Version 0.2 Build 25855
  GenPage Version 0.2 Build 25855
 *GenPatchPcdTable.exe Version 0.10 Build 25882
  GenSec Version 0.1 Build 25855
  GenVtf Version 0.1 Build 25855
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 25855
  LzmaF86Compress Version 0.2 Build 25855
 *PatchPcdValue.exe Version 0.10 Build 25882
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
  Split Version 1.0 Build Build 25855
 *TargetTool.exe Version 0.01 Build 25882
  TianoCompress Version 0.1 Build 25855
 *Trim.exe Version 0.10 Build 25882
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
  VfrCompile version  2.01 (UEFI 2.4) Build Build 25855
  VolInfo Version 1.0 Build Build 25855
 *build.exe Version 0.60 Build 25882

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/10/2017 3:12:44AM Engine version = 5900.7806
  12/10/2017 3:12:44AM AntiVirus DAT version = 8740.0
  12/10/2017 3:12:44AM Number of detection signatures in EXTRA.DAT = None
  12/10/2017 3:12:44AM Names of detection signatures in EXTRA.DAT = None
  12/10/2017 3:12:44AM Scan Started On-Demand Scan
  12/10/2017 3:12:54AM Scan Summary
  12/10/2017 3:12:54AM Processes scanned : 0
  12/10/2017 3:12:54AM Processes detected : 0
  12/10/2017 3:12:54AM Processes cleaned : 0
  12/10/2017 3:12:54AM Boot sectors scanned : 2
  12/10/2017 3:12:54AM Boot sectors detected: 0
  12/10/2017 3:12:54AM Boot sectors cleaned : 0
  12/10/2017 3:12:54AM Files scanned : 64
  12/10/2017 3:12:54AM Files with detections: 0
  12/10/2017 3:12:54AM File detections : 0
  12/10/2017 3:12:54AM Files cleaned : 0
  12/10/2017 3:12:54AM Files deleted : 0
  12/10/2017 3:12:54AM Files not scanned : 0
  12/10/2017 3:12:54AM Scan Summary (Registry Scanning)
  12/10/2017 3:12:54AM Keys scanned : 0
  12/10/2017 3:12:54AM Keys detected : 0
  12/10/2017 3:12:54AM Keys cleaned : 0
  12/10/2017 3:12:54AM Keys deleted : 0
  12/10/2017 3:12:54AM Run time : 0:00:11
  12/10/2017 3:12:54AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25855:HEAD Source
------------------------------------------------------------------------  r25855 | edk2buildsystem | 2017-12-08 02:07:58 -0800 (Fri, 08 Dec 2017) | 24 lines
  BaseTools: align ERROR/WARNING/RETURN macros with MdePkg versions
  BaseTools' BaseTypes.h defined the ENCODE_ERROR macro as
  #define ENCODE_ERROR(a)              ((RETURN_STATUS)(MAX_BIT | (a)))
  whereas MdePkg defines it as
  #define ENCODE_ERROR(StatusCode)     ((RETURN_STATUS)(MAX_BIT | (StatusCode)))
  When building with GCC 6.3 (at least) the former triggers
  "error: overflow in implicit constant conversion [-Werror=overflow]"
  Resolve this by aligning it with the latter one.
  This also requires aligning the BaseTools typedef of RETURN_STATUS with
  the MdePkg one: INTN -> UINTN.
  While at it, update adjacent ENCODE_WARNING and RETURN_ERROR as well.
  Add an explicit initialization of *Alignment to 0 in GenFfs.c
  GetAlignmentFromFile to get rid of a warning occuring with GCC after
  this change (-Werror=maybe-uninitialized).
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Leif Lindholm <leif.lindholm@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 978779d7b50cc30cad64b79e24224efa3c6082dc)

------------------------------------------------------------------------  r25882 | edk2buildsystem | 2017-12-10 02:05:24 -0800 (Sun, 10 Dec 2017) | 10 lines
  BaseTools: Add object_files.lst as dependency of lib target
  Seems object_files.lst is not added as dependency of lib target, this
  patch update BaseTools to generate Makefile with this dependency.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1c62af9ec1086b9e3066b25bfd6bee6d03186c0f)

------------------------------------------------------------------------