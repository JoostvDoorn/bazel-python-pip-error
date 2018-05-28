git_repository(
    name = "io_bazel_rules_python",
    remote = "https://github.com/bazelbuild/rules_python.git",
    commit = "8b5d0683a7d878b28fffe464779c8a53659fc645",
)

# Only needed for PIP support:
load("@io_bazel_rules_python//python:pip.bzl", "pip_repositories")

pip_repositories()

load("@io_bazel_rules_python//python:pip.bzl", "pip_import")
# This rule translates the specified requirements.txt into
# @semioticlabs//:requirements.bzl, which itself exposes a pip_install method.
pip_import(
   name = "my_deps",
   requirements = "//:requirements.txt",
)
load("@my_deps//:requirements.bzl", "pip_install")
pip_install()
