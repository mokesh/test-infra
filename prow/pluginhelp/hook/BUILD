load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["hook.go"],
    importpath = "k8s.io/test-infra/prow/pluginhelp/hook",
    visibility = ["//visibility:public"],
    deps = [
        "//prow/github:go_default_library",
        "//prow/pluginhelp:go_default_library",
        "//prow/pluginhelp/externalplugins:go_default_library",
        "//prow/plugins:go_default_library",
        "//vendor/github.com/sirupsen/logrus:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/util/sets:go_default_library",
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

go_test(
    name = "go_default_test",
    srcs = ["hook_test.go"],
    embed = [":go_default_library"],
    importpath = "k8s.io/test-infra/prow/pluginhelp/hook",
    deps = [
        "//prow/github:go_default_library",
        "//prow/pluginhelp:go_default_library",
        "//prow/pluginhelp/externalplugins:go_default_library",
        "//prow/plugins:go_default_library",
        "//vendor/github.com/sirupsen/logrus:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/util/sets:go_default_library",
    ],
)
