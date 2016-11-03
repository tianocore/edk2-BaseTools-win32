Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23086

This directory contains the Win32 binaries.

Build Date:       Thu, 03 Nov 2016 03:11:09 Pacific Daylight Time
Last Changed Rev: 23086

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23074
  BootSectImage Version 1.0 Build Build 22854
  Ecc.exe Version 1.0 Build Build 22854
  EfiLdrImage Version 1.0 Build Build 22854
  EfiRom Version 0.1 Build 22854
  GenBootSector Version 0.2 Build 22854
  GenCrc32 Version 0.2 Build 22854
  GenDepex.exe Version 0.04 Build 23074
  GenFds.exe 1.0 Build 23074
  GenFfs Version 0.1 Build 22854
  GenFv Version 0.1 Build 22854
  GenFw Version 0.2 Build 22854
  GenPage Version 0.2 Build 22854
  GenPatchPcdTable.exe Version 0.10 Build 23074
  GenSec Version 0.1 Build 22854
  GenVtf Version 0.1 Build 22854
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 23086
  LzmaF86Compress Version 0.2 Build 23086
  PatchPcdValue.exe Version 0.10 Build 23074
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
  Split Version 1.0 Build Build 22854
  TargetTool.exe Version 0.01 Build 23074
  TianoCompress Version 0.1 Build 22854
  Trim.exe Version 0.10 Build 23074
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22854
  VolInfo Version 1.0 Build Build 22854
  build.exe Version 0.60 Build 23074

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/3/2016 3:11:10AM Engine version = 5700.7163
  11/3/2016 3:11:10AM AntiVirus DAT version = 8337.0
  11/3/2016 3:11:10AM Number of detection signatures in EXTRA.DAT = None
  11/3/2016 3:11:10AM Names of detection signatures in EXTRA.DAT = None
  11/3/2016 3:11:10AM Scan Started On-Demand Scan
  11/3/2016 3:11:14AM Scan Summary
  11/3/2016 3:11:14AM Processes scanned : 0
  11/3/2016 3:11:14AM Processes detected : 0
  11/3/2016 3:11:14AM Processes cleaned : 0
  11/3/2016 3:11:14AM Boot sectors scanned : 1
  11/3/2016 3:11:14AM Boot sectors detected: 0
  11/3/2016 3:11:14AM Boot sectors cleaned : 0
  11/3/2016 3:11:14AM Files scanned : 62
  11/3/2016 3:11:14AM Files with detections: 0
  11/3/2016 3:11:14AM File detections : 0
  11/3/2016 3:11:14AM Files cleaned : 0
  11/3/2016 3:11:14AM Files deleted : 0
  11/3/2016 3:11:14AM Files not scanned : 0
  11/3/2016 3:11:14AM Scan Summary (Registry Scanning)
  11/3/2016 3:11:14AM Keys scanned : 0
  11/3/2016 3:11:14AM Keys detected : 0
  11/3/2016 3:11:14AM Keys cleaned : 0
  11/3/2016 3:11:14AM Keys deleted : 0
  11/3/2016 3:11:14AM Run time : 0:00:04
  11/3/2016 3:11:14AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23074:HEAD Source
------------------------------------------------------------------------  r23079 | edk2buildsystem | 2016-11-03 02:05:55 -0700 (Thu, 03 Nov 2016) | 11 lines
  BaseTools LzmaCompress: Update LZMA to new 16.04 version
  New version LZMA SDK improves the compression performance on windows OS,
  and has no change on the compression ratio. I compress 8M FVMAIN image,
  the compression time is reduced from 2.590s to 1.419s.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit c4ab09ef2f543ebf420da5d7cd8d48988c99b89c)

------------------------------------------------------------------------  r23086 | edk2buildsystem | 2016-11-03 02:06:50 -0700 (Thu, 03 Nov 2016) | 15 lines
  BaseTool/Pkcs7: Add TestRoot.cer.
  We add this binary data file for TestRoot.cer.
  So that a platform may include this default file in FDF,
  to check if the platform is using default test key,
  or different production key.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Michael D Kinney <michael.d.kinney@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Jiewen Yao <jiewen.yao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Michael D Kinney <michael.d.kinney@intel.com>
  (cherry picked from commit e9d0933d45e51027836f570427141fd2e3a7dfbd)

------------------------------------------------------------------------