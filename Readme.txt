Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22444

This directory contains the Win32 binaries.

Build Date:       Fri, 19 Aug 2016 03:11:24 Pacific Daylight Time
Last Changed Rev: 22444

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22444
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
 *GenDepex.exe Version 0.04 Build 22444
 *GenFds.exe 1.0 Build 22444
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 22370
  GenFw Version 0.2 Build 22308
  GenPage Version 0.2 Build 20909
 *GenPatchPcdTable.exe Version 0.10 Build 22444
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
 *PatchPcdValue.exe Version 0.10 Build 22444
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
 *TargetTool.exe Version 0.01 Build 22444
  TianoCompress Version 0.1 Build 20909
 *Trim.exe Version 0.10 Build 22444
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22316
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22367
  VolInfo Version 1.0 Build Build 20909
 *build.exe Version 0.60 Build 22444

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/19/2016 3:11:25AM Engine version = 5700.7163
  8/19/2016 3:11:25AM AntiVirus DAT version = 8261.0
  8/19/2016 3:11:25AM Number of detection signatures in EXTRA.DAT = None
  8/19/2016 3:11:25AM Names of detection signatures in EXTRA.DAT = None
  8/19/2016 3:11:25AM Scan Started On-Demand Scan
  8/19/2016 3:11:34AM Scan Summary
  8/19/2016 3:11:34AM Processes scanned : 0
  8/19/2016 3:11:34AM Processes detected : 0
  8/19/2016 3:11:34AM Processes cleaned : 0
  8/19/2016 3:11:34AM Boot sectors scanned : 2
  8/19/2016 3:11:34AM Boot sectors detected: 0
  8/19/2016 3:11:34AM Boot sectors cleaned : 0
  8/19/2016 3:11:34AM Files scanned : 55
  8/19/2016 3:11:34AM Files with detections: 0
  8/19/2016 3:11:34AM File detections : 0
  8/19/2016 3:11:34AM Files cleaned : 0
  8/19/2016 3:11:34AM Files deleted : 0
  8/19/2016 3:11:34AM Files not scanned : 0
  8/19/2016 3:11:34AM Scan Summary (Registry Scanning)
  8/19/2016 3:11:34AM Keys scanned : 0
  8/19/2016 3:11:34AM Keys detected : 0
  8/19/2016 3:11:34AM Keys cleaned : 0
  8/19/2016 3:11:34AM Keys deleted : 0
  8/19/2016 3:11:34AM Run time : 0:00:09
  8/19/2016 3:11:34AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22370:HEAD Source
------------------------------------------------------------------------  r22436 | edk2buildsystem | 2016-08-19 02:05:53 -0700 (Fri, 19 Aug 2016) | 12 lines
  BaseTools: check CONF_PATH env to get the configure files
  Add CONF_PATH env check. First priority is user set the conf dir by
  --conf option, then the CONF_PATH env, the last one is the standard
  WORKSPACE(PACKAGE_PATH)/Conf.
  Also print the conf path directory in the build log.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 00bcb5c27a5bb781099482c5763937334be91e76)

------------------------------------------------------------------------  r22441 | edk2buildsystem | 2016-08-19 02:06:22 -0700 (Fri, 19 Aug 2016) | 11 lines
  BaseTools: Add the PKCS7 tool
  Provide the PKCS7 Tool to support the CertType - EFI_CERT_TYPE_PKCS7_GUID,
  then user can use this tool to add EFI_FIRMWARE_IMAGE_AUTHENTICATION
  for a binary.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Jiewen Yao <jiewen.yao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit cd1c96046968581cc87d306ca8b06cc97784554b)

------------------------------------------------------------------------  r22442 | edk2buildsystem | 2016-08-19 02:06:27 -0700 (Fri, 19 Aug 2016) | 11 lines
  BaseTools: Rsa2048Sha256Sign add new option to support Monotonic count
  the EFI_FIRMWARE_IMAGE_AUTHENTICATION struct require the AuthInfo which
  is a signature across the image data and the Monotonic Count value, so we
  add the new option to support Monotonic count.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9b98c4164013845ba80befd66fd38ce827a4c034)

------------------------------------------------------------------------  r22443 | edk2buildsystem | 2016-08-19 02:06:33 -0700 (Fri, 19 Aug 2016) | 13 lines
  BaseTools: FMP capsule add the support to generate auth info
  Current BaseTools cannot generate EFI_FIRMWARE_IMAGE_AUTHENTICATION
  for FMP capsule. this patch fix it by FDF spec's update to add the
  definition for CERTIFICATE_GUID and  MONOTONIC_COUNT. BaseTools call
  the tool by CERTIFICATE_GUID to generate the certdata and fill the header
  info.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 91ae2988c62f03987fe02159d26b001a5201d812)

------------------------------------------------------------------------  r22444 | edk2buildsystem | 2016-08-19 02:06:39 -0700 (Fri, 19 Aug 2016) | 13 lines
  BaseTools: Fix a bug use 'COMMON' as CodeBase in BuildOptions section
  Current BaseTools query the BuildOptions not cover the case that use
  'COMMON' as CodeBase, while DSC spec allow this usage. This Patch add
  support for such 'common.DXE_RUNTIME_DRIVER' as the Scope2 in the query
  Condition.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Kurt Kennett <Kurt.Kennett@microsoft.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 35dc964bf1eab3f0725389811d2316b1331d6cee)

------------------------------------------------------------------------