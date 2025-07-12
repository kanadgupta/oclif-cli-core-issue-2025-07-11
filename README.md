# oclif-cli-core-issue-2025-07-11

this repository reproduces an issue with [`@oclif/core@4.5.0`](https://github.com/oclif/core/releases/tag/4.5.0) where certain errors are not throwing properly.

## reproduction steps

1. check out this repo

2. install the dependencies:

   ```sh
   npm ci
   ```

3. build the CLI:

   ```sh
   npm run build
   ```

4. run a command that doesn't exist and note how the command succeeds with no output:

   ```sh
   bin/run.js test
   ```

   > expected behavior is that an error saying `Error: command asdfasdf not found` is thrown

5. attempt to run an existing command with an invalid argument and note how the command fails but no error message is printed:

   ```sh
   bin/run.js test
   ```

   > expected behavior is that an error saying `Error: Missing 1 required arg:` is printed to the console

6. run the following command to install an older version of `@oclif/core`, repeat steps 3-5 above, and notice the differing behavior:

   ```sh
   npm install @oclif/core@4.4
   ```

## about this reproduction environment

the result of `npx envinfo --system --npmPackages '{oclif*,@oclif/*}' --binaries`:

```
  System:
    OS: macOS 15.5
    CPU: (16) arm64 Apple M4 Max
    Memory: 28.55 GB / 128.00 GB
    Shell: 5.9 - /bin/zsh
  Binaries:
    Node: 20.19.0 - /usr/local/bin/node
    Yarn: 1.22.22 - ~/Code/kanadgupta/oclif-cli-core-issue-2025-07-11/node_modules/.bin/yarn
    npm: 10.9.3 - ~/Code/kanadgupta/oclif-cli-core-issue-2025-07-11/node_modules/.bin/npm
    pnpm: 10.6.5 - /usr/local/bin/pnpm
  npmPackages:
    @oclif/core: ^4 => 4.5.0
    @oclif/plugin-help: ^6 => 6.2.30
    @oclif/plugin-plugins: ^5 => 5.4.44
    @oclif/prettier-config: ^0.2.1 => 0.2.1
    @oclif/test: ^4 => 4.1.13
    oclif: ^4 => 4.20.5
```

this repository was scaffolded out using the following command: `npx oclif@latest generate oclif-cli-core-issue-2025-07-11`.

here were all of the answers i returned in the prompts:

```
? Select a module type ESM
? NPM package name oclif-cli-core-issue-2025-07-11
? Command bin name the CLI will export cli-test
? Description A new CLI generated with oclif
? Author Kanad Gupta
? License MIT
? Who is the GitHub owner of repository (https://github.com/OWNER/repo) kanadgupta
? What is the GitHub name of repository (https://github.com/owner/REPO) oclif-cli-core-issue-2025-07-11
? Select a package manager npm
```
