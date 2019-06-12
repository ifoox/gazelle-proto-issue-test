workspace(name = "gazelle_proto_issue_test")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Go rules.
http_archive(
    name = "io_bazel_rules_go",
    sha256 = "86ae934bd4c43b99893fc64be9d9fc684b81461581df7ea8fc291c816f5ee8c5",
    urls = ["https://github.com/bazelbuild/rules_go/releases/download/0.18.3/rules_go-0.18.3.tar.gz"],
)
load("@io_bazel_rules_go//go:deps.bzl", "go_rules_dependencies", "go_register_toolchains")
go_rules_dependencies()
go_register_toolchains()
