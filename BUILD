load("@rules_java//java:defs.bzl", "java_library")
java_library(
    name = "greeter",
    srcs = ["src/main/java/com/example/Greeter.java"],
    visibility = ["//src/main/java/com/example/cmdline:__pkg__"],
)

load("@io_bazel_rules_docker//java:image.bzl", "java_image")
java_image(
    name = "ProjectRunner",
    srcs = ["src/main/java/com/example/ProjectRunner.java"],
    layers = [":greeter"],
    main_class = "com.example.ProjectRunner",
)
