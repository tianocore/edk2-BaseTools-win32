Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2016, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 23152

This directory contains the Win32 binaries.

Build Date:       Tue, 08 Nov 2016 03:11:52 Pacific Standard Time
Last Changed Rev: 23152

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.3 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
  Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 23090
 *BootSectImage Version 1.0 Build Build 23152
  Ecc.exe Version 1.0 Build Build 22854
 *EfiLdrImage Version 1.0 Build Build 23152
 *EfiRom Version 0.1 Build 23152
 *GenBootSector Version 0.2 Build 23152
 *GenCrc32 Version 0.2 Build 23152
  GenDepex.exe Version 0.04 Build 23090
  GenFds.exe 1.0 Build 23090
 *GenFfs Version 0.1 Build 23152
 *GenFv Version 0.1 Build 23152
 *GenFw Version 0.2 Build 23152
 *GenPage Version 0.2 Build 23152
  GenPatchPcdTable.exe Version 0.10 Build 23095
 *GenSec Version 0.1 Build 23152
 *GenVtf Version 0.1 Build 23152
  ImportTool.bat Version 1.0
 *LzmaCompress Version 0.2 Build 23152
  LzmaF86Compress Version 0.2 Build 23152
  PatchPcdValue.exe Version 0.10 Build 23090
  Pkcs7Sign Version 0.9 Build 22854
  Rsa2048Sha256GenerateKeys Version 0.9 Build 22854
  Rsa2048Sha256Sign Version 0.9 Build 22854
 *Split Version 1.0 Build Build 23152
  TargetTool.exe Version 0.01 Build 23090
 *TianoCompress Version 0.1 Build 23152
  Trim.exe Version 0.10 Build 23090
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 22854
 *VfrCompile version  2.01 (UEFI 2.4) Build Build 23152
 *VolInfo Version 1.0 Build Build 23152
  build.exe Version 0.60 Build 23095

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  11/8/2016 3:11:54AM Engine version = 5700.7163
  11/8/2016 3:11:54AM AntiVirus DAT version = 8342.0
  11/8/2016 3:11:54AM Number of detection signatures in EXTRA.DAT = None
  11/8/2016 3:11:54AM Names of detection signatures in EXTRA.DAT = None
  11/8/2016 3:11:54AM Scan Started On-Demand Scan
  11/8/2016 3:12:04AM Scan Summary
  11/8/2016 3:12:04AM Processes scanned : 0
  11/8/2016 3:12:04AM Processes detected : 0
  11/8/2016 3:12:04AM Processes cleaned : 0
  11/8/2016 3:12:04AM Boot sectors scanned : 2
  11/8/2016 3:12:04AM Boot sectors detected: 0
  11/8/2016 3:12:04AM Boot sectors cleaned : 0
  11/8/2016 3:12:04AM Files scanned : 77
  11/8/2016 3:12:04AM Files with detections: 0
  11/8/2016 3:12:04AM File detections : 0
  11/8/2016 3:12:04AM Files cleaned : 0
  11/8/2016 3:12:04AM Files deleted : 0
  11/8/2016 3:12:04AM Files not scanned : 0
  11/8/2016 3:12:04AM Scan Summary (Registry Scanning)
  11/8/2016 3:12:04AM Keys scanned : 0
  11/8/2016 3:12:04AM Keys detected : 0
  11/8/2016 3:12:04AM Keys cleaned : 0
  11/8/2016 3:12:04AM Keys deleted : 0
  11/8/2016 3:12:04AM Run time : 0:00:11
  11/8/2016 3:12:04AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 23095:HEAD Source
------------------------------------------------------------------------  r23100 | edk2buildsystem | 2016-11-08 02:07:02 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/C/Common: Avoid possible NULL pointer dereference
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 2ff3293d7bdf32c5e7ab8728f2caa464e33eda0d)

------------------------------------------------------------------------  r23101 | edk2buildsystem | 2016-11-08 02:07:08 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/EfiRom: Avoid possible NULL pointer dereference
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 02875ba228545f506cb40cfc8a20a4e067fb2a9f)

------------------------------------------------------------------------  r23102 | edk2buildsystem | 2016-11-08 02:07:13 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenFfs: Avoid possible NULL pointer dereference
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 2cb874352423fcfd180199e6de8298567dff8e7f)

------------------------------------------------------------------------  r23103 | edk2buildsystem | 2016-11-08 02:07:17 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenFv: Avoid possible NULL pointer dereference
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 22247021349d8835026efe9511f25503e7dbb95c)

------------------------------------------------------------------------  r23104 | edk2buildsystem | 2016-11-08 02:07:23 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenFw: Avoid possible NULL pointer dereference
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 06b4573598f803d37b4b95c1c8c2ca69fc03ea3a)

------------------------------------------------------------------------  r23105 | edk2buildsystem | 2016-11-08 02:07:28 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenPage: Avoid possible NULL pointer dereference
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 18c2a7621d5e06fdaf38002d5cbcc064f576cf64)

------------------------------------------------------------------------  r23106 | edk2buildsystem | 2016-11-08 02:07:32 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenSec: Avoid possible NULL pointer dereference
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 248fce0329c1bfdfa9486e357e40a911361003bd)

------------------------------------------------------------------------  r23107 | edk2buildsystem | 2016-11-08 02:07:37 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenVtf: Avoid possible NULL pointer dereference
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 90114c101f2149ec02f7ba66af78addc2d72cb2e)

------------------------------------------------------------------------  r23108 | edk2buildsystem | 2016-11-08 02:07:42 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/TianoCompress: Avoid possible NULL pointer dereference
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d1f6eb27fe49345fa7fe13b01471c85f7feb0a65)

------------------------------------------------------------------------  r23109 | edk2buildsystem | 2016-11-08 02:07:47 -0800 (Tue, 08 Nov 2016) | 10 lines
  BaseTools/VfrCompile: Avoid possible NULL pointer dereference
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Dandan Bi <dandan.bi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9b78c54a09280ca852130b3ef76272a5d31d5035)

------------------------------------------------------------------------  r23110 | edk2buildsystem | 2016-11-08 02:07:52 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/VolInfo: Avoid possible NULL pointer dereference
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9dd00cb66e3e4a4be38068ef9700137ac6c0fb3f)

------------------------------------------------------------------------  r23111 | edk2buildsystem | 2016-11-08 02:07:57 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/TianoCompress: Initialize local variables before being used
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 10bcabc6be01aa72584610844d58c9e041952ca2)

------------------------------------------------------------------------  r23112 | edk2buildsystem | 2016-11-08 02:08:03 -0800 (Tue, 08 Nov 2016) | 10 lines
  BaseTools/VfrCompile: Initialize local variables before being used
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Dandan Bi <dandan.bi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 61eb9834a30299f506e61deef6337dc77c726517)

------------------------------------------------------------------------  r23113 | edk2buildsystem | 2016-11-08 02:08:08 -0800 (Tue, 08 Nov 2016) | 11 lines
  BaseTools/GenBootSector: Fix parameter format mismatch in printf functions
  The return value of GetLastError() API is 32-bit unsigned integer, change
  the relating format specification from '%x' to '%lx' to keep them matched.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f8708503cf354afcbb989583746f1e331014c059)

------------------------------------------------------------------------  r23114 | edk2buildsystem | 2016-11-08 02:08:13 -0800 (Tue, 08 Nov 2016) | 11 lines
  BaseTools/VolInfo: Fix parameter format mismatch in printf functions
  Format specification '%ls' for printf expects type 'wchar_t *', cast the
  type of the parameter to 'wchar_t *' to keep them matched.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit ed9ff2688a6329b0eed8bc14d287e7a644975a6c)

------------------------------------------------------------------------  r23115 | edk2buildsystem | 2016-11-08 02:08:18 -0800 (Tue, 08 Nov 2016) | 13 lines
  BaseTools/C/Common: Fix parameter format mismatch in scanf functions
  According to MSDN https://msdn.microsoft.com/en-us/library/6ttkkkhh.aspx
  Format specification '%x' for scanf expects type 'int *', modify the type
  of the relating variable to 'int' to keep them matched.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 851c97ce78393d5875eec984fbd870e8e85e5fd8)

------------------------------------------------------------------------  r23116 | edk2buildsystem | 2016-11-08 02:08:23 -0800 (Tue, 08 Nov 2016) | 14 lines
  BaseTools/GenFv: Fix parameter format mismatch in scanf functions
  According to MSDN https://msdn.microsoft.com/en-us/library/6ttkkkhh.aspx &
  https://msdn.microsoft.com/en-us/library/xdb9w69d.aspx
  Format specification '%llx' for scanf expects type 'long long *', modify
  the type of the relating variable to 'long long' to keep them matched.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 488ace56a6b135f79b56e3905d5c989638a0ec90)

------------------------------------------------------------------------  r23117 | edk2buildsystem | 2016-11-08 02:08:28 -0800 (Tue, 08 Nov 2016) | 13 lines
  BaseTools/GenFw: Fix parameter format mismatch in scanf functions
  According to MSDN https://msdn.microsoft.com/en-us/library/6ttkkkhh.aspx
  Format specification '%X' for scanf expects type 'int *', modify the type
  of the relating variable to 'int' to keep them matched.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit bd82cb4f21985b4d703091d750d5d7e5e9e04ea7)

------------------------------------------------------------------------  r23118 | edk2buildsystem | 2016-11-08 02:08:33 -0800 (Tue, 08 Nov 2016) | 13 lines
  BaseTools/GenVtf: Fix parameter format mismatch in scanf functions
  According to MSDN https://msdn.microsoft.com/en-us/library/6ttkkkhh.aspx
  Format specification '%x' for scanf expects type 'int *', modify the type
  of the relating variable to 'int' to keep them matched.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit f45b5a760530752bd6ea8125416cb6620a375468)

------------------------------------------------------------------------  r23119 | edk2buildsystem | 2016-11-08 02:08:37 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/C/Common: Add checks for array access
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b3520abde896e5e3f251054092f084580bfcdc37)

------------------------------------------------------------------------  r23120 | edk2buildsystem | 2016-11-08 02:08:42 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/TianoCompress: Add checks for array access
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5acc8d3cdd280f00ab316023e1f77dbce6025eb4)

------------------------------------------------------------------------  r23121 | edk2buildsystem | 2016-11-08 02:08:47 -0800 (Tue, 08 Nov 2016) | 10 lines
  BaseTools/VfrCompile: Add checks for array access
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Dandan Bi <dandan.bi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit bab5ad2fd14bf8d1e9e688327a11136c8bfb523e)

------------------------------------------------------------------------  r23122 | edk2buildsystem | 2016-11-08 02:08:52 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/EfiRom: Add checks for user/file inputs
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 47affb48e9baf3966842919acc0c419129c65392)

------------------------------------------------------------------------  r23123 | edk2buildsystem | 2016-11-08 02:08:58 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenFv: Add checks for user/file inputs
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 6f30cefd79864bfc983f47b740d90eebe93d10d9)

------------------------------------------------------------------------  r23124 | edk2buildsystem | 2016-11-08 02:09:03 -0800 (Tue, 08 Nov 2016) | 10 lines
  BaseTools/VfrCompile: Add checks for user/file inputs
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Dandan Bi <dandan.bi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit a6ac965bca117ef33b38a96c36643b36757b7698)

------------------------------------------------------------------------  r23125 | edk2buildsystem | 2016-11-08 02:09:10 -0800 (Tue, 08 Nov 2016) | 13 lines
  BaseTools/VfrCompile: Avoid freeing memory with mismatched functions
  Memory allocated by operator new[] should be freed using delete[] to avoid
  possible memory leak.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Dandan Bi <dandan.bi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit fd5425230ed22872126b52f22a7294e352ca3349)

------------------------------------------------------------------------  r23126 | edk2buildsystem | 2016-11-08 02:09:16 -0800 (Tue, 08 Nov 2016) | 16 lines
  BaseTools/VfrCompile: Add assignment operator definition for some classes
  For class that defines the copy constructor, it is better to add the
  assignment operator definition as well.
  This commit adds the definition for assignment operator for the classes
  with the copy constructor defined.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Dandan Bi <dandan.bi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 0d46defefa871d0b9583dfc4cb1985a5b0835ada)

------------------------------------------------------------------------  r23127 | edk2buildsystem | 2016-11-08 02:09:22 -0800 (Tue, 08 Nov 2016) | 19 lines
  BaseTools/VfrCompile: Avoid freeing freed memory in classes
  For classes that contain dynamically allocated data members, copy
  constructor and assignment operator should be implemented or both
  operations should be prohibited to avoid freeing freed memory caused by
  shallow copy.
  This commit declares both copy constructor and assignment operator as
  'private' for classes that contain dynamically allocated data members.
  This will prevent freeing already freed memory.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Dandan Bi <dandan.bi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 77dee0b1859dd0c7698b9f5a9510bee6d733c8c4)

------------------------------------------------------------------------  r23128 | edk2buildsystem | 2016-11-08 02:09:28 -0800 (Tue, 08 Nov 2016) | 10 lines
  BaseTools/VfrCompile: Remove unused local variables
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Dandan Bi <dandan.bi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5e85fb52d0838b15eb8787d08be27b4f9c3f964a)

------------------------------------------------------------------------  r23129 | edk2buildsystem | 2016-11-08 02:09:33 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/C/Common: Fix potential memory leak
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit aee346514d224a90622fe4cc553ba8ae79fe2828)

------------------------------------------------------------------------  r23130 | edk2buildsystem | 2016-11-08 02:09:39 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/EfiRom: Fix potential memory leak
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit fb4ea38c46cf28d46efe82a000af9c4421b6cb39)

------------------------------------------------------------------------  r23131 | edk2buildsystem | 2016-11-08 02:09:43 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenFv: Fix potential memory leak
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 6db97871107cba3d92ec2f3b7eb350f1fff47a11)

------------------------------------------------------------------------  r23132 | edk2buildsystem | 2016-11-08 02:09:47 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenPage: Fix potential memory leak
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 3f63e1755149286bef02b5d84841f7d9b1dffe95)

------------------------------------------------------------------------  r23133 | edk2buildsystem | 2016-11-08 02:09:53 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenSec: Fix potential memory leak
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 77e4cf5f11ed4543cbd91a9c45c7209e36bfd97a)

------------------------------------------------------------------------  r23134 | edk2buildsystem | 2016-11-08 02:09:58 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenVtf: Fix potential memory leak
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 399caf2d14b4e933fc1f0050f29d290359ba3614)

------------------------------------------------------------------------  r23135 | edk2buildsystem | 2016-11-08 02:10:03 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/Split: Fix potential memory and resource leak
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit b14f278de4c8a3a5b8aec99d70083b02d786d6c9)

------------------------------------------------------------------------  r23136 | edk2buildsystem | 2016-11-08 02:10:08 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/TianoCompress: Fix potential memory leak
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 076947cfceaa5c87f18306bd29b22caaa392d2f5)

------------------------------------------------------------------------  r23137 | edk2buildsystem | 2016-11-08 02:10:13 -0800 (Tue, 08 Nov 2016) | 10 lines
  BaseTools/VfrCompile: Fix potential memory leak
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Dandan Bi <dandan.bi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit bdf5f73120b6db1b598a6ac7f17a9d5f6cca7c35)

------------------------------------------------------------------------  r23138 | edk2buildsystem | 2016-11-08 02:10:18 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/VolInfo: Fix potential memory leak
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 85006654944a0f9e64974f23705beb7bc4906bcc)

------------------------------------------------------------------------  r23139 | edk2buildsystem | 2016-11-08 02:10:22 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/EfiRom: Fix file handles not being closed
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1e124de0188e6e3ed557500cc429cf7a756786d3)

------------------------------------------------------------------------  r23140 | edk2buildsystem | 2016-11-08 02:10:27 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenBootSector: Fix file handles not being closed
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 197b8f261b45c6900c2dc8e650e82e606184d50f)

------------------------------------------------------------------------  r23141 | edk2buildsystem | 2016-11-08 02:10:33 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenCrc32: Fix file handles not being closed
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 9639f7d3783f2e624d6e11be19c49461d62cb5b5)

------------------------------------------------------------------------  r23142 | edk2buildsystem | 2016-11-08 02:10:38 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenFv: Fix file handles not being closed
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 320ba37a567c91b716d7fd8c33e28681e00ee84e)

------------------------------------------------------------------------  r23143 | edk2buildsystem | 2016-11-08 02:10:43 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/GenVtf: Fix file handles not being closed
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 181c95593741b0d10e1cf52f21d2c86669900369)

------------------------------------------------------------------------  r23144 | edk2buildsystem | 2016-11-08 02:10:47 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/LzmaCompress: Fix file handles not being closed
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 1880d5e4d0b12695bec02e72e154a415e5085298)

------------------------------------------------------------------------  r23145 | edk2buildsystem | 2016-11-08 02:10:51 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/TianoCompress: Fix file handles not being closed
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 4d32be8888f4b7d8e337259fe1a5afd71b6b0046)

------------------------------------------------------------------------  r23146 | edk2buildsystem | 2016-11-08 02:10:56 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/VolInfo: Fix file handles not being closed
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 2a9afe80c3390d2f3540fbb461bb398e49159838)

------------------------------------------------------------------------  r23147 | edk2buildsystem | 2016-11-08 02:11:01 -0800 (Tue, 08 Nov 2016) | 14 lines
  BaseTools/GenVtf: Provide string width in '%s' specifier in format string
  String width is not specified for '%s' specifier in the format string for
  scanf functions.
  This commit now specifies the string length for '%s' in format strings
  according to the size of receiving buffers.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 5baa399e50854317c8788bc1cbae09c1af3b34c6)

------------------------------------------------------------------------  r23148 | edk2buildsystem | 2016-11-08 02:11:06 -0800 (Tue, 08 Nov 2016) | 14 lines
  BaseTools/VolInfo: Provide string width in '%s' specifier in format string
  String width is not specified for '%s' specifier in the format string for
  scanf functions.
  This commit now specifies the string length for '%s' in format strings
  according to the size of receiving buffers.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d6a1ce3b130800b84c1335a810798e6147eca431)

------------------------------------------------------------------------  r23149 | edk2buildsystem | 2016-11-08 02:11:11 -0800 (Tue, 08 Nov 2016) | 13 lines
  BaseTools/VfrCompile: Explicitly state format string for DebugMsg()
  For calls to API DebugMsg(), explicitly state format string as "%s" when
  the given variable list is a sting.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Dandan Bi <dandan.bi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 38eb573b0966af0879b85d5d83b430d95b31a884)

------------------------------------------------------------------------  r23150 | edk2buildsystem | 2016-11-08 02:11:17 -0800 (Tue, 08 Nov 2016) | 8 lines
  BaseTools/VolInfo: Add definitions for command format strings
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit aeadb1c453174d543ad95d2a601e229506b2679e)

------------------------------------------------------------------------  r23151 | edk2buildsystem | 2016-11-08 02:11:22 -0800 (Tue, 08 Nov 2016) | 17 lines
  BaseTools/VfrCompile/Pccts: Add virtual destructor for class DLGInputStream
  Class DLGInputStream defined in DLexerBase.h has a virtual method but no
  virtual destructor.
  This commit add an empty virtual destructor to avoid potential
  memory/resource leak when an object of a class derived from class
  DLGInputStream is deleted through a pointer to the DLGInputStream class.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Dandan Bi <dandan.bi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit d55638362727fd03d0ad97f9fe937984f9456e1b)

------------------------------------------------------------------------  r23152 | edk2buildsystem | 2016-11-08 02:11:27 -0800 (Tue, 08 Nov 2016) | 16 lines
  BaseTools/VfrCompile/Pccts: Make assignment operator not returning void
  The assignment operators for class ANTLRTokenPtr return void in current
  code.
  This commit makes them return the reference to the object just like
  primitive types do.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Eric Dong <eric.dong@intel.com>
  Cc: Dandan Bi <dandan.bi@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.0
  Signed-off-by: Hao Wu <hao.a.wu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit fef15ecd20dd8db5bf0c33b00908fc59491dba8a)

------------------------------------------------------------------------