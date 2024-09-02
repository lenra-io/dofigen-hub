# muslrust Builder

This template is used to build a Rust project using the muslrust image.
The muslrust image is a Docker image that contains the musl libc and the musl-gcc compiler.
This allows you to build a statically linked Rust binary that can be run on any Linux system without any dependencies.
It's a great way to build a Rust binary in a Docker container from `scratch`.

## Getting started

To use this template, create a new file in your project's, extend it in your project Dofigen file, define the `APP_NAME` environment variable and copy the resulting binary from the `/tmp` directory:

```yml
extend:
  - https://raw.githubusercontent.com/lenra-io/dofigen-hub/main/rust/muslrust.builder.yml
builders:
  muslrust:
    env:
      APP_NAME: myapp
copy:
  - fromBuilder: muslrust
    paths: "/tmp/myapp"
    target: "/bin/"
entrypoint: myapp
```

## Environment variables

- `APP_NAME`: the name of the binary file that will be created
- `BUILD_ARGS`: additional arguments to pass to the `cargo build` command
- `CARGO_TARGET`: the target to build for (default: `x86_64-unknown-linux-musl`)