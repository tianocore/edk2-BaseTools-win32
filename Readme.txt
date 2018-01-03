Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26075

This directory contains the Win32 binaries.

Build Date:       Wed, 03 Jan 2018 03:13:46 Pacific Standard Time
Last Changed Rev: 26075

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26061
 *BootSectImage Version 1.0 Build Build 26075
 *Brotli Version 0.5.2 Build 26075
  Brotli Version 0.5.2 Build 26075
 *DevicePath Version 0.1 Build 26075
  Ecc.exe Version 1.0 Build Build 24602
 *EfiLdrImage Version 1.0 Build Build 26075
 *EfiRom Version 0.1 Build 26075
 *GenBootSector Version 0.2 Build 26075
 *GenCrc32 Version 0.2 Build 26075
  GenDepex.exe Version 0.04 Build 26061
 *GenFds.exe 1.0 Build 26075
 *GenFfs Version 0.1 Build 26075
 *GenFv Version 0.1 Build 26075
 *GenFw Version 0.2 Build 26075
 *GenPage Version 0.2 Build 26075
  GenPatchPcdTable.exe Version 0.10 Build 26061
 *GenSec Version 0.1 Build 26075
 *GenVtf Version 0.1 Build 26075
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 26075
  LzmaF86Compress Version 0.2 Build 26075
  PatchPcdValue.exe Version 0.10 Build 26061
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
 *Split Version 1.0 Build Build 26075
  TargetTool.exe Version 0.01 Build 26061
 *TianoCompress Version 0.1 Build 26075
  Trim.exe Version 0.10 Build 26061
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 26075
 *VolInfo Version 1.0 Build Build 26075
 *build.exe Version 0.60 Build 26075

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  1/3/2018 3:13:48AM Engine version = 5900.7806
  1/3/2018 3:13:48AM AntiVirus DAT version = 8762.0
  1/3/2018 3:13:48AM Number of detection signatures in EXTRA.DAT = None
  1/3/2018 3:13:48AM Names of detection signatures in EXTRA.DAT = None
  1/3/2018 3:13:48AM Scan Started On-Demand Scan
  1/3/2018 3:13:56AM Scan Summary
  1/3/2018 3:13:56AM Processes scanned : 0
  1/3/2018 3:13:56AM Processes detected : 0
  1/3/2018 3:13:56AM Processes cleaned : 0
  1/3/2018 3:13:56AM Boot sectors scanned : 2
  1/3/2018 3:13:56AM Boot sectors detected: 0
  1/3/2018 3:13:56AM Boot sectors cleaned : 0
  1/3/2018 3:13:56AM Files scanned : 83
  1/3/2018 3:13:56AM Files with detections: 0
  1/3/2018 3:13:56AM File detections : 0
  1/3/2018 3:13:56AM Files cleaned : 0
  1/3/2018 3:13:56AM Files deleted : 0
  1/3/2018 3:13:56AM Files not scanned : 0
  1/3/2018 3:13:56AM Scan Summary (Registry Scanning)
  1/3/2018 3:13:56AM Keys scanned : 0
  1/3/2018 3:13:56AM Keys detected : 0
  1/3/2018 3:13:56AM Keys cleaned : 0
  1/3/2018 3:13:56AM Keys deleted : 0
  1/3/2018 3:13:56AM Run time : 0:00:08
  1/3/2018 3:13:56AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26061:HEAD Source
------------------------------------------------------------------------  r26061 | edk2buildsystem | 2017-12-31 02:05:31 -0800 (Sun, 31 Dec 2017) | 12 lines
  BaseTools: Add DevicePath support for PCD values
  Use C code parse device path to output hex string, and Python
  run command when PCD Value need device path parse.
  https://bugzilla.tianocore.org/show_bug.cgi?id=541
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 7dbc50bd244d95fdc1741b9cfc561f0bfd724de1)

------------------------------------------------------------------------  r26067 | edk2buildsystem | 2018-01-02 14:05:30 -0800 (Tue, 02 Jan 2018) | 10 lines
  BaseTools: correct mal-typed CVfrDLGLexer::errstd
  The member function CVfrDLGLexer::errstd is intended as an override virtual
  function of DLGLexerBase::errstd, but due to mismatched prototype, it
  didn't override, and never got called.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zenith432 <zenith432@users.sourceforge.net>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 8b13e18143cc4199eedd2597572ade34061a5c33)

------------------------------------------------------------------------  r26068 | edk2buildsystem | 2018-01-02 14:05:36 -0800 (Tue, 02 Jan 2018) | 9 lines
  BaseTools: eliminate unused expression result
  Remove some code generated by antlr that causes clang to emit warning
  warning: expression result unused [-Wunused-value]
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zenith432 <zenith432@users.sourceforge.net>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a5b84d3480b4cebf06f61cbe4c84c5de4d1ce445)

------------------------------------------------------------------------  r26069 | edk2buildsystem | 2018-01-02 14:05:43 -0800 (Tue, 02 Jan 2018) | 12 lines
  BaseTools: silence parentheses-equality warning
  Some code generated by antlr causes clang to emit warning
  warning: equality comparison with extraneous parentheses
  [-Wparentheses-equality]
  The warning is suppressed specifically for clang without affecting other
  compilers.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zenith432 <zenith432@users.sourceforge.net>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 4e97974c1e52c2fcd2640398b17266dff001b699)

------------------------------------------------------------------------  r26070 | edk2buildsystem | 2018-01-02 14:05:49 -0800 (Tue, 02 Jan 2018) | 47 lines
  BaseTools: resolve initialization order errors in VfrFormPkg.h
  clang generates many warnings
  warning: field 'XXX' is uninitialized when used here [-Wuninitialized]
  for VfrFormPkg.h.
  VfrFormPkg.h defines many classes derived from CIfrObj (along with other
  base classes.)
  Each of these derived classes defines a non-static member field that serves
  as a duplicate pointer to an original pointer defined in the CIfrObj base
  class, but cast to a different pointer type.
  The derived class constructor passes the duplicate pointer to base class
  constructors:
  1) Once passes the address of the duplicate pointer to the CIfrObj
  constructor to have it initialized.
  2) Then passes the duplicate pointer to one or more subsequent base class
  constructors to be used.
  Both 1) and 2) constitute undefined behavior in C++.  C++ prescribes that
  base classes are initialized before non-static members when initializing a
  derived class.  So when base class constructors are executing, it is not
  permitted to assume any non-static members of the derived class exist (even
  to the stage of having their storage allocated.)
  clang does not issue warnings for 1), but issues warnings -Wuninitialized
  for 2).
  This coding methodology is resolved as follows:
  a) The CIfrObj object accessor method for retrieving the original pointer
  is revised to a template member function that returns the original
  pointer cast to a desired target type.
  b) The call to CIfrObj constructor is no longer used to initialize the
  duplicate pointer in the derived class.
  c) Any subsequent calls to a base class constructor that need to use the
  pointer, retrieve it from the CIfrObj base class using the template
  accessor method.
  d) If the derived class makes no further use of the pointer, then the
  duplicate pointer defined in it is eliminated.
  e) If the derived class needs the duplicate pointer for other use, the
  duplicate pointer remains in the derived class and is initialized in
  proper order from the original pointer in CIfrObj.
  f) Existing source code that previously used the CIfrObj pointer accessor
  method is revised to use the template method.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Zenith432 <zenith432@users.sourceforge.net>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5397bd425eba0cd00c5f76c8d35f328ca625db0e)

------------------------------------------------------------------------  r26071 | edk2buildsystem | 2018-01-03 02:05:29 -0800 (Wed, 03 Jan 2018) | 9 lines
  BaseTools: Fix the regression bug of a74398 for SubFv Image
  in version a74398 we use guid value and Fv name as ffs dir for FILE
  statement, this patch apply this rule on subFv image.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit ff260aa7abbeefdea591bb0b15e7d89e73d6c334)

------------------------------------------------------------------------  r26073 | edk2buildsystem | 2018-01-03 02:05:40 -0800 (Wed, 03 Jan 2018) | 10 lines
  BaseTools CommonLib: Fix printf %llx issue on UINT64
  UINT64 is defined as the different type for the different ARCHs. To
  let it work for all archs and compilers, add (unsigned long long) for
  the input value together with %llx.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit beacbc7492393992a8d10cd0a450c308a482f315)

------------------------------------------------------------------------  r26074 | edk2buildsystem | 2018-01-03 02:05:45 -0800 (Wed, 03 Jan 2018) | 32 lines
  BaseTools/DevicePath: fix GCC build error in print_mem(), and clean it up
  Currently "BaseTools/Source/C/DevicePath/DevicePath.c" fails to build with
  GCC48:
  > DevicePath.c: In function 'print_mem':
  > DevicePath.c:109:5: error: 'for' loop initial declarations are only
  > allowed in C99 mode
  >      for (size_t i=0; i<n; i++) {
  >      ^
  > DevicePath.c:109:5: note: use option -std=c99 or -std=gnu99 to compile
  > your code
  In addition, the print_mem() function does not conform to the edk2 coding
  style:
  - we use CamelCase and no underscores in identifiers,
  - the types and type qualifiers should follow the edk2 style,
  - initialization as part of definition is forbidden for local variables.
  Clean these up.
  While updating the print_mem()/PrintMem() call sites, also remove the
  superfluous parentheses around the second argument.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Fixes: 7dbc50bd244d95fdc1741b9cfc561f0bfd724de1
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 9a6b445bc2e6e2db6f67ab3cc425d5831aa1b7c8)

------------------------------------------------------------------------  r26075 | edk2buildsystem | 2018-01-03 02:05:50 -0800 (Wed, 03 Jan 2018) | 8 lines
  BaseTools: Fix compile error on VS2010
  VS2010 also defined RSIZE_MAX, so we undef it first.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit e4fb8f1d313858bd5e415725e65e65679f2b05a0)

------------------------------------------------------------------------