Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20651

This directory contains the Win32 binaries.

Build Date:       Tue, 26 Apr 2016 03:11:12 Pacific Daylight Time
Last Changed Rev: 20643

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20615
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
  GenDepex.exe Version 0.04 Build 20615
  GenFds.exe 1.0 Build 20615
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 20600
  GenPage Version 0.2 Build 19914
  GenPatchPcdTable.exe Version 0.10 Build 20615
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
  PatchPcdValue.exe Version 0.10 Build 20615
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20182
  TargetTool.exe Version 0.01 Build 20615
  TianoCompress Version 0.1 Build 19914
  Trim.exe Version 0.10 Build 20615
 *UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20600
  build.exe Version 0.60 Build 20615

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/26/2016 3:11:13AM Engine version = 5700.7163
  4/26/2016 3:11:13AM AntiVirus DAT version = 8146.0
  4/26/2016 3:11:13AM Number of detection signatures in EXTRA.DAT = None
  4/26/2016 3:11:13AM Names of detection signatures in EXTRA.DAT = None
  4/26/2016 3:11:13AM Scan Started On-Demand Scan
  4/26/2016 3:11:16AM Scan Summary
  4/26/2016 3:11:16AM Processes scanned : 0
  4/26/2016 3:11:16AM Processes detected : 0
  4/26/2016 3:11:16AM Processes cleaned : 0
  4/26/2016 3:11:16AM Boot sectors scanned : 1
  4/26/2016 3:11:16AM Boot sectors detected: 0
  4/26/2016 3:11:16AM Boot sectors cleaned : 0
  4/26/2016 3:11:16AM Files scanned : 55
  4/26/2016 3:11:16AM Files with detections: 0
  4/26/2016 3:11:16AM File detections : 0
  4/26/2016 3:11:16AM Files cleaned : 0
  4/26/2016 3:11:16AM Files deleted : 0
  4/26/2016 3:11:16AM Files not scanned : 0
  4/26/2016 3:11:16AM Scan Summary (Registry Scanning)
  4/26/2016 3:11:16AM Keys scanned : 0
  4/26/2016 3:11:16AM Keys detected : 0
  4/26/2016 3:11:16AM Keys cleaned : 0
  4/26/2016 3:11:16AM Keys deleted : 0
  4/26/2016 3:11:16AM Run time : 0:00:03
  4/26/2016 3:11:16AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20615:HEAD Source
------------------------------------------------------------------------  r20615 | edk2buildsystem | 2016-04-20 02:05:36 -0700 (Wed, 20 Apr 2016) | 10 lines
  BaseTools: add the support for --pcd feature to patch the binary efi
  the original --pcd feature can override the Pcd value when build the
  source driver, while it missed the binary driver. this patch add the
  support to patch the binary efi for --pcd feature.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 6b17c11b6f45b4196adb8a9fcbdba5576a0d872b)

------------------------------------------------------------------------  r20641 | edk2buildsystem | 2016-04-26 02:05:36 -0700 (Tue, 26 Apr 2016) | 6 lines
  Update ECC to support more doxygen keywords
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit f8895c2ad4fe0191732aa376333eaf49649e3760)

------------------------------------------------------------------------  r20642 | edk2buildsystem | 2016-04-26 02:05:41 -0700 (Tue, 26 Apr 2016) | 6 lines
  BaseTools/ECC: Remove UNI checkpoint from ECC
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b739e14d7fbfce5b58411bf214a33bbcb7cf4102)

------------------------------------------------------------------------  r20643 | edk2buildsystem | 2016-04-26 02:05:46 -0700 (Tue, 26 Apr 2016) | 6 lines
  BaseTools/UPT: UPT to Support UTF-8
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4a21fb3b67a0ef1655b43e9368b6b697bbf327af)

------------------------------------------------------------------------