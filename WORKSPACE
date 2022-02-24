workspace(
    name = "example",
    managed_directories = {"@npm": ["node_modules"]},
)

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
http_archive(
    name = "build_bazel_rules_nodejs",
    sha256 = "2644a66772938db8d8c760334a252f1687455daa7e188073f2d46283f2f6fbb7",
    urls = ["https://github.com/bazelbuild/rules_nodejs/releases/download/4.6.2/rules_nodejs-4.6.2.tar.gz"],
)

# http_archive(
#     name = "build_bazel_rules_nodejs",
#     sha256 = "121f17d8b421ce72f3376431c3461cd66bfe14de49059edc7bb008d5aebd16be",
#     urls = ["https://github.com/bazelbuild/rules_nodejs/releases/download/2.3.1/rules_nodejs-2.3.1.tar.gz"],
# )

load("@build_bazel_rules_nodejs//:index.bzl", "node_repositories")
node_repositories(
    node_version = "16.14.0",
    yarn_version = "1.22.4",
    node_urls = [
        "https://nodejs.org/dist/v{version}/{filename}",
    ],
    yarn_urls = [
        "https://github.com/yarnpkg/yarn/releases/download/v{version}/{filename}",
    ],
)

load("@build_bazel_rules_nodejs//:index.bzl", "yarn_install")
yarn_install(
    name = "npm",
    package_json = "//:package.json",
    yarn_lock = "//:yarn.lock",
)
