package(default_visibility = ["//visibility:public"])

load("/tools/rules/pex_rules", "pex_library", "pex_binary")

pex_library(
    name = "heron-explorer-lib",
    srcs = glob(["**/*.py"],),
    deps = [
        "//heron/common/src/python:tracker-access",
        "//heron/common/src/python:common",
        "//heron/statemgrs/src/python:zk-statemgr-py",
        "//heron/proto:proto-py",
    ],
    reqs = [
        "tornado==4.0.2",
        "tabulate==0.7.4",
    ],
)

pex_binary(
    name = "heron-explorer",
    srcs = ["main.py"],
    deps = [
        ":heron-explorer-lib",
    ],
)
