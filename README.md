Minimal reproduction for https://github.com/biomejs/biome/issues/1360.

`npm run lint` correctly identifies linter issues in the `./formatter-ignored/` directory.

`npm run format` correctly identifies formatter issues in the `./lint-ignored/` directory.

`npm run ci` _should_ identify both of the above linter and formatter issues, but it only identifies the linter issues. The formatter appears not to run over `lint.ignore` directories when invoked via `biome ci`.
