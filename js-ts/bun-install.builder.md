# bun-install builder

This template is used to load Node modules using Bun.

## Getting started

To use this template, extend it in your project's Dofigen file and copy the resulting `node_modules` directory from the `/app` directory:

```yml
extend:
  - https://raw.githubusercontent.com/lenra-io/dofigen-hub/main/js-ts/bun-install.builder.yml
copy:
  - fromBuilder: bun-install
    paths: /app/node_modules
    target: /app/node_modules
```
