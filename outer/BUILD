package(default_visibility = ["//visibility:public"])
load("@io_bazel_rules_go//proto:def.bzl", "go_proto_library")
load("@io_bazel_rules_go//go:def.bzl", "go_library")


proto_library(
    name = "outer_proto",
    srcs = ["outer.proto"],
    deps = [
        "//inner:inner_proto",
    ]
)

go_proto_library(
    name = "outer_go_proto",
    # Not sure if this is needed for repro.
    compilers = ["@io_bazel_rules_go//proto:go_grpc"],
    importpath = "github.com/ifoox/remote-apis/outer",
    proto = ":outer_proto",
    deps = [
        "//inner:go_default_library",
        ]
)
