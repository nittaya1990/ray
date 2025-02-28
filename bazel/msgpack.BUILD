# This library is for internal use, because the library assumes a
# different include prefix for itself than external libraries do.
cc_library(
    name = "_msgpack",
    hdrs = glob([
        "include/**/*.h",
        "include/**/*.hpp",
    ]),
    strip_include_prefix = "include",
)

cc_library(
    name = "msgpack",
    srcs = [
        "src/objectc.c",
        "src/unpack.c",
        "src/version.c",
        "src/vrefbuffer.c",
        "src/zone.c",
    ],
    hdrs = [
        "include/msgpack.h",
        "include/msgpack.hpp",
    ],
    includes = [
        "include/",
    ],
    strip_include_prefix = "include",
    copts = [
    ],
    deps = [
        ":_msgpack",
    ],
    visibility = ["//visibility:public"],
)
