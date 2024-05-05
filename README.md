afg
=================

A new CLI generated with oclif


[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/afg.svg)](https://npmjs.org/package/afg)
[![Downloads/week](https://img.shields.io/npm/dw/afg.svg)](https://npmjs.org/package/afg)


<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g afg
$ afg COMMAND
running command...
$ afg (--version)
afg/0.0.0 darwin-arm64 node-v20.12.2
$ afg --help [COMMAND]
USAGE
  $ afg COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`afg hello PERSON`](#afg-hello-person)
* [`afg hello world`](#afg-hello-world)
* [`afg help [COMMAND]`](#afg-help-command)
* [`afg plugins`](#afg-plugins)
* [`afg plugins add PLUGIN`](#afg-plugins-add-plugin)
* [`afg plugins:inspect PLUGIN...`](#afg-pluginsinspect-plugin)
* [`afg plugins install PLUGIN`](#afg-plugins-install-plugin)
* [`afg plugins link PATH`](#afg-plugins-link-path)
* [`afg plugins remove [PLUGIN]`](#afg-plugins-remove-plugin)
* [`afg plugins reset`](#afg-plugins-reset)
* [`afg plugins uninstall [PLUGIN]`](#afg-plugins-uninstall-plugin)
* [`afg plugins unlink [PLUGIN]`](#afg-plugins-unlink-plugin)
* [`afg plugins update`](#afg-plugins-update)

## `afg hello PERSON`

Say hello

```
USAGE
  $ afg hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ afg hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/Personal/afg/blob/v0.0.0/src/commands/hello/index.ts)_

## `afg hello world`

Say hello world

```
USAGE
  $ afg hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ afg hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/Personal/afg/blob/v0.0.0/src/commands/hello/world.ts)_

## `afg help [COMMAND]`

Display help for afg.

```
USAGE
  $ afg help [COMMAND...] [-n]

ARGUMENTS
  COMMAND...  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for afg.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.0.21/src/commands/help.ts)_

## `afg plugins`

List installed plugins.

```
USAGE
  $ afg plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ afg plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.18/src/commands/plugins/index.ts)_

## `afg plugins add PLUGIN`

Installs a plugin into afg.

```
USAGE
  $ afg plugins add PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into afg.

  Uses bundled npm executable to install plugins into /Users/pkim/.local/share/afg

  Installation of a user-installed plugin will override a core plugin.

  Use the AFG_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the AFG_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ afg plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ afg plugins add myplugin

  Install a plugin from a github url.

    $ afg plugins add https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ afg plugins add someuser/someplugin
```

## `afg plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ afg plugins inspect PLUGIN...

ARGUMENTS
  PLUGIN...  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ afg plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.18/src/commands/plugins/inspect.ts)_

## `afg plugins install PLUGIN`

Installs a plugin into afg.

```
USAGE
  $ afg plugins install PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into afg.

  Uses bundled npm executable to install plugins into /Users/pkim/.local/share/afg

  Installation of a user-installed plugin will override a core plugin.

  Use the AFG_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the AFG_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ afg plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ afg plugins install myplugin

  Install a plugin from a github url.

    $ afg plugins install https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ afg plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.18/src/commands/plugins/install.ts)_

## `afg plugins link PATH`

Links a plugin into the CLI for development.

```
USAGE
  $ afg plugins link PATH [-h] [--install] [-v]

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help          Show CLI help.
  -v, --verbose
      --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ afg plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.18/src/commands/plugins/link.ts)_

## `afg plugins remove [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ afg plugins remove [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ afg plugins unlink
  $ afg plugins remove

EXAMPLES
  $ afg plugins remove myplugin
```

## `afg plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ afg plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.18/src/commands/plugins/reset.ts)_

## `afg plugins uninstall [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ afg plugins uninstall [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ afg plugins unlink
  $ afg plugins remove

EXAMPLES
  $ afg plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.18/src/commands/plugins/uninstall.ts)_

## `afg plugins unlink [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ afg plugins unlink [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ afg plugins unlink
  $ afg plugins remove

EXAMPLES
  $ afg plugins unlink myplugin
```

## `afg plugins update`

Update installed plugins.

```
USAGE
  $ afg plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.18/src/commands/plugins/update.ts)_
<!-- commandsstop -->
