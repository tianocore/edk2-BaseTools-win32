Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2015, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 18276

This directory contains the Win32 binaries.

Build Date:       Mon, 24 Aug 2015 03:19:22 Pacific Daylight Time
Last Changed Rev: 18272

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 12.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 0.1 Build 18276
 *BootSectImage Version 0.1 Build 18276
  Ecc.exe Version 0.01 Build 17712
 *EfiLdrImage Version 0.1 Build 18276
 *EfiRom Version 0.1 Build 18276
 *GenBootSector Version 0.2 Build 18276
 *GenCrc32 Version 0.2 Build 18276
 *GenDepex.exe Version 0.04 Build 18276
 *GenFds.exe 1.0 Build 18276
 *GenFfs Version 0.1 Build 18276
 *GenFv Version 0.1 Build 18276
 *GenFw Version 0.2 Build 18276
 *GenPage Version 0.2 Build 18276
 *GenPatchPcdTable.exe Version 0.10 Build 18276
 *GenSec Version 0.1 Build 18276
 *GenVtf Version 0.1 Build 18276
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 18276
  LzmaF86Compress Version 0.2 Build 18276
 *PatchPcdValue.exe Version 0.10 Build 18276
  Rsa2048Sha256GenerateKeys Version 0.9 Build 17553
  Rsa2048Sha256Sign Version 0.9 Build 17821
 *Split Version 0.1 Build 18276
 *TargetTool.exe Version 0.01 Build 18276
 *TianoCompress Version 0.1 Build 18276
 *Trim.exe Version 0.10 Build 18276
  UEFI Packaging Tool (UEFIPT) - Revision 1.0 Build 17927
 *VfrCompile version  2.00 (UEFI 2.4) Build 18276
 *VolInfo Version 0.83 Build 18276, Aug 24 2015
 *build.exe Version 0.60 Build 18276

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/24/2015 3:19:23AM Engine version = 5700.7163
  8/24/2015 3:19:23AM AntiVirus DAT version = 7901.0
  8/24/2015 3:19:23AM Number of detection signatures in EXTRA.DAT = None
  8/24/2015 3:19:23AM Names of detection signatures in EXTRA.DAT = None
  8/24/2015 3:19:23AM Scan Started On-Demand Scan
  8/24/2015 3:19:27AM Scan Summary
  8/24/2015 3:19:27AM Processes scanned : 0
  8/24/2015 3:19:27AM Processes detected : 0
  8/24/2015 3:19:27AM Processes cleaned : 0
  8/24/2015 3:19:27AM Boot sectors scanned : 1
  8/24/2015 3:19:27AM Boot sectors detected: 0
  8/24/2015 3:19:27AM Boot sectors cleaned : 0
  8/24/2015 3:19:27AM Files scanned : 71
  8/24/2015 3:19:27AM Files with detections: 0
  8/24/2015 3:19:27AM File detections : 0
  8/24/2015 3:19:27AM Files cleaned : 0
  8/24/2015 3:19:27AM Files deleted : 0
  8/24/2015 3:19:27AM Files not scanned : 0
  8/24/2015 3:19:27AM Scan Summary (Registry Scanning)
  8/24/2015 3:19:27AM Keys scanned : 0
  8/24/2015 3:19:27AM Keys detected : 0
  8/24/2015 3:19:27AM Keys cleaned : 0
  8/24/2015 3:19:27AM Keys deleted : 0
  8/24/2015 3:19:27AM Run time : 0:00:04
  8/24/2015 3:19:27AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 18256:HEAD Source
------------------------------------------------------------------------  r18256 | bobfeng | 2015-08-20 18:09:16 -0700 (Thu, 20 Aug 2015) | 8 lines
  BaseTools: Fix build fail when the number in validlist is long type.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: "Bob Feng" <bob.c.feng@intel.com>
  Reviewed-by: "Chen, Hesheng" <hesheng.chen@intel.com>

------------------------------------------------------------------------  r18262 | lzeng14 | 2015-08-23 18:42:37 -0700 (Sun, 23 Aug 2015) | 13 lines
  BaseTools: Follow PI spec to update ExtendedSize in EFI_FFS_FILE_HEADER2
  for FFS data above 16 bytes alignment requirement.
  PI spec requires FFS header to be at 8 bytes alignment to FV header.
  And, FFS data alignment requires the beginning of the file data must
  be aligned on a particular boundary, such as 1, 16, 128 bytes or above.
  If FFS data alignment requires to be above 16 bytes, and FFS header
  must be at 8 byte alignment, so FFS header size must be multiple of 8.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Star Zeng <star.zeng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>

------------------------------------------------------------------------  r18264 | hchen30 | 2015-08-23 19:53:27 -0700 (Sun, 23 Aug 2015) | 7 lines
  BaseTools/Ecc: Remove checkpoint for STATIC modifier
  Remove checkpoint for STATIC modifier to allow this usage
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: YangX Li <yangx.li@intel.com>

------------------------------------------------------------------------  r18267 | lgao4 | 2015-08-23 22:00:05 -0700 (Sun, 23 Aug 2015) | 9 lines
  BaseTools: Add NULL pointer check in AutoGen code
  For DynamicEx PCD, if NULL pointer is specified as token space GUID,
  it will directly be used to compare GUID value in AutoGen code.
  To avoid access NULL pointer, NULL pointer will be checked first.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Star Zeng <star.zeng@intel.com>

------------------------------------------------------------------------  r18270 | lgao4 | 2015-08-23 22:01:38 -0700 (Sun, 23 Aug 2015) | 8 lines
  BaseTools: Generate macro for the size of PCD value
  PcdLib introduces new APIs to get the size of PCD value.
  BaseTools generates those macros in AutoGen code.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Reviewed-by: Star Zeng <star.zeng@intel.com>

------------------------------------------------------------------------  r18271 | lgao4 | 2015-08-23 22:02:07 -0700 (Sun, 23 Aug 2015) | 9 lines
  BaseTools: Fix AutoGen issue for Patchable VOID* PCD.
  Patchable VOID* PCD set operation should map LibPatchPcdSetPtr()
  and LibPatchPcdSetPtrS() API. This has been done when PCD is used
  in driver, but not done when PCD is used in library.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Star Zeng <star.zeng@intel.com>

------------------------------------------------------------------------  r18272 | lgao4 | 2015-08-23 22:02:35 -0700 (Sun, 23 Aug 2015) | 8 lines
  BaseTools: Update SetPcdPtr in AutoGen Code
  For patchable PCD, map SetPcdPtr() to LibPatchPcdSetPtrAndSize(),
  then the size of the updated VOID* value can be cached.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Star Zeng <star.zeng@intel.com>

------------------------------------------------------------------------