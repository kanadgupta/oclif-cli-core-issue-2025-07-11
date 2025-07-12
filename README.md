oclif-cli-core-issue-2025-07-11
=================

A new CLI generated with oclif


[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-cli-core-issue-2025-07-11.svg)](https://npmjs.org/package/oclif-cli-core-issue-2025-07-11)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-cli-core-issue-2025-07-11.svg)](https://npmjs.org/package/oclif-cli-core-issue-2025-07-11)


<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g oclif-cli-core-issue-2025-07-11
$ cli-test COMMAND
running command...
$ cli-test (--version)
oclif-cli-core-issue-2025-07-11/0.0.0 darwin-arm64 node-v20.19.0
$ cli-test --help [COMMAND]
USAGE
  $ cli-test COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`cli-test hello PERSON`](#cli-test-hello-person)
* [`cli-test hello world`](#cli-test-hello-world)
* [`cli-test help [COMMAND]`](#cli-test-help-command)
* [`cli-test plugins`](#cli-test-plugins)
* [`cli-test plugins add PLUGIN`](#cli-test-plugins-add-plugin)
* [`cli-test plugins:inspect PLUGIN...`](#cli-test-pluginsinspect-plugin)
* [`cli-test plugins install PLUGIN`](#cli-test-plugins-install-plugin)
* [`cli-test plugins link PATH`](#cli-test-plugins-link-path)
* [`cli-test plugins remove [PLUGIN]`](#cli-test-plugins-remove-plugin)
* [`cli-test plugins reset`](#cli-test-plugins-reset)
* [`cli-test plugins uninstall [PLUGIN]`](#cli-test-plugins-uninstall-plugin)
* [`cli-test plugins unlink [PLUGIN]`](#cli-test-plugins-unlink-plugin)
* [`cli-test plugins update`](#cli-test-plugins-update)

## `cli-test hello PERSON`

Say hello

```
USAGE
  $ cli-test hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ cli-test hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/kanadgupta/oclif-cli-core-issue-2025-07-11/blob/v0.0.0/src/commands/hello/index.ts)_

## `cli-test hello world`

Say hello world

```
USAGE
  $ cli-test hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ cli-test hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/kanadgupta/oclif-cli-core-issue-2025-07-11/blob/v0.0.0/src/commands/hello/world.ts)_

## `cli-test help [COMMAND]`

Display help for cli-test.

```
USAGE
  $ cli-test help [COMMAND...] [-n]

ARGUMENTS
  COMMAND...  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for cli-test.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.2.30/src/commands/help.ts)_

## `cli-test plugins`

List installed plugins.

```
USAGE
  $ cli-test plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ cli-test plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.44/src/commands/plugins/index.ts)_

## `cli-test plugins add PLUGIN`

Installs a plugin into cli-test.

```
USAGE
  $ cli-test plugins add PLUGIN... [--json] [-f] [-h] [-s | -v]

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
  Installs a plugin into cli-test.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the CLI_TEST_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the CLI_TEST_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ cli-test plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ cli-test plugins add myplugin

  Install a plugin from a github url.

    $ cli-test plugins add https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ cli-test plugins add someuser/someplugin
```

## `cli-test plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ cli-test plugins inspect PLUGIN...

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
  $ cli-test plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.44/src/commands/plugins/inspect.ts)_

## `cli-test plugins install PLUGIN`

Installs a plugin into cli-test.

```
USAGE
  $ cli-test plugins install PLUGIN... [--json] [-f] [-h] [-s | -v]

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
  Installs a plugin into cli-test.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the CLI_TEST_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the CLI_TEST_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ cli-test plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ cli-test plugins install myplugin

  Install a plugin from a github url.

    $ cli-test plugins install https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ cli-test plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.44/src/commands/plugins/install.ts)_

## `cli-test plugins link PATH`

Links a plugin into the CLI for development.

```
USAGE
  $ cli-test plugins link PATH [-h] [--install] [-v]

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
  $ cli-test plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.44/src/commands/plugins/link.ts)_

## `cli-test plugins remove [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ cli-test plugins remove [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ cli-test plugins unlink
  $ cli-test plugins remove

EXAMPLES
  $ cli-test plugins remove myplugin
```

## `cli-test plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ cli-test plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.44/src/commands/plugins/reset.ts)_

## `cli-test plugins uninstall [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ cli-test plugins uninstall [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ cli-test plugins unlink
  $ cli-test plugins remove

EXAMPLES
  $ cli-test plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.44/src/commands/plugins/uninstall.ts)_

## `cli-test plugins unlink [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ cli-test plugins unlink [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ cli-test plugins unlink
  $ cli-test plugins remove

EXAMPLES
  $ cli-test plugins unlink myplugin
```

## `cli-test plugins update`

Update installed plugins.

```
USAGE
  $ cli-test plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.44/src/commands/plugins/update.ts)_
<!-- commandsstop -->
