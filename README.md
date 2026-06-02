# rules_oci_dockerfile

Demonstrates using [rules_oci](https://github.com/bazel-contrib/rules_oci) with a Dockerfile to create a Dockerized F# app.

Build the image:

```bash
bazel run //:tarball
```

Run the image:

```bash
docker run --rm bazel/oci_dockerfile_demo:latest
```
