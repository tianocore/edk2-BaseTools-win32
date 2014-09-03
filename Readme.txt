Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 16055

This directory contains the Win32 binaries.

Build Date:       Wed, 03 Sep 2014 03:02:08 Pacific Daylight Time
Last Changed Rev: 16041

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.1.3

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 16006
 *BootSectImage Version 0.1 Build 16055
 *EfiLdrImage Version 0.1 Build 16055
 *EfiRom Version 0.1 Build 16055
 *GenBootSector Version 0.2 Build 16055
 *GenCrc32 Version 0.2 Build 16055
  GenDepex.exe Version 0.04 Build 16006
  GenFds.exe 1.0 Build 16006
 *GenFfs Version 0.1 Build 16055
 *GenFv Version 0.1 Build 16055
 *GenFw Version 0.2 Build 16055
 *GenPage Version 0.2 Build 16055
  GenPatchPcdTable.exe Version 0.10 Build 16006
 *GenSec Version 0.1 Build 16055
 *GenVtf Version 0.1 Build 16055
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 16055
  LzmaF86Compress Version 0.2 Build 16055
  PatchPcdValue.exe Version 0.10 Build 16006
  Rsa2048Sha256GenerateKeys Version 0.9 Build 16006
  Rsa2048Sha256Sign Version 0.9 Build 16006
 *Split Version 0.1 Build 16055
  TargetTool.exe Version 0.01 Build 16006
 *TianoCompress Version 0.1 Build 16055
  Trim.exe Version 0.10 Build 16006
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 16006
 *VfrCompile version  2.00 (UEFI 2.4) Build 16055
 *VolInfo Version 0.83 Build 16055, Sep  3 2014
  build.exe Version 0.51 Build 16006

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.975
  9/3/2014 3:02:09AM Engine version = 5400.1158
  9/3/2014 3:02:09AM AntiVirus DAT version = 7549.0
  9/3/2014 3:02:09AM Number of detection signatures in EXTRA.DAT = None
  9/3/2014 3:02:09AM Names of detection signatures in EXTRA.DAT = None
  9/3/2014 3:02:09AM Scan Started On-Demand Scan
  9/3/2014 3:02:17AM Scan Summary
  9/3/2014 3:02:17AM Processes scanned : 0
  9/3/2014 3:02:17AM Processes detected : 0
  9/3/2014 3:02:17AM Processes cleaned : 0
  9/3/2014 3:02:17AM Boot sectors scanned : 2
  9/3/2014 3:02:17AM Boot sectors detected: 0
  9/3/2014 3:02:17AM Boot sectors cleaned : 0
  9/3/2014 3:02:17AM Files scanned : 69
  9/3/2014 3:02:17AM Files with detections: 0
  9/3/2014 3:02:17AM File detections : 0
  9/3/2014 3:02:17AM Files cleaned : 0
  9/3/2014 3:02:17AM Files deleted : 0
  9/3/2014 3:02:17AM Files not scanned : 0
  9/3/2014 3:02:17AM Scan Summary (Registry Scanning)
  9/3/2014 3:02:17AM Keys scanned : 0
  9/3/2014 3:02:17AM Keys detected : 0
  9/3/2014 3:02:17AM Keys cleaned : 0
  9/3/2014 3:02:17AM Keys deleted : 0
  9/3/2014 3:02:17AM Scan Summary (Cookie Scanning)
  9/3/2014 3:02:17AM Cookies scanned : 0
  9/3/2014 3:02:17AM Cookies detected : 0
  9/3/2014 3:02:17AM Cookies cleaned : 0
  9/3/2014 3:02:17AM Cookies deleted : 0
  9/3/2014 3:02:17AM Run time : 0:00:08
  9/3/2014 3:02:17AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 16006:HEAD Source
------------------------------------------------------------------------  r16006 | bobfeng | 2014-08-30 05:59:03 -0700 (Sat, 30 Aug 2014) | 5 lines
  This patch is going to fix the issue of only Default SkuId is built into the External Pcd DataBase.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Feng, Bob C <bob.c.feng@intel.com>
  Reviewed-by: Gao, Liming <liming.gao@intel.com>

------------------------------------------------------------------------  r16039 | hchen30 | 2014-09-02 19:09:19 -0700 (Tue, 02 Sep 2014) | 8 lines
  BaseTools/CommonLib: Add a step to convert ":\\" to ":\"
  Convert ":\\\\" to ":\\", because it doesn't work with WINDOWS_EXTENSION_PATH.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r16041 | hchen30 | 2014-09-03 01:25:10 -0700 (Wed, 03 Sep 2014) | 7 lines
  BaseTools/UPT: Replace os.linesep with '\r\n' when generating UNI files.
  Replace os.linesep with '\r\n' when generating UNI files to make sure all files are under DOS format.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Gao, Liming <liming.gao@intel.com>

------------------------------------------------------------------------