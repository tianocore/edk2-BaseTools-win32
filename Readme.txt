Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 20993

This directory contains the Win32 binaries.

Build Date:       Thu, 26 May 2016 03:11:18 Pacific Daylight Time
Last Changed Rev: 20990

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 20993
  BootSectImage Version 1.0 Build Build 20909
  Ecc.exe Version 1.0 Build Build 20528
  EfiLdrImage Version 1.0 Build Build 20909
  EfiRom Version 0.1 Build 20909
  GenBootSector Version 0.2 Build 20909
  GenCrc32 Version 0.2 Build 20909
 *GenDepex.exe Version 0.04 Build 20993
 *GenFds.exe 1.0 Build 20993
  GenFfs Version 0.1 Build 20909
  GenFv Version 0.1 Build 20909
  GenFw Version 0.2 Build 20909
  GenPage Version 0.2 Build 20909
 *GenPatchPcdTable.exe Version 0.10 Build 20993
  GenSec Version 0.1 Build 20909
  GenVtf Version 0.1 Build 20909
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 20909
  LzmaF86Compress Version 0.2 Build 20909
 *PatchPcdValue.exe Version 0.10 Build 20993
  Rsa2048Sha256GenerateKeys Version 0.9 Build 20528
  Rsa2048Sha256Sign Version 0.9 Build 20528
  Split Version 1.0 Build Build 20909
 *TargetTool.exe Version 0.01 Build 20993
  TianoCompress Version 0.1 Build 20909
 *Trim.exe Version 0.10 Build 20993
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 20651
  VfrCompile version  2.01 (UEFI 2.4) Build Build 20909
  VolInfo Version 1.0 Build Build 20909
 *build.exe Version 0.60 Build 20993

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/26/2016 3:11:19AM Engine version = 5700.7163
  5/26/2016 3:11:19AM AntiVirus DAT version = 8176.0
  5/26/2016 3:11:19AM Number of detection signatures in EXTRA.DAT = 1
  5/26/2016 3:11:19AM Names of detection signatures in EXTRA.DAT = W97M/Downloader.bdj (ED)
  5/26/2016 3:11:19AM Scan Started On-Demand Scan
  5/26/2016 3:11:25AM Scan Summary
  5/26/2016 3:11:25AM Processes scanned : 0
  5/26/2016 3:11:25AM Processes detected : 0
  5/26/2016 3:11:25AM Processes cleaned : 0
  5/26/2016 3:11:25AM Boot sectors scanned : 2
  5/26/2016 3:11:25AM Boot sectors detected: 0
  5/26/2016 3:11:25AM Boot sectors cleaned : 0
  5/26/2016 3:11:25AM Files scanned : 55
  5/26/2016 3:11:25AM Files with detections: 0
  5/26/2016 3:11:25AM File detections : 0
  5/26/2016 3:11:25AM Files cleaned : 0
  5/26/2016 3:11:25AM Files deleted : 0
  5/26/2016 3:11:25AM Files not scanned : 0
  5/26/2016 3:11:25AM Scan Summary (Registry Scanning)
  5/26/2016 3:11:25AM Keys scanned : 0
  5/26/2016 3:11:25AM Keys detected : 0
  5/26/2016 3:11:25AM Keys cleaned : 0
  5/26/2016 3:11:25AM Keys deleted : 0
  5/26/2016 3:11:25AM Run time : 0:00:06
  5/26/2016 3:11:25AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 20979:HEAD Source
------------------------------------------------------------------------  r20988 | edk2buildsystem | 2016-05-26 02:05:39 -0700 (Thu, 26 May 2016) | 9 lines
  BaseTools: Fix GenFds issue to wrongly get file without postfix.
  GenFds GenSection will search the output file based on the file extension.
  If the output file has no extension, it should be skip.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Andrew Fish <afish@apple.com>
  (cherry picked from commit 483b01d2da22bab88f0815a2f01025ea6b9333f5)

------------------------------------------------------------------------  r20989 | edk2buildsystem | 2016-05-26 02:05:42 -0700 (Thu, 26 May 2016) | 6 lines
  BaseTools: Fix comments about return value of 'LoadToolDefFile'
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Michael Zimmermann <sigmaepsilon92@gmail.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 8b14b35b192dc57eb01e091b7bf32af3b0e960b3)

------------------------------------------------------------------------  r20990 | edk2buildsystem | 2016-05-26 02:05:47 -0700 (Thu, 26 May 2016) | 6 lines
  BaseTools: add '!include' support to tools_def.txt parser
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Michael Zimmermann <sigmaepsilon92@gmail.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 8ac46e4ef76ee56778430bb3dbcc545cce49d208)

------------------------------------------------------------------------