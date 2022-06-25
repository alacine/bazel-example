load(
    "@bazel_tools//tools/jdk:default_java_toolchain.bzl",
    "BASE_JDK9_JVM_OPTS",
    "DEFAULT_JAVACOPTS",
    "DEFAULT_TOOLCHAIN_CONFIGURATION",
    "default_java_toolchain",
)

default_java_toolchain(
    name = "default_java_toolchain",
    configuration = DEFAULT_TOOLCHAIN_CONFIGURATION,  # One of predefined configurations
    # Other parameters are from java_toolchain rule:
    java_runtime = "@openjdk11_linux//:jdk",  # JDK to use for compilation and toolchain's tools execution
    #javacopts = DEFAULT_JAVACOPTS + ["--enable_preview"],  # Additional javac options
    #jvm_opts = BASE_JDK9_JVM_OPTS + ["--enable_preview"],  # Additional JDK options
    source_version = "11",
    target_version = "11",
    #visibility = ["//visibility:public"],
)

# 下面这几个版本的 openjdk 需要额外指定 jvm_opts，否则会有以下问题（没有研究具体是什么意思，这里先记录一下）
# java.lang.IllegalArgumentException: error: invalid source release: 18
default_java_toolchain(
    name = "java15_toolchain",
    configuration = DEFAULT_TOOLCHAIN_CONFIGURATION,  # One of predefined configurations
    # Other parameters are from java_toolchain rule:
    java_runtime = "@openjdk15_linux//:jdk",  # JDK to use for compilation and toolchain's tools execution
    javacopts = DEFAULT_JAVACOPTS,  # Additional javac options
    jvm_opts = BASE_JDK9_JVM_OPTS,  # Additional JDK options
    source_version = "15",
    target_version = "15",
    #visibility = ["//visibility:public"],
)

default_java_toolchain(
    name = "java17_toolchain",
    configuration = DEFAULT_TOOLCHAIN_CONFIGURATION,  # One of predefined configurations
    # Other parameters are from java_toolchain rule:
    java_runtime = "@openjdk17_linux//:jdk",  # JDK to use for compilation and toolchain's tools execution
    javacopts = DEFAULT_JAVACOPTS,  # Additional javac options
    jvm_opts = BASE_JDK9_JVM_OPTS,  # Additional JDK options
    source_version = "17",
    target_version = "17",
    #visibility = ["//visibility:public"],
)

default_java_toolchain(
    name = "java18_toolchain",
    configuration = DEFAULT_TOOLCHAIN_CONFIGURATION,  # One of predefined configurations
    # Other parameters are from java_toolchain rule:
    java_runtime = "@openjdk18_linux//:jdk",  # JDK to use for compilation and toolchain's tools execution
    javacopts = DEFAULT_JAVACOPTS,  # Additional javac options
    #jvm_opts = BASE_JDK9_JVM_OPTS,  # Additional JDK options
    source_version = "18",
    target_version = "18",
    #visibility = ["//visibility:public"],
)
