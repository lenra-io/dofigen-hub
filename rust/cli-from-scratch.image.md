# cli-from-scratch image

This template is used to build a Rust project image from scratch using the muslrust image.
The muslrust image is a Docker image that contains the musl libc and the musl-gcc compiler.


## Getting started

To use this template, extend it in your project's Dofigen file, define the `APP_NAME` environment variable:

```yml
extend:
  - https://raw.githubusercontent.com/lenra-io/dofigen-hub/main/rust/cli-from-scratch.image.yml
globalArg:
  APP_NAME: myapp
```

## Build arguments

They must be defined in the `globalArg` section of the Dofigen file.

- `APP_NAME`: the name of the binary file that will be created
- `BUILD_ARGS`: additional arguments to pass to the `cargo build` command
