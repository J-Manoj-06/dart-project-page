---
title: dart pub remove
description: Use dart pub remove to remove a dependency.
---

_Remove_ is one of the commands of the [pub tool](/tools/pub/cmd).

```plaintext
$ dart pub remove <package> [options]
```

This command removes the specified package from the pubspec as a dependency.

For example, the following command is equivalent to
editing `pubspec.yaml` (removing `http` from `dependencies` or `dev_dependencies`)
and then calling `dart pub get`:

```console
$ dart pub remove http
```

## Options

For options that apply to all pub commands, see
[Global options](/tools/pub/cmd#global-options).

### `--[no-]offline`

{% render 'tools/pub-option-no-offline.md' %}

### `-n, --dry-run`

Reports which dependencies would change,
but doesn't change any.

### `--[no-]precompile`

By default, pub precompiles executables
in immediate dependencies (`--precompile`).
To prevent precompilation, use `--no-precompile`.

## In a workspace

In a [Pub workspace](/tools/pub/workspaces) `dart pub remove` removes
dependencies from the package in the current directory.

{% render 'pub-problems.md' %}
