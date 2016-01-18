Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 20165, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 19661

This directory contains the Win32 binaries.

Build Date:       Mon, 18 Jan 2016 14:29:54 Pacific Standard Time
Last Changed Rev: 19651

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 19661
  BootSectImage Version 0.1 Build 19148
  Ecc.exe Version 0.01 Build 18595
  EfiLdrImage Version 0.1 Build 19148
  EfiRom Version 0.1 Build 19148
  GenBootSector Version 0.2 Build 19610
  GenCrc32 Version 0.2 Build 19148
 *GenDepex.exe Version 0.04 Build 19661
 *GenFds.exe 1.0 Build 19661
  GenFfs Version 0.1 Build 19148
  GenFv Version 0.1 Build 19610
  GenFw Version 0.2 Build 19244
  GenPage Version 0.2 Build 19148
 *GenPatchPcdTable.exe Version 0.10 Build 19661
  GenSec Version 0.1 Build 19148
  GenVtf Version 0.1 Build 19148
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 19148
  LzmaF86Compress Version 0.2 Build 19148
 *PatchPcdValue.exe Version 0.10 Build 19661
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
  Split Version 0.1 Build 19148
 *TargetTool.exe Version 0.01 Build 19661
  TianoCompress Version 0.1 Build 19148
 *Trim.exe Version 0.10 Build 19661
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 19580
  VfrCompile version  2.00 (UEFI 2.4) Build 19148
  VolInfo Version 0.83 Build 19148, Dec  7 2015
 *build.exe Version 0.60 Build 19661

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/18/2016 2:29:56PM Engine version = 5700.7163
  1/18/2016 2:29:56PM AntiVirus DAT version = 8048.0
  1/18/2016 2:29:56PM Number of detection signatures in EXTRA.DAT = None
  1/18/2016 2:29:56PM Names of detection signatures in EXTRA.DAT = None
  1/18/2016 2:29:56PM Scan Started On-Demand Scan
  1/18/2016 2:30:06PM Scan Summary
  1/18/2016 2:30:06PM Processes scanned : 0
  1/18/2016 2:30:06PM Processes detected : 0
  1/18/2016 2:30:06PM Processes cleaned : 0
  1/18/2016 2:30:06PM Boot sectors scanned : 2
  1/18/2016 2:30:06PM Boot sectors detected: 0
  1/18/2016 2:30:06PM Boot sectors cleaned : 0
  1/18/2016 2:30:06PM Files scanned : 55
  1/18/2016 2:30:06PM Files with detections: 0
  1/18/2016 2:30:06PM File detections : 0
  1/18/2016 2:30:06PM Files cleaned : 0
  1/18/2016 2:30:06PM Files deleted : 0
  1/18/2016 2:30:06PM Files not scanned : 0
  1/18/2016 2:30:06PM Scan Summary (Registry Scanning)
  1/18/2016 2:30:06PM Keys scanned : 0
  1/18/2016 2:30:06PM Keys detected : 0
  1/18/2016 2:30:06PM Keys cleaned : 0
  1/18/2016 2:30:06PM Keys deleted : 0
  1/18/2016 2:30:06PM Run time : 0:00:11
  1/18/2016 2:30:06PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 19610:HEAD Source
------------------------------------------------------------------------  r19636 | yzhu52 | 2016-01-10 23:42:03 -0800 (Sun, 10 Jan 2016) | 5 lines
  BaseTools/VfrCompile: honor CC if it is set
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Michael Thomas <malinka@entropy-development.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>

------------------------------------------------------------------------  r19649 | yzhu52 | 2016-01-17 17:42:20 -0800 (Sun, 17 Jan 2016) | 9 lines
  BaseTools: Fix GenPatchPcdTable to support '-' characters in file names
  The Regular Expression parsing of lines in MAP files does not currently
  support the use of '-' in the column for the filename the symbol is
  sources from, it cause a build break from the GenPatchPcdTable.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r19650 | yzhu52 | 2016-01-17 17:46:25 -0800 (Sun, 17 Jan 2016) | 11 lines
  BaseTools: VOID* PCDs in VPD region must be aligned based on value type
  Base on build spec update, ASCII strings(“string”), will be byte aligned,
  Unicode strings(L”string”) will be two-byte aligned, Byte arrays,
  {0x00, 0x01} will be 8-byte aligned.
  This patch is going to halt with an error message if a VOID* PCD has an
  offset value that is not aligned based on the syntax of the PCD value.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r19651 | yzhu52 | 2016-01-17 17:47:50 -0800 (Sun, 17 Jan 2016) | 11 lines
  BaseTools: VPD Tool to allocate VPD region be aligned based on value type
  Base on build spec update, ASCII strings(“string”), will be byte aligned,
  Unicode strings(L”string”) will be two-byte aligned, Byte arrays,
  {0x00, 0x01} will be 8-byte aligned.
  This patch is going to update VPD Tool to allocate VOID* PCDs to an offset
  value that is aligned based in syntax of the PCD value.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------