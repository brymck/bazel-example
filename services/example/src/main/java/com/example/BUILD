load("@rules_java//java:defs.bzl", "java_library", "java_binary")

DEPS = [
    "//libs/greeter/src/main/java/io/brymck"
]

java_library(
    name = "lib",
    srcs = glob(["*.java"]),
    visibility = ["//src/test:__subpackages__"],
    deps = DEPS,
)

java_binary(
    name = "app",
    main_class = "com.example.ProjectRunner",
    runtime_deps = [":lib"],
)

# load("@io_bazel_rules_docker//java:image.bzl", "java_image")
# java_image(
    # name = "ProjectRunner",
    # srcs = ["src/main/java/com/example/ProjectRunner.java"],
    # layers = ["//libs/greeter"],
    # main_class = "com.example.ProjectRunner",
# )
