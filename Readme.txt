Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23074

This directory contains the Win32 binaries.

Build Date:       Wed, 02 Nov 2016 03:11:21 Pacific Daylight Time
Last Changed Rev: 23071

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23074
  BootSectImage Version 1.0 Build Build 22854
  Ecc.exe Version 1.0 Build Build 22854
  EfiLdrImage Version 1.0 Build Build 22854
  EfiRom Version 0.1 Build 22854
  GenBootSector Version 0.2 Build 22854
  GenCrc32 Version 0.2 Build 22854
 *GenDepex.exe Version 0.04 Build 23074
 *GenFds.exe 1.0 Build 23074
  GenFfs Version 0.1 Build 22854
  GenFv Version 0.1 Build 22854
  GenFw Version 0.2 Build 22854
  GenPage Version 0.2 Build 22854
 *GenPatchPcdTable.exe Version 0.10 Build 23074
  GenSec Version 0.1 Build 22854
  GenVtf Version 0.1 Build 22854
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 22854
  LzmaF86Compress Version 0.2 Build 22854
 *PatchPcdValue.exe Version 0.10 Build 23074
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 22854
 *TargetTool.exe Version 0.01 Build 23074
  TianoCompress Version 0.1 Build 22854
 *Trim.exe Version 0.10 Build 23074
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22854
  VolInfo Version 1.0 Build Build 22854
 *build.exe Version 0.60 Build 23074

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/2/2016 3:11:22AM Engine version = 5700.7163
  11/2/2016 3:11:22AM AntiVirus DAT version = 8336.0
  11/2/2016 3:11:22AM Number of detection signatures in EXTRA.DAT = None
  11/2/2016 3:11:22AM Names of detection signatures in EXTRA.DAT = None
  11/2/2016 3:11:22AM Scan Started On-Demand Scan
  11/2/2016 3:11:25AM Scan Summary
  11/2/2016 3:11:25AM Processes scanned : 0
  11/2/2016 3:11:25AM Processes detected : 0
  11/2/2016 3:11:25AM Processes cleaned : 0
  11/2/2016 3:11:25AM Boot sectors scanned : 1
  11/2/2016 3:11:25AM Boot sectors detected: 0
  11/2/2016 3:11:25AM Boot sectors cleaned : 0
  11/2/2016 3:11:25AM Files scanned : 62
  11/2/2016 3:11:25AM Files with detections: 0
  11/2/2016 3:11:25AM File detections : 0
  11/2/2016 3:11:25AM Files cleaned : 0
  11/2/2016 3:11:25AM Files deleted : 0
  11/2/2016 3:11:25AM Files not scanned : 0
  11/2/2016 3:11:25AM Scan Summary (Registry Scanning)
  11/2/2016 3:11:25AM Keys scanned : 0
  11/2/2016 3:11:25AM Keys detected : 0
  11/2/2016 3:11:25AM Keys cleaned : 0
  11/2/2016 3:11:25AM Keys deleted : 0
  11/2/2016 3:11:25AM Run time : 0:00:03
  11/2/2016 3:11:25AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22854:HEAD Source
------------------------------------------------------------------------  r23069 | edk2buildsystem | 2016-11-02 02:05:56 -0700 (Wed, 02 Nov 2016) | 11 lines
  BaseTools: Fix the bug for OptionRom generation with different arch
  The GenFds tool uses the same output for the same module with the
  different arch, IA32 and X64 module will have the same output. The
  solution is add the arch info in the output directory.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 2a6402d490a2da818b7650ffe0330d3020e5b020)

------------------------------------------------------------------------  r23070 | edk2buildsystem | 2016-11-02 02:06:01 -0700 (Wed, 02 Nov 2016) | 12 lines
  BaseTools: Fix a bug for ExpandMacros to support mixed case ENV var
  os.environ contains all environment variables uppercase on Windows which
  cause the key in the self.MacroDictionary is uppercase, but the real
  variable name maybe mixed case, eg:WINSDK81x86, then we can't find the
  variable in the self.MacroDictionary.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 18ca2fec97010e8a79407ec092539218c04ee1c5)

------------------------------------------------------------------------  r23071 | edk2buildsystem | 2016-11-02 02:06:06 -0700 (Wed, 02 Nov 2016) | 11 lines
  BaseTools: Fix a bug for tooldef class not include the newly Env
  Prebuild script may update os.environ, but the tooldef class not include
  the new ENV variables. so after the Launch prebuild script, we should
  re-init the tooldef class to include the new ENV variables.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a0c9ce31b686f1aad449e3572fddbe981fe9e1c7)

------------------------------------------------------------------------