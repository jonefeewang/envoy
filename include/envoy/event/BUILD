licenses(["notice"])  # Apache 2

load(
    "//bazel:envoy_build_system.bzl",
    "envoy_cc_library",
    "envoy_package",
)

envoy_package()

envoy_cc_library(
    name = "deferred_deletable",
    hdrs = ["deferred_deletable.h"],
)

envoy_cc_library(
    name = "dispatcher_interface",
    hdrs = ["dispatcher.h"],
    deps = [
        ":deferred_deletable",
        ":file_event_interface",
        ":signal_interface",
        ":timer_interface",
        "//include/envoy/filesystem:filesystem_interface",
        "//include/envoy/network:connection_handler_interface",
        "//include/envoy/network:connection_interface",
        "//include/envoy/network:dns_interface",
        "//include/envoy/network:listen_socket_interface",
        "//include/envoy/network:listener_interface",
    ],
)

envoy_cc_library(
    name = "file_event_interface",
    hdrs = ["file_event.h"],
)

envoy_cc_library(
    name = "signal_interface",
    hdrs = ["signal.h"],
)

envoy_cc_library(
    name = "timer_interface",
    hdrs = ["timer.h"],
)
