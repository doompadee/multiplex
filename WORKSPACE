workspace(name = "multiplex")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")


http_archive(
    name = "remote_java_tools_linux",
    sha256 = "196128eadc68a55fb42a1f990c84ee816f5b29320a72fe542fcfc4206ac3978a",
    urls = [
        "https://mirror.bazel.build/bazel_java_tools/releases/javac14/v1.0/java_tools_javac14_linux-v1.0.zip",
        "https://github.com/bazelbuild/java_tools/releases/download/javac14-v1.0/java_tools_javac14_linux-v1.0.zip",
    ],
)

http_archive(
    name = "openjdk14_linux_archive",
    build_file_content = """
java_runtime(name = 'runtime', srcs =  glob(['**']), visibility = ['//visibility:public'])
exports_files(["WORKSPACE"], visibility = ["//visibility:public"])
""",
    sha256 = "7f4310a98ea0e52bacbec389012d859dbb51e759fe35a2cfebb11300271872d2",
    strip_prefix = "zulu14.29.23-ca-jdk14.0.2-linux_x64",
    urls = ["https://cdn.azul.com/zulu/bin/zulu14.29.23-ca-jdk14.0.2-linux_x64.tar.gz"],
)
