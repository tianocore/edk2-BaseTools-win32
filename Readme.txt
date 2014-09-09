Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 16068

This directory contains the Win32 binaries.

Build Date:       Tue, 09 Sep 2014 08:24:51 Pacific Daylight Time
Last Changed Rev: 16063

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio Team System 2008 Team Suite SP 1
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################

** ALL TOOLS WERE REBUILT **
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 16068
  BootSectImage Version 0.1 Build 16068
  EfiLdrImage Version 0.1 Build 16068
  EfiRom Version 0.1 Build 16068
  GenBootSector Version 0.2 Build 16068
  GenCrc32 Version 0.2 Build 16068
  GenDepex.exe Version 0.04 Build 16068
  GenFds.exe 1.0 Build 16068
  GenFfs Version 0.1 Build 16068
  GenFv Version 0.1 Build 16068
  GenFw Version 0.2 Build 16068
  GenPage Version 0.2 Build 16068
  GenPatchPcdTable.exe Version 0.10 Build 16068
  GenSec Version 0.1 Build 16068
  GenVtf Version 0.1 Build 16068
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 16068
  LzmaF86Compress Version 0.2 Build 16068
  PatchPcdValue.exe Version 0.10 Build 16068
  Rsa2048Sha256GenerateKeys Version 0.9 Build 16068
  Rsa2048Sha256Sign Version 0.9 Build 16068
  Split Version 0.1 Build 16068
  TargetTool.exe Version 0.01 Build 16068
  TianoCompress Version 0.1 Build 16068
  Trim.exe Version 0.10 Build 16068
  Intel(r) UEFI Packaging Tool (Intel(r) UEFIPT) - Revision 1.0 Build 16068
  VfrCompile version  2.00 (UEFI 2.4) Build 16068
  VolInfo Version 0.83 Build 16068, Sep  9 2014
  build.exe Version 0.51 Build 16068

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.975
  9/9/2014 8:24:53AM Engine version = 5400.1158
  9/9/2014 8:24:53AM AntiVirus DAT version = 7555.0
  9/9/2014 8:24:53AM Number of detection signatures in EXTRA.DAT = None
  9/9/2014 8:24:53AM Names of detection signatures in EXTRA.DAT = None
  9/9/2014 8:24:53AM Scan Started On-Demand Scan
  9/9/2014 8:25:01AM Scan Summary
  9/9/2014 8:25:01AM Processes scanned : 0
  9/9/2014 8:25:01AM Processes detected : 0
  9/9/2014 8:25:01AM Processes cleaned : 0
  9/9/2014 8:25:01AM Boot sectors scanned : 2
  9/9/2014 8:25:01AM Boot sectors detected: 0
  9/9/2014 8:25:01AM Boot sectors cleaned : 0
  9/9/2014 8:25:01AM Files scanned : 67
  9/9/2014 8:25:01AM Files with detections: 0
  9/9/2014 8:25:01AM File detections : 0
  9/9/2014 8:25:01AM Files cleaned : 0
  9/9/2014 8:25:01AM Files deleted : 0
  9/9/2014 8:25:01AM Files not scanned : 0
  9/9/2014 8:25:01AM Scan Summary (Registry Scanning)
  9/9/2014 8:25:01AM Keys scanned : 0
  9/9/2014 8:25:01AM Keys detected : 0
  9/9/2014 8:25:01AM Keys cleaned : 0
  9/9/2014 8:25:01AM Keys deleted : 0
  9/9/2014 8:25:01AM Scan Summary (Cookie Scanning)
  9/9/2014 8:25:01AM Cookies scanned : 0
  9/9/2014 8:25:01AM Cookies detected : 0
  9/9/2014 8:25:01AM Cookies cleaned : 0
  9/9/2014 8:25:01AM Cookies deleted : 0
  9/9/2014 8:25:01AM Run time : 0:00:09
  9/9/2014 8:25:01AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 16055:HEAD Source
------------------------------------------------------------------------  r16057 | hchen30 | 2014-09-04 01:32:44 -0700 (Thu, 04 Sep 2014) | 7 lines
  BaseTools/AutoGen: Remove redundant copy action for binary module
  Remove redundant copy action for binary module to copy binary files to output directory only when the binary module is a library
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yingke Liu <yingke.d.liu@Intel.com>

------------------------------------------------------------------------  r16063 | lhauch | 2014-09-05 07:15:40 -0700 (Fri, 05 Sep 2014) | 27 lines
  This file allows a developer to add a new tool in either the C or Python trees, add the executable (and any supporting files, such as the TestSigningPrivateKey.pem file) to this file and the build server will automatically make sure that the new files are added to the BaseTools\Bin\Win32 directory. The Win32 directory is located in https://svn.code.sf.net/p/edk2-toolbinaries/code/trunk/Win32 repository.
  Developer - Tool add process:
  1)	Developer adds code for the new tool.
  2)	Developer updates the Makefile in the C or Python directory
  a)	The entry must make sure that the executable is generated in the BaseTools\Bin\Win32 directory and any supporting files are copied to the same directory as part of the build step.
  3)	Developer adds the <Toolname>.exe under the [Bin.Win32] section in the BinaryFiles.txt file.
  4)	Developer adds other files required to be present in the [ExtraFiles.Win32] section in the BinaryFiles.txt file.
  Build Server:
  1)	Build all binaries by calling nmake on the Source\C\Makefile and Source\Python\Makefile
  2)	After building the binaries, the build server verify that the files listed in BaseTools\Source\BinFiles.txt are also in the edk2-toolbinaries project,
  a.	If a file is not under source control, then the build server will add file as long as it is present.
  File format:
  [SectionName.TargetDir]
  File1
  File2
  …
  Where:
  SectionName is one of Bin, ExtraFiles or CxFreeze
  TargeDir is the name of the subdirectory in the BaseTools\Bin directory tree.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: lhauch <larry.hauch@intel.com>

------------------------------------------------------------------------
Forcing build to fix roll-back for using antlr 3.0.1 required for the EXECUTION_ORDER report generation, also picking up change to UPT which was not rebuilt due to an issue with the Makefile that only checked UPT.py
