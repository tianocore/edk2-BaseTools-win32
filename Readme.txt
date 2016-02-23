Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 20165, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 19914

This directory contains the Win32 binaries.

Build Date:       Tue, 23 Feb 2016 11:26:45 Pacific Standard Time
Last Changed Rev: 19875

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################

** ALL TOOLS WERE REBUILT **
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 19914
  BootSectImage Version 1.0 Build Build 19914
  Ecc.exe Version 1.0 Build Build 19914
  EfiLdrImage Version 1.0 Build Build 19914
  EfiRom Version 0.1 Build 19914
  GenBootSector Version 0.2 Build 19914
  GenCrc32 Version 0.2 Build 19914
  GenDepex.exe Version 0.04 Build 19914
  GenFds.exe 1.0 Build 19914
  GenFfs Version 0.1 Build 19914
  GenFv Version 0.1 Build 19914
  GenFw Version 0.2 Build 19914
  GenPage Version 0.2 Build 19914
  GenPatchPcdTable.exe Version 0.10 Build 19914
  GenSec Version 0.1 Build 19914
  GenVtf Version 0.1 Build 19914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 19914
  LzmaF86Compress Version 0.2 Build 19914
  PatchPcdValue.exe Version 0.10 Build 19914
  Rsa2048Sha256GenerateKeys Version 0.9 Build 19914
  Rsa2048Sha256Sign Version 0.9 Build 19914
  Split Version 1.0 Build Build 19914
  TargetTool.exe Version 0.01 Build 19914
  TianoCompress Version 0.1 Build 19914
  Trim.exe Version 0.10 Build 19914
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 19914
  VfrCompile version  2.01 (UEFI 2.4) Build Build 19914
  VolInfo Version 1.0 Build Build 19914
  build.exe Version 0.60 Build 19914

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  2/23/2016 11:26:46AM Engine version = 5700.7163
  2/23/2016 11:26:46AM AntiVirus DAT version = 8083.0
  2/23/2016 11:26:46AM Number of detection signatures in EXTRA.DAT = None
  2/23/2016 11:26:46AM Names of detection signatures in EXTRA.DAT = None
  2/23/2016 11:26:46AM Scan Started On-Demand Scan
  2/23/2016 11:26:53AM Scan Summary
  2/23/2016 11:26:53AM Processes scanned : 0
  2/23/2016 11:26:53AM Processes detected : 0
  2/23/2016 11:26:53AM Processes cleaned : 0
  2/23/2016 11:26:53AM Boot sectors scanned : 2
  2/23/2016 11:26:53AM Boot sectors detected: 0
  2/23/2016 11:26:53AM Boot sectors cleaned : 0
  2/23/2016 11:26:53AM Files scanned : 70
  2/23/2016 11:26:53AM Files with detections: 0
  2/23/2016 11:26:53AM File detections : 0
  2/23/2016 11:26:53AM Files cleaned : 0
  2/23/2016 11:26:53AM Files deleted : 0
  2/23/2016 11:26:53AM Files not scanned : 0
  2/23/2016 11:26:53AM Scan Summary (Registry Scanning)
  2/23/2016 11:26:53AM Keys scanned : 0
  2/23/2016 11:26:53AM Keys detected : 0
  2/23/2016 11:26:53AM Keys cleaned : 0
  2/23/2016 11:26:53AM Keys deleted : 0
  2/23/2016 11:26:53AM Run time : 0:00:07
  2/23/2016 11:26:53AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 19857:HEAD Source
------------------------------------------------------------------------  r19857 | jljusten | 2016-02-17 10:34:22 -0800 (Wed, 17 Feb 2016) | 13 lines
  BaseTools/GenFw: Correct datatypes in diagnostic messages and check for string termination
  This patch revises multiple diagnostic messages to use correct
  datatypes.  It also checks that a symbol name that is about to be used
  in a diagnostic message is terminated by a null character within the
  contents of the string table section so that the print routine does
  not read past the end of the string table section contents when
  reading the symbol name.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Michael LeMay <michael.lemay@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ea3e924a0c91e2dd7fbb5e2f79899367222f27eb)

------------------------------------------------------------------------  r19861 | edk2buildsystem | 2016-02-18 08:25:28 -0800 (Thu, 18 Feb 2016) | 9 lines
  BaseTools/GenFw: Fix a bug for GCC build
  current GCC build report error: 'for' loop initial declarations are only
  allowed in C99 or C11 mode, the patch fix this failure.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a754c70ceec880038f0e61e413398e96468b34f1)

------------------------------------------------------------------------  r19862 | edk2buildsystem | 2016-02-18 08:25:31 -0800 (Thu, 18 Feb 2016) | 10 lines
  BaseTools: report an error message when failed to start build command
  when build.py was failing to build packages but was not providing any
  error message except for “Failed to start command.” this patch provide
  the error message.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 790f60f22efb829903b6d308decaa4b1506ab928)

------------------------------------------------------------------------  r19863 | edk2buildsystem | 2016-02-18 08:25:35 -0800 (Thu, 18 Feb 2016) | 10 lines
  BaseTools/VolInfo: add some generic options
  The Help information provided by VolInfo does not follow the EDK II Tools
  Design doc, so this patch update the help text and add the generic
  options: -d, -v, -q, -s.
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 730ffca1943d8965f68faa55216ba5857635bcd2)

------------------------------------------------------------------------  r19864 | edk2buildsystem | 2016-02-18 08:25:42 -0800 (Thu, 18 Feb 2016) | 25 lines
  BaseTools: LzmaCompress: fix gcc-6 warning "misleading-indentation"
  The way the first use of the "_maxMode" variable is commented out (i.e.,
  together with the enclosing "if" statement) in GetOptimum() triggers the
  "misleading-indentation" warning that is new in gcc-6.0, for the block of
  code that originally depended on the "if" statement. Gcc believes
  (mistakenly) that the programmer believes (mistakenly) that the block
  depends on (repIndex == 0) higher up.
  Restore the if statement, with a controlling expression that comprises the
  constant 1 and "_maxMode" commented out.
  Cc: Jordan Justen <jordan.l.justen@intel.com>
  Cc: Cole Robinson <crobinso@redhat.com>
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Reported-by: Cole Robinson <crobinso@redhat.com>
  Suggested-by: Jordan Justen <jordan.l.justen@intel.com>
  Build-tested-by: Cole Robinson <crobinso@redhat.com>
  Ref: https://bugzilla.redhat.com/show_bug.cgi?id=1307439
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Jordan Justen <jordan.l.justen@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 6cc7ada465a7c5a6dab6e32abd5a4b6f1734c1d0)

------------------------------------------------------------------------  r19875 | edk2buildsystem | 2016-02-19 09:17:15 -0800 (Fri, 19 Feb 2016) | 9 lines
  BaseTools/Trim: Fix the bug for stripping when no line directive in file
  when no line directive in file, the tool still need to strip the typedef
  statement (eg: typedef struct, typedef union ..).
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 7cf1e91d611c5dbe8bdaefd5a48b61e63ea58263)

------------------------------------------------------------------------
"Rebuilding
