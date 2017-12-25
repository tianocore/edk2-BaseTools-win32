Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2017, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 25982

This directory contains the Win32 binaries.

Build Date:       Sun, 24 Dec 2017 18:03:52 Pacific Standard Time
Last Changed Rev: 25982

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 25927
 *BootSectImage Version 1.0 Build Build 25982
 *Brotli Version 0.5.2 Build 25982
  Brotli Version 0.5.2 Build 25982
  Ecc.exe Version 1.0 Build Build 24602
 *EfiLdrImage Version 1.0 Build Build 25982
 *EfiRom Version 0.1 Build 25982
 *GenBootSector Version 0.2 Build 25982
 *GenCrc32 Version 0.2 Build 25982
  GenDepex.exe Version 0.04 Build 25927
  GenFds.exe 1.0 Build 25927
 *GenFfs Version 0.1 Build 25982
 *GenFv Version 0.1 Build 25982
 *GenFw Version 0.2 Build 25982
 *GenPage Version 0.2 Build 25982
  GenPatchPcdTable.exe Version 0.10 Build 25927
 *GenSec Version 0.1 Build 25982
 *GenVtf Version 0.1 Build 25982
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 25982
  LzmaF86Compress Version 0.2 Build 25982
  PatchPcdValue.exe Version 0.10 Build 25927
  Pkcs7Sign Version 0.9 Build 24507
  Rsa2048Sha256GenerateKeys Version 0.9 Build 24507
  Rsa2048Sha256Sign Version 0.9 Build 24507
 *Split Version 1.0 Build Build 25982
  TargetTool.exe Version 0.01 Build 25927
 *TianoCompress Version 0.1 Build 25982
  Trim.exe Version 0.10 Build 25927
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 25166
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 25982
 *VolInfo Version 1.0 Build Build 25982
  build.exe Version 0.60 Build 25927

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  12/24/2017 6:03:53PM Engine version = 5900.7806
  12/24/2017 6:03:53PM AntiVirus DAT version = 8755.0
  12/24/2017 6:03:53PM Number of detection signatures in EXTRA.DAT = None
  12/24/2017 6:03:53PM Names of detection signatures in EXTRA.DAT = None
  12/24/2017 6:03:53PM Scan Started On-Demand Scan
  12/24/2017 6:04:04PM Scan Summary
  12/24/2017 6:04:04PM Processes scanned : 0
  12/24/2017 6:04:04PM Processes detected : 0
  12/24/2017 6:04:04PM Processes cleaned : 0
  12/24/2017 6:04:04PM Boot sectors scanned : 2
  12/24/2017 6:04:04PM Boot sectors detected: 0
  12/24/2017 6:04:04PM Boot sectors cleaned : 0
  12/24/2017 6:04:04PM Files scanned : 80
  12/24/2017 6:04:04PM Files with detections: 0
  12/24/2017 6:04:04PM File detections : 0
  12/24/2017 6:04:04PM Files cleaned : 0
  12/24/2017 6:04:04PM Files deleted : 0
  12/24/2017 6:04:04PM Files not scanned : 0
  12/24/2017 6:04:04PM Scan Summary (Registry Scanning)
  12/24/2017 6:04:04PM Keys scanned : 0
  12/24/2017 6:04:04PM Keys detected : 0
  12/24/2017 6:04:04PM Keys cleaned : 0
  12/24/2017 6:04:04PM Keys deleted : 0
  12/24/2017 6:04:04PM Run time : 0:00:11
  12/24/2017 6:04:04PM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 25927:HEAD Source
------------------------------------------------------------------------  r25966 | edk2buildsystem | 2017-12-24 17:58:47 -0800 (Sun, 24 Dec 2017) | 7 lines
  BaseTools/C/Common: Add checks for array access
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 58356e9478d62811746db283bce3e751c6206006)

------------------------------------------------------------------------  r25967 | edk2buildsystem | 2017-12-24 17:58:54 -0800 (Sun, 24 Dec 2017) | 11 lines
  BaseTools/EfiRom: Refine the logic in main()
  This commit refines the logic for main(). It makes the logic more
  straightforward to prevent possible mis-reports by static code
  checkers.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 31c295e71aafed85c75a772dabf6e5e09d2f4a60)

------------------------------------------------------------------------  r25968 | edk2buildsystem | 2017-12-24 17:58:58 -0800 (Sun, 24 Dec 2017) | 7 lines
  BaseTools/LzmaCompress: Fix possible uninitialized variable
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9cdda7baa0819d544987d8fc909abdac549b27aa)

------------------------------------------------------------------------  r25969 | edk2buildsystem | 2017-12-24 17:59:02 -0800 (Sun, 24 Dec 2017) | 7 lines
  BaseTools/C/Common: Remove redundant type cast
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b567adb81e16e009ada73dfa2fbd5a0f9688d78f)

------------------------------------------------------------------------  r25970 | edk2buildsystem | 2017-12-24 17:59:07 -0800 (Sun, 24 Dec 2017) | 10 lines
  BaseTools/VfrCompile: Assign 'NULL' for closed file handle
  Assign 'NULL' value to the already-closed file handle to avoid closing
  the handle multiple times.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9edcd2788d7baa767b0761f0917c014612b6d72a)

------------------------------------------------------------------------  r25971 | edk2buildsystem | 2017-12-24 17:59:12 -0800 (Sun, 24 Dec 2017) | 10 lines
  BaseTools/GenFv: Add check to ensure the file handle status is correct
  Add an extra NULL check for the file handle to ensure that its status is
  correct.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f6401aedca2d576f4229c54c1356fea23387981f)

------------------------------------------------------------------------  r25972 | edk2buildsystem | 2017-12-24 17:59:17 -0800 (Sun, 24 Dec 2017) | 11 lines
  BaseTools/C/Common: Add/refine boundary checks for strcpy/strcat calls
  Add checks to ensure when the destination string buffer is of fixed
  size, the strcpy/strcat functions calls will not access beyond the
  boundary.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 938cf4b9bd91167e4de637de3c1e7fa449e9de94)

------------------------------------------------------------------------  r25973 | edk2buildsystem | 2017-12-24 17:59:22 -0800 (Sun, 24 Dec 2017) | 11 lines
  BaseTools/C/Common: Refine using sprintf() with '%s' in format string
  The commit removes the usages of sprintf() function calls with '%s' in
  the format string. And uses strncpy/strncat instead to ensure the
  destination string buffers will not be accessed beyond their boundary.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 3e1497334e45d09b8eccbc24ca571308e015e995)

------------------------------------------------------------------------  r25974 | edk2buildsystem | 2017-12-24 17:59:26 -0800 (Sun, 24 Dec 2017) | 11 lines
  BaseTools/EfiRom: Add/refine boundary checks for strcpy/strcat calls
  Add checks to ensure when the destination string buffer is of fixed
  size, the strcpy/strcat functions calls will not access beyond the
  boundary.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 52e8c5683843f3d5f9e979cbc0261d3951a7e0be)

------------------------------------------------------------------------  r25975 | edk2buildsystem | 2017-12-24 17:59:32 -0800 (Sun, 24 Dec 2017) | 11 lines
  BaseTools/GenBootSector: Add/refine boundary checks for strcpy/strcat
  Add checks to ensure when the destination string buffer is of fixed
  size, the strcpy/strcat functions calls will not access beyond the
  boundary.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1bdd9465c12e53246e88dc91cd22879ceb269f5c)

------------------------------------------------------------------------  r25976 | edk2buildsystem | 2017-12-24 17:59:37 -0800 (Sun, 24 Dec 2017) | 11 lines
  BaseTools/GenFv: Add/refine boundary checks for strcpy/strcat calls
  Add checks to ensure when the destination string buffer is of fixed
  size, the strcpy/strcat functions calls will not access beyond the
  boundary.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit fc42d0e89002af2d23f83edb5b64d9a56e825922)

------------------------------------------------------------------------  r25977 | edk2buildsystem | 2017-12-24 17:59:43 -0800 (Sun, 24 Dec 2017) | 11 lines
  BaseTools/GenVtf: Add/refine boundary checks for strcpy/strcat calls
  Add checks to ensure when the destination string buffer is of fixed
  size, the strcpy/strcat functions calls will not access beyond the
  boundary.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1c47ab04046d8a4123d4bcf8826f42aca2777292)

------------------------------------------------------------------------  r25978 | edk2buildsystem | 2017-12-24 17:59:48 -0800 (Sun, 24 Dec 2017) | 11 lines
  BaseTools/VfrCompile: Add/refine boundary checks for strcpy/strcat
  Add checks to ensure when the destination string buffer is of fixed
  size, the strcpy/strcat functions calls will not access beyond the
  boundary.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d837f33ab00ce9a0708382bfcf8f48f39d287644)

------------------------------------------------------------------------  r25979 | edk2buildsystem | 2017-12-24 17:59:54 -0800 (Sun, 24 Dec 2017) | 10 lines
  BaseTools/VfrCompile: Resolve uninit class variables in constructor
  The commit initializes those possibly uninitialized class variables in
  class constructors.
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b748e35c2bb0b6bcd1d89ef67e8f905b0a1c5c11)

------------------------------------------------------------------------  r25980 | edk2buildsystem | 2017-12-24 17:59:59 -0800 (Sun, 24 Dec 2017) | 11 lines
  BaseTools/GenFfs: Enlarge the size of 'AlignmentBuffer'
  As a workaround for the static code checkers, enlarge the size of the
  string buffer 'AlignmentBuffer' so that it can hold all the digits of an
  unsigned 32-bit integer plus the size unit character (e.g. 'M' & 'K').
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 33fc1fc46deb3b7779b92228b1c2d0aba2d16e44)

------------------------------------------------------------------------  r25981 | edk2buildsystem | 2017-12-24 18:00:04 -0800 (Sun, 24 Dec 2017) | 7 lines
  BaseTools/GenSec: Fix potential memory leak
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit ae0fbb7f5ad41866bca89320f501282e173b373d)

------------------------------------------------------------------------  r25982 | edk2buildsystem | 2017-12-24 18:00:08 -0800 (Sun, 24 Dec 2017) | 7 lines
  BaseTools/GenSec: Fix potential null pointer dereference
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit c40dbe5e7bf9f3f841d4f1c717c245e99854b786)

------------------------------------------------------------------------