load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")




# rules_pkg
http_archive(
  name = "rules_pkg",
  urls = [
    "https://mirror.bazel.build/github.com/bazelbuild/rules_pkg/releases/download/1.0.1/rules_pkg-1.0.1.tar.gz",
    "https://github.com/bazelbuild/rules_pkg/releases/download/1.0.1/rules_pkg-1.0.1.tar.gz",
  ],
  sha256 = "d20c951960ed77cb7b341c2a59488534e494d5ad1d30c4818c736d57772a9fef",
)

load("@rules_pkg//:deps.bzl", "rules_pkg_dependencies")

rules_pkg_dependencies()




# rules_oci
http_archive(
  name = "rules_oci",
  sha256 = "46ce9edcff4d3d7b3a550774b82396c0fa619cc9ce9da00c1b09a08b45ea5a14",
  strip_prefix = "rules_oci-1.8.0",
  url = "https://github.com/bazel-contrib/rules_oci/releases/download/v1.8.0/rules_oci-v1.8.0.tar.gz",
)

load("@rules_oci//oci:dependencies.bzl", "rules_oci_dependencies")

rules_oci_dependencies()

load("@rules_oci//oci:repositories.bzl", "LATEST_CRANE_VERSION", "oci_register_toolchains")

oci_register_toolchains(
  name = "oci",
  crane_version = LATEST_CRANE_VERSION,
)




# rules_dotnet
http_archive(
  name = "rules_dotnet",
  sha256 = "14735664c4f9dff606923862c196810ba2aa8a9deb17474d265fbdf09a94a9e2",
  strip_prefix = "rules_dotnet-22568f4906d0786f35b9cc6dc67516126f8f11db",
  url = "https://github.com/bazelbuild/rules_dotnet/archive/22568f4906d0786f35b9cc6dc67516126f8f11db.zip",
)

load(
  "@rules_dotnet//dotnet:repositories.bzl",
  "dotnet_register_toolchains",
  "rules_dotnet_dependencies",
)

rules_dotnet_dependencies()

load("@rules_dotnet//dotnet:paket.paket2bazel_dependencies.bzl", "paket2bazel_dependencies")

paket2bazel_dependencies()

dotnet_register_toolchains("dotnet", "6.0.200")

load("@rules_dotnet//dotnet:paket.rules_dotnet_nuget_packages.bzl", "rules_dotnet_nuget_packages")

rules_dotnet_nuget_packages()

# paket
load("//deps:paket.main.bzl", paket_main = "main")

paket_main()




# buildx
load("//:buildx.bzl", "fetch_buildx")

fetch_buildx()
