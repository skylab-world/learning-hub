# cmd/BUILD

load("@rules_go//go:def.bzl", "go_binary", "go_library", "go_test")

# Define the Go binary
go_binary(
    name = "learning-hub",
    embed = [":go_default_library"],
    importpath = "github.com/skylab-world/learning-hub/cmd",
    visibility = ["//visibility:public"],
)

# Optional: Define a Go library if you have reusable code in cmd/
go_library(
    name = "go_default_library",
    srcs = ["main.go"],
    importpath = "github.com/skylab-world/learning-hub/cmd",
    visibility = ["//visibility:private"],
)

go_test(
    name = "learning-hub_tests",
    size = "small",  # Options: small, medium, large, enormous
    timeout = "short",  # Options: short, moderate, long, eternal
    srcs = glob(["**/*_test.go"]),
    embed = [":go_default_library"],
    # Optionally, you can specify data, deps, etc. based on your tests' needs.
    importpath = "github.com/skylab-world/learning-hub/cmd",
)
