package(default_visibility = ["//semioticlabs:__subpackages__"])
load("@my_deps//:requirements.bzl", "requirement")

load(
  "@io_bazel_rules_python//python:python.bzl",
  "py_binary", "py_library", "py_test",
)

py_library(
    name = "test",
    srcs = glob(["*.py"]),
    imports = [],
    srcs_version = "PY3ONLY",
    deps=[
        requirement('requests_oauthlib')
    ]
)
