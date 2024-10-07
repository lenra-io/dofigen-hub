# muslrust builder

This template is used to build a Rust project using the muslrust image.
The muslrust image is a Docker image that contains the musl libc and the musl-gcc compiler.
This allows you to build a statically linked Rust binary that can be run on any Linux system without any dependencies.
It's a great way to build a Rust binary in a Docker container from `scratch`.

## Getting started

To use this template, extend it in your project's Dofigen file, define the `APP_NAME` argument and copy the resulting binary from the `/tmp` directory:

```yml
extend: https://raw.githubusercontent.com/lenra-io/dofigen-hub/main/rust/muslrust.builder.yml
builders:
  muslrust:
    arg:
      APP_NAME: myapp
copy:
  fromBuilder: muslrust
  paths: /tmp/myapp
  target: /bin/
```

## Build arguments

They must be defined in the `arg` field of the `muslrust` builder:

- `APP_NAME`: the name of the binary file that will be created
- `BUILD_ARGS` (optional): additional arguments to pass to the `cargo build` command
