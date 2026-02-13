# Copyright 2024 The TCMalloc Authors
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     https://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# This library provides standard tcmalloc as a shared (loadable) library.
cc_binary(
    name = "tcmalloc",
    srcs = [
        "libc_override.h",
        "libc_override_gcc_and_weak.h",
        "libc_override_glibc.h",
        "sampler.h",
        "tcmalloc.cc",
        "tcmalloc.h",
    ],
    copts = TCMALLOC_DEFAULT_COPTS,
    visibility = ["//visibility:public"],
    deps = overlay_deps + tcmalloc_deps + [
        ":common",
    ],
    linkshared = True,
)
