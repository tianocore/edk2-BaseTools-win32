Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 27752

This directory contains the Win32 binaries.

Build Date:       Mon, 20 Aug 2018 15:48:17 Pacific Daylight Time
Last Changed Rev: 27749

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.14 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
ERROR : This tool is missing --version option: BPDG.exe
 *BootSectImage Version 1.0 Build Build 27752
  Brotli Version 0.5.2 Build 27191
  Brotli Version 0.5.2 Build 27191
 *DevicePath Version 0.1 Build 27752
  Ecc.exe Version 1.0 Build Build 27306
 *EfiLdrImage Version 1.0 Build Build 27752
 *EfiRom Version 0.1 Build 27752
 *GenBootSector Version 0.2 Build 27752
 *GenCrc32 Version 0.2 Build 27752
 *GenDepex.exe Version 0.04 Build 27752
ERROR : This tool is missing --version option: GenFds.exe
 *GenFfs Version 0.1 Build 27752
 *GenFv Version 0.1 Build 27752
 *GenFw Version 0.2 Build 27752
 *GenPage Version 0.2 Build 27752
 *GenPatchPcdTable.exe Version 0.10 Build 27752
 *GenSec Version 0.1 Build 27752
 *GenVtf Version 0.1 Build 27752
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 27752
 *LzmaF86Compress Version 0.2 Build 27752
 *PatchPcdValue.exe Version 0.10 Build 27752
 *Pkcs7Sign Version 0.9 Build 27752
 *Rsa2048Sha256GenerateKeys Version 0.9 Build 27752
 *Rsa2048Sha256Sign Version 0.9 Build 27752
  Split Version 1.0 Build Build 27191
 *TargetTool.exe Version 0.01 Build 27752
 *TianoCompress Version 0.1 Build 27752
 *Trim.exe Version 0.10 Build 27752
 *UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 27752
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 27752
 *VolInfo Version 1.0 Build Build 27752
 *build.exe Version 0.60 Build 27752

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  8/20/2018 3:48:20PM Engine version = 5900.7806
  8/20/2018 3:48:20PM AntiVirus DAT version = 8991.0
  8/20/2018 3:48:20PM Number of detection signatures in EXTRA.DAT = None
  8/20/2018 3:48:20PM Names of detection signatures in EXTRA.DAT = None
  8/20/2018 3:48:20PM Scan Started On-Demand Scan
  8/20/2018 3:48:31PM Scan Summary
  8/20/2018 3:48:31PM Processes scanned : 0
  8/20/2018 3:48:31PM Processes detected : 0
  8/20/2018 3:48:31PM Processes cleaned : 0
  8/20/2018 3:48:31PM Boot sectors scanned : 2
  8/20/2018 3:48:31PM Boot sectors detected: 0
  8/20/2018 3:48:31PM Boot sectors cleaned : 0
  8/20/2018 3:48:31PM Files scanned : 82
  8/20/2018 3:48:31PM Files with detections: 0
  8/20/2018 3:48:31PM File detections : 0
  8/20/2018 3:48:31PM Files cleaned : 0
  8/20/2018 3:48:31PM Files deleted : 0
  8/20/2018 3:48:31PM Files not scanned : 0
  8/20/2018 3:48:31PM Scan Summary (Registry Scanning)
  8/20/2018 3:48:31PM Keys scanned : 0
  8/20/2018 3:48:31PM Keys detected : 0
  8/20/2018 3:48:31PM Keys cleaned : 0
  8/20/2018 3:48:31PM Keys deleted : 0
  8/20/2018 3:48:31PM Run time : 0:00:12
  8/20/2018 3:48:31PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 27306:HEAD Source
------------------------------------------------------------------------  r27310 | edk2buildsystem | 2018-06-11 17:39:59 -0700 (Mon, 11 Jun 2018) | 10 lines
  BaseTools/UPT: Update the import statement to use StringUtils
  The patch 5a57246eab80 Rename String to StringUtils, but it didn't
  update the UPT Tool for the import statement which cause UPT tool
  break.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 64285f15264906c761b5a6772b5b590b32caa03c)

------------------------------------------------------------------------  r27316 | edk2buildsystem | 2018-06-11 17:42:41 -0700 (Mon, 11 Jun 2018) | 9 lines
  BaseTools: Remove dsc nested include checking.
  The dsc nested include checking make unexpected build error when
  building project A and switch to project B.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Derek Lin <derek.lin2@hpe.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 5163d89398c541ab03e8f6f6ab6ed479e95b4be9)

------------------------------------------------------------------------  r27326 | edk2buildsystem | 2018-06-13 02:05:49 -0700 (Wed, 13 Jun 2018) | 13 lines
  BaseTools: Fix one bug of nest !include parser
  The case is DSC file include file1, file1 include file2, after parse
  file2 finished, DSC parser get the wrong section type, then it would
  report invalid error.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Tested-by: Michael D Kinney <michael.d.kinney@intel.com>
  (cherry picked from commit 46e4b3940e2f1862aa605900616a543a43f17222)

------------------------------------------------------------------------  r27327 | edk2buildsystem | 2018-06-13 02:06:11 -0700 (Wed, 13 Jun 2018) | 10 lines
  BaseTools: refactor to remove functions
  refactoring almost identical functions to delete and use the other.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit c14b58614ffb992dfc668966a19becb86614aafc)

------------------------------------------------------------------------  r27328 | edk2buildsystem | 2018-06-13 02:06:39 -0700 (Wed, 13 Jun 2018) | 8 lines
  BaseTools: Cleanup unneeded code
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit caf744956d4c8c0ef358bdc3df2cdb10265c2ea8)

------------------------------------------------------------------------  r27333 | edk2buildsystem | 2018-06-14 02:05:31 -0700 (Thu, 14 Jun 2018) | 9 lines
  BaseTools: remove including Base.h if the module type is not BASE
  According the module type to include the header file.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=867
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b1aff264bf6a007a27d0ebadcce96b72b727c3c8)

------------------------------------------------------------------------  r27356 | edk2buildsystem | 2018-06-19 02:05:58 -0700 (Tue, 19 Jun 2018) | 11 lines
  BaseTools/WorkspaceCommon: Import used BuildToolError messages.
  Commit c14b58614ffb992dfc668966a19becb86614aafc added a few build
  error message display calls to WorkspaceCommon.py without importing
  the message resources explicitely. This commit adds imports the
  missing directives.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Marvin Haeuser <Marvin.Haeuser@outlook.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 87a46244723ad8ddce2fcf611e569ada86dc80f2)

------------------------------------------------------------------------  r27372 | edk2buildsystem | 2018-06-22 02:05:42 -0700 (Fri, 22 Jun 2018) | 8 lines
  BaseTools: remove the unneeded code
  Do a clean up to remove the unneeded code.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c91fb6b4fc8b484e13ba180fa12c6736908d8017)

------------------------------------------------------------------------  r27373 | edk2buildsystem | 2018-06-22 02:06:03 -0700 (Fri, 22 Jun 2018) | 10 lines
  BaseTools: Enhance BaseTools supports FeaturePcd usage in VFR file
  Bugzilla 348 only fixed FixedAtBuild Pcd type, now this patch also add
  support for FeaturePcd type.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=348
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 58cf30f71f03bcf2fbf369d51e05c8f17176e129)

------------------------------------------------------------------------  r27374 | edk2buildsystem | 2018-06-22 02:06:27 -0700 (Fri, 22 Jun 2018) | 14 lines
  BaseTools: introduce !error statement
  The DSC and FDF file can use `!error` statement. The argument of this
  statement is an error message, it causes build tool to stop at the
  location where the statement is encountered and error message following
  the `!error` statement is output as a message.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=701
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 09ef8e92580caddc24f8f1db6ea0e8223890085f)

------------------------------------------------------------------------  r27403 | edk2buildsystem | 2018-06-27 02:09:09 -0700 (Wed, 27 Jun 2018) | 11 lines
  BaseTools: Refactor python except statements
  Convert "except ... ," to "except ... as" to be compatible with python3.
  Based on "futurize -f lib2to3.fixes.fix_except"
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 5b0671c1e514e534c6d5be9604da33bfc2cd0a24)

------------------------------------------------------------------------  r27404 | edk2buildsystem | 2018-06-27 02:10:43 -0700 (Wed, 27 Jun 2018) | 11 lines
  BaseTools: Refactor python print statements
  Refactor print statements to be compatible with python 3.
  Based on "futurize -f libfuturize.fixes.fix_print_with_import"
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 72443dd25014a8b6209895640af36dec33da51e0)

------------------------------------------------------------------------  r27405 | edk2buildsystem | 2018-06-27 02:11:30 -0700 (Wed, 27 Jun 2018) | 10 lines
  BaseTools: Remove the old python "not-equal"
  Replace "<>" with "!=" to be compatible with python3.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 87d2afd07c822e6d5ab12bc8dc0f0bfa31bea679)

------------------------------------------------------------------------  r27406 | edk2buildsystem | 2018-06-27 02:11:54 -0700 (Wed, 27 Jun 2018) | 11 lines
  BaseTools: Remove tuple parameter in python scripts
  According to PEP3113, tuple parameter is removed in python 3.
  (PEP3113: https://www.python.org/dev/peps/pep-3113/)
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 890d8ede6867dd43d96b5b04454f0b571938e3a3)

------------------------------------------------------------------------  r27407 | edk2buildsystem | 2018-06-27 02:12:55 -0700 (Wed, 27 Jun 2018) | 11 lines
  BaseTools: Remove the deprecated hash_key()
  Replace "has_key()" with "in" to be compatible with python3.
  Based on "futurize -f lib2to3.fixes.fix_has_key"
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 27c4ceb41cf6b79d440deae215c68e117d69d641)

------------------------------------------------------------------------  r27408 | edk2buildsystem | 2018-06-27 02:13:19 -0700 (Wed, 27 Jun 2018) | 11 lines
  BaseTools: Replace StandardError with Expression
  StandardError has been removed from python 3.
  Replace it with Exception.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 92beb1e4c73a40a708c7c0cade5c7cee314b3887)

------------------------------------------------------------------------  r27411 | edk2buildsystem | 2018-06-27 02:15:25 -0700 (Wed, 27 Jun 2018) | 10 lines
  BaseTools: Adjust the spaces around commas and colons
  Based on "futurize -f lib2to3.fixes.fix_ws_comma"
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ccaa7754a29728df0a7485932aab4909f6be116a)

------------------------------------------------------------------------  r27412 | edk2buildsystem | 2018-06-27 02:16:11 -0700 (Wed, 27 Jun 2018) | 11 lines
  BaseTools: Migrate to the new octal literal
  Change the octal literals according to PEP3127
  https://www.python.org/dev/peps/pep-3127/
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 2617a73c3628473bacea887d885bdd1e7808ccc6)

------------------------------------------------------------------------  r27413 | edk2buildsystem | 2018-06-27 02:17:16 -0700 (Wed, 27 Jun 2018) | 35 lines
  BaseTools: Fix old python2 idioms
  Based on "futurize -f lib2to3.fixes.fix_idioms"
  * Change some type comparisons to isinstance() calls:
  type(x) == T -> isinstance(x, T)
  type(x) is T -> isinstance(x, T)
  type(x) != T -> not isinstance(x, T)
  type(x) is not T -> not isinstance(x, T)
  * Change "while 1:" into "while True:".
  * Change both
  v = list(EXPR)
  v.sort()
  foo(v)
  and the more general
  v = EXPR
  v.sort()
  foo(v)
  into
  v = sorted(EXPR)
  foo(v)
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0d1f5b2b5dc3c1cf381be0a1ec8f960dc6029a93)

------------------------------------------------------------------------  r27414 | edk2buildsystem | 2018-06-27 02:18:07 -0700 (Wed, 27 Jun 2018) | 12 lines
  BaseTools: Replace StringIO.StringIO with io.BytesIO
  Replace StringIO.StringIO with io.BytesIO to be compatible with python3.
  This commit also removes "import StringIO" from those python scripts
  that don't really use it.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 86379ac48ba17c71d4623c57099b064b15118e21)

------------------------------------------------------------------------  r27415 | edk2buildsystem | 2018-06-27 02:18:42 -0700 (Wed, 27 Jun 2018) | 11 lines
  BaseTools: AutoGen - Remove unused variables.
  There are 2 variables that we populate, but never use.
  remove them entirely.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 3c920616bb22c7f08d473ee555c1f51930aba35e)

------------------------------------------------------------------------  r27417 | edk2buildsystem | 2018-06-28 02:06:09 -0700 (Thu, 28 Jun 2018) | 10 lines
  BaseTools: Move variable out of Global
  Move single use list from GlobalData (gTempInfs) into the file that uses it as _TempInfs
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 2b5c643ae8f7e72a56deeacead6b5302a076d329)

------------------------------------------------------------------------  r27442 | edk2buildsystem | 2018-06-29 02:05:56 -0700 (Fri, 29 Jun 2018) | 27 lines
  BaseTools: Fix parsing multiple nest !include issue
  Fix the bug !include file in Components subsection meet syntax error.
  Case example:
  DSC components:
  !include Test1.txt
  Test1.txt:
  TestPkg/TestDriver.inf {
  <PcdsFixedAtBuild>
  PcdToken.PcdTest1 | "A"
  !include Test2.txt
  }
  Test2.txt:
  !include Test3.txt
  Test3.txt:
  PcdToken.PcdTest2 | "B"
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit cd7bd491f3f9c43e4bb6c9516784ef3a09b6e337)

------------------------------------------------------------------------  r27443 | edk2buildsystem | 2018-06-29 02:06:18 -0700 (Fri, 29 Jun 2018) | 22 lines
  BaseTools: Fix two drivers include the same file issue
  Two drivers include the same PCD file, the PCD value in the first
  driver is correct, but it in the second driver is incorrect.
  DSC:
  [Components]
  Testpkg/Testdriver1.inf {
  <PcdsFixedAtBuild>
  !include Test.txt
  }
  Testpkg/Testdriver2.inf {
  <PcdsFixedAtBuild>
  !include Test.txt
  }
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 395f33368620e13b64f7f5c10fd1d87c7559a2fc)

------------------------------------------------------------------------  r27444 | edk2buildsystem | 2018-06-29 02:06:38 -0700 (Fri, 29 Jun 2018) | 12 lines
  BaseTools: AutoGen - clean up access
  1) add a property so others can access needed data
  2) change GenMake to use property
  3) add local variable in GenMake to speed up access
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7c12d613ba78d2b5ab781a91bbb011304ffab705)

------------------------------------------------------------------------  r27445 | edk2buildsystem | 2018-06-29 02:06:56 -0700 (Fri, 29 Jun 2018) | 10 lines
  BaseTools: AutoGen - move constructor out of loop
  Create the 2 comparison objects once outside the loop.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b420d9850282ebbcb452ce24ac42f27802fa0c70)

------------------------------------------------------------------------  r27479 | edk2buildsystem | 2018-07-04 02:05:32 -0700 (Wed, 04 Jul 2018) | 29 lines
  BaseTools/Trim: Normalize filepaths to fix comparisons on Windows
  When using Linaro GCC5+ arm-eabi toolchain on Windows, the generated
  DSDT.iii contains a canonicalized ("\.\" removed and lower case)
  filepath for the preprocessed DSDT.i file in the first line.
  Trim.exe is called on DSDT.iii to generate DSDT.iiii, which does a
  line for line comparison of filepaths encountered to the preprocessed
  DSDT.i filepath found in the first line to determine what lines to
  place in DSDT.iiii. Since the DSDT.i filepath is canonicalized and
  all later filepaths in DSDT.iii are not canonicalized, all comparisons
  fail and the result is in an empty DSDT.iiii.
  Issue was first reported to Linaro here:
  https://bugs.linaro.org/show_bug.cgi?id=2909
  where the recommendation was to address the issue in Trim.exe.
  This patch normalizes the case and pathname of all filepaths
  encountered during Trim.exe execution on preprocessed files.  This
  fixes comparisons of filepaths that contain mismatching case on
  case-insensitive filesystems, redundant separators, and uplevel
  references.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Christopher Co <christopher.co@microsoft.com>
  Cc: Leif Lindholm <leif.lindholm@linaro.org>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5895956dd955714c0e578a413d0e289153cc9eea)

------------------------------------------------------------------------  r27489 | edk2buildsystem | 2018-07-08 02:05:44 -0700 (Sun, 08 Jul 2018) | 10 lines
  BaseTools: Remove the old python "not-equal" in DscBuildData.py
  Replace "<>" with "!=" to be compatible with python3.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 9fb2cbdac4cb3122d72223cff02395daf751e365)

------------------------------------------------------------------------  r27490 | edk2buildsystem | 2018-07-08 02:06:08 -0700 (Sun, 08 Jul 2018) | 19 lines
  BaseTools: Unify long and int in Expression.py
  Per PEP237(*), 'long' is unified with 'int' and removed from python3.
  * To make the script compatible with both python2 and python3,
  'type(0L)' is replaced with 'type(sys.maxsize + 1)'. In python2,
  the number is 'long', while it's 'int' in python3. We can remove
  the workaround after moving to python3 completely.
  * long() is replaced with int() since int() returns a long when need.
  (*) https://www.python.org/dev/peps/pep-0237/
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 39456d00f36e04b7e7efb208f350f4e83b6c3531)

------------------------------------------------------------------------  r27491 | edk2buildsystem | 2018-07-09 02:10:36 -0700 (Mon, 09 Jul 2018) | 11 lines
  BaseTools: Clean up source files
  1. Do not use tab characters
  2. No trailing white space in one line
  3. All files must end with CRLF
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit f7496d717357b9af78414d19679b073403812340)

------------------------------------------------------------------------  r27492 | edk2buildsystem | 2018-07-09 02:12:34 -0700 (Mon, 09 Jul 2018) | 10 lines
  BaseTool: Add cache for the result of SkipAutogen.
  Add a cache for the value of skip ModuleAutoGen
  process flag. This cache can improve build performance.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 18ef4e713f2fb5d2f84d179b9861b4afee212f65)

------------------------------------------------------------------------  r27494 | edk2buildsystem | 2018-07-10 02:05:37 -0700 (Tue, 10 Jul 2018) | 11 lines
  BaseTools: Fix the bug that incorrect size info in the Lib autogen
  The case is a PCD used in one library only, and in DSC component
  section the PCD value is override in one of module inf. Then it cause
  the bug the PCD size in the Lib autogen use the PCD value in the DSC
  PCD section, but not use the override value.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9edba51f93d8e81e09f905afc994efe02dbe524e)

------------------------------------------------------------------------  r27500 | edk2buildsystem | 2018-07-11 02:06:38 -0700 (Wed, 11 Jul 2018) | 45 lines
  BaseTools/GenFw: Add X64 GOTPCREL Support to GenFw
  Adds support for the following X64 ELF relocations to GenFw
  R_X86_64_GOTPCREL
  R_X86_64_GOTPCRELX
  R_X86_64_REX_GOTPCRELX
  Background:
  The GCC49 and GCC5 toolchains use the small pie model for X64.  In the
  small pie model, gcc emits a GOTPCREL relocation whenever C code takes
  the address of a global function.  The emission of GOTPCREL is mitigated
  by several factors
  1. In GCC49, all global symbols are declared hidden thereby eliminating
  the emission of GOTPCREL.
  2. In GCC5, LTO is used.  In LTO, the complier first creates intermediate
  representation (IR) files.  During the static link stage, the LTO compiler
  combines all IR files as a single compilation unit, using linker symbol
  assistance to generate code.  Any global symbols defined in the IR that
  are not referenced from outside the IR are converted to local symbols -
  thereby eliminating the emission of GOTPCREL for them.
  3. The linker (binutils ld) further transforms any GOTPCREL used with
  the movq opcode to a direct rip-relative relocation used with the leaq
  opcode.  This linker optimization can be disabled with the option
  -Wl,--no-relax.  Furthermore, gcc is able to emit GOTPCREL with other
  opcodes
  - pushq opcode for passing arguments to functions.
  - addq/subq opcodes for pointer arithmetic.
  These other opcode uses are not transformed by the linker.
  Ultimately, in GCC5 there are some emissions of GOTPCREL that survive
  all these mitigations - if C code takes the address of a global function
  defined in assembly code - and performs pointer arithmetic on the
  address - then the GOTPCREL remains in the final linker product.
  A GOTPCREL relocation today causes the build to stop since GenFw does
  not handle them.  It is possible to eliminate any remaining GOTPCREL
  emissions by manually declaring the global symbols causing them to have
  hidden visibility.  This patch is offered instead to allow GenFw to
  handle any residual GOTPCREL.
  Cc: Shi Steven <steven.shi@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zenith432 <zenith432@users.sourceforge.net>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit ecbaa856da0c94b7054f795d001ee3f5aaee033e)

------------------------------------------------------------------------  r27501 | edk2buildsystem | 2018-07-11 02:06:48 -0700 (Wed, 11 Jul 2018) | 9 lines
  BaseTools/GenFw: Disable support for R_X86_64_32S
  REF:https://bugzilla.tianocore.org/show_bug.cgi?id=999
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zenith432 <zenith432@users.sourceforge.net>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c6a14de3ef30291918f3b15436cf6a75db413eea)

------------------------------------------------------------------------  r27504 | edk2buildsystem | 2018-07-12 02:06:58 -0700 (Thu, 12 Jul 2018) | 10 lines
  BaseTool: Fixed the incorrect cache key.
  This patch is to fix the incorrect cache key of
  skip ModuleAutoGen cache.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 0a563f3fecfd9baffe8dce51bb4411d6a748a936)

------------------------------------------------------------------------  r27516 | edk2buildsystem | 2018-07-16 02:06:09 -0700 (Mon, 16 Jul 2018) | 7 lines
  BaseTools: Enable structure pcd in FDF file
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 543f5ac30facfbb40eafb2b4908649a427784080)

------------------------------------------------------------------------  r27518 | edk2buildsystem | 2018-07-16 02:06:46 -0700 (Mon, 16 Jul 2018) | 51 lines
  BaseTools: Use absolute import in GenFds
  Based on "futurize -f libfuturize.fixes.fix_absolute_import"
  Since circular import is not allowed after adopting absolute import, the
  following changes are applied to break the circles.
  * BaseTools/Source/Python/GenFds/Capsule.py
  - Delay "from .GenFds import GenFds" until GenCapsule()
  - Delay "from .GenFds import FindExtendTool" until GenFmpCapsule()
  To break the circle:
  AutoGen.AutoGen => GenFds.FdfParser => GenFds.Capsule => GenFds.GenFds =>
  GenFds.FdfParser
  * BaseTools/Source/Python/GenFds/Fd.py
  - Delay "from .GenFds import GenFds" until GenFd()
  To break the circle:
  AutoGen.AutoGen => GenFds.FdfParser => GenFds.Fd => GenFds.GenFds =>
  GenFds.FdfParser
  * BaseTools/Source/Python/GenFds/Fv.py
  - Delay "from .GenFds import GenFds" until AddToBuffer()
  To break the circle:
  AutoGen.AutoGen => GenFds.FdfParser => GenFds.Fd => GenFds.Fv =>
  GenFds.GenFds => GenFds.FdfParser
  * BaseTools/Source/Python/GenFds/GuidSection.py
  - Delay "from .GenFds import FindExtendTool" until GuidSection()
  To break the circle:
  AutoGen.AutoGen => GenFds.FdfParser => GenFds.Fd => GenFds.Fv =>
  GenFds.AprioriSection => GenFds.FfsFileStatement => GenFds.GuidSection =>
  GenFds.GenFds => GenFds.FdfParser
  * BaseTools/Source/Python/GenFds/OptRomInfStatement.py
  - Delay "from . import OptionRom" until __GetOptRomParams()
  To break the circle:
  AutoGen.AutoGen => GenFds.FdfParser => GenFds.OptionRom =>
  GenFds.OptRomInfStatement => GenFds.OptionRom
  * BaseTools/Source/Python/GenFds/OptionRom.py
  - Remove the unused "from GenFds import GenFds"
  To break the circle:
  AutoGen.AutoGen => GenFds.FdfParser => GenFds.OptionRom =>
  GenFds.GenFds => GenFds.FdfParser
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit bfa65b61dde887a9586e070101202bd37e3221fd)

------------------------------------------------------------------------  r27519 | edk2buildsystem | 2018-07-16 02:07:09 -0700 (Mon, 16 Jul 2018) | 12 lines
  BaseTools: Move OverrideAttribs to OptRomInfStatement.py
  Move "class OverrideAttribs" to OptRomInfStatement.py to remove
  "import OptionRom" which may form a circular import:
  GenFds.OptionRom => GenFds.OptRomInfStatement => GenFds.OptionRom
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit 8f3f5794b4b0027ee118fc6e03ea01620e6cd9d4)

------------------------------------------------------------------------  r27520 | edk2buildsystem | 2018-07-16 02:07:38 -0700 (Mon, 16 Jul 2018) | 26 lines
  BaseTools: Move FindExtendTool to GenFdsGlobalVariable.py
  Importing "FindExtendTool" from GenFds.GenFds could create the following
  circular imports:
  * GenFds.FdfParser => GenFds.Capsule => GenFds.GenFds => GenFds.FdfParser
  * GenFds.FdfParser => GenFds.Fd => GenFds.Fv => GenFds.AprioriSection =>
  GenFds.FfsFileStatement => GenFds.GuidSection => GenFds.GenFds =>
  GenFds.FdfParser
  This commit moves "FindExtendTool" to GenFdsGlobalVariable.py to break
  the circles. Besides, FindExtendTool is tweaked slightly with the
  following changes:
  ToolDefClassObject.ToolDefDict => ToolDefDict
  TAB_GUID => DataType.TAB_GUID
  TAB_TOD_DEFINES_TARGET => DataType.TAB_TOD_DEFINES_TARGET
  TAB_TOD_DEFINES_TOOL_CHAIN_TAG => DataType.TAB_TOD_DEFINES_TOOL_CHAIN_TAG
  TAB_TOD_DEFINES_TARGET_ARCH => DataType.TAB_TOD_DEFINES_TARGET_ARCH
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit 89a69d4b643803d0b52945ca0620376e79f51ed7)

------------------------------------------------------------------------  r27521 | edk2buildsystem | 2018-07-16 02:08:18 -0700 (Mon, 16 Jul 2018) | 17 lines
  BaseTools: Move ImageBinDict to GenFdsGlobalVariable.py
  Move "ImageBinDict" from GenFds.py to GenFdsGlobalVariable.py so that we
  can remove the requirement to import GenFds.GenFds in Capsule.py, Fd.py and
  Fv.py. This breaks the following circular imports:
  * GenFds.FdfParser => GenFds.Capsule => GenFds.GenFds => GenFds.FdfParser
  * GenFds.FdfParser => GenFds.Fd => GenFds.GenFds => GenFds.FdfParser
  * GenFds.FdfParser => GenFds.Fd => GenFds.Fv => GenFds.GenFds =>
  GenFds.FdfParser
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit 7de0083812245ec2d0b35667ef4a1aa262e006e0)

------------------------------------------------------------------------  r27522 | edk2buildsystem | 2018-07-16 02:08:48 -0700 (Mon, 16 Jul 2018) | 10 lines
  BaseTools: Use absolute import in AutoGen
  Based on "futurize -f libfuturize.fixes.fix_absolute_import
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit 0ff3b52e065cc702a64d5a9016ee7926025dfbc7)

------------------------------------------------------------------------  r27524 | edk2buildsystem | 2018-07-16 02:09:09 -0700 (Mon, 16 Jul 2018) | 10 lines
  BaseTools: Use absolute import in BPDG
  Based on "futurize -f libfuturize.fixes.fix_absolute_import
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit 72a836c00a3bd57420a324bd9cf086298849e21b)

------------------------------------------------------------------------  r27525 | edk2buildsystem | 2018-07-16 02:09:24 -0700 (Mon, 16 Jul 2018) | 10 lines
  BaseTools: Use absolute import in Common
  Based on "futurize -f libfuturize.fixes.fix_absolute_import
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit f3fc5b47ad195dd9e2b644cb294448a386e18a53)

------------------------------------------------------------------------  r27527 | edk2buildsystem | 2018-07-16 02:09:59 -0700 (Mon, 16 Jul 2018) | 10 lines
  BaseTools: Use absolute import in Ecc
  Based on "futurize -f libfuturize.fixes.fix_absolute_import
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit b6f6b636b038e780c87892b17835bb6d043523b8)

------------------------------------------------------------------------  r27528 | edk2buildsystem | 2018-07-16 02:10:15 -0700 (Mon, 16 Jul 2018) | 10 lines
  BaseTools: Use absolute import in Eot
  Based on "futurize -f libfuturize.fixes.fix_absolute_import
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit 64429fbd61d445b892a78f4e55b0b83c184790bd)

------------------------------------------------------------------------  r27529 | edk2buildsystem | 2018-07-16 02:10:34 -0700 (Mon, 16 Jul 2018) | 10 lines
  BaseTools: Use absolute import in Table
  Based on "futurize -f libfuturize.fixes.fix_absolute_import
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit 3d87290487d174656fa6dee9d1f0d82a4c4294b5)

------------------------------------------------------------------------  r27530 | edk2buildsystem | 2018-07-16 02:10:47 -0700 (Mon, 16 Jul 2018) | 10 lines
  BaseTools: Use absolute import in UPT
  Based on "futurize -f libfuturize.fixes.fix_absolute_import
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit ac107416484b74e5d412f7b48268761f9ba95afe)

------------------------------------------------------------------------  r27531 | edk2buildsystem | 2018-07-16 02:11:17 -0700 (Mon, 16 Jul 2018) | 10 lines
  BaseTools: Use absolute import in Workspace
  Based on "futurize -f libfuturize.fixes.fix_absolute_import
  Contributed-under: TianoCore Contribution Agreement 1.1
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Signed-off-by: Gary Lin <glin@suse.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit 1100bc5aa05097306cdecc4d0118cc312da79d45)

------------------------------------------------------------------------  r27533 | edk2buildsystem | 2018-07-16 14:05:39 -0700 (Mon, 16 Jul 2018) | 9 lines
  BaseTools: Fixed build Ovmfpkg failed issue.
  Fixed the regression issues caused by 543f5ac30facfbb40eafb2b4908649a427784080
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 4c6d0de7bad46fc15fd34d394dffda3766e3a6a1)

------------------------------------------------------------------------  r27535 | edk2buildsystem | 2018-07-18 02:05:34 -0700 (Wed, 18 Jul 2018) | 14 lines
  BaseTools: Remove the duplicate Pcd items
  The case is the Pcd item both used in 1 module inf and 1 lib inf, and
  in the DSC component section, it override the Pcd value.
  In the module, the pcd value is the override value, but in the lib inf
  the pcd value is the value that in the DSC PCD section's value, then it
  cause the Pcd value is different in the module and lib. but actually we
  only need use the Pcd value in the module to decide whether it use the
  same value.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d900d7c9857a676d9271a0ab499c12b379dc3652)

------------------------------------------------------------------------  r27559 | edk2buildsystem | 2018-07-23 02:06:09 -0700 (Mon, 23 Jul 2018) | 16 lines
  BaseTools: enable FixedAtBuild (VOID*) PCD use in the [DEPEX] section
  V3: Add some invalid type and datum check
  V2: limit the PCD used in the [Depex] section should be used in the module
  The PCD item used in INF [Depex] section must be defined as FixedAtBuild
  type and VOID* datum type, and the size of the PCD must be 16 bytes.
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=443
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a10def91653163dbc6a38a609a87b370e9035654)

------------------------------------------------------------------------  r27566 | edk2buildsystem | 2018-07-23 02:07:41 -0700 (Mon, 23 Jul 2018) | 7 lines
  BaseTools: ElfConvert Tool update VerboseMsg to same with the comment
  Fixes: https://bugzilla.tianocore.org/show_bug.cgi?id=994
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1794b98f72fb087f012602c4d1450762dd62906d)

------------------------------------------------------------------------  r27567 | edk2buildsystem | 2018-07-23 02:07:53 -0700 (Mon, 23 Jul 2018) | 13 lines
  BaseTools/AutoGen: Update header file for MM modules.
  This patch corrects the Module Type Header file for Management Mode(MM)
  as specified in PI v1.6 Specification. Also, it updates parameter for
  auto generated template functions from EFI_SMM_SYSTEM_TABLE2 to
  EFI_MM_SYSTEM_TABLE.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Supreeth Venkatesh <supreeth.venkatesh@arm.com>
  Reviewed-by: Jiewen Yao <jiewen.yao@intel.com>
  Cc: Jiewen Yao <jiewen.yao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 549ae85ce1b00228c3abcf6a9e4022c4f4fba5ed)

------------------------------------------------------------------------  r27569 | edk2buildsystem | 2018-07-24 02:05:41 -0700 (Tue, 24 Jul 2018) | 9 lines
  BaseTools: Correct _PCD_PATCHABLE_TokenName_SIZE's value
  current if user use PatchPcdSetPtr in library, it will report the
  _PCD_PATCHABLE_TokenName_SIZE is not defined.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit bfa7eeb61d94623ddbe43b916a0bb1dc0f73a292)

------------------------------------------------------------------------  r27570 | edk2buildsystem | 2018-07-24 02:06:03 -0700 (Tue, 24 Jul 2018) | 15 lines
  BaseTools: Fix the different token with the same PCD
  If the different token with the same PCD names are used in the driver,
  build can pass. If the different token with the same PCD name are used
  in the different library, then the driver build will fail. The reason
  is that the driver autogen.c is not generated correctly for the second
  case. BaseTools should check the duplicated PCD name is the driver and
  its linked libraries.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5b73e17fb17c6935d894b0084f32421e717c247f)

------------------------------------------------------------------------  r27573 | edk2buildsystem | 2018-07-25 02:05:32 -0700 (Wed, 25 Jul 2018) | 12 lines
  BaseTools: AutoGen - change class variable to funciton variable
  This variable is only used in one function, make it local there.
  Also when iterating on the variable, use dict.items() to get value
  instead of re-looking up the value multiple times.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0f78fd73496f26d45516f6c453a66f35edca6ab0)

------------------------------------------------------------------------  r27574 | edk2buildsystem | 2018-07-25 02:05:40 -0700 (Wed, 25 Jul 2018) | 11 lines
  BaseTools: Fix build report for *P and *M flag incorrectly
  Flag *M for INF defined value and DSC components value
  Flag *P only for platform defined value
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 5df16ecb7fcfc611d35af494658e0793c16e687f)

------------------------------------------------------------------------  r27577 | edk2buildsystem | 2018-07-26 02:05:36 -0700 (Thu, 26 Jul 2018) | 10 lines
  BaseTools/Ecc: Add some new checkpoints
  1. Add a checkpoint to check NO TABs.
  2. Add a checkpoint to check line ending with CRLF.
  3. Add a checkpoint to check no trailing spaces.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a1583a877b9aba07facd567dfe4c72679ae3ca04)

------------------------------------------------------------------------  r27600 | edk2buildsystem | 2018-07-27 02:06:09 -0700 (Fri, 27 Jul 2018) | 15 lines
  BaseTools: Parse decimal format INF_VERSION incorrect
  hex number 0x00010019, the major number is 0001, the
  minor number is 0019.
  the decimal number 1.25, the major number is 1, and the
  minor number is 25
  Fix https://bugzilla.tianocore.org/show_bug.cgi?id=921
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit f413763b6b8f2798595d468cf868ae5985d3eabc)

------------------------------------------------------------------------  r27601 | edk2buildsystem | 2018-07-27 02:06:18 -0700 (Fri, 27 Jul 2018) | 13 lines
  BaseTools: Fix bug about *M value not display decimal and hexadecimal
  V2: Add the check for Pcd DatumType
  report format like as below:
  *M     Shell.inf         = 0xFF (255)
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit cef7ecf6cdb44de1520c5d0be9b2c982b59eabc4)

------------------------------------------------------------------------  r27621 | edk2buildsystem | 2018-07-30 02:05:32 -0700 (Mon, 30 Jul 2018) | 12 lines
  BaseTools: Fix build crash when fdf is empty file
  Fix build crash when fdf is empty file
  Fix https://bugzilla.tianocore.org/show_bug.cgi?id=912
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 3b46dd93ddf65a2cf1377bc72cdeb8ae3f7d81c8)

------------------------------------------------------------------------  r27622 | edk2buildsystem | 2018-07-30 02:05:44 -0700 (Mon, 30 Jul 2018) | 11 lines
  BaseTools: Update build report for StructurePcd value
  Update build report to display the structure Pcd value that from
  FDF file.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 39f0156fce373c0c0a04d85928b7d8761037134e)

------------------------------------------------------------------------  r27637 | edk2buildsystem | 2018-08-02 02:05:56 -0700 (Thu, 02 Aug 2018) | 10 lines
  BaseTools: remove unused import thread
  remove unused import thread
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 26067e30c48da27df41252444fce66a6418a613b)

------------------------------------------------------------------------  r27638 | edk2buildsystem | 2018-08-02 02:06:06 -0700 (Thu, 02 Aug 2018) | 10 lines
  BaseTools: Use pickle to replace cPickle
  Use pickle to replace cPickle because of python3 removed cPickle
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 3a0c1bf64b5deaa4e227b311cc43aa1513beae5e)

------------------------------------------------------------------------  r27639 | edk2buildsystem | 2018-08-03 02:06:08 -0700 (Fri, 03 Aug 2018) | 88 lines
  BaseTools/Capsule: Add Capsule Generation Tools
  https://bugzilla.tianocore.org/show_bug.cgi?id=945
  Based on content from the following branch
  https://github.com/Microsoft/MS_UEFI/tree/share/beta/CapsuleTools
  * Convert C tools to Python
  * Add common python modules to:
  BaseTools/Source/Python/Common/Uefi/Capsule
  BaseTools/Source/Python/Common/Edk2/Capsule
  * Add GenerateCapsule.py to BaseTools/Source/Python/Capsule
  * Add Windows and Posix wrappers for GenerateCapsule.py
  usage: GenerateCapsule [-h] [-o OUTPUTFILE] (-e | -d | --dump-info)
  [--capflag {PersistAcrossReset,PopulateSystemTable,InitiateReset}]
  [--capoemflag CAPSULEOEMFLAG] [--guid GUID]
  [--hardware-instance HARDWAREINSTANCE]
  [--monotonic-count MONOTONICCOUNT]
  [--fw-version FWVERSION] [--lsv LOWESTSUPPORTEDVERSION]
  [--pfx-file SIGNTOOLPFXFILE]
  [--signer-private-cert OPENSSLSIGNERPRIVATECERTFILE]
  [--other-public-cert OPENSSLOTHERPUBLICCERTFILE]
  [--trusted-public-cert OPENSSLTRUSTEDPUBLICCERTFILE]
  [--signing-tool-path SIGNINGTOOLPATH] [--version] [-v]
  [-q] [--debug [0-9]]
  InputFile
  Generate a capsule. Copyright (c) 2018, Intel Corporation. All rights
  reserved.
  positional arguments:
  InputFile             Input binary payload filename.
  optional arguments:
  -h, --help            show this help message and exit
  -o OUTPUTFILE, --output OUTPUTFILE
  Output filename.
  -e, --encode          Encode file
  -d, --decode          Decode file
  --dump-info           Display FMP Payload Header information
  --capflag {PersistAcrossReset,PopulateSystemTable,InitiateReset}
  Capsule flag can be PersistAcrossReset, or
  PopulateSystemTable or InitiateReset or not set
  --capoemflag CAPSULEOEMFLAG
  Capsule OEM Flag is an integer between 0x0000 and
  0xffff.
  --guid GUID           The FMP/ESRT GUID in registry format. Required for
  encode operations.
  --hardware-instance HARDWAREINSTANCE
  The 64-bit hardware instance. The default is
  0x0000000000000000
  --monotonic-count MONOTONICCOUNT
  64-bit monotonic count value in header. Default is
  0x0000000000000000.
  --fw-version FWVERSION
  The 32-bit version of the binary payload (e.g.
  0x11223344 or 5678).
  --lsv LOWESTSUPPORTEDVERSION
  The 32-bit lowest supported version of the binary
  payload (e.g. 0x11223344 or 5678).
  --pfx-file SIGNTOOLPFXFILE
  signtool PFX certificate filename.
  --signer-private-cert OPENSSLSIGNERPRIVATECERTFILE
  OpenSSL signer private certificate filename.
  --other-public-cert OPENSSLOTHERPUBLICCERTFILE
  OpenSSL other public certificate filename.
  --trusted-public-cert OPENSSLTRUSTEDPUBLICCERTFILE
  OpenSSL trusted public certificate filename.
  --signing-tool-path SIGNINGTOOLPATH
  Path to signtool or OpenSSL tool. Optional if path to
  tools are already in PATH.
  --version             show program's version number and exit
  -v, --verbose         Turn on verbose output with informational messages
  printed, including capsule headers and warning
  messages.
  -q, --quiet           Disable all messages except fatal errors.
  --debug [0-9]         Set debug level
  Cc: Sean Brogan <sean.brogan@microsoft.com>
  Cc: Jiewen Yao <jiewen.yao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 8b63877aca1e5a3576b7275439c494a6d40ed1b5)

------------------------------------------------------------------------  r27641 | edk2buildsystem | 2018-08-03 02:06:31 -0700 (Fri, 03 Aug 2018) | 14 lines
  BaseTools/Capsule: Add max value checks to Capsule Generation tools
  https://bugzilla.tianocore.org/show_bug.cgi?id=1021
  https://bugzilla.tianocore.org/show_bug.cgi?id=1022
  https://bugzilla.tianocore.org/show_bug.cgi?id=1026
  Cc: Sean Brogan <sean.brogan@microsoft.com>
  Cc: Jiewen Yao <jiewen.yao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 6ed4651cb560caba91a989550734206f01ffd7d1)

------------------------------------------------------------------------  r27642 | edk2buildsystem | 2018-08-03 02:06:40 -0700 (Fri, 03 Aug 2018) | 12 lines
  BaseTools/Capsule: Remove support for PopulateSystemTable
  https://bugzilla.tianocore.org/show_bug.cgi?id=1030
  Cc: Sean Brogan <sean.brogan@microsoft.com>
  Cc: Jiewen Yao <jiewen.yao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 2779c222c80533677e0cb54cc19d0287d280647f)

------------------------------------------------------------------------  r27643 | edk2buildsystem | 2018-08-03 02:06:50 -0700 (Fri, 03 Aug 2018) | 12 lines
  BaseTools/Capsule: Fix CertType GUID byte order
  https://bugzilla.tianocore.org/show_bug.cgi?id=1024
  Cc: Sean Brogan <sean.brogan@microsoft.com>
  Cc: Jiewen Yao <jiewen.yao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4619b183f71c1a7c966927060e99aa1f887f605e)

------------------------------------------------------------------------  r27644 | edk2buildsystem | 2018-08-03 02:06:59 -0700 (Fri, 03 Aug 2018) | 12 lines
  BaseTools/Capsule: Do not support -o with --dump-info
  https://bugzilla.tianocore.org/show_bug.cgi?id=1025
  Cc: Sean Brogan <sean.brogan@microsoft.com>
  Cc: Jiewen Yao <jiewen.yao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit f33d5d68abc02727dc828c1079e72ab65e1d63af)

------------------------------------------------------------------------  r27645 | edk2buildsystem | 2018-08-03 02:07:07 -0700 (Fri, 03 Aug 2018) | 15 lines
  BaseTools/Capsule: Update help for --fw-version and --lsv
  Update help to state that --fw-version and -=-lsv are required
  for encode operations that sign a payload.
  https://bugzilla.tianocore.org/show_bug.cgi?id=1029
  Cc: Sean Brogan <sean.brogan@microsoft.com>
  Cc: Jiewen Yao <jiewen.yao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ff307fba9857145875839fdca33c95236e238153)

------------------------------------------------------------------------  r27646 | edk2buildsystem | 2018-08-03 02:07:17 -0700 (Fri, 03 Aug 2018) | 17 lines
  BaseTools/Capsule: Update file header with tool limitations
  Update file header to state that the tool does not support:
  * Multiple payloads
  * Drivers
  * Vendor code bytes
  https://bugzilla.tianocore.org/show_bug.cgi?id=1031
  Cc: Sean Brogan <sean.brogan@microsoft.com>
  Cc: Jiewen Yao <jiewen.yao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit d6f079b600cc88367c20b5eec5a28d28d3ceaca8)

------------------------------------------------------------------------  r27647 | edk2buildsystem | 2018-08-03 02:07:28 -0700 (Fri, 03 Aug 2018) | 18 lines
  BaseTools/Capsule: Prevent traceback during signing operations
  https://bugzilla.tianocore.org/show_bug.cgi?id=1046
  https://bugzilla.tianocore.org/show_bug.cgi?id=1048
  https://bugzilla.tianocore.org/show_bug.cgi?id=1050
  Remove raise statements that generate Tracebacks that were only
  intended for development/debug.  With the raise statements removed
  proper error messages are shown.
  Cc: Sean Brogan <sean.brogan@microsoft.com>
  Cc: Jiewen Yao <jiewen.yao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit e49eee4c51a6cb8b2f35735e375c211c41d9f6cb)

------------------------------------------------------------------------  r27648 | edk2buildsystem | 2018-08-03 02:07:40 -0700 (Fri, 03 Aug 2018) | 16 lines
  BaseTools/Capsule: Support capsules without a payload header
  https://bugzilla.tianocore.org/show_bug.cgi?id=1028
  Update --dump-info and --decode to show auth header information
  even if a payload header is not present.  The --decode operation
  still fails if a payload header is not present.
  Cc: Sean Brogan <sean.brogan@microsoft.com>
  Cc: Jiewen Yao <jiewen.yao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit de652b14a78b4767ff460999b6728d7ccc50b057)

------------------------------------------------------------------------  r27675 | edk2buildsystem | 2018-08-03 02:12:37 -0700 (Fri, 03 Aug 2018) | 20 lines
  BaseTools: Guid.xref doesn't specify the correct GUID value for Driver
  In DSC, we can define the driver with the different FILE GUID. So this
  driver name and its FILE GUID should also be listed in Build output
  Guid.xref. But now, Guid.xref still lists the driver MODULE_GUID.
  The case in Platform.dsc:
  MdeModulePkg/Universal/DriverSampleDxe/DriverSampleDxe.inf {
  <Defines>
  FILE_GUID = 3A4A354F-6935-40fa-B19C-500EEEBF0BC2
  <LibraryClasses>
  PcdLib|MdePkg/Library/BasePcdLibNull/BasePcdLibNull.inf
  }
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1d802e234e813a6726f4c6fd161ae9bd146bc552)

------------------------------------------------------------------------  r27677 | edk2buildsystem | 2018-08-04 02:05:30 -0700 (Sat, 04 Aug 2018) | 18 lines
  BaseTools/Pkcs7Sign: Add PKCS7 test key include files
  https://bugzilla.tianocore.org/show_bug.cgi?id=1073
  Add PCD statement include files for the PKCS7 test key.
  * gEfiSecurityPkgTokenSpaceGuid.PcdPkcs7CertBuffer
  * gFmpDevicePkgTokenSpaceGuid.PcdFmpDevicePkcs7CertBufferXdr
  These include files can be used in !include statements in PCD
  sections of a platform DSC file to assign these PCDs to the
  test key certificate values.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Michael D Kinney <michael.d.kinney@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 526dd0245bf0db6a01c21943201a4572747bca7f)

------------------------------------------------------------------------  r27688 | edk2buildsystem | 2018-08-08 02:05:45 -0700 (Wed, 08 Aug 2018) | 12 lines
  BaseTools: Debug message make confused
  Debug message make confused
  Fix https://bugzilla.tianocore.org/show_bug.cgi?id=995
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit e5cbb982562c354a6c040552d0ff20a38202c284)

------------------------------------------------------------------------  r27690 | edk2buildsystem | 2018-08-08 02:06:08 -0700 (Wed, 08 Aug 2018) | 10 lines
  BaseTools: Use gGuidPattern for Guid regular expression
  Use GlobalData.py gGuidPattern for Guid regular expression
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit cefc8d8821f0a5ec7995901146dd6b055d7b956a)

------------------------------------------------------------------------  r27709 | edk2buildsystem | 2018-08-16 02:05:53 -0700 (Thu, 16 Aug 2018) | 10 lines
  BaseTool: Fixed the bug of Boolean Hii Pcd packing.
  When packing HiiPcd into PcdNvStoreDefaultValueBuffer,
  The boolean type pcd value packing incorrect.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 669b55e6d560f06aef5a21d843451ae3b1351116)

------------------------------------------------------------------------  r27710 | edk2buildsystem | 2018-08-16 02:06:04 -0700 (Thu, 16 Aug 2018) | 12 lines
  BaseTools: Remove a unused function.
  the call statement of _CheckDuplicateInFV() was commented out
  in 2014. There is no call statement of _CheckDuplicateInFV(),
  so remove it.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 0fc5e71c68b1827750111ae0bf3031b667c1f893)

------------------------------------------------------------------------  r27718 | edk2buildsystem | 2018-08-16 02:07:34 -0700 (Thu, 16 Aug 2018) | 11 lines
  BaseTools: Remove the redundant if statement
  after analysis the BuildOptionValue function, we found the if statement
  IsFieldValueAnArray is redundant because ValueExpressionEx will handle
  it.
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b2282e5369c10a26e8cbf125cc22032ba903d619)

------------------------------------------------------------------------  r27719 | edk2buildsystem | 2018-08-16 02:07:51 -0700 (Thu, 16 Aug 2018) | 10 lines
  BaseTools: Fix report flexible value issue
  Report flexible value in INF file encounter error
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit af24640290a79e974710629db91fb39512d0b54b)

------------------------------------------------------------------------  r27720 | edk2buildsystem | 2018-08-16 02:08:45 -0700 (Thu, 16 Aug 2018) | 11 lines
  BaseTools/Ecc: Fix import issues
  1. Complete the full path for import statement. Use "EccMain" to
  replace "Ecc" for the absolute path support.
  2. Fix some issues on configuration file.
  3. Fix an issue of RaiseError not working in EdkLogger.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 855698fb69fdb85fa24c4374d07947106f4de828)

------------------------------------------------------------------------  r27723 | edk2buildsystem | 2018-08-16 02:09:40 -0700 (Thu, 16 Aug 2018) | 10 lines
  BaseTools: Remove duplicate function declaration
  Remove duplicate function declaration
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 6f06101ddfedbe3ebbb0b950fcc7449691446ed3)

------------------------------------------------------------------------  r27724 | edk2buildsystem | 2018-08-16 02:09:52 -0700 (Thu, 16 Aug 2018) | 10 lines
  BaseTools: Add Dns and BluetoothLE DevicePath
  Add Dns and BluetoothLE for support DevicePath
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit f52c3ed019011e5d86d66ee317a8003867f0956d)

------------------------------------------------------------------------  r27725 | edk2buildsystem | 2018-08-16 02:10:03 -0700 (Thu, 16 Aug 2018) | 14 lines
  BaseTools: Clean up not used code in BuildClassObject
  V2: Add back "from Common.DataType import *"
  1. Remove some import statement that are not used.
  2. Remove the Type value in the LibraryClassObject because we don't
  actually use it.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Jaben Carsey <jaben.carsey@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Jaben Carsey <jaben.carsey@intel.com>
  (cherry picked from commit f64fbdde8c99bcf0c97f1348f02fdcd8685f1df2)

------------------------------------------------------------------------  r27727 | edk2buildsystem | 2018-08-16 02:10:22 -0700 (Thu, 16 Aug 2018) | 12 lines
  BaseTools: Eot - fix variable names
  1) currently a couple classes use m instead of self (including some mixed
  functions that should have previously failed).
  2) deleted some blank lines.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4fea08b9c9df2271de5200a1dd3189ddbf525922)

------------------------------------------------------------------------  r27728 | edk2buildsystem | 2018-08-16 02:10:31 -0700 (Thu, 16 Aug 2018) | 12 lines
  BaseTools: Optimizing code for function doesn't match
  Optimizing code for function doesn't match name and comment
  Fix https://bugzilla.tianocore.org/show_bug.cgi?id=924
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7b85a1afa38c13fd40095f277cd26e5aa159b2f5)

------------------------------------------------------------------------  r27738 | edk2buildsystem | 2018-08-16 14:09:00 -0700 (Thu, 16 Aug 2018) | 14 lines
  BaseTools/footer.makefile: expand BUILD_CFLAGS last for C files too
  BUILD_CPPFLAGS should be expanded before BUILD_CFLAGS. (The rule for C++
  source files already does this, with BUILD_CPPFLAGS and BUILD_CXXFLAGS.)
  This patch doesn't change behavior.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Ref: https://bugzilla.redhat.com/show_bug.cgi?id=1540244
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 67983484a4430c5f82bb5f1397e010c759136321)

------------------------------------------------------------------------  r27739 | edk2buildsystem | 2018-08-16 14:09:08 -0700 (Thu, 16 Aug 2018) | 17 lines
  BaseTools/header.makefile: remove "-c" from BUILD_CFLAGS
  Option "-c" is a mode selection flag (choosing between compiling and
  linking); it should not be in BUILD_CFLAGS, which applies only to
  compiling anyway. The compilation rule for C source files, in
  "footer.makefile", already includes "-c" -- currently we have double "-c"
  options.
  This patch doesn't change behavior.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Ref: https://bugzilla.redhat.com/show_bug.cgi?id=1540244
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 03252ae287c4a61983b3793ff71baeabe2ff3df7)

------------------------------------------------------------------------  r27740 | edk2buildsystem | 2018-08-16 14:09:20 -0700 (Thu, 16 Aug 2018) | 20 lines
  BaseTools/Source/C: split "-O2" to BUILD_OPTFLAGS
  The option "-O2" is not a preprocessor flag, but a code generation
  (compilation) flag. Move it from BUILD_CPPFLAGS to BUILD_CFLAGS and
  BUILD_CXXFLAGS.
  Because "VfrCompile/GNUmakefile" uses "-O2" through BUILD_CPPFLAGS, and
  because it doesn't use BUILD_CXXFLAGS, we have to introduce BUILD_OPTFLAGS
  separately, so that "VfrCompile/GNUmakefile" can continue using just this
  flag.
  This patch doesn't change behavior.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Ref: https://bugzilla.redhat.com/show_bug.cgi?id=1540244
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b8a66170264395edeaa61e6d22930a58e576a685)

------------------------------------------------------------------------  r27741 | edk2buildsystem | 2018-08-16 14:09:31 -0700 (Thu, 16 Aug 2018) | 14 lines
  BaseTools/Source/C: take EXTRA_OPTFLAGS from the caller
  Allow the caller of the top-level makefile either to set EXTRA_OPTFLAGS in
  the environment or to pass EXTRA_OPTFLAGS as a macro definition on the
  command line. EXTRA_OPTFLAGS extends (and potentially overrides) default C
  compilation flags set in the makefiles.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Ref: https://bugzilla.redhat.com/show_bug.cgi?id=1540244
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b0ca5dae78ff71397a8ef568f1914da7668ff5a9)

------------------------------------------------------------------------  r27742 | edk2buildsystem | 2018-08-16 14:09:38 -0700 (Thu, 16 Aug 2018) | 14 lines
  BaseTools/Source/C: take EXTRA_LDFLAGS from the caller
  Allow the caller of the top-level makefile either to set EXTRA_LDFLAGS in
  the environment or to pass EXTRA_LDFLAGS as a macro definition on the
  command line. EXTRA_LDFLAGS extends (and potentially overrides) default
  link-editing flags set in the makefiles.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Ref: https://bugzilla.redhat.com/show_bug.cgi?id=1540244
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 81502cee20ac4046f08bb4aec754c7091c8808dc)

------------------------------------------------------------------------  r27744 | edk2buildsystem | 2018-08-17 02:05:30 -0700 (Fri, 17 Aug 2018) | 9 lines
  BaseTools: Add check for VOID* PCD Max Size
  Per spec VOID* PCD max size should be a UINT16 value. so this patch
  add the value check whether it is in range 0x0 .. 0xFFFF.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f843a328772a30c11162c281adaf2afc1b4a972f)

------------------------------------------------------------------------  r27745 | edk2buildsystem | 2018-08-20 02:05:47 -0700 (Mon, 20 Aug 2018) | 42 lines
  BaseTools: AutoGen refactor ModuleAutoGen caching
  1) Add a new file Common/caching.py
  a.	Allows for automated caching of repeated class functions, class
  properties, and non-class functions
  b.	When called the first time the value is cached and if called a
  second time, the cached result is called, not the function.
  c.	When used, this saves lots of memory since the actual function
  pointers are replaced with smaller data elements.
  d.  note that not all features are used yet.
  2) Fix AutoGen/GenMake and AutoGen/GetC to not call into private member
  variables of ModuleAutoGen class
  a. use the existing accessor properties for the data
  3) Change AutoGen classes to remove a exception for duplicate members in
  __new__ and use ?in? testing to speed up
  4)	Work on ModuleAutoGen class
  a.	Change all properties that use caching to use @caching_property
  (see #1 above)
  b.	Change all properties that do not use caching to use standard python
  decorator "@property"
  c.	Change all cases where a dictionary/set/list/object was created
  and then immediately updated to use constructor parameters
  d.	Refactor each property function to remove the internal variable
  that is no longer needed (this helps find items like #2 above)
  e.  Refactor _ApplyBuildRule with optional parameter to work around
  circular dependency with BinaryFileList.
  Note that 4e was almost certainly unintended as the functions were acting on
  incomplete information since they were directly accessing private instance
  variables at the same time another function on the stack was creating the same
  private isntance data.
  This overall changes behavior slightly, but makes the codebase smaller and
  easier to read.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Bob Feng <bob.c.feng@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b23414f6540d4f336b6f00b44681911d469f9a04)

------------------------------------------------------------------------  r27746 | edk2buildsystem | 2018-08-20 02:05:59 -0700 (Mon, 20 Aug 2018) | 12 lines
  BaseTools: AutoGen - tag a function as cachable
  MakeFile generation is once per module, so mark it as such.
  also move the time stamp creation function inside as it's
  only called from one place.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 830bf22fa5525263ea10cd2f4a0dc843a4c05122)

------------------------------------------------------------------------  r27747 | edk2buildsystem | 2018-08-20 02:06:08 -0700 (Mon, 20 Aug 2018) | 15 lines
  BaseTools: AutoGen refactor to iterate less
  Don't iterate over new dictionaries with one item
  Create the data and then add to dictionary.
  Note: if you diff ignoring whitespace changes you
  can more easily see the relevant changes.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0258ba6256ca193e8fd896a40ceef1bc06a3e0e8)

------------------------------------------------------------------------  r27748 | edk2buildsystem | 2018-08-20 02:06:17 -0700 (Mon, 20 Aug 2018) | 11 lines
  BaseTools: remove unused code
  the if statment just has pass statement.
  invert if condition and just use do the else work.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit fe6fdfe2bb015bbd64c45c5d6ae028ecdf2437e2)

------------------------------------------------------------------------  r27749 | edk2buildsystem | 2018-08-20 02:06:28 -0700 (Mon, 20 Aug 2018) | 8 lines
  BaseTools: remove unused setter functions
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 43fe4c4052922c6baa36cf4664ce63b8699d9176)

------------------------------------------------------------------------