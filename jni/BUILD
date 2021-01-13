load("@io_bazel_rules_scala//scala:scala.bzl", "scala_binary", "scala_library")

java_binary(
    name = "hello-from-jni-java",
    srcs = [
        "Hello.java",
        "Main.java",
    ],
    jvm_flags = ["-Djava.library.path=jni/cc"],
    main_class = "Main",
    runtime_deps = ["//jni/cc:hello-jni"],
)

scala_binary(
    name = "hello-from-jni-scala",
    srcs = [
        "HelloScala.scala",
        "MainScala.scala",
    ],
    jvm_flags = ["-Djava.library.path=jni/cc"],
    main_class = "MainScala",
    data = ["//jni/cc:hello-jni"],
)
