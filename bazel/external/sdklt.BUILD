#
# Copyright 2018-present Open Networking Foundation
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

licenses(["notice"])  # Apache v2

package(
    default_visibility = [ "//visibility:public" ],
)

cc_library(
    name = "error",
    hdrs = [
        "src/shr/include/shr/shr_error.h",
    ],
    srcs = [
        "src/shr/error/shr_error.c",
    ],
    strip_include_prefix = "src/shr/include",
)

# trick to export headers in a convenient way
cc_library(
    name = "bcm_headers",
    hdrs = glob(["bcm-bin/include/sdklt/**/*.h" ]),
    includes = ["bcm-bin/include/sdklt"],
)

cc_import(
  name = "bcm_sdklt",
  hdrs = [],  # see cc_library rule above
  static_library = "bcm-bin/lib/libsdklt.a",
)
