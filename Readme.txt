Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 16114

This directory contains the Win32 binaries.

Build Date:       Tue, 16 Sep 2014 03:04:24 Pacific Daylight Time
Last Changed Rev: 16114

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 16114
  BootSectImage Version 0.1 Build 16068
  EfiLdrImage Version 0.1 Build 16068
  EfiRom Version 0.1 Build 16068
  GenBootSector Version 0.2 Build 16068
  GenCrc32 Version 0.2 Build 16068
 *GenDepex.exe Version 0.04 Build 16114
 *GenFds.exe 1.0 Build 16114
  GenFfs Version 0.1 Build 16068
  GenFv Version 0.1 Build 16068
  GenFw Version 0.2 Build 16068
  GenPage Version 0.2 Build 16068
 *GenPatchPcdTable.exe Version 0.10 Build 16114
  GenSec Version 0.1 Build 16068
  GenVtf Version 0.1 Build 16068
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 16068
  LzmaF86Compress Version 0.2 Build 16068
 *PatchPcdValue.exe Version 0.10 Build 16114
  Rsa2048Sha256GenerateKeys Version 0.9 Build 16068
  Rsa2048Sha256Sign Version 0.9 Build 16068
  Split Version 0.1 Build 16068
 *TargetTool.exe Version 0.01 Build 16114
  TianoCompress Version 0.1 Build 16068
 *Trim.exe Version 0.10 Build 16114
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 16068
  VfrCompile version  2.00 (UEFI 2.4) Build 16068
  VolInfo Version 0.83 Build 16068, Sep  9 2014
 *build.exe Version 0.60 Build 16114

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.975
  9/16/2014 3:04:25AM Engine version = 5400.1158
  9/16/2014 3:04:25AM AntiVirus DAT version = 7560.0
  9/16/2014 3:04:25AM Number of detection signatures in EXTRA.DAT = None
  9/16/2014 3:04:25AM Names of detection signatures in EXTRA.DAT = None
  9/16/2014 3:04:25AM Scan Started On-Demand Scan
  9/16/2014 3:04:32AM Scan Summary
  9/16/2014 3:04:32AM Processes scanned : 0
  9/16/2014 3:04:32AM Processes detected : 0
  9/16/2014 3:04:32AM Processes cleaned : 0
  9/16/2014 3:04:32AM Boot sectors scanned : 2
  9/16/2014 3:04:32AM Boot sectors detected: 0
  9/16/2014 3:04:32AM Boot sectors cleaned : 0
  9/16/2014 3:04:32AM Files scanned : 69
  9/16/2014 3:04:32AM Files with detections: 0
  9/16/2014 3:04:32AM File detections : 0
  9/16/2014 3:04:32AM Files cleaned : 0
  9/16/2014 3:04:32AM Files deleted : 0
  9/16/2014 3:04:32AM Files not scanned : 0
  9/16/2014 3:04:32AM Scan Summary (Registry Scanning)
  9/16/2014 3:04:32AM Keys scanned : 0
  9/16/2014 3:04:32AM Keys detected : 0
  9/16/2014 3:04:32AM Keys cleaned : 0
  9/16/2014 3:04:32AM Keys deleted : 0
  9/16/2014 3:04:32AM Scan Summary (Cookie Scanning)
  9/16/2014 3:04:32AM Cookies scanned : 0
  9/16/2014 3:04:32AM Cookies detected : 0
  9/16/2014 3:04:32AM Cookies cleaned : 0
  9/16/2014 3:04:32AM Cookies deleted : 0
  9/16/2014 3:04:32AM Run time : 0:00:07
  9/16/2014 3:04:32AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 16103:HEAD Source
------------------------------------------------------------------------  r16103 | lhauch | 2014-09-12 15:59:04 -0700 (Fri, 12 Sep 2014) | 9 lines
  The current Makefile only checks the primary python file, such as build.py and does not check other files in tool’s directory tree.
  This modification adds all of the other files within the tool’s directory tree that would be a cause to rebuild the tool.
  The format in the Makefile for listing these other files was selected to allow the nightly build script to detect changes in the additional files.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: lhauch <larry.hauch@intel.com>
  Reviewed-by: Gao, Liming <liming.gao@intel.com>

------------------------------------------------------------------------  r16106 | oliviermartin | 2014-09-15 17:38:12 -0700 (Mon, 15 Sep 2014) | 9 lines
  BaseTools/Source/C: Only used '-Wno-self-assign' when BaseTools are built on DARWIN
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Andrew Fish <afish@apple.com>
  Reviewed-By: Olivier Martin <olivier.martin@arm.com>
  Tested-By: Olivier Martin <olivier.martin@arm.com>
  Reviewed-by: Gao, Liming <liming.gao@intel.com>

------------------------------------------------------------------------  r16113 | yingke | 2014-09-16 01:33:40 -0700 (Tue, 16 Sep 2014) | 5 lines
  Support DSC and FDF file out of WORKSPACE by GenFds.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yingke Liu <yingke.d.liu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r16114 | lgao4 | 2014-09-16 02:03:00 -0700 (Tue, 16 Sep 2014) | 5 lines
  Update Build Tool version from 0.51 to 0.60
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Gao, Liming <liming.gao@intel.com>

------------------------------------------------------------------------