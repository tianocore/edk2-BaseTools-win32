Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 22700

This directory contains the Win32 binaries.

Build Date:       Tue, 27 Sep 2016 03:11:34 Pacific Daylight Time
Last Changed Rev: 22700

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 22700
  BootSectImage Version 1.0 Build Build 22449
 *Ecc.exe Version 1.0 Build Build 22700
  EfiLdrImage Version 1.0 Build Build 22449
  EfiRom Version 0.1 Build 22617
  GenBootSector Version 0.2 Build 22449
  GenCrc32 Version 0.2 Build 22449
 *GenDepex.exe Version 0.04 Build 22700
 *GenFds.exe 1.0 Build 22700
  GenFfs Version 0.1 Build 22449
  GenFv Version 0.1 Build 22543
  GenFw Version 0.2 Build 22466
  GenPage Version 0.2 Build 22449
 *GenPatchPcdTable.exe Version 0.10 Build 22700
  GenSec Version 0.1 Build 22449
  GenVtf Version 0.1 Build 22449
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 22449
  LzmaF86Compress Version 0.2 Build 22449
 *PatchPcdValue.exe Version 0.10 Build 22700
  Pkcs7Sign Version 0.9 Build 22543
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 22444
  Split Version 1.0 Build Build 22449
 *TargetTool.exe Version 0.01 Build 22700
  TianoCompress Version 0.1 Build 22449
 *Trim.exe Version 0.10 Build 22700
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22316
  VfrCompile version  2.01 (UEFI 2.4) Build Build 22449
  VolInfo Version 1.0 Build Build 22449
 *build.exe Version 0.60 Build 22700

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  9/27/2016 3:11:35AM Engine version = 5700.7163
  9/27/2016 3:11:35AM AntiVirus DAT version = 8300.0
  9/27/2016 3:11:35AM Number of detection signatures in EXTRA.DAT = None
  9/27/2016 3:11:35AM Names of detection signatures in EXTRA.DAT = None
  9/27/2016 3:11:35AM Scan Started On-Demand Scan
  9/27/2016 3:11:38AM Scan Summary
  9/27/2016 3:11:38AM Processes scanned : 0
  9/27/2016 3:11:38AM Processes detected : 0
  9/27/2016 3:11:38AM Processes cleaned : 0
  9/27/2016 3:11:38AM Boot sectors scanned : 1
  9/27/2016 3:11:38AM Boot sectors detected: 0
  9/27/2016 3:11:38AM Boot sectors cleaned : 0
  9/27/2016 3:11:38AM Files scanned : 62
  9/27/2016 3:11:38AM Files with detections: 0
  9/27/2016 3:11:38AM File detections : 0
  9/27/2016 3:11:38AM Files cleaned : 0
  9/27/2016 3:11:38AM Files deleted : 0
  9/27/2016 3:11:38AM Files not scanned : 0
  9/27/2016 3:11:38AM Scan Summary (Registry Scanning)
  9/27/2016 3:11:38AM Keys scanned : 0
  9/27/2016 3:11:38AM Keys detected : 0
  9/27/2016 3:11:38AM Keys cleaned : 0
  9/27/2016 3:11:38AM Keys deleted : 0
  9/27/2016 3:11:38AM Run time : 0:00:03
  9/27/2016 3:11:38AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 22688:HEAD Source
------------------------------------------------------------------------  r22688 | edk2buildsystem | 2016-09-25 02:05:28 -0700 (Sun, 25 Sep 2016) | 11 lines
  BaseTools: handling the case that map file is not exist
  We meet a case that add the library inf file which has the uni file in
  the [Sources] section, for this case there will no map file exist, it
  cause build tools report Traceback  error.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 587e9dfbbafe7d4e772c1870b8c880c6d7a8a70c)

------------------------------------------------------------------------  r22697 | edk2buildsystem | 2016-09-27 02:06:04 -0700 (Tue, 27 Sep 2016) | 18 lines
  BaseTools: support generating image package from BMP/JPEG/PNG files
  BaseTools add support to generating image package from BMP/JPEG/PNG
  files.
  1) New file type *.idf Image definition file to describe HII image
  resource. It is the ASCII text file, and includes one or more "#image
  IMAGE_ID [TRANSPARENT] ImageFileName".
  2) New IMAGE_TOKEN macro is used to refer to IMAGE_ID.
  3) New AutoGen header file $(MODULE_NAME)ImgDefs.h to include the
  generated ImageId definition.
  4) New $(MODULE_NAME)Idf.hpk or $(MODULE_NAME)Images are generated
  as the output binary HII image package.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 333ba578fef4dff8921051410c5b56f63e7eeadb)

------------------------------------------------------------------------  r22700 | edk2buildsystem | 2016-09-27 02:06:19 -0700 (Tue, 27 Sep 2016) | 12 lines
  BaseTools: List missing source python files for Ecc tool in Makefile
  Add missing python sources files that are dependent for Ecc tool in
  Makefile.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7807dea57fba6a019bb8641572e0159ffa03ad9e)

------------------------------------------------------------------------