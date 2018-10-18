############### NOTE ###############
This directory Win32 binaries doesn't work any longer to build EDK2 project.
Please run BaseTools Python from source in Windows OS. Here is wiki:
https://github.com/tianocore/tianocore.github.io/wiki/Windows-systems#compile-tools

Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 28123

This directory contains the Win32 binaries.

Build Date:       Tue, 16 Oct 2018 17:27:31 Pacific Daylight Time
Last Changed Rev: 28122

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.14 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
ERROR : This tool is missing --version option: BPDG.exe
 *BootSectImage Version 1.0 Build Build 28123
ERROR : This tool is missing --version option: Brotli.exe
ERROR : This tool is missing --version option: BrotliCompress.bat
 *DevicePath Version 0.1 Build 28123
  Ecc.exe Version 1.0 Build Build 27306
 *EfiLdrImage Version 1.0 Build Build 28123
 *EfiRom Version 0.1 Build 28123
 *GenBootSector Version 0.2 Build 28123
 *GenCrc32 Version 0.2 Build 28123
  GenDepex.exe Version 0.04 Build 27752
ERROR : This tool is missing --version option: GenFds.exe
 *GenFfs Version 0.1 Build 28123
 *GenFv Version 0.1 Build 28123
 *GenFw Version 0.2 Build 28123
 *GenPage Version 0.2 Build 28123
  GenPatchPcdTable.exe Version 0.10 Build 27752
 *GenSec Version 0.1 Build 28123
 *GenVtf Version 0.1 Build 28123
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 28123
  LzmaF86Compress Version 0.2 Build 28123
  PatchPcdValue.exe Version 0.10 Build 27752
  Pkcs7Sign Version 0.9 Build 27752
  Rsa2048Sha256GenerateKeys Version 0.9 Build 27752
  Rsa2048Sha256Sign Version 0.9 Build 27752
 *Split Version 1.0 Build Build 28123
  TargetTool.exe Version 0.01 Build 27752
 *TianoCompress Version 0.1 Build 28123
  Trim.exe Version 0.10 Build 27752
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 27752
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 28123
 *VolInfo Version 1.0 Build Build 28123
  build.exe Version 0.60 Build 27752

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  10/16/2018 5:27:34PM Engine version = 5900.7806
  10/16/2018 5:27:34PM AntiVirus DAT version = 9048.0
  10/16/2018 5:27:34PM Number of detection signatures in EXTRA.DAT = None
  10/16/2018 5:27:34PM Names of detection signatures in EXTRA.DAT = None
  10/16/2018 5:27:34PM Scan Started On-Demand Scan
  10/16/2018 5:27:40PM Scan Summary
  10/16/2018 5:27:40PM Processes scanned : 0
  10/16/2018 5:27:40PM Processes detected : 0
  10/16/2018 5:27:40PM Processes cleaned : 0
  10/16/2018 5:27:40PM Boot sectors scanned : 2
  10/16/2018 5:27:40PM Boot sectors detected: 0
  10/16/2018 5:27:40PM Boot sectors cleaned : 0
  10/16/2018 5:27:40PM Files scanned : 84
  10/16/2018 5:27:40PM Files with detections: 0
  10/16/2018 5:27:40PM File detections : 0
  10/16/2018 5:27:40PM Files cleaned : 0
  10/16/2018 5:27:40PM Files deleted : 0
  10/16/2018 5:27:40PM Files not scanned : 0
  10/16/2018 5:27:40PM Scan Summary (Registry Scanning)
  10/16/2018 5:27:40PM Keys scanned : 0
  10/16/2018 5:27:40PM Keys detected : 0
  10/16/2018 5:27:40PM Keys cleaned : 0
  10/16/2018 5:27:40PM Keys deleted : 0
  10/16/2018 5:27:40PM Run time : 0:00:06
  10/16/2018 5:27:40PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 28122:HEAD Source
------------------------------------------------------------------------  r28122 | edk2buildsystem | 2018-10-16 02:12:28 -0700 (Tue, 16 Oct 2018) | 9 lines
  BaseTools/EOT: Change to call a program instead of calling Python API.
  Update the EOT tool to call the program itself instead of calling the Python API when parsing FV images.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Acked-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit 47f15da16053f031bcf7c50f6960bd0f6c83d2db)

------------------------------------------------------------------------