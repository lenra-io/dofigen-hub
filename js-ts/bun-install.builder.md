# bun-install builder

This template is used to load Node modules using Bun.

## Getting started

To use this template, extend it in your project's Dofigen file and copy the resulting `node_modules` directory from the `/tmp` directory:

```yml
extend:
  - https://raw.githubusercontent.com/lenra-io/dofigen-hub/main/js-ts/bun-install.builder.yml
copy:
  - fromBuilder: bun-install
    paths: /tmp/node_modules
    target: /app/node_modules
```

## Build arguments

They must be defined in the `globalArg` section of the Dofigen file.

- `BUN_VERSION`: the version of Bun to use (default is `latest`)
