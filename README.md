# buck-ycm-example

Example showing how to connect Buck with the [YouCompleteMe](http://valloric.github.io/YouCompleteMe/) plugin for Vim.

This project depends on the Eigen [Buckaroo](https://buckaroo.pm) package to demonstrate code-completion for packages.

## Usage

```bash
buckaroo install
buck build //:app#compilation-database --out compile_commands.json
vim ./src/main.cpp
```

## How it Works

To generate the `compile_commands.json` file, use the `compilation-database` flavor:

```bash
buck build //:app#compilation-database --out compile_commands.json
```

The extra flag `--out compile_commands.json` will tell Buck to copy the database to `compile_commands.json`.

YouCompleteMe will discover this file automatically.

You should add it your `.gitignore` since it is a build artefact.
