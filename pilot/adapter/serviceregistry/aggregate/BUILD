load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["controller.go"],
    visibility = ["//visibility:public"],
    deps = [
        "//pilot/model:go_default_library",
        "//pilot/platform:go_default_library",
        "//pkg/log:go_default_library",

        # TODO(nmittler): Remove this
        "@com_github_golang_glog//:go_default_library",
        "@com_github_hashicorp_go_multierror//:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    size = "small",
    srcs = ["controller_test.go"],
    library = ":go_default_library",
    deps = [
        "//pilot/model:go_default_library",
        "//pilot/platform:go_default_library",
        "//pilot/test/mock:go_default_library",
    ],
)
