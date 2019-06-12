package(default_visibility = ["//visibility:public"])
load("@io_bazel_rules_go//proto:def.bzl", "go_proto_library")
load("@io_bazel_rules_go//go:def.bzl", "go_library")


proto_library(
    name = "inner_proto",
    srcs = ["inner.proto"],
)

go_proto_library(
    name = "inner_go_proto",
    importpath = "github.com/ifoox/remote-apis/inner",
    proto = ":inner_proto",
)


go_library(
    name = "go_default_library",
    embed = [":inner_go_proto"],
    importpath = "github.com/ifoox/remote-apis/inner",
)
