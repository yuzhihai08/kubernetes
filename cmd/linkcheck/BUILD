package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
)

go_binary(
    name = "linkcheck",
    library = ":go_default_library",
    tags = ["automanaged"],
)

go_library(
    name = "go_default_library",
    srcs = ["links.go"],
    tags = ["automanaged"],
    deps = [
        "//vendor:github.com/mvdan/xurls",
        "//vendor:github.com/spf13/pflag",
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
)
