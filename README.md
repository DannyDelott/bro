# bro
A package manager for JavaScript built on git submodules.

# Abstract

bro is a package manager for JavaScript that uses the same conventions as npm (ie: `package.json` and `node_modules/`) but is built on top of [git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

Optionally, you can self-host your project's dependencies by integrating with your favorite Git repository hosting service, like GitHub, GitLab, and BitBucket. Create new repos to backup all of your packages to your account. Update to the latest version by pulling from upstream. (There's a command for that.)

# configuration

bro uses your existing `package.json` to store project information, scripts/hooks, and dependency configuration.

property name | description
---|---
[`name`](#name) | 

## `name`

# cli commands

command | description
---|---
[`bro init`](#bro-init) | Create and configure a new `package.json`
[`bro install`](#bro-install) | Clone a package to your local `node_modules/` directory
[`bro uninstall`](#bro-uninstall) | Delete a package from your local `node_modules/` directory

## `bro init`

## `bro install`

**Synopsis:**

`bro install [-options] [--] <[package-name][clone-url]> [source...]`

**Description:**

Install a package to your local `node_modules/` directory. This will install all of its dependencies as well.

Packages names are derived by a scope, usually the author's username, and the repo name.

**Options:**

* `--save`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;TODO
<br /><br />

* `--save-dev`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;TODO
<br /><br />

* `--host`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Begin hosting the package on your own Git repository hosting service
<br /><br />

* `[package-name]`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Takes the form `scope/name` to identify the package
<br /><br />

* `[<clone-url>[#branch-name]]`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Clone URL must end in `.git`. An optional branch can be specified with a `#`. Default is set to `master`.
<br /><br />

* `[source]`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Can be one of `github`, `gitlab`, or `bitbucket`. If none are specified, then the default in `.broconfig` will be used.
<br /><br />

**Examples:**

`bro install expressjs/express github`

Clones [express](https://github.com/expressjs/express) as a submodule from github into the `node_modules/` folder.

<br />

`bro install --host expressjs/express github`

Clones [express](https://github.com/expressjs/express) as a submodule from github into the `node_modules/` folder.

Also, pushes the clone up as a new repository to the Git repository hosting service specified in `.broconfig`.

---

## `bro uninstall [-options]`
