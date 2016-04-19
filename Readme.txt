Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20605

This directory contains the Win32 binaries.

Build Date:       Tue, 19 Apr 2016 03:11:19 Pacific Daylight Time
Last Changed Rev: 20604

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20605
  BootSectImage Version 1.0 Build Build 20182
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20182
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
 *GenDepex.exe Version 0.04 Build 20605
 *GenFds.exe 1.0 Build 20605
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 20208
  GenFw Version 0.2 Build 20600
  GenPage Version 0.2 Build 19914
 *GenPatchPcdTable.exe Version 0.10 Build 20605
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20119
  LzmaF86Compress Version 0.2 Build 20119
 *PatchPcdValue.exe Version 0.10 Build 20605
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20182
 *TargetTool.exe Version 0.01 Build 20605
  TianoCompress Version 0.1 Build 19914
 *Trim.exe Version 0.10 Build 20605
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20528
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20182
  VolInfo Version 1.0 Build Build 20600
 *build.exe Version 0.60 Build 20605

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/19/2016 3:11:21AM Engine version = 5700.7163
  4/19/2016 3:11:21AM AntiVirus DAT version = 8139.0
  4/19/2016 3:11:21AM Number of detection signatures in EXTRA.DAT = None
  4/19/2016 3:11:21AM Names of detection signatures in EXTRA.DAT = None
  4/19/2016 3:11:21AM Scan Started On-Demand Scan
  4/19/2016 3:11:31AM Scan Summary
  4/19/2016 3:11:31AM Processes scanned : 0
  4/19/2016 3:11:31AM Processes detected : 0
  4/19/2016 3:11:31AM Processes cleaned : 0
  4/19/2016 3:11:31AM Boot sectors scanned : 2
  4/19/2016 3:11:31AM Boot sectors detected: 0
  4/19/2016 3:11:31AM Boot sectors cleaned : 0
  4/19/2016 3:11:31AM Files scanned : 55
  4/19/2016 3:11:31AM Files with detections: 0
  4/19/2016 3:11:31AM File detections : 0
  4/19/2016 3:11:31AM Files cleaned : 0
  4/19/2016 3:11:31AM Files deleted : 0
  4/19/2016 3:11:31AM Files not scanned : 0
  4/19/2016 3:11:31AM Scan Summary (Registry Scanning)
  4/19/2016 3:11:31AM Keys scanned : 0
  4/19/2016 3:11:31AM Keys detected : 0
  4/19/2016 3:11:31AM Keys cleaned : 0
  4/19/2016 3:11:31AM Keys deleted : 0
  4/19/2016 3:11:31AM Run time : 0:00:10
  4/19/2016 3:11:31AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20600:HEAD Source
------------------------------------------------------------------------  r20604 | edk2buildsystem | 2016-04-19 02:05:31 -0700 (Tue, 19 Apr 2016) | 17 lines
  BaseTools/Build: Consider only build-specified architectures
  When building for any specific architecture, the build script today
  is loading DSC sections for other architectures not in the build.
  The build process should disregard DSC sections that are not
  relevant to the build.
  This fixes scenario whereby a build occurs in a source tree that was
  been cleaned of non-essential directories.  For instance, X64 builds
  do not require the ArmPkg directory to build a firmware image.  This
  condition (build break when ArmPkg is absent) occurs when included
  DSCs have sections for multiple architectures.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Thomas Palmer <thomas.palmer@hpe.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 77177984087654ff2888e182d40c20480da29811)

------------------------------------------------------------------------