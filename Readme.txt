Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25090

This directory contains the Win32 binaries.

Build Date:       Sat, 12 Aug 2017 03:13:20 Pacific Daylight Time
Last Changed Rev: 25090

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25090
 *BootSectImage Version 1.0 Build Build 25090
 *Brotli Version 0.5.2 Build 25090
  Brotli Version 0.5.2 Build 25090
  Ecc.exe Version 1.0 Build Build 24602
 *EfiLdrImage Version 1.0 Build Build 25090
 *EfiRom Version 0.1 Build 25090
 *GenBootSector Version 0.2 Build 25090
 *GenCrc32 Version 0.2 Build 25090
 *GenDepex.exe Version 0.04 Build 25090
 *GenFds.exe 1.0 Build 25090
 *GenFfs Version 0.1 Build 25090
 *GenFv Version 0.1 Build 25090
 *GenFw Version 0.2 Build 25090
 *GenPage Version 0.2 Build 25090
 *GenPatchPcdTable.exe Version 0.10 Build 25090
 *GenSec Version 0.1 Build 25090
 *GenVtf Version 0.1 Build 25090
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 25090
  LzmaF86Compress Version 0.2 Build 25090
 *PatchPcdValue.exe Version 0.10 Build 25090
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
 *Split Version 1.0 Build Build 25090
 *TargetTool.exe Version 0.01 Build 25090
 *TianoCompress Version 0.1 Build 25090
 *Trim.exe Version 0.10 Build 25090
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 24289
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 25090
 *VolInfo Version 1.0 Build Build 25090
 *build.exe Version 0.60 Build 25090

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/12/2017 3:13:22AM Engine version = 5800.7501
  8/12/2017 3:13:22AM AntiVirus DAT version = 8619.0
  8/12/2017 3:13:22AM Number of detection signatures in EXTRA.DAT = None
  8/12/2017 3:13:22AM Names of detection signatures in EXTRA.DAT = None
  8/12/2017 3:13:23AM Scan Started On-Demand Scan
  8/12/2017 3:14:08AM Scan Summary
  8/12/2017 3:14:08AM Processes scanned : 0
  8/12/2017 3:14:08AM Processes detected : 0
  8/12/2017 3:14:08AM Processes cleaned : 0
  8/12/2017 3:14:08AM Boot sectors scanned : 2
  8/12/2017 3:14:08AM Boot sectors detected: 0
  8/12/2017 3:14:08AM Boot sectors cleaned : 0
  8/12/2017 3:14:08AM Files scanned : 81
  8/12/2017 3:14:08AM Files with detections: 0
  8/12/2017 3:14:08AM File detections : 0
  8/12/2017 3:14:08AM Files cleaned : 0
  8/12/2017 3:14:08AM Files deleted : 0
  8/12/2017 3:14:08AM Files not scanned : 0
  8/12/2017 3:14:08AM Scan Summary (Registry Scanning)
  8/12/2017 3:14:08AM Keys scanned : 0
  8/12/2017 3:14:08AM Keys detected : 0
  8/12/2017 3:14:08AM Keys cleaned : 0
  8/12/2017 3:14:08AM Keys deleted : 0
  8/12/2017 3:14:08AM Run time : 0:00:46
  8/12/2017 3:14:08AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25038:HEAD Source
------------------------------------------------------------------------  r25076 | edk2buildsystem | 2017-08-11 14:05:33 -0700 (Fri, 11 Aug 2017) | 10 lines
  BaseTools: Fix Xcode 9 Beta treating 32-bit left shift as undefined
  Bug: https://bugzilla.tianocore.org/show_bug.cgi?id=635
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Michael D Kinney <michael.d.kinney@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Andrew Fish <afish@apple.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 59bc913c10a2296b0c5c83e4024c8b91000c8c8c)

------------------------------------------------------------------------  r25086 | edk2buildsystem | 2017-08-11 14:06:24 -0700 (Fri, 11 Aug 2017) | 23 lines
  BaseTools/build: Expand PREBUILD/POSTBUILD DSC actions
  https://bugzilla.tianocore.org/show_bug.cgi?id=670
  * Extend PREBUILD/POSTBUILD define values to support more than
  one argument.
  * Delay normalization of PREBUILD/POSTBUILD define values
  until all arguments in the define values can be processed.
  * Convert PREBUILD/POSTBUILD build define value arguments
  that are WORKSPACE or PACKAGES_PATH relative paths to
  absolute paths.
  * Append -p PlatformFile, --conf=ConfDirectory, and build target
  flags to command line used to execute PREBUILD/POSTBUILD
  actions.
  * Remove PrebuildScript and PostbuildScript fields from the
  Build class and use Prebuild and Postbuild fields instead.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Michael Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit af9c4e5e67ab12a77434564ff61c124ef0e5b5dd)

------------------------------------------------------------------------  r25089 | edk2buildsystem | 2017-08-12 02:05:29 -0700 (Sat, 12 Aug 2017) | 9 lines
  BaseTools/UPT: Support Multiple Installation
  Add a new feature to UPT to support installing
  multiple DIST packages in one time.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 566368148c014702f98d6c37a3934b1c1e60dfd4)

------------------------------------------------------------------------  r25090 | edk2buildsystem | 2017-08-12 02:05:36 -0700 (Sat, 12 Aug 2017) | 11 lines
  BaseTools: Don't need to add extra quotes when UI string from file
  when the UI string is read from files, we don't need to add the extra
  quotes. Otherwise, it will cause UI name has this extra quotes.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Bin Wang <binx.a.wang@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1e892df6860dc655f8e570450d74791b84de9928)

------------------------------------------------------------------------