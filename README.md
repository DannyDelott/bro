# bro
A package manager for JavaScript built on git submodules.

# Abstract

bro is a package manager for JavaScript that uses the same conventions as npm (ie: `package.json` and `node_modules/`) but is built on top of [git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

Optionally, you can self-host your project's dependencies by integrating with your favorite Git repository hosting service, like GitHub. 

Create new repos to backup all of your packages to your account. Update to the latest version by pulling from upstream.

# configuration

bro uses your existing `package.json` to store project information, scripts, and dependency configuration.

property name | description
---|---
[`name`](#name) | 

## `name`

# cli commands

command | description
---|---
[`bro init [-options]`](#bro-init--options) | Create and configure a new `package.json`
[`bro install [-options]`](#bro-install--options) | Install a package to your local `bro_modules/` directory
[`bro uninstall [-options]`](#bro-uninstall--options) | Uninstall a package from your local `bro_modules/` directory

## `bro init [-options]`

## `bro install [-options]`

## `bro uninstall [-options]`
