# Bun app image

Create a Docker image for a Bun project.

## Getting started

To use this template, extend it in your project's Dofigen file:

```yml
extend:
  - https://raw.githubusercontent.com/lenra-io/dofigen-hub/main/js-ts/bun.image.yml
```

## Build arguments

They must be defined in the `globalArg` section of the Dofigen file.

- `BUN_VERSION`: the version of Bun to use (default is `latest`)
