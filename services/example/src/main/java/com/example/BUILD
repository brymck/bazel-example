load("@rules_java//java:defs.bzl", "java_library")
load("@io_bazel_rules_docker//java:image.bzl", "java_image")

DEPS = [
    "//libs/greeter/src/main/java/io/brymck"
]

java_library(
    name = "lib",
    srcs = glob(["*.java"]),
    visibility = ["//src/test:__subpackages__"],
    deps = DEPS,
)

java_image(
    name = "app",
    main_class = "com.example.ProjectRunner",
    runtime_deps = [":lib"],
)
