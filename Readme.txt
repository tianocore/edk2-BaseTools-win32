Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 26914

This directory contains the Win32 binaries.

Build Date:       Mon, 16 Apr 2018 09:47:34 Pacific Daylight Time
Last Changed Rev: 26913

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.14 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 26914
  BootSectImage Version 1.0 Build Build 26482
  Brotli Version 0.5.2 Build 26482
  Brotli Version 0.5.2 Build 26482
  DevicePath Version 0.1 Build 26482
 *Ecc.exe Version 1.0 Build Build 26914
  EfiLdrImage Version 1.0 Build Build 26482
  EfiRom Version 0.1 Build 26482
  GenBootSector Version 0.2 Build 26482
  GenCrc32 Version 0.2 Build 26482
 *GenDepex.exe Version 0.04 Build 26914
 *GenFds.exe 1.0 Build 26914
  GenFfs Version 0.1 Build 26482
  GenFv Version 0.1 Build 26482
  GenFw Version 0.2 Build 26482
  GenPage Version 0.2 Build 26482
 *GenPatchPcdTable.exe Version 0.10 Build 26914
 *GenSec Version 0.1 Build 26914
 *GenVtf Version 0.1 Build 26914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26482
  LzmaF86Compress Version 0.2 Build 26482
 *PatchPcdValue.exe Version 0.10 Build 26914
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
 *Rsa2048Sha256Sign Version 0.9 Build 26914
  Split Version 1.0 Build Build 26482
 *TargetTool.exe Version 0.01 Build 26914
  TianoCompress Version 0.1 Build 26482
 *Trim.exe Version 0.10 Build 26914
 *UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26914
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 26914
  VolInfo Version 1.0 Build Build 26482
 *build.exe Version 0.60 Build 26914

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  4/16/2018 9:47:37AM Engine version = 5900.7806
  4/16/2018 9:47:37AM AntiVirus DAT version = 8864.0
  4/16/2018 9:47:37AM Number of detection signatures in EXTRA.DAT = None
  4/16/2018 9:47:37AM Names of detection signatures in EXTRA.DAT = None
  4/16/2018 9:47:37AM Scan Started On-Demand Scan
  4/16/2018 9:47:50AM Scan Summary
  4/16/2018 9:47:50AM Processes scanned : 0
  4/16/2018 9:47:50AM Processes detected : 0
  4/16/2018 9:47:50AM Processes cleaned : 0
  4/16/2018 9:47:50AM Boot sectors scanned : 2
  4/16/2018 9:47:50AM Boot sectors detected: 0
  4/16/2018 9:47:50AM Boot sectors cleaned : 0
  4/16/2018 9:47:50AM Files scanned : 69
  4/16/2018 9:47:50AM Files with detections: 0
  4/16/2018 9:47:50AM File detections : 0
  4/16/2018 9:47:50AM Files cleaned : 0
  4/16/2018 9:47:50AM Files deleted : 0
  4/16/2018 9:47:50AM Files not scanned : 0
  4/16/2018 9:47:50AM Scan Summary (Registry Scanning)
  4/16/2018 9:47:50AM Keys scanned : 0
  4/16/2018 9:47:50AM Keys detected : 0
  4/16/2018 9:47:50AM Keys cleaned : 0
  4/16/2018 9:47:50AM Keys deleted : 0
  4/16/2018 9:47:50AM Run time : 0:00:14
  4/16/2018 9:47:50AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 26482:HEAD Source
------------------------------------------------------------------------  r26483 | edk2buildsystem | 2018-03-05 14:05:30 -0800 (Mon, 05 Mar 2018) | 8 lines
  BaseTools: update DNS_DEVICE_PATH/URI_DEVICE_PATH definition
  Update this two definition to align with MdePkg.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 20203d3f98d671d7d7d78f33bbb02cf1d1b3cabe)

------------------------------------------------------------------------  r26484 | edk2buildsystem | 2018-03-05 14:05:40 -0800 (Mon, 05 Mar 2018) | 46 lines
  BaseTools/header.makefile: add "-Wno-stringop-truncation"
  gcc-8 (which is part of Fedora 28) enables the new warning
  "-Wstringop-truncation" in "-Wall". This warning is documented in detail
  at <https://gcc.gnu.org/onlinedocs/gcc/Warning-Options.html>; the
  introduction says
  > Warn for calls to bounded string manipulation functions such as strncat,
  > strncpy, and stpncpy that may either truncate the copied string or leave
  > the destination unchanged.
  It breaks the BaseTools build with:
  > EfiUtilityMsgs.c: In function 'PrintMessage':
  > EfiUtilityMsgs.c:484:9: error: 'strncat' output may be truncated copying
  > between 0 and 511 bytes from a string of length 511
  > [-Werror=stringop-truncation]
  >          strncat (Line, Line2, MAX_LINE_LEN - strlen (Line) - 1);
  >          ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  > EfiUtilityMsgs.c:469:9: error: 'strncat' output may be truncated copying
  > between 0 and 511 bytes from a string of length 511
  > [-Werror=stringop-truncation]
  >          strncat (Line, Line2, MAX_LINE_LEN - strlen (Line) - 1);
  >          ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  > EfiUtilityMsgs.c:511:5: error: 'strncat' output may be truncated copying
  > between 0 and 511 bytes from a string of length 511
  > [-Werror=stringop-truncation]
  >      strncat (Line, Line2, MAX_LINE_LEN - strlen (Line) - 1);
  >      ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  The right way to fix the warning would be to implement string concat with
  snprintf(). However, Microsoft does not appear to support snprintf()
  before VS2015
  <https://stackoverflow.com/questions/2915672/snprintf-and-visual-studio-2010>,
  so we just have to shut up the warning. The strncat() calls flagged above
  are valid BTW.
  Cc: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Cc: Cole Robinson <crobinso@redhat.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Paolo Bonzini <pbonzini@redhat.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1d212a83df0eaf32a6f5d4159beb2d77832e0231)

------------------------------------------------------------------------  r26485 | edk2buildsystem | 2018-03-05 14:05:47 -0800 (Mon, 05 Mar 2018) | 78 lines
  BaseTools/header.makefile: add "-Wno-restrict"
  gcc-8 (which is part of Fedora 28) enables the new warning
  "-Wrestrict" in "-Wall". This warning is documented in detail
  at <https://gcc.gnu.org/onlinedocs/gcc/Warning-Options.html>; the
  introduction says
  > Warn when an object referenced by a restrict-qualified parameter (or, in
  > C++, a __restrict-qualified parameter) is aliased by another argument,
  > or when copies between such objects overlap.
  It breaks the BaseTools build (in the Brotli compression library) with:
  > In function 'ProcessCommandsInternal',
  >     inlined from 'ProcessCommands' at dec/decode.c:1828:10:
  > dec/decode.c:1781:9: error: 'memcpy' accessing between 17 and 2147483631
  > bytes at offsets 16 and 16 overlaps between 17 and 2147483631 bytes at
  > offset 16 [-Werror=restrict]
  >          memcpy(copy_dst + 16, copy_src + 16, (size_t)(i - 16));
  >          ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  > In function 'ProcessCommandsInternal',
  >     inlined from 'SafeProcessCommands' at dec/decode.c:1833:10:
  > dec/decode.c:1781:9: error: 'memcpy' accessing between 17 and 2147483631
  > bytes at offsets 16 and 16 overlaps between 17 and 2147483631 bytes at
  > offset 16 [-Werror=restrict]
  >          memcpy(copy_dst + 16, copy_src + 16, (size_t)(i - 16));
  >          ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  Paolo Bonzini <pbonzini@redhat.com> analyzed the Brotli source in detail,
  and concluded that the warning is a false positive:
  > This seems safe to me, because it's preceded by:
  >
  >     uint8_t* copy_dst = &s->ringbuffer[pos];
  >     uint8_t* copy_src = &s->ringbuffer[src_start];
  >     int dst_end = pos + i;
  >     int src_end = src_start + i;
  >     if (src_end > pos && dst_end > src_start) {
  >       /* Regions intersect. */
  >       goto CommandPostWrapCopy;
  >     }
  >
  > If [src_start, src_start + i) and [pos, pos + i) don't intersect, then
  > neither do [src_start + 16, src_start + i) and [pos + 16, pos + i).
  >
  > The if seems okay:
  >
  >        (src_start + i > pos && pos + i > src_start)
  >
  > which can be rewritten to:
  >
  >        (pos < src_start + i && src_start < pos + i)
  >
  > Then the numbers are in one of these two orders:
  >
  >      pos <= src_start < pos + i <= src_start + i
  >      src_start <= pos < src_start + i <= pos + i
  >
  > These two would be allowed by the "if", but they can only happen if pos
  > == src_start so they degenerate to the same two orders above:
  >
  >      pos <= src_start < src_start + i <= pos + i
  >      src_start <= pos < pos + i <= src_start + i
  >
  > So it is a false positive in GCC.
  Disable the warning for now.
  Cc: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Cc: Cole Robinson <crobinso@redhat.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Paolo Bonzini <pbonzini@redhat.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Reported-by: Cole Robinson <crobinso@redhat.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9222154ae7b3eef75ae88cdb56158256227cb929)

------------------------------------------------------------------------  r26486 | edk2buildsystem | 2018-03-05 14:05:55 -0800 (Mon, 05 Mar 2018) | 38 lines
  BaseTools/GenVtf: silence false "stringop-overflow" warning with memcpy()
  gcc-8 (which is part of Fedora 28) enables the new warning
  "-Wstringop-overflow" in "-Wall". This warning is documented in detail at
  <https://gcc.gnu.org/onlinedocs/gcc/Warning-Options.html>; the
  introduction says
  > Warn for calls to string manipulation functions such as memcpy and
  > strcpy that are determined to overflow the destination buffer.
  It breaks the BaseTools build with:
  > GenVtf.c: In function 'ConvertVersionInfo':
  > GenVtf.c:132:7: error: 'strncpy' specified bound depends on the length
  > of the source argument [-Werror=stringop-overflow=]
  >        strncpy (TemStr + 4 - Length, Str, Length);
  >        ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  > GenVtf.c:130:14: note: length computed here
  >      Length = strlen(Str);
  >               ^~~~~~~~~~~
  It is a false positive because, while the bound equals the length of the
  source argument, the destination pointer is moved back towards the
  beginning of the destination buffer by the same amount (and this amount is
  range-checked first, so we can't precede the start of the dest buffer).
  Replace both strncpy() calls with memcpy().
  Cc: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  Cc: Cole Robinson <crobinso@redhat.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Paolo Bonzini <pbonzini@redhat.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Reported-by: Cole Robinson <crobinso@redhat.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9de306701312f986c9638cb819d3f1f848d55cab)

------------------------------------------------------------------------  r26518 | edk2buildsystem | 2018-03-08 02:12:27 -0800 (Thu, 08 Mar 2018) | 31 lines
  BaseTools/header.makefile: revert gcc-8 "-Wno-xxx" options on OSX
  I recently added the gcc-8 specific "-Wno-stringop-truncation" and
  "-Wno-restrict" options to BUILD_CFLAGS, both for "Darwin" (XCODE5 /
  clang, OSX) and otherwise (gcc, Linux / Cygwin).
  I also regression-tested the change with gcc-4.8 on Linux -- gcc-4.8 does
  not know either of the (gcc-8 specific) "-Wno-stringop-truncation" and
  "-Wno-restrict" options, yet the build completed fine (by GCC design).
  Regarding OSX, my expectation was that
  - XCODE5 / clang would either recognize these warnings options (because
  clang does recognize most -W options of gcc),
  - or, similarly to gcc, clang would simply ignore the "-Wno-xxx" flags
  that it didn't recognize.
  Neither is the case; the new flags have broken the BaseTools build on OSX.
  Revert them (for OSX only).
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Reported-by: Liming Gao <liming.gao@intel.com>
  Fixes: 1d212a83df0eaf32a6f5d4159beb2d77832e0231
  Fixes: 9222154ae7b3eef75ae88cdb56158256227cb929
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  Acked-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
  (cherry picked from commit 777f4aa083e9f8b1853e454a0390d71dde2616da)

------------------------------------------------------------------------  r26533 | edk2buildsystem | 2018-03-10 02:05:43 -0800 (Sat, 10 Mar 2018) | 9 lines
  BaseTools: Fixed Pcd from command line issue.
  Save the pcd command line value in Pcd object
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 0f228f19fb40ffe60b13962ff639917435c562a9)

------------------------------------------------------------------------  r26534 | edk2buildsystem | 2018-03-10 02:06:14 -0800 (Sat, 10 Mar 2018) | 8 lines
  BaseTools: Update --pcd parser to support flexible pcd format
  This patch update --pcd parser to support flexible pcd format.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 8565b5829c1f30408020a4adb37074dba5492378)

------------------------------------------------------------------------  r26535 | edk2buildsystem | 2018-03-10 02:06:53 -0800 (Sat, 10 Mar 2018) | 9 lines
  BaseTools: Fix a bug for --pcd used in ConditionalStatement calculate
  Move the GlobalData.BuildOptionPcd before FdfParser() function and add
  type check for Pcd item.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 705ed563de86475a32fb555d4238cc10717294f8)

------------------------------------------------------------------------  r26536 | edk2buildsystem | 2018-03-10 02:07:01 -0800 (Sat, 10 Mar 2018) | 10 lines
  BaseTools: Fix parse OFFSET_OF get wrong offset
  Fix parse OFFSET_OF get wrong offset
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b31501c90abcea74c03e86a3bd9f6190cb4e1ddd)

------------------------------------------------------------------------  r26537 | edk2buildsystem | 2018-03-10 02:07:29 -0800 (Sat, 10 Mar 2018) | 10 lines
  BaseTools: GlobalData remove unused variable
  gWideStringPattern is not used.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7878f706e7eb8f29f66961d20eaa3e97dac22b00)

------------------------------------------------------------------------  r26550 | edk2buildsystem | 2018-03-12 02:06:12 -0700 (Mon, 12 Mar 2018) | 9 lines
  BaseTools: Get Pcd DatumType from DEC file for --pcd
  It is regression bug that missing the Pcd DatumType info from DEC file
  for --pcd .
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 87a1f65e80cf183a87072df04d749b0aa12171d9)

------------------------------------------------------------------------  r26617 | edk2buildsystem | 2018-03-16 02:06:47 -0700 (Fri, 16 Mar 2018) | 11 lines
  BaseTools: UPT: remove unused variable and inaccessible code.
  gINCLUDE_PATTERN is never used.
  IncList is always empty.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b3fa393f477a12fe0e1aedb36395ca9b345ae110)

------------------------------------------------------------------------  r26656 | edk2buildsystem | 2018-03-17 02:08:54 -0700 (Sat, 17 Mar 2018) | 22 lines
  BaseTools: --hash --binary-destination generate wrong binary path
  Option --hash --binary-destination generate Binaries section in
  the inf file, but the path of ASL file is begin with
  Output directory,  so need replace Output directory with '',
  will get the file name RamDisk.aml
  Incorrect AML file path in inf file on linux:
  [Binaries.X64]
  PE32|RamDiskDxe.efi
  ASL|home/tiano/Desktop/hash/edk2/Build/OvmfX64/RELEASE_GCC5/X64
  /MdeModulePkg/Universal/Disk/RamDiskDxe/RamDiskDxe/OUTPUT/RamDisk.aml
  DXE_DEPEX|RamDiskDxe.depex
  BIN|RamDiskDxeOffset.bin
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 90456c3c06d9c370b48417754ece2fb8252da5f8)

------------------------------------------------------------------------  r26657 | edk2buildsystem | 2018-03-17 14:05:56 -0700 (Sat, 17 Mar 2018) | 9 lines
  BaseTools: Detect structure pcd header file change.
  Detect structure pcd header file change
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 34d808add3dc23aaa37e1c9edb2fcc2b50118367)

------------------------------------------------------------------------  r26658 | edk2buildsystem | 2018-03-18 02:05:24 -0700 (Sun, 18 Mar 2018) | 11 lines
  BaseTools: Fix bug for VOID* DynamicDefault Pcd use Flexible format
  define a flexible pcd format in Dyanmic/DynamicExDefault section,
  it cause build error.
  [PcdsDynamicExDefault.common.DEFAULT]
  pcdToken.Name|{GUID("11111111-2222-42eb-b5eb-fef31d207cb4")}
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 316b43dee56837ed7d382e8de4a78d6bb9d14eb7)

------------------------------------------------------------------------  r26668 | edk2buildsystem | 2018-03-19 02:05:55 -0700 (Mon, 19 Mar 2018) | 10 lines
  BaseTools: Expression - remove redundant variable
  Str is created and not needed.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ae4cc2b084a67d671a116808ac82e59ab770afc0)

------------------------------------------------------------------------  r26669 | edk2buildsystem | 2018-03-19 14:05:53 -0700 (Mon, 19 Mar 2018) | 11 lines
  BaseTools: Expression refactor function
  The function is about C Names, not C Strings.
  Move the re.compile outside the function call
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1f901a89f053dfa8c64904a582622a33a669b605)

------------------------------------------------------------------------  r26670 | edk2buildsystem | 2018-03-19 14:06:00 -0700 (Mon, 19 Mar 2018) | 11 lines
  BaseTools: Expression - change from series of if to elif
  since the first character of the string cannot be found by multiple if
  statements, use elif to optomize the behavior.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 3e8bab960eca8464ab1d0f2ad3f06a2ccc925f95)

------------------------------------------------------------------------  r26671 | edk2buildsystem | 2018-03-19 14:06:05 -0700 (Mon, 19 Mar 2018) | 10 lines
  BaseTools: Expression - remove variable
  The InArary variable serves no purpose.  just do the work immediately.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 47f7040ddbdfea033ef6e6b76f4c8fa19f67aaae)

------------------------------------------------------------------------  r26672 | edk2buildsystem | 2018-03-19 14:06:22 -0700 (Mon, 19 Mar 2018) | 10 lines
  BaseTools: RangeExpression - remove unused variable
  remove a never used variable.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit c1e732344a1a157267ff0b550b7a35f1a4f1178f)

------------------------------------------------------------------------  r26674 | edk2buildsystem | 2018-03-19 14:06:35 -0700 (Mon, 19 Mar 2018) | 9 lines
  BaseTool: Error handling for PCD datumtype.
  Report error if the Pcd DatumType is wrong.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 065a7d406cf8ebc71edb2afc66a70f11d9e83a58)

------------------------------------------------------------------------  r26686 | edk2buildsystem | 2018-03-20 02:06:18 -0700 (Tue, 20 Mar 2018) | 9 lines
  BaseTools: Add Feature Flag Pcd Type into Override list
  when only define the PCD in the DEC file, and use --pcd feature,
  we also need cover this case for Feature Flag Type.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b7bfcd1a7e96524d15345e420c3f7120c29a107f)

------------------------------------------------------------------------  r26687 | edk2buildsystem | 2018-03-20 02:06:24 -0700 (Tue, 20 Mar 2018) | 12 lines
  BaseTools: Fix bug for --pcd VOID* type when no max size is specified
  when VOID* type non-structure pcd used in --pcd, and its max size is not
  specified in DSC or its value is hex value, build break due to the code
  int(Pcd.MaxDatumSize,10).
  Now this patch remove this code, because tool will calculate the size
  info in later phase.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 29d521b9fa00045eb036c353e0b8f5ebe9c12a98)

------------------------------------------------------------------------  r26690 | edk2buildsystem | 2018-03-21 02:06:12 -0700 (Wed, 21 Mar 2018) | 10 lines
  BaseTools: Override Max size by build Option Pcd for HII type
  Current code will generate maxsize for HII type PCD when parser DSC
  file, while this HII type PCD value maybe override in build command
  per --pcd option, so the max size need re-calculate.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c8ae65ac5218973e473ba1ba4bd5f9ccb547a219)

------------------------------------------------------------------------  r26691 | edk2buildsystem | 2018-03-21 02:06:18 -0700 (Wed, 21 Mar 2018) | 11 lines
  BaseTools: StrGather has redundant declaration
  remove COMPATIBLE_STRING_TOKEN as it is the same as STRING_TOKEN
  remove if statement that used one or the other (identical) re
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit afb04ba198799e1a377e7518965c7eb29c26732b)

------------------------------------------------------------------------  r26692 | edk2buildsystem | 2018-03-21 02:06:28 -0700 (Wed, 21 Mar 2018) | 11 lines
  BaseTools: StrGather simplify string/int conversion functions
  use ''.format instead of eval() and use some list comprehension for making list
  delete some unused variables
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 549c59b30cdd5ca9c1b707df1d1ebda0060675e4)

------------------------------------------------------------------------  r26693 | edk2buildsystem | 2018-03-21 02:06:34 -0700 (Wed, 21 Mar 2018) | 10 lines
  BaseTools: StrGather remove functions no one calls
  simplify the code and remove functions not called anymore
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4d83616f9d7731934e7f91058efb165a2bc5b9d7)

------------------------------------------------------------------------  r26694 | edk2buildsystem | 2018-03-21 02:06:44 -0700 (Wed, 21 Mar 2018) | 11 lines
  BaseTools: FdfParser & FdfParserLite refactor regular expression for GUIDs
  Instead of recompiling it each time the API is called, just use
  the global one that exists.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 2eb370ffdb179a865a65a3bca40d284958e42424)

------------------------------------------------------------------------  r26695 | edk2buildsystem | 2018-03-21 02:07:08 -0700 (Wed, 21 Mar 2018) | 10 lines
  BaseTools: FdfParser remove class never used.
  the MacroProfile class is never instantiated nor referenced.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ca2c8725c4894c55ffd7ce091e5f0c4ef9c794ed)

------------------------------------------------------------------------  r26716 | edk2buildsystem | 2018-03-23 02:05:32 -0700 (Fri, 23 Mar 2018) | 8 lines
  BaseTools: Add the missing package include directory in PcdValueInit Makefile
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Cc: Feng Bob C <bob.c.feng@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b005802a1c860a0f7ed9a727ce3ffc3ea7f9c441)

------------------------------------------------------------------------  r26717 | edk2buildsystem | 2018-03-23 02:05:40 -0700 (Fri, 23 Mar 2018) | 10 lines
  BaseTool: Fixed the issue of empty PcdDB.
  If there is no dynamic pcds, there should be DB header
  in the Pcd DataBase.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bob Feng <bob.c.feng@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 0a4f2d48696f094cec73e28a4402775dc6262eef)

------------------------------------------------------------------------  r26718 | edk2buildsystem | 2018-03-23 02:06:12 -0700 (Fri, 23 Mar 2018) | 10 lines
  BaseTool/VfrCompile: make delete[] match with new[]
  REF: https://bugzilla.tianocore.org/show_bug.cgi?id=764
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f7e98581021b2dd29824f1de03c523b9c1ec617a)

------------------------------------------------------------------------  r26719 | edk2buildsystem | 2018-03-23 02:06:22 -0700 (Fri, 23 Mar 2018) | 10 lines
  BaseTool/VfrCompile: Fix potential memory leak issue
  REF: https://bugzilla.tianocore.org/show_bug.cgi?id=771
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Dandan Bi <dandan.bi@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 65e0e10d23323b18f31bf9aa9eef3c2434f53780)

------------------------------------------------------------------------  r26724 | edk2buildsystem | 2018-03-27 02:06:15 -0700 (Tue, 27 Mar 2018) | 8 lines
  BaseTools/ECC: Add a new exception support
  Add a new exception support for the checkPoint of no use C type.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hess Chen <hesheng.chen@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit dbc85eb993439a7006bb20091c1cc6de43d19e80)

------------------------------------------------------------------------  r26725 | edk2buildsystem | 2018-03-27 02:06:37 -0700 (Tue, 27 Mar 2018) | 10 lines
  BaseTools: Autogen - modify to use standard parent/child class relationships
  use __new__ and __init__ to create/manage/initialize objects in standard flow.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b24e99f7c4270e7c5e2df511a41ff70e46138612)

------------------------------------------------------------------------  r26726 | edk2buildsystem | 2018-03-27 02:06:49 -0700 (Tue, 27 Mar 2018) | 17 lines
  BaseTools: Update Rsa2048Sha256Sign to use openssl standard options
  sha256 is not the standard option. It should be replaced by sha -sha256.
  Otherwise, it doesn't work in MAC OS.
  In V2, update the option to sha1 -sha256.
  In late openssl version >= 1.1, there is no sha option, but has sha1,sha256.
  In previous openssl version < 1.1, there is no sha256, but has sha,sha1.
  To work with all openssl version, use sha1 -sha256 for it.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liao Jui-peng <jui-pengx.liao@intel.com>
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Cc: Michael Kinney <michael.d.kinney@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1d574dfc15e4495a4063ce4faf3c2e9191677d8d)

------------------------------------------------------------------------  r26727 | edk2buildsystem | 2018-03-28 02:05:29 -0700 (Wed, 28 Mar 2018) | 8 lines
  BaseTools: Update Rsa2048Sha256Sign to use openssl dgst option
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Qin Long <qin.long@intel.com>
  Reviewed-by: Qin Long <qin.long@intel.com>
  (cherry picked from commit d1b777440bc616f1e6da9204f3eec9f7a5a6f2e2)

------------------------------------------------------------------------  r26742 | edk2buildsystem | 2018-03-29 02:05:38 -0700 (Thu, 29 Mar 2018) | 12 lines
  BaseTools: FdfParser and FdfParserLite share reg exp
  FdfParser can share regular expression from FdfParserLite.
  reduce overlap and reduce recompile of the same expression.
  v2: fix missed replacement of Pattern with shared variable
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4d603daa3a2276d98ac6749d1db8e327ff7c1f5f)

------------------------------------------------------------------------  r26743 | edk2buildsystem | 2018-03-29 02:05:45 -0700 (Thu, 29 Mar 2018) | 10 lines
  BaseTools: GlobalData share same MACRO name definition
  use the same MACRO name definition across shared regular expression patterns.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0f17c9fef104d5f0eaa382266e0489f1fa0ed986)

------------------------------------------------------------------------  r26744 | edk2buildsystem | 2018-03-29 02:05:50 -0700 (Thu, 29 Mar 2018) | 10 lines
  BaseTools: add GUID pattern to global data
  add a shared global regular expression for GUID matching
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit cd67d66484e44af587183d52f0affa9105547518)

------------------------------------------------------------------------  r26745 | edk2buildsystem | 2018-03-29 02:05:56 -0700 (Thu, 29 Mar 2018) | 13 lines
  BaseTools: Regular Expressions refactor out the hex char for later reuse
  move hex character info from GUID expressions into seperate variable to
  facilitate reuse.
  I had a type with insufficient {} in the first version.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 256e2d885b053a6c6a04bf3b3eaffe128c023ba7)

------------------------------------------------------------------------  r26746 | edk2buildsystem | 2018-03-29 02:06:01 -0700 (Thu, 29 Mar 2018) | 11 lines
  BaseTools: Add new RegExp for future use
  Add a precompiled RegExp for 4 hex chars.
  v2: fixed incorrect numbers of {}
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 9e7790a352ee4cbe4b8d2a051345c750c086c9a6)

------------------------------------------------------------------------  r26747 | edk2buildsystem | 2018-03-29 02:06:07 -0700 (Thu, 29 Mar 2018) | 10 lines
  BaseTools: GlobalData Add a regular expression for a hex number
  add a shared precompiled regular expression
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0760ed06a139aa6f84568147e3ee4fe919469238)

------------------------------------------------------------------------  r26749 | edk2buildsystem | 2018-03-29 02:06:22 -0700 (Thu, 29 Mar 2018) | 11 lines
  BaseTools: use new shared GUID regular expressions
  remove local variables that are GUID matching and replace with shared
  expression.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b1a9e404d4e91729b99d690fa849451269dd3a47)

------------------------------------------------------------------------  r26750 | edk2buildsystem | 2018-03-29 02:06:28 -0700 (Thu, 29 Mar 2018) | 10 lines
  BaseTools: Use precompiled RegExp
  avoid recompiling the regular expression for each use in a while loop
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 018f7b827fa4def3476f76cdf1d6400d4a8e6ebc)

------------------------------------------------------------------------  r26751 | edk2buildsystem | 2018-03-29 02:06:35 -0700 (Thu, 29 Mar 2018) | 10 lines
  BaseTools: remove local hex number regular expression
  Change to using the new shared hex number regular expression
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 56326323e6579d4cde9802c684baba06acbdb1d2)

------------------------------------------------------------------------  r26752 | edk2buildsystem | 2018-03-29 02:06:41 -0700 (Thu, 29 Mar 2018) | 10 lines
  BaseTools: expression can use single in instead of 3 API calls.
  change 3 StartsWith() calls to a single 'in' operation.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 663b9e061ed1b48e562159e51333e996f1efc830)

------------------------------------------------------------------------  r26753 | edk2buildsystem | 2018-03-29 02:06:47 -0700 (Thu, 29 Mar 2018) | 10 lines
  BaseTools: move regular expression compile out of function call.
  move to the root of the file and dont recompile.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 38504ad3e3163fd8afbfc66760455df9dd223713)

------------------------------------------------------------------------  r26754 | edk2buildsystem | 2018-03-29 02:06:53 -0700 (Thu, 29 Mar 2018) | 11 lines
  BaseTools: dont use enumerate when un-needed
  Since we only use the item from the list and not the numeric value,
  dont bother with enumerate()
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit e52aed0d855218f23cbd94629561eb4155936cec)

------------------------------------------------------------------------  r26755 | edk2buildsystem | 2018-03-29 02:06:59 -0700 (Thu, 29 Mar 2018) | 10 lines
  BaseTools: refactor repeated RegExp when no special searching is needed.
  use str.replace and try/except.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit cc0321f22ac7422a2d477c98fed209547eaf0cb5)

------------------------------------------------------------------------  r26756 | edk2buildsystem | 2018-03-29 02:07:04 -0700 (Thu, 29 Mar 2018) | 12 lines
  BaseTools: compare GUID value should not case-sensitive
  build report error when the same Guid value in FDF file use lowercase,
  in tools_def.txt file use uppercase.
  The guid value's compare should not case-sensitive.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Bin Wang <binx.a.wang@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b1956b5d42182309604d008036882e62f17d1ccf)

------------------------------------------------------------------------  r26758 | edk2buildsystem | 2018-03-30 02:06:52 -0700 (Fri, 30 Mar 2018) | 10 lines
  BaseTools: Remove equality operator with None
  replace "== None" with "is None" and "!= None" with "is not None"
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4231a8193ec0d52df7e0a101d96c51b1a2b7a996)

------------------------------------------------------------------------  r26759 | edk2buildsystem | 2018-03-30 02:07:22 -0700 (Fri, 30 Mar 2018) | 10 lines
  BaseTools: no need to do int() API work for it
  int() with base=0 will already auto determine base from preceeding 0x/0X
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0944818a1972b07b09b53a2a1e88295cd92361cf)

------------------------------------------------------------------------  r26760 | edk2buildsystem | 2018-03-30 02:07:27 -0700 (Fri, 30 Mar 2018) | 10 lines
  BaseTools: use in to compare single chars
  instead if 3 Startswith for single chars, just use in with a list of chars
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0a014fba41b631258687f56e630518b54817d062)

------------------------------------------------------------------------  r26761 | edk2buildsystem | 2018-03-30 02:07:32 -0700 (Fri, 30 Mar 2018) | 11 lines
  BaseTools: remove loop and variables.
  this loop does nothing. none of Key, Item, nor DevicePathList
  are ever used.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 5fbb0f9908ded1944aa4bba599ccc4c605987cb7)

------------------------------------------------------------------------  r26762 | edk2buildsystem | 2018-03-30 02:07:38 -0700 (Fri, 30 Mar 2018) | 10 lines
  BaseTools: cleanup class heirarchy
  remove totally empty classes from class heirarchy
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0b560b980ce00588e540a480532dd48328a9f003)

------------------------------------------------------------------------  r26774 | edk2buildsystem | 2018-04-05 02:05:51 -0700 (Thu, 05 Apr 2018) | 10 lines
  BaseTools: use single RegExp for token matching
  same pattern was compiled 3 places in the file.  just compile once and share.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4f9e71e1f75cafa2ed1c87e8a4e91b9f1f23c90a)

------------------------------------------------------------------------  r26775 | edk2buildsystem | 2018-04-05 02:06:01 -0700 (Thu, 05 Apr 2018) | 10 lines
  BaseTools: use new RegEx from FdfParserLite
  FdfParser has identical one.  import and share.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 147a656b3414667aeafdad0a8fd5504ddad96367)

------------------------------------------------------------------------  r26776 | edk2buildsystem | 2018-04-05 02:06:07 -0700 (Thu, 05 Apr 2018) | 10 lines
  BaseTools: change hex parsing to use built in
  use <char> in string.hexdigits instead of custom functions.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit cfbe3c3500a64e218e7d357dacb18d8b95eddfec)

------------------------------------------------------------------------  r26777 | edk2buildsystem | 2018-04-05 02:06:15 -0700 (Thu, 05 Apr 2018) | 10 lines
  BaseTools: remove uncalled function
  no one calls __IsWhiteSpace() (none of the 4 copies)
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 231fdbb2107a2b359042626263317d8e494165dd)

------------------------------------------------------------------------  r26778 | edk2buildsystem | 2018-04-05 02:06:22 -0700 (Thu, 05 Apr 2018) | 10 lines
  BaseTools: make static functions when self is not needed
  remove self, and add @staticmethod to functions
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 5bcf1d5671061bbcc3ee752fdf9b9d7bcce84665)

------------------------------------------------------------------------  r26779 | edk2buildsystem | 2018-04-05 02:06:28 -0700 (Thu, 05 Apr 2018) | 10 lines
  BaseTools: remove uncalled functions
  this same function in 2 classes is never called.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit c4172f80051effc62f3eceeeced4c0b66a80eb94)

------------------------------------------------------------------------  r26798 | edk2buildsystem | 2018-04-08 02:06:34 -0700 (Sun, 08 Apr 2018) | 10 lines
  BaseTools: Use local variable for list of constants.
  instead of listing in multiple places, use a single list.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 5060928b12724d7d6030aa9a472dc113f226386c)

------------------------------------------------------------------------  r26799 | edk2buildsystem | 2018-04-08 02:06:53 -0700 (Sun, 08 Apr 2018) | 10 lines
  BaseTools: use built in dict instead of custom version.
  We dont use any feature added by custom dictionary class.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 5af2a627d13f00f7dd782dde9db2ac7b821e8816)

------------------------------------------------------------------------  r26800 | edk2buildsystem | 2018-04-08 02:07:06 -0700 (Sun, 08 Apr 2018) | 11 lines
  BaseTools: Eot tool never populates this dictionary
  we initialize this dict and then check it's contents, but never add items.
  we can remove it without any effect.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 140b2b11a0dc7a414b93a9b8a50f5944d7a55d3e)

------------------------------------------------------------------------  r26801 | edk2buildsystem | 2018-04-08 02:07:20 -0700 (Sun, 08 Apr 2018) | 8 lines
  BaseTools: remove unused import statement
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 386eb9d7935505ff13b07379832a02fe971ff61c)

------------------------------------------------------------------------  r26802 | edk2buildsystem | 2018-04-08 02:07:41 -0700 (Sun, 08 Apr 2018) | 10 lines
  BaseTools - AutoGen - replace custom dictionary class with python standard one
  We have a custom ordered dictionary class.  works fine with python OrderedDict version.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 9006a2c6a35bfa607ddaa6d6c2a0738b65f6da97)

------------------------------------------------------------------------  r26803 | edk2buildsystem | 2018-04-08 02:07:48 -0700 (Sun, 08 Apr 2018) | 10 lines
  BaseTools: Eot remove unused code
  2 functions and a dictionary that are not used.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0d8ff45567fd8fc8e89cdfd646f585c4984ec1b1)

------------------------------------------------------------------------  r26804 | edk2buildsystem | 2018-04-08 02:08:36 -0700 (Sun, 08 Apr 2018) | 10 lines
  BaseTools: use built in OrderedDict instead of custom version.
  We dont use any feature added by custom dictionary class.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 6e6d767edf855320e49892e5f8773e0b3394b975)

------------------------------------------------------------------------  r26805 | edk2buildsystem | 2018-04-08 02:10:40 -0700 (Sun, 08 Apr 2018) | 11 lines
  BaseTools: use combined version of OrderedDict
  since we need order and a default entry, use collections dicts to
  auto generate.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1f1c67128430bfd8a57213f7147d56f194880a51)

------------------------------------------------------------------------  r26806 | edk2buildsystem | 2018-04-08 02:11:54 -0700 (Sun, 08 Apr 2018) | 10 lines
  BaseTools: Workspace - use built in OrderedDict instead of custom version.
  We dont use any feature added by custom dictionary class.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a0767bae298443c91bae1e1fb43eb0ed9a436004)

------------------------------------------------------------------------  r26807 | edk2buildsystem | 2018-04-08 02:12:09 -0700 (Sun, 08 Apr 2018) | 11 lines
  BaseTools: Remove unused code from Misc
  remove the functions and classes
  remove any imports of these
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ab0ff0b0a633f5f566e434f7625009a92f02304c)

------------------------------------------------------------------------  r26808 | edk2buildsystem | 2018-04-08 02:12:27 -0700 (Sun, 08 Apr 2018) | 10 lines
  BaseTools: Autogen - move RegEx compile
  compile each RegEx once not in loops/functions
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit c8802c3dccbead06fb69ec2e91a361d6ac1e93fb)

------------------------------------------------------------------------  r26809 | edk2buildsystem | 2018-04-08 02:12:50 -0700 (Sun, 08 Apr 2018) | 10 lines
  BaseTools: GenFds - move RegEx compile
  compile each RegEx once not in loops/functions
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ffe720c53ecf57296e396ee64a78773539047fb8)

------------------------------------------------------------------------  r26810 | edk2buildsystem | 2018-04-08 02:13:02 -0700 (Sun, 08 Apr 2018) | 8 lines
  BaseTools: Add new RegEx pattern to GlobalData
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 7da06eeede10fc8b908327b375bcdf36707ff7b5)

------------------------------------------------------------------------  r26811 | edk2buildsystem | 2018-04-08 02:13:27 -0700 (Sun, 08 Apr 2018) | 8 lines
  BaseTools: AutoGen - use the new shared RegEx
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1f26f5fdb96b4a0010c4388273fc42d551170dd6)

------------------------------------------------------------------------  r26812 | edk2buildsystem | 2018-04-08 02:13:41 -0700 (Sun, 08 Apr 2018) | 10 lines
  BaseTools: remove redundant check
  The RegEx matches begining and end of the string, dont then check length.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit bfc8f5667a68071e7f12a9ba2a0cf076b1285107)

------------------------------------------------------------------------  r26813 | edk2buildsystem | 2018-04-08 02:13:59 -0700 (Sun, 08 Apr 2018) | 10 lines
  BaseTools: move RegEx to root of file and share it
  make it easy to import and use by others
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit e6c2468a9e6158b6bf669f05129a1dd362d52753)

------------------------------------------------------------------------  r26814 | edk2buildsystem | 2018-04-08 02:14:07 -0700 (Sun, 08 Apr 2018) | 12 lines
  BaseTools: Autogen - change from list to set
  by changing from list to set(), we can skip all the preprocessing
  to prevent duplication and we dont need to convert to a set() later
  on for each use
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ff5635e9acbf8a4d0c4095e78f72f97ae94ce43b)

------------------------------------------------------------------------  r26815 | edk2buildsystem | 2018-04-08 02:14:21 -0700 (Sun, 08 Apr 2018) | 10 lines
  BaseTools: small cleanup
  just deleting else: then pass as they have no effect.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit f8c0a004a54b955b4d1dc4e6dc2fae3b87008224)

------------------------------------------------------------------------  r26817 | edk2buildsystem | 2018-04-09 02:06:00 -0700 (Mon, 09 Apr 2018) | 10 lines
  BaseTools: Remove FdfParserLite.py from source since it is not used
  Remove FdfParserLite.py from source code since it is not used.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 95cc4962167572089a99be324574094ba22415ad)

------------------------------------------------------------------------  r26818 | edk2buildsystem | 2018-04-09 02:08:01 -0700 (Mon, 09 Apr 2018) | 10 lines
  BaseTools: dont make temporary dict
  just make the key list directly
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 175a4b5db39f57721022990ac8b92cf33015fa0b)

------------------------------------------------------------------------  r26819 | edk2buildsystem | 2018-04-09 02:09:25 -0700 (Mon, 09 Apr 2018) | 9 lines
  BaseTools: Pcd not used info should not in Module PCD section
  Pcds in Conditional Directives and Pcds not used are Platform Level
  info, it should not display in Module PCD Section.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b91b8ee4c97a8ac52986f850e05765bffcfc9479)

------------------------------------------------------------------------  r26820 | edk2buildsystem | 2018-04-09 02:10:24 -0700 (Mon, 09 Apr 2018) | 10 lines
  BaseTools: Pcds in [Components] are not display correct in the report
  The Pcd used in [Components] section, the PCD value is displayed
  incorrect in the build report because the PCD default value was not
  override.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 64797018df0cf5c1f11523bb575355aba918b940)

------------------------------------------------------------------------  r26830 | edk2buildsystem | 2018-04-13 21:34:35 -0700 (Fri, 13 Apr 2018) | 10 lines
  BaseTools: remove unused file
  ToolsDefClassObject didnt need Dictionary, it needed an import from there.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ce3082a6e799ebcd621c8983ee4a8b6d6ca9b472)

------------------------------------------------------------------------  r26831 | edk2buildsystem | 2018-04-13 21:49:44 -0700 (Fri, 13 Apr 2018) | 8 lines
  BaseTools: remove uncalled functions
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit eb2c0b2c80fc684f7ff230daf99b9f0d2fb77d4a)

------------------------------------------------------------------------  r26832 | edk2buildsystem | 2018-04-13 21:49:52 -0700 (Fri, 13 Apr 2018) | 10 lines
  BaseTools: defaultdict(set) allows us to just add to the set
  New sets will get created automatically when needed
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a993dc03abf55bac0eead1efea7c4d15b8b8894a)

------------------------------------------------------------------------  r26833 | edk2buildsystem | 2018-04-13 21:50:01 -0700 (Fri, 13 Apr 2018) | 15 lines
  BaseTools: sets are faster to check via "in" due to hashing
  switch list to set:
  1)we dont care about order
  2)we only check for membership.
  then remove ".keys()" from dict looping:
  allow generators opportunity to optimize
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b74b419a0156fbc60423c721165b3741469bc1a1)

------------------------------------------------------------------------  r26834 | edk2buildsystem | 2018-04-13 21:50:13 -0700 (Fri, 13 Apr 2018) | 10 lines
  BaseTools: replace a dict with a set
  As we never use the values, just keep the keys in a set.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 6b26dd716524114a7379a8e87882d8851882b73c)

------------------------------------------------------------------------  r26835 | edk2buildsystem | 2018-04-13 21:50:22 -0700 (Fri, 13 Apr 2018) | 11 lines
  BaseTools: remove unused variables
  some were populated, but never used after.
  some were never used.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit d98cce8e6364296909135ba27b53d3b31bff73d2)

------------------------------------------------------------------------  r26836 | edk2buildsystem | 2018-04-13 21:50:30 -0700 (Fri, 13 Apr 2018) | 11 lines
  BaseTools: change list to set
  Order is irelevant
  duplication is auto-prevented
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ac55e47818a960fe1d3f9047035ebfa8a59ca227)

------------------------------------------------------------------------  r26837 | edk2buildsystem | 2018-04-13 21:50:40 -0700 (Fri, 13 Apr 2018) | 10 lines
  BaseTools: simplify testing for existance and containing data
  and remove a duplicate "if" block from 6 lines up.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 6be947438f746baf16afe290ec4ca23ade71400f)

------------------------------------------------------------------------  r26838 | edk2buildsystem | 2018-04-13 21:50:49 -0700 (Fri, 13 Apr 2018) | 11 lines
  BaseTools: optimize buildoptions loop
  change a dict to a double defaultdict to prevent needing to seed innter values.
  move "Value" determination under a conditional continue statement
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 339fe8dd6a4e756f87825c8f1dd5c38204951985)

------------------------------------------------------------------------  r26839 | edk2buildsystem | 2018-04-13 21:50:58 -0700 (Fri, 13 Apr 2018) | 10 lines
  BaseTools: change another list to set
  potentially accelerate "in" testing which is the use for this variable
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 29189291e5927381d1465d96792115e39ef4da69)

------------------------------------------------------------------------  r26840 | edk2buildsystem | 2018-04-13 21:51:07 -0700 (Fri, 13 Apr 2018) | 8 lines
  BaseTools: remove unneeded function call
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit e1ed31e65e8cc0359c0948f6edc6abb7191c26e6)

------------------------------------------------------------------------  r26841 | edk2buildsystem | 2018-04-13 21:51:19 -0700 (Fri, 13 Apr 2018) | 11 lines
  BaseTools: change more list to set
  potentially accelerate "in" testing
  remove uncalled function
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit d0ef841c8e46327b029965f2b4a79127428ce6a5)

------------------------------------------------------------------------  r26842 | edk2buildsystem | 2018-04-13 21:51:28 -0700 (Fri, 13 Apr 2018) | 10 lines
  BaseTools: GenC - move content from both parts of if/else
  move identical lines out of both if and else and move 1 level up.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 674e2014ce63040880208f2a0494fa1849f28f43)

------------------------------------------------------------------------  r26843 | edk2buildsystem | 2018-04-13 21:51:40 -0700 (Fri, 13 Apr 2018) | 10 lines
  BaseTools: refactor and remove out of date use of .keys()
  this is no longer required to make dictionary objects iterable.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 98120f5fe2199de29c0cce8e92c692b23adf0cf7)

------------------------------------------------------------------------  r26844 | edk2buildsystem | 2018-04-13 21:51:50 -0700 (Fri, 13 Apr 2018) | 17 lines
  BaseTools: Parse PCD GUID name in FILE statement issue
  FDF format as below:
  FILE APPLICATION = PCD(PcdToken.PcdCName) {
  }
  when parse PCD, need get all PCDs from Platform and Packages,
  use self.BuildObject[self.Platform, Arch] get some modules is wrong.
  so use self.BuildObject[self.Platform, Arch, TargetName, ToolChainTag]
  get all modules.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b9a6d9d7ca59563b769fbf0218f204913bddf45d)

------------------------------------------------------------------------  r26845 | edk2buildsystem | 2018-04-13 21:51:59 -0700 (Fri, 13 Apr 2018) | 9 lines
  BaseTools: Fix a bug for VOID* type Fixatbuild Pcd in Library
  The case is a FixedAtBuild VOID* PCD is used from a lib, but is set to a
  different sized value in a module INF scope <PcdsFixedAtBuild> section.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1bfcf64f39ce33fd6529c91fad6e9fe50f1698b1)

------------------------------------------------------------------------  r26846 | edk2buildsystem | 2018-04-13 21:52:09 -0700 (Fri, 13 Apr 2018) | 11 lines
  BaseTools: Fix a bug for Size incorrect of Void* Fixatbuild Pcd
  when driver link library and there have pcd override in DSC component
  section, in the library autogen file, the pcd's size is incorrect, the
  size value is from DSC [pcd] section, but not from the override pcd
  value that in the [component] section.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit eca980c0c899d9c2c57327e8af03fabe1da5feef)

------------------------------------------------------------------------  r26847 | edk2buildsystem | 2018-04-13 21:52:24 -0700 (Fri, 13 Apr 2018) | 10 lines
  BaseTools: Fix size override issue for Void* Patchable pcd
  when multiple driver link same library, and the drivers override the pcd
  to different value in the DSC component section, it cause the pcd size
  incorrect.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f7b31aa540435f43f5c60e7bde456c272b31f7ee)

------------------------------------------------------------------------  r26848 | edk2buildsystem | 2018-04-13 21:52:43 -0700 (Fri, 13 Apr 2018) | 10 lines
  BaseTools: Fix the bug for VOID* pcd max size from component section
  When the Pcd defined in components section, its value's size is larger
  than the value's size in [pcd] section, it cause build error, because
  original code use the size get in [pcd] section as max size.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c33081c912968da46fd6f0c7d2d2e52b7b410626)

------------------------------------------------------------------------  r26849 | edk2buildsystem | 2018-04-13 21:53:04 -0700 (Fri, 13 Apr 2018) | 17 lines
  BaseTools: Fix two cases that use GUID CName as PCD Value
  1. use CName format in components section:
  [Components]
  TestPkg/TestDriver.inf {
  <PcdsFixedAtBuild>
  PcdToken.PcdName |{GUID(TestGuid)}|VOID*|16
  }
  2. Use Guid CName format in INF and the Guid is defined in the DEC
  file but not write in driver's [Guids] section.
  PcdToken.PcdName  | {GUID(TestGuid)}
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f9fa014ee01cd8ecda091e1c1d9cb09724957e72)

------------------------------------------------------------------------  r26850 | edk2buildsystem | 2018-04-13 21:53:22 -0700 (Fri, 13 Apr 2018) | 10 lines
  BaseTools: copy a dictionary from InfClassObject to BuildReport
  InfClassObject will be deleted.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit f6562949e4e9bf8f83969ec851b7319fbc4db509)

------------------------------------------------------------------------  r26851 | edk2buildsystem | 2018-04-13 21:53:46 -0700 (Fri, 13 Apr 2018) | 10 lines
  BaseTools: Remove EdkIIWorkspaceBuild.py from source code
  Remove EdkIIWorkspaceBuild.py from source code
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit e96995a134bb689147c7856e842dd0a3678d5153)

------------------------------------------------------------------------  r26852 | edk2buildsystem | 2018-04-13 21:54:09 -0700 (Fri, 13 Apr 2018) | 14 lines
  BaseTools: Remove unneeded files
  These files are not used by any tool:
  BaseTools/Source/Python/Common/DecClassObject.py
  BaseTools/Source/Python/Common/DscClassObject.py
  BaseTools/Source/Python/Common/FdfClassObject.py
  BaseTools/Source/Python/Common/InfClassObject.py
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 13d909f89a3cee1c1f6b851a4cda7bd1a44e90ae)

------------------------------------------------------------------------  r26854 | edk2buildsystem | 2018-04-13 21:54:37 -0700 (Fri, 13 Apr 2018) | 10 lines
  BaseTools: Fix the build error caused by eca980c0c899
  Roll back the fixed at build pcd collection to include the pcd in
  Module and Library.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Tested-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 8b0e67821bd66af70433ee4bb858325f3033609a)

------------------------------------------------------------------------  r26855 | edk2buildsystem | 2018-04-13 21:54:46 -0700 (Fri, 13 Apr 2018) | 10 lines
  BaseTools: Correct GenSec argument dummy free memory issue
  Free DummyFileBuffer and set DummyFileBuffer to NULL.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 6ecab5ad077ea34467ff29ea1f5b77fa5c1e3447)

------------------------------------------------------------------------  r26856 | edk2buildsystem | 2018-04-13 21:54:55 -0700 (Fri, 13 Apr 2018) | 15 lines
  BaseTools: argument genfds-multi-thread create GenSec command issue
  Issue:
  genfds-multi-thread create makefile before section file generation,
  so it get alignment is zero from empty file. It is incorrect.
  solution:
  GenSec get section alignment from input file when the input alignment
  is zero.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 9a8d7aa7f796ce68ece2815d268889ac4e2ac318)

------------------------------------------------------------------------  r26857 | edk2buildsystem | 2018-04-13 21:55:06 -0700 (Fri, 13 Apr 2018) | 19 lines
  BaseTools: fix --genfds-multi-thread generate makefile issue
  1. when inf file is binary module, not generate makefile,
  so need generate ffs with previous method.
  2. generate Ui section maybe override and the string is not
  $(MODULE_NAME)
  like as:
  INF  RuleOverride = UI MdeModulePkg/Application/UiApp/UiApp.inf
  3. Trim generate incorrect Offset.raw when some vfr not generate .lst
  file in Debug directory, Trim get the VFR name with the .c files
  replacement.
  4. fix some depex file not generate issue
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a146c532c754106431b063fec9985a838afd82be)

------------------------------------------------------------------------  r26913 | edk2buildsystem | 2018-04-15 02:05:29 -0700 (Sun, 15 Apr 2018) | 11 lines
  BaseTools: Fix one or more multiply defined symbols found issue
  self.Guids update with package Guids will generate multiply defined
  GUID symbols in AutoGen file
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yunhua Feng <yunhuax.feng@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit e7df35b2bc53aecaca0792398f5d0ad163e50abb)

------------------------------------------------------------------------