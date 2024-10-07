# bun-binary builder

This template is used to load Node modules using Bun and then [build the Bun app as a binary executable](https://bun.sh/docs/bundler/executables).

## Getting started

To use this template, extend it in your project's Dofigen file, define the `APP_NAME` argument and copy the resulting binary from the `/tmp` directory:

```yml
extend:
  - https://raw.githubusercontent.com/lenra-io/dofigen-hub/main/js-ts/bun-install.builder.yml
builders:
  bun-binary:
    arg:
      MAIN_FILE: src/index.ts
      APP_NAME: myapp
copy:
  - fromBuilder: bun-binary
    paths: /tmp/myapp
    target: /bin/
```

## Build arguments

They must be defined in the `arg` field of the `bun-binary` builder:

- `APP_NAME`: the name of the binary file that will be created
- `MAIN_FILE`: the path of the Bun app main file
