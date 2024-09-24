# @podium/typescript-config

Shared config for TypeScript, used in Podium projects to generate type definitions from JSDoc and test them.

## Install

```
npm install --save-dev typescript @podium/typescript-config
```

## Usage

Create two files in your root directory.

`tsconfig.json` (assuming source in `lib/`):

```json
{
    "extends": "@podium/typescript-config/module.json",
    "include": ["./lib/**/*.js"],
    "compilerOptions": {
        "outDir": "types"
    }
}
```

`tsconfig.test.json` (assuming tests in `tests/`):

```json
{
    "extends": "@podium/typescript-config/test.json",
    "include": ["./tests/**/*.js"]
}
```

You should have a similar setup in your `package.json`:

```json
{
    "scripts": {
        "types": "run-s types:module types:test",
        "types:module": "tsc",
        "types:test": "tsc --project tsconfig.test.json"
    },
    "dependencies": {
        "npm-run-all2": "6.2.3"
    }
}
```
