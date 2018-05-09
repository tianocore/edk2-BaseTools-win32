Intel is a trademark or registered trademark of Intel Corporation or its
subsidiaries in the United States and other countries.
* Other names and brands may be claimed as the property of others.

Copyright (c) 2014 - 2018, Intel Corporation. All rights reserved.

EDK II packages can be checked out from the following SVN address:
https://svn.code.sf.net/p/edk2/code/trunk/edk2 Source HEAD Revision used for this build: 27082

This directory contains the Win32 binaries.

Build Date:       Wed, 09 May 2018 09:37:53 Pacific Daylight Time
Last Changed Rev: 27078

############### Build System Information ###############
  OS_Name       = Windows Server 2008 R2 Enterprise (X64)
  OS_Version    = 6.1.7601 Service Pack SP1 Build 7601
  Visual Studio = Microsoft Visual Studio 14.0
  Python        = 2.7.14 (32-bit)
  cxFreeze      = 4.2.3
  antlr3        = 3.0.1

##################### Tool Versions #####################
 *Intel(r) Binary Product Data Generation Tool (Intel(r) BPDG) - Version 1.0 Build Build 27082
  BootSectImage Version 1.0 Build Build 26482
  Brotli Version 0.5.2 Build 26482
  Brotli Version 0.5.2 Build 26482
  DevicePath Version 0.1 Build 26482
 *Ecc.exe Version 1.0 Build Build 27082
  EfiLdrImage Version 1.0 Build Build 26482
  EfiRom Version 0.1 Build 26482
  GenBootSector Version 0.2 Build 26482
  GenCrc32 Version 0.2 Build 26482
 *GenDepex.exe Version 0.04 Build 27082
 *GenFds.exe 1.0 Build 27082
  GenFfs Version 0.1 Build 26482
  GenFv Version 0.1 Build 26482
  GenFw Version 0.2 Build 26482
  GenPage Version 0.2 Build 26482
 *GenPatchPcdTable.exe Version 0.10 Build 27082
  GenSec Version 0.1 Build 26914
  GenVtf Version 0.1 Build 26914
  ImportTool.bat Version 1.0
  LzmaCompress Version 0.2 Build 26482
  LzmaF86Compress Version 0.2 Build 26482
 *PatchPcdValue.exe Version 0.10 Build 27082
  Pkcs7Sign Version 0.9 Build 26163
  Rsa2048Sha256GenerateKeys Version 0.9 Build 26163
  Rsa2048Sha256Sign Version 0.9 Build 26914
  Split Version 1.0 Build Build 26482
 *TargetTool.exe Version 0.01 Build 27082
  TianoCompress Version 0.1 Build 26482
 *Trim.exe Version 0.10 Build 27082
  UEFI Packaging Tool (UEFIPT) - Revision 1.1 Build Build 26914
  VfrCompile version  2.01 (UEFI 2.4) Build Build 27029
  VolInfo Version 1.0 Build Build 26482
 *build.exe Version 0.60 Build 27082

* This tool was updated

##################### Anti-Virus Scan #####################
McAfee VirusScan Enterprise Version 8.8.0.1385
  5/9/2018 9:37:55AM Engine version = 5900.7806
  5/9/2018 9:37:55AM AntiVirus DAT version = 8887.0
  5/9/2018 9:37:55AM Number of detection signatures in EXTRA.DAT = None
  5/9/2018 9:37:55AM Names of detection signatures in EXTRA.DAT = None
  5/9/2018 9:37:55AM Scan Started On-Demand Scan
  5/9/2018 9:38:07AM Scan Summary
  5/9/2018 9:38:07AM Processes scanned : 0
  5/9/2018 9:38:07AM Processes detected : 0
  5/9/2018 9:38:07AM Processes cleaned : 0
  5/9/2018 9:38:07AM Boot sectors scanned : 2
  5/9/2018 9:38:07AM Boot sectors detected: 0
  5/9/2018 9:38:07AM Boot sectors cleaned : 0
  5/9/2018 9:38:07AM Files scanned : 66
  5/9/2018 9:38:07AM Files with detections: 0
  5/9/2018 9:38:07AM File detections : 0
  5/9/2018 9:38:07AM Files cleaned : 0
  5/9/2018 9:38:07AM Files deleted : 0
  5/9/2018 9:38:07AM Files not scanned : 0
  5/9/2018 9:38:07AM Scan Summary (Registry Scanning)
  5/9/2018 9:38:07AM Keys scanned : 0
  5/9/2018 9:38:07AM Keys detected : 0
  5/9/2018 9:38:07AM Keys cleaned : 0
  5/9/2018 9:38:07AM Keys deleted : 0
  5/9/2018 9:38:07AM Run time : 0:00:12
  5/9/2018 9:38:07AM Scan Complete On-Demand Scan

############### SVN Log Since Last Build ################
svn log -r 27029:HEAD Source
------------------------------------------------------------------------  r27030 | edk2buildsystem | 2018-05-04 02:06:18 -0700 (Fri, 04 May 2018) | 11 lines
  BaseTools: FdfParser - update to remove duplicate constant value
  PCD size by type is shared so this change both removes duplication
  and makes the function work for all numeric PCD types.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit bff747501b98d2685782dc742db5f32d8490c99e)

------------------------------------------------------------------------  r27031 | edk2buildsystem | 2018-05-04 02:06:43 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: AutoGen - update to remove duplicate constant value
  PCD size by type is shared.  just use it.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a7360838d7cc0b645b41d8b1713832ef4fbfdd64)

------------------------------------------------------------------------  r27032 | edk2buildsystem | 2018-05-04 02:07:30 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: check before accessing members in __eq__
  minimize risk for exceptions.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b7b51025b94f77130f355a2c7b00a0fbcf533b2d)

------------------------------------------------------------------------  r27033 | edk2buildsystem | 2018-05-04 02:08:00 -0700 (Fri, 04 May 2018) | 11 lines
  BaseTools: this function has no purpose.
  it looks like a old POC of the concepts then used to make the classes
  in the file.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 18011927b1b9083df1dae4a271cb2492c4438ab8)

------------------------------------------------------------------------  r27034 | edk2buildsystem | 2018-05-04 02:08:29 -0700 (Fri, 04 May 2018) | 11 lines
  BaseTools: AutoGen - refactor assemble_variable
  make this function @staticmethod since self parameter is not used.
  change valuelist to valuedict since it is a dictionary.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit dea5ef9dc41c5d7a1a6b20a9457433faf92cc623)

------------------------------------------------------------------------  r27035 | edk2buildsystem | 2018-05-04 02:09:05 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: AutoGen - refactor dictionary access
  dont use dict.get() inside loops of dictionary contents. its not needed.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit bffcfca88f398ea42a6275f87561ed57db3c7619)

------------------------------------------------------------------------  r27036 | edk2buildsystem | 2018-05-04 02:09:44 -0700 (Fri, 04 May 2018) | 11 lines
  BaseTools: AutoGen - GenVar refactor static methods
  change methods which do not use self to @staticmethod
  change their calls to use class name instead of instance
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit c5419897415ad31fc83efa94b370a38f8a097aa5)

------------------------------------------------------------------------  r27037 | edk2buildsystem | 2018-05-04 02:10:30 -0700 (Fri, 04 May 2018) | 12 lines
  BaseTools: AutoGen - share StripComments API
  add the API root in one class file.
  delete the static API out of both classes.
  share it in the single location.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit c23ef28c205875f59f785e0028086e98ec58030c)

------------------------------------------------------------------------  r27038 | edk2buildsystem | 2018-05-04 02:11:04 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: AutoGen - refactor class factory
  since instances are not added to cache, the factory does nothing.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit aaa5a23c95a1ebc5625c88d436ceefcbeb38330f)

------------------------------------------------------------------------  r27039 | edk2buildsystem | 2018-05-04 02:11:42 -0700 (Fri, 04 May 2018) | 8 lines
  BaseTools: Eot - remove unused lists
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 5373d8a0f9f50d42d812d27384d9487022a70199)

------------------------------------------------------------------------  r27040 | edk2buildsystem | 2018-05-04 02:12:16 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: Eot - refactor global data
  remove unused lists, dicts, and duplicate variables
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit cdd04623d73924103c22bdaf28e33f3bf5296b58)

------------------------------------------------------------------------  r27041 | edk2buildsystem | 2018-05-04 02:13:01 -0700 (Fri, 04 May 2018) | 8 lines
  BaseTools: AutoGen - remove global line
  this serves no purpose since we dont change the global or assign to it.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 124d672ee6356f6cf6cc0188f5747e4a2a49d0db)

------------------------------------------------------------------------  r27042 | edk2buildsystem | 2018-05-04 02:13:41 -0700 (Fri, 04 May 2018) | 11 lines
  BaseTools: AutoGen - UniClassObject refactor static methods
  change methods which do not use self to @staticmethod
  change their calls to use class name instead of instance
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 3b743b3b158bfaed6bd539086861c1307678163a)

------------------------------------------------------------------------  r27043 | edk2buildsystem | 2018-05-04 02:13:57 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: refactor to use list not dict
  since we never access the values in the copied dict, just use a list instead.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 13d9e0511e1c247b324c2ec6d3b4806c8a4daaa2)

------------------------------------------------------------------------  r27044 | edk2buildsystem | 2018-05-04 02:14:15 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: eliminate {} from dictionary contructor call
  no need to construct 2 dictionaries.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 817e36690ad3156b9413d48e3ff5c3509d34c03f)

------------------------------------------------------------------------  r27045 | edk2buildsystem | 2018-05-04 02:14:30 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: remove Compound statements
  split them into 2 seperate lines.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 8ac64c5b1271e260b6ae11d6bd98099f60cb0112)

------------------------------------------------------------------------  r27046 | edk2buildsystem | 2018-05-04 02:15:31 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: Workspace - refactor a dict
  change a dict to a set since we never examine the contents, just the keys.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 88252a90d1ca7846731cd2e4e8e860454f7d97a3)

------------------------------------------------------------------------  r27047 | edk2buildsystem | 2018-05-04 02:16:25 -0700 (Fri, 04 May 2018) | 11 lines
  BaseTools: move PCD size calculation functions to PcdClassObject
  move both GetPcdMaxSize and GetPcdSize to the PcdClassObject.
  fix MAX_SIZE_TYPE to have int values
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 5565a8c4d2196b5e55e702169feefeeb07a330d9)

------------------------------------------------------------------------  r27048 | edk2buildsystem | 2018-05-04 02:17:08 -0700 (Fri, 04 May 2018) | 8 lines
  BaseTools: AutoGen - refactor out functions only called in __init__
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit def89ed0256fd903dbd1c54aa756fcb1fb5842df)

------------------------------------------------------------------------  r27049 | edk2buildsystem | 2018-05-04 02:17:32 -0700 (Fri, 04 May 2018) | 11 lines
  BaseTools: AutoGen - refactor out a list
  the lists were used in __init__ then converted to sets
  instead just use the sets from the begining
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0caa769dbb87133c43774b1bb8821b34fa51753f)

------------------------------------------------------------------------  r27050 | edk2buildsystem | 2018-05-04 02:17:55 -0700 (Fri, 04 May 2018) | 11 lines
  BaseTools: AutoGen - refactor out a useless class
  this class was never instantiated.  the static function was called.
  save the function, remove the rest.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 92a4eebb3719ef38139d99ddfe4fa302560f79dd)

------------------------------------------------------------------------  r27051 | edk2buildsystem | 2018-05-04 02:18:17 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: AutoGen - no need to recompute
  looping over a list and recomputing the same value has no impact on final value
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 61f5b77dd5eefe5e92ba89281e95037c8d457a72)

------------------------------------------------------------------------  r27052 | edk2buildsystem | 2018-05-04 02:19:10 -0700 (Fri, 04 May 2018) | 11 lines
  BaseTools: refactor __init__ functions to not compute temporary variable
  just assign correct value to member variable in __init__ or call
  parent __init__
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 64bb8d4d51ec72051fffa96ddc91178fb6b33288)

------------------------------------------------------------------------  r27053 | edk2buildsystem | 2018-05-04 02:20:49 -0700 (Fri, 04 May 2018) | 8 lines
  BaseTools: AutoGen - remove function no one calls
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 032a7c9fe26dfbab91ec83baa46d4a6b96878e88)

------------------------------------------------------------------------  r27054 | edk2buildsystem | 2018-05-04 02:21:12 -0700 (Fri, 04 May 2018) | 9 lines
  BaseTools: AutoGen - move function to clean file namespace
  the function is only used in one other function.
  just move it there.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 8b88b1634fa91fc8c3faedae8fec85c52d5a9260)

------------------------------------------------------------------------  r27055 | edk2buildsystem | 2018-05-04 02:21:32 -0700 (Fri, 04 May 2018) | 8 lines
  BaseTools: AutoGen - remove another function no one calls
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a2e721704bb5ee1ffd293711a02ac0c650d7cdd5)

------------------------------------------------------------------------  r27056 | edk2buildsystem | 2018-05-04 02:22:17 -0700 (Fri, 04 May 2018) | 8 lines
  BaseTools: Refactor to share GUID packing function
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit d3054be59ef0a4b007064c9d7844c1fbeed4443f)

------------------------------------------------------------------------  r27057 | edk2buildsystem | 2018-05-04 02:22:32 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: AutoGen - refactor function to remove extra variables
  we dont need to keep data we already have in different formats...
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1549328f5f48c657137c3ead96f2ad3586713a33)

------------------------------------------------------------------------  r27058 | edk2buildsystem | 2018-05-04 02:22:50 -0700 (Fri, 04 May 2018) | 8 lines
  BaseTools: AutoGen - refactor more functions only called in __init__
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit cb7e6aa77a937f2c28dc57bcffccde69c4080ffb)

------------------------------------------------------------------------  r27059 | edk2buildsystem | 2018-05-04 02:23:08 -0700 (Fri, 04 May 2018) | 8 lines
  BaseTools: remove unused member variable
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 1360bcb84e3aeef869f7dfe8124da10534b57929)

------------------------------------------------------------------------  r27060 | edk2buildsystem | 2018-05-04 02:23:23 -0700 (Fri, 04 May 2018) | 8 lines
  BaseTools: remove redundant content in InfSectionParser
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 6c2d8cb238c8d076fd177a30b5e1e3c5e0912145)

------------------------------------------------------------------------  r27061 | edk2buildsystem | 2018-05-04 02:23:41 -0700 (Fri, 04 May 2018) | 11 lines
  BaseTools: AutoGen - add Opcode constants
  add constants for dependency expression opcode strings
  use these new opcode string constants
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 31ff1c443e25d6bff758bdcd9a248a907cff651b)

------------------------------------------------------------------------  r27062 | edk2buildsystem | 2018-05-04 02:24:02 -0700 (Fri, 04 May 2018) | 12 lines
  BaseTools: standardize GUID and pack size
  currently GUID packing and pack size determination is spread
  throughout the code. This introduces a shared function and dict and
  routes all code paths through them.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit d0a0c52c221e5dcf82f24d4346c1cf52109d6dfb)

------------------------------------------------------------------------  r27063 | edk2buildsystem | 2018-05-04 02:24:17 -0700 (Fri, 04 May 2018) | 8 lines
  BaseTools: remove unused variable
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit d5d2b6bd244be4b6fa495c10c19908ac1076aea5)

------------------------------------------------------------------------  r27064 | edk2buildsystem | 2018-05-04 02:24:27 -0700 (Fri, 04 May 2018) | 8 lines
  BaseTools: GenFds - use existing shared string
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit ef4f218b3d019b111bde5b95dbcece896b48c632)

------------------------------------------------------------------------  r27065 | edk2buildsystem | 2018-05-04 02:24:36 -0700 (Fri, 04 May 2018) | 8 lines
  BaseTools: missed a copyright update
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 0ed0372a6b536a27a72365311897f3a273258b59)

------------------------------------------------------------------------  r27066 | edk2buildsystem | 2018-05-04 02:24:48 -0700 (Fri, 04 May 2018) | 11 lines
  BaseTools: Remove lists form set construction
  There is no need to make a list to make a set.  remove lists
  that are only used in constructing sets.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit c5c7e68a915954d8fd15f6c8f3523c65ee06f489)

------------------------------------------------------------------------  r27067 | edk2buildsystem | 2018-05-04 02:25:01 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: refactor Depex optomization
  No need to make a list from the set.  just pop the item off.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit cf3062901d6e8574c6322bb6236d8b004694b8f1)

------------------------------------------------------------------------  r27068 | edk2buildsystem | 2018-05-04 02:25:21 -0700 (Fri, 04 May 2018) | 11 lines
  BaseTools: create base expression class
  this class has a fucntion to share between Exception and RangeExpression
  change both classes to call this function init in their init
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit b2aeaf573ee5454c4dc3227da696286cdba35ac1)

------------------------------------------------------------------------  r27069 | edk2buildsystem | 2018-05-04 02:25:37 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: use set instead of list
  as we only do membership (in) testing for this, set is better
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 4d601fc6b17d69cf20c23cfbaf063bb337b4876d)

------------------------------------------------------------------------  r27070 | edk2buildsystem | 2018-05-04 02:26:04 -0700 (Fri, 04 May 2018) | 10 lines
  BaseTools: dont make iterator into list if not needed
  functions (like join) can use the iterator just as easily.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 8252e6bf2ddfa210992c3590008029933592ad16)

------------------------------------------------------------------------  r27071 | edk2buildsystem | 2018-05-06 14:05:28 -0700 (Sun, 06 May 2018) | 18 lines
  BaseTools: Ecc - add dict for config file to internal translation
  Commit eece4292acc80 changed a variable name, which was tied directly to
  a config file entry. This seperates the internal variable names from
  the config file entries by having the internal dict accessed through a
  translation of key words.
  added a test when this is run straight from command line.
  Cc: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Cc: Laszlo Ersek <lersek@redhat.com>
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Jaben Carsey <jaben.carsey@intel.com>
  Tested-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Laszlo Ersek <lersek@redhat.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit a4c35dedd92f2b9b7c68e9bd0490bc14b96457ef)

------------------------------------------------------------------------  r27077 | edk2buildsystem | 2018-05-07 02:15:13 -0700 (Mon, 07 May 2018) | 9 lines
  BaseTools: Retrieve /U and -U CC flags to structure PcdValueInit Makefile
  /D and -D flags have been added. So, /U and -U flags should be added.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Liming Gao <liming.gao@intel.com>
  Cc: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Yonghong Zhu <yonghong.zhu@intel.com>
  (cherry picked from commit 5d9af6a55ae1fcd1bbd19b5c55f039e9556d5cec)

------------------------------------------------------------------------  r27078 | edk2buildsystem | 2018-05-07 02:16:51 -0700 (Mon, 07 May 2018) | 9 lines
  BaseTools: Correct the variable name
  the commit bff74750 introduce a undefined variable name 'scope' cause build
  failure, it should use 'Scope'.
  Contributed-under: TianoCore Contribution Agreement 1.1
  Signed-off-by: Yonghong Zhu <yonghong.zhu@intel.com>
  Reviewed-by: Liming Gao <liming.gao@intel.com>
  (cherry picked from commit 053cd183c9f25929f056239a173e0106b2322d17)

------------------------------------------------------------------------