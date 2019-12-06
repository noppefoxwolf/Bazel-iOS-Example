load(
    "@build_bazel_rules_apple//apple:ios.bzl",
    "ios_application"
)

load(
    "@build_bazel_rules_swift//swift:swift.bzl",
    "swift_library",
)

swift_library(
    name = "Sources",
    srcs =[
        "src/AppDelegate.swift",
        "src/ViewController.swift",
    ],
    data = [
        "Resources/Main.storyboard",
    ],
)

ios_application(
    name = "App",
    bundle_id = "com.noppelabs.app",
    families = ["iphone"],
    infoplists = [":Info.plist"],
    visibility = ["//visibility:public"],
    deps = [":Sources"],
    minimum_os_version = "13.0",
)