package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_test",
    "go_library",
)

go_test(
    name = "go_default_test",
    srcs = ["rpc_test.go"],
    embed = [":go_default_library"],
    rundir = ".",
    tags = ["automanaged"],
    deps = [
        "//app/interface/main/tag/conf:go_default_library",
        "//app/interface/main/tag/model:go_default_library",
        "//app/interface/main/tag/service:go_default_library",
        "//library/log:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "channel.go",
        "rpc.go",
        "rpc2.go",
    ],
    importpath = "go-common/app/interface/main/tag/rpc/server",
    tags = ["automanaged"],
    deps = [
        "//app/interface/main/tag/conf:go_default_library",
        "//app/interface/main/tag/model:go_default_library",
        "//app/interface/main/tag/service:go_default_library",
        "//library/ecode:go_default_library",
        "//library/log:go_default_library",
        "//library/net/rpc:go_default_library",
        "//library/net/rpc/context:go_default_library",
        "//library/xstr:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
