# bun-binary image

Create a Docker image for a Bun project.

## Getting started

To use this template, extend it in your project's Dofigen file:

```yml
extend:
  - https://raw.githubusercontent.com/lenra-io/dofigen-hub/main/js-ts/bun-binary.image.yml
builders:
  bun-binary:
    arg:
      APP_NAME: myapp
      MAIN_FILE: src/index.ts
arg:
  APP_NAME: myapp
```

## Build arguments

Here are the Docker build arguments:

- `APP_NAME`: the name of the binary file that will be created. Must be defined in the `bun-binary` builder and in the runtime arguments.
- `MAIN_FILE`: the path of the Bun app main file. Must be defined in the `bun-binary` builder.
