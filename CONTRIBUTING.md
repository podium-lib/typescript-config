# Contributing

Thank you for showing an interest in contributing to Podium 🧡

You can find [the general contribution docs here](https://github.com/podium-lib/.github/blob/main/CONTRIBUTING.md).

This module is a [shared config for TypeScript](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html#tsconfig-bases). We accept changes that should apply to all repositories in the [podium-lib origanisation](https://github.com/podium-lib).

Exports from this module are handled via the `"files"` property. Configurations should be at the root level so user's `"extends"` field is `@podium/typescript-config/module.json` and so on.

A change in configuration is considered a `patch` in [semantic versioning](https://semver.org/). A new export would be a `minor`. Depending on a newer major version of TypeScript would be a `major`.
