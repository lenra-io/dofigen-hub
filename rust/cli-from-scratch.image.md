# cli-from-scratch image

This template is used to build a Rust project image from scratch using the muslrust image.
The muslrust image is a Docker image that contains the musl libc and the musl-gcc compiler.


## Getting started

To use this template, extend it in your project's Dofigen file, define the `APP_NAME` environment variable:

```yml
extend: https://raw.githubusercontent.com/lenra-io/dofigen-hub/main/rust/cli-from-scratch.image.yml
builders:
  muslrust:
    arg:
      APP_NAME: myapp
arg:
  APP_NAME: myapp
```

## Build arguments

Here are the Docker build arguments:

- `APP_NAME`: the name of the binary file that will be created. Must be defined in the `muslrust` builder and in the runtime arguments.
- `BUILD_ARGS` (optional): additional arguments to pass to the `cargo build` command. Can be defined in the `muslrust` builder.

Unfortunately, global arguments are not supported yet.