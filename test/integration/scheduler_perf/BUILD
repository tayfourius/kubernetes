package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
    "go_test",
    "cgo_library",
)

go_library(
    name = "go_default_library",
    srcs = ["util.go"],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/apimachinery/registered:go_default_library",
        "//pkg/client/clientset_generated/internalclientset:go_default_library",
        "//pkg/client/clientset_generated/internalclientset/typed/core/internalversion:go_default_library",
        "//pkg/client/record:go_default_library",
        "//pkg/client/restclient:go_default_library",
        "//plugin/pkg/scheduler:go_default_library",
        "//plugin/pkg/scheduler/algorithmprovider:go_default_library",
        "//plugin/pkg/scheduler/factory:go_default_library",
        "//test/integration/framework:go_default_library",
        "//vendor:github.com/golang/glog",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "scheduler_bench_test.go",
        "scheduler_test.go",
    ],
    library = "go_default_library",
    tags = ["automanaged"],
    deps = [
        "//test/integration/framework:go_default_library",
        "//test/utils:go_default_library",
        "//vendor:github.com/golang/glog",
    ],
)
