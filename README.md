# An Issue Reproduction for `nr` Command

This document provides steps to reproduce an issue that occurs in the following repository:

- https://github.com/antfu/ni.git

## Reproduction Steps

1. Install `ni` package globally.

   ```sh
   npm install -g @antfu/ni
   ```

1. Specify the agent to be used by `ni` by referring to [this config](https://github.com/antfu/ni#config).

1. Run the following commands to concurrently run scripts with different string lengths.

   ```sh
   # You can choose any script names.
   nr un & nr deux & nr trois & nr quatre
   ```

   > **Note**
   > If the issue does not occur on the first run, repeat the command multiple times.

1. Once the issue occurs, the `nr` command will stop working. For example, if you try to run a script that does not exist, it will not output an error message.
