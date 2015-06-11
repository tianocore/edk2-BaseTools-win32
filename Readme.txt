Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 17624

This directory contains the Win32 binaries.

Build Date:       Thu, 11 Jun 2015 03:15:45 Pacific Daylight Time
Last Changed Rev: 17623

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Not available
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 17624
  BootSectImage Version 0.1 Build 17553
  Ecc.exe Version 0.01 Build 17553
  EfiLdrImage Version 0.1 Build 17553
  EfiRom Version 0.1 Build 17553
  GenBootSector Version 0.2 Build 17553
  GenCrc32 Version 0.2 Build 17553
 *GenDepex.exe Version 0.04 Build 17624
 *GenFds.exe 1.0 Build 17624
  GenFfs Version 0.1 Build 17553
  GenFv Version 0.1 Build 17553
  GenFw Version 0.2 Build 17553
  GenPage Version 0.2 Build 17553
 *GenPatchPcdTable.exe Version 0.10 Build 17624
  GenSec Version 0.1 Build 17553
  GenVtf Version 0.1 Build 17553
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 17553
  LzmaF86Compress Version 0.2 Build 17553
 *PatchPcdValue.exe Version 0.10 Build 17624
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17553
  Split Version 0.1 Build 17553
 *TargetTool.exe Version 0.01 Build 17624
  TianoCompress Version 0.1 Build 17553
 *Trim.exe Version 0.10 Build 17624
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 17553
  VfrCompile version  2.00 (UEFI 2.4) Build 17553
  VolInfo Version 0.83 Build 17553, Jun  3 2015
 *build.exe Version 0.60 Build 17624

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1263
  6/11/2015 3:15:46AM Engine version = 5700.7163
  6/11/2015 3:15:46AM AntiVirus DAT version = 7827.0
  6/11/2015 3:15:46AM Number of detection signatures in EXTRA.DAT = None
  6/11/2015 3:15:46AM Names of detection signatures in EXTRA.DAT = None
  6/11/2015 3:15:47AM Scan Started On-Demand Scan
  6/11/2015 3:16:30AM Scan Summary
  6/11/2015 3:16:30AM Processes scanned : 0
  6/11/2015 3:16:30AM Processes detected : 0
  6/11/2015 3:16:30AM Processes cleaned : 0
  6/11/2015 3:16:30AM Boot sectors scanned : 1
  6/11/2015 3:16:30AM Boot sectors detected: 0
  6/11/2015 3:16:30AM Boot sectors cleaned : 0
  6/11/2015 3:16:30AM Files scanned : 55
  6/11/2015 3:16:30AM Files with detections: 0
  6/11/2015 3:16:30AM File detections : 0
  6/11/2015 3:16:30AM Files cleaned : 0
  6/11/2015 3:16:30AM Files deleted : 0
  6/11/2015 3:16:30AM Files not scanned : 0
  6/11/2015 3:16:30AM Scan Summary (Registry Scanning)
  6/11/2015 3:16:30AM Keys scanned : 0
  6/11/2015 3:16:30AM Keys detected : 0
  6/11/2015 3:16:30AM Keys cleaned : 0
  6/11/2015 3:16:30AM Keys deleted : 0
  6/11/2015 3:16:30AM Run time : 0:00:43
  6/11/2015 3:16:30AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 17611:HEAD Source
------------------------------------------------------------------------  r17612 | lhauch | 2015-06-10 07:34:40 -0700 (Wed, 10 Jun 2015) | 17 lines
  Adds new files to the Makefile for testing changed sources
  The files were added April 9th, revision 17158, but the Makefile was not updated.
  Converted all tabs in this make file to space characters.
  [Test]
  nmake cleanall
  nmake
  Successfully built all binaries
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: lhauch <larry.hauch@intel.com>
  Reviewed-by: Joe Peterson <joe.peterson@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r17621 | yingke | 2015-06-10 22:16:40 -0700 (Wed, 10 Jun 2015) | 7 lines
  BaseTools: Support build options for specific module type in DSC.
  This patch extended BuildOptions section in DSC to support [BuildOptions.ARCH.CodeBase.MODULE_TYPE]
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r17622 | yingke | 2015-06-10 22:20:00 -0700 (Wed, 10 Jun 2015) | 7 lines
  BaseTools: Generate a binary file and list it in Binary section of As Built INF.
  This binary file contains offset of VFR and UNI data.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r17623 | yingke | 2015-06-10 22:21:59 -0700 (Wed, 10 Jun 2015) | 5 lines
  BaseTools: Fixed an error reported during generating report.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------