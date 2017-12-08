Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25855

This directory contains the Win32 binaries.

Build Date:       Fri, 08 Dec 2017 03:12:55 Pacific Standard Time
Last Changed Rev: 25855

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25818
 *BootSectImage Version 1.0 Build Build 25855
 *Brotli Version 0.5.2 Build 25855
  Brotli Version 0.5.2 Build 25855
  Ecc.exe Version 1.0 Build Build 24602
 *EfiLdrImage Version 1.0 Build Build 25855
 *EfiRom Version 0.1 Build 25855
 *GenBootSector Version 0.2 Build 25855
 *GenCrc32 Version 0.2 Build 25855
  GenDepex.exe Version 0.04 Build 25818
 *GenFds.exe 1.0 Build 25855
 *GenFfs Version 0.1 Build 25855
 *GenFv Version 0.1 Build 25855
 *GenFw Version 0.2 Build 25855
 *GenPage Version 0.2 Build 25855
  GenPatchPcdTable.exe Version 0.10 Build 25818
 *GenSec Version 0.1 Build 25855
 *GenVtf Version 0.1 Build 25855
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 25855
  LzmaF86Compress Version 0.2 Build 25855
  PatchPcdValue.exe Version 0.10 Build 25818
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
 *Split Version 1.0 Build Build 25855
  TargetTool.exe Version 0.01 Build 25818
 *TianoCompress Version 0.1 Build 25855
  Trim.exe Version 0.10 Build 25818
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 25855
 *VolInfo Version 1.0 Build Build 25855
 *build.exe Version 0.60 Build 25855

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/8/2017 3:12:56AM Engine version = 5900.7806
  12/8/2017 3:12:56AM AntiVirus DAT version = 8738.0
  12/8/2017 3:12:56AM Number of detection signatures in EXTRA.DAT = None
  12/8/2017 3:12:56AM Names of detection signatures in EXTRA.DAT = None
  12/8/2017 3:12:56AM Scan Started On-Demand Scan
  12/8/2017 3:13:05AM Scan Summary
  12/8/2017 3:13:05AM Processes scanned : 0
  12/8/2017 3:13:05AM Processes detected : 0
  12/8/2017 3:13:05AM Processes cleaned : 0
  12/8/2017 3:13:05AM Boot sectors scanned : 2
  12/8/2017 3:13:05AM Boot sectors detected: 0
  12/8/2017 3:13:05AM Boot sectors cleaned : 0
  12/8/2017 3:13:05AM Files scanned : 81
  12/8/2017 3:13:05AM Files with detections: 0
  12/8/2017 3:13:05AM File detections : 0
  12/8/2017 3:13:05AM Files cleaned : 0
  12/8/2017 3:13:05AM Files deleted : 0
  12/8/2017 3:13:05AM Files not scanned : 0
  12/8/2017 3:13:05AM Scan Summary (Registry Scanning)
  12/8/2017 3:13:05AM Keys scanned : 0
  12/8/2017 3:13:05AM Keys detected : 0
  12/8/2017 3:13:05AM Keys cleaned : 0
  12/8/2017 3:13:05AM Keys deleted : 0
  12/8/2017 3:13:05AM Run time : 0:00:09
  12/8/2017 3:13:05AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25825:HEAD Source
------------------------------------------------------------------------  r25832 | edk2buildsystem | 2017-12-08 02:05:50 -0800 (Fri, 08 Dec 2017) | 11 lines
  BaseTools: Fix GenSec can't found the depex file
  Filter the FileList when multiple genfds thread options is not enabled.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Tested-by: Leif Lindholm <leif.lindholm@linaro.org>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit cf245466a56a7be7405142753c6c6a6689b7461b)

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

------------------------------------------------------------------------