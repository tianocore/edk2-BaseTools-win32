Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 27306

This directory contains the Win32 binaries.

Build Date:       Fri, 08 Jun 2018 15:21:01 Pacific Daylight Time
Last Changed Rev: 27302

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.14 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 27306
  BootSectImage Version 1.0 Build Build 27191
  Brotli Version 0.5.2 Build 27191
  Brotli Version 0.5.2 Build 27191
  DevicePath Version 0.1 Build 27191
 *Ecc.exe Version 1.0 Build Build 27306
  EfiLdrImage Version 1.0 Build Build 27191
  EfiRom Version 0.1 Build 27191
  GenBootSector Version 0.2 Build 27191
  GenCrc32 Version 0.2 Build 27191
 *GenDepex.exe Version 0.04 Build 27306
 *GenFds.exe 1.0 Build 27306
  GenFfs Version 0.1 Build 27191
  GenFv Version 0.1 Build 27191
 *GenFw Version 0.2 Build 27306
  GenPage Version 0.2 Build 27191
 *GenPatchPcdTable.exe Version 0.10 Build 27306
  GenSec Version 0.1 Build 27191
  GenVtf Version 0.1 Build 27191
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 27191
  LzmaF86Compress Version 0.2 Build 27191
 *PatchPcdValue.exe Version 0.10 Build 27306
  Pkcs7Sign Version 0.9 Build 27191
  Rsa2048Sha256GenerateKeys Version 0.9 Build 27191
  Rsa2048Sha256Sign Version 0.9 Build 27191
  Split Version 1.0 Build Build 27191
 *TargetTool.exe Version 0.01 Build 27306
  TianoCompress Version 0.1 Build 27191
 *Trim.exe Version 0.10 Build 27306
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 27191
  VfrCompile version  2.01 (UEFI 2.4) Build Build 27191
 *VolInfo Version 1.0 Build Build 27306
 *build.exe Version 0.60 Build 27306

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  6/8/2018 3:21:03PM Engine version = 5900.7806
  6/8/2018 3:21:03PM AntiVirus DAT version = 8918.0
  6/8/2018 3:21:03PM Number of detection signatures in EXTRA.DAT = None
  6/8/2018 3:21:03PM Names of detection signatures in EXTRA.DAT = None
  6/8/2018 3:21:03PM Scan Started On-Demand Scan
  6/8/2018 3:21:09PM Scan Summary
  6/8/2018 3:21:09PM Processes scanned : 0
  6/8/2018 3:21:09PM Processes detected : 0
  6/8/2018 3:21:09PM Processes cleaned : 0
  6/8/2018 3:21:09PM Boot sectors scanned : 2
  6/8/2018 3:21:09PM Boot sectors detected: 0
  6/8/2018 3:21:09PM Boot sectors cleaned : 0
  6/8/2018 3:21:09PM Files scanned : 68
  6/8/2018 3:21:09PM Files with detections: 0
  6/8/2018 3:21:09PM File detections : 0
  6/8/2018 3:21:09PM Files cleaned : 0
  6/8/2018 3:21:09PM Files deleted : 0
  6/8/2018 3:21:09PM Files not scanned : 0
  6/8/2018 3:21:09PM Scan Summary (Registry Scanning)
  6/8/2018 3:21:09PM Keys scanned : 0
  6/8/2018 3:21:09PM Keys detected : 0
  6/8/2018 3:21:09PM Keys cleaned : 0
  6/8/2018 3:21:09PM Keys deleted : 0
  6/8/2018 3:21:09PM Run time : 0:00:06
  6/8/2018 3:21:09PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 27191:HEAD Source
------------------------------------------------------------------------  r27191 | edk2buildsystem | 2018-05-16 02:05:29 -0700 (Wed, 16 May 2018) | 10 lines
  BaseTools: Fix --hash Package and Module hash value.
  The order of List enumeration is arbitrary.
  Need to be sorted while calculating Package/Module hash, otherwise it
  generate different hash value even nothing changes.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Derek Lin <derek.lin2@hpe.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 3f34e36d04a8de4992a696f738643b5a11261469)

------------------------------------------------------------------------  r27221 | edk2buildsystem | 2018-05-22 14:05:47 -0700 (Tue, 22 May 2018) | 17 lines
  BaseTools: Fix bug PCD type in component is not same with Pcd section
  Per DSC spec 3.11 [Components] Sections:
  The PCD access methods (and storage methods) are selected on a platform
  basis - it is not permitted to have a PCD listed in one of the Pcd
  sections and use it differently in an individual module. For example,
  if a PCD is listed in a [PcdsFixedAtBuild] section, it is not permitted
  to list it in a <PcdsPatchableInModule> sub-section of an INF file.
  but current code doesn't report error for this case.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=951
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 74f59e927520f50c4ebeeb2ccaa8e611b7d48dd1)

------------------------------------------------------------------------  r27222 | edk2buildsystem | 2018-05-22 14:06:06 -0700 (Tue, 22 May 2018) | 13 lines
  BaseTools: Library PCD type will inherit from the driver
  If a PCD is not referenced in global PCD section of DSC file at all,
  but is referenced in module scope, then the default PCD type for libs
  should be the module scoped PCD type.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=901
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 5a444dfd7c0039b33f0c26e1294297fb7e358f60)

------------------------------------------------------------------------  r27223 | edk2buildsystem | 2018-05-22 14:06:19 -0700 (Tue, 22 May 2018) | 25 lines
  BaseTools: Report more clear error message when PCD type mismatch
  Error message is not clear when PCD type defined in driver's Library
  is different with PCD type defined in DSC components or PCD type
  defined in DSC PCD section.
  Case as below:
  DSC:
  [PcdsFixedAtBuild]
  PcdToken.PcdCName | "A"
  [Components]
  TestPkg/TestDriver.inf {
  <PcdsPatchableInModule>
  PcdToken.PcdCName | "B"
  }
  Library:
  [Pcd]
  PcdToken.PcdCName
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a253d217ee3477fde46cadba0dfe364f9a826694)

------------------------------------------------------------------------  r27224 | edk2buildsystem | 2018-05-22 14:06:32 -0700 (Tue, 22 May 2018) | 15 lines
  BaseTools: Enhance error message when file is not exist for Gensec
  When the file is not exist in workspace or packages path, current
  Gensec tool doesn't report exactly error message.
  FILE FV_IMAGE = 11111111-4CF1-42D8-A0C3-B3F60779dF4D  {
  SECTION GUIDED A7717414-C616-4977-9420-844712A735BF {
  SECTION FV_IMAGE = TestPkg/Test.fd
  }
  }
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit 75135cc6988e7e7e84b7f3652f570bb8742841e0)

------------------------------------------------------------------------  r27232 | edk2buildsystem | 2018-05-23 02:09:22 -0700 (Wed, 23 May 2018) | 16 lines
  BaseTools/Workspace: Fix ValueChain set
  Commit 88252a90d1ca7846731cd2e4e8e860454f7d97a3 changed ValueChain
  from a dict to a set, but also changed the (former) key type from a
  touple to two separate values, which was probably unintended and also
  breaks build for packages involving Structured PCDs, because add()
  only takes one argument.
  This commit changes the values back to touples.
  V2:
  - Removed a whitespace change.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Marvin Haeuser <Marvin.Haeuser@outlook.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1d4f84f9f42525356aaf25033ab541c0225b3886)

------------------------------------------------------------------------  r27250 | edk2buildsystem | 2018-05-28 02:05:42 -0700 (Mon, 28 May 2018) | 14 lines
  BaseTools: loop to retry remove when it fails.
  There is a common race condition when the OS fails to release a file
  fast enough.  this adds a retry loop.
  v2 - Add a timeout.
  Cc: Mike Kinney <michael.d.kinney@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit efa88d51da7163200f13dfc796a328847c45a058)

------------------------------------------------------------------------  r27251 | edk2buildsystem | 2018-05-28 02:06:04 -0700 (Mon, 28 May 2018) | 8 lines
  BaseTools: Add missing content to EOT tool.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit e95a0dfb46339d459add8af848d5042ec6ff9a8d)

------------------------------------------------------------------------  r27252 | edk2buildsystem | 2018-05-28 02:06:18 -0700 (Mon, 28 May 2018) | 13 lines
  BaseTools/GenFds: Remove redundant GetRealFileLine call
  The EvaluateConditional function should not call GetRealFileLine
  because this is already done in Warning init and only needs to be
  calculated in the event of a parsing failure. This fix stops
  InsertedLines from being subtracted twice during error handling.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zurcher, Christopher J <christopher.j.zurcher@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 20274d2389eb012812f4561c8eb7cffc57a68850)

------------------------------------------------------------------------  r27255 | edk2buildsystem | 2018-05-28 02:11:00 -0700 (Mon, 28 May 2018) | 12 lines
  BaseTools: Rename String to StringUtils.
  For case-insensitive file systems, edk2 String.py collides with the
  Python string.py, which results in build errors. This,for example,
  applies to building via the Windows Subsystem for Linux from a
  DriveFS file system. This patch renames String to StringUtils to
  prevent conflicts for case-insensitive file systems.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Marvin Haeuser <Marvin.Haeuser@outlook.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5a57246eab80f00ae2481970d12a2abc345a2730)

------------------------------------------------------------------------  r27288 | edk2buildsystem | 2018-06-06 02:05:49 -0700 (Wed, 06 Jun 2018) | 10 lines
  BaseTools: Sort PCD by token space first then by PcdCName
  Sort PCD by token space first, then by PcdCName in the build report.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 238d9b5c64520acdd784667a29326804dde7ea31)

------------------------------------------------------------------------  r27289 | edk2buildsystem | 2018-06-06 02:06:20 -0700 (Wed, 06 Jun 2018) | 12 lines
  BaseTools: Display both Hex and integer value format of PCD value
  If the PCD's datum type is UINT8, UINT16, UINT32 or UINT64, then in
  the report will display both hexadecimal format and integer format
  of PCD value.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 179c2f97f949509ec55f0ec7cb84480fb0c015a7)

------------------------------------------------------------------------  r27290 | edk2buildsystem | 2018-06-06 02:06:31 -0700 (Wed, 06 Jun 2018) | 10 lines
  BaseTools/VolInfo: Update EFI FV FILETYPES for new MM types.
  Add support for the following types to VolInfo:
  EFI_FV_FILETYPE_MM_STANDALONE
  EFI_FV_FILETYPE_MM_CORE_STANDALONE
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Ezra Godfrey <egodfrey.qdt@qualcommdatacenter.com>
  Reviewed-by: Jiewen Yao <jiewen.yao@intel.com>
  (cherry picked from commit cb004eb0ad308a4bac86037ce67a56d9ed924e50)

------------------------------------------------------------------------  r27301 | edk2buildsystem | 2018-06-08 02:05:56 -0700 (Fri, 08 Jun 2018) | 11 lines
  BaseTools: Check elf sections alignment with MAX_COFF_ALIGNMENT
  Add the logic to check whether mCoffAlignment is larger than
  MAX_COFF_ALIGNMENT, and report error for it.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 3f0218003141ae38152f5a2520c969445afc721f)

------------------------------------------------------------------------  r27302 | edk2buildsystem | 2018-06-08 02:06:27 -0700 (Fri, 08 Jun 2018) | 11 lines
  BaseTools: Fix Section header size larger than elf file size bug
  Add the logic to handle the case that Section header size larger than
  elf file size.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d78675d1956aaae05d5db872eddd4119a01d0ecb)

------------------------------------------------------------------------