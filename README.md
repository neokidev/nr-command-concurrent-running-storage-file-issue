# An Issue Reproduction for `ni` Package

This document provides steps to reproduce an issue that occurs in the following repository:

- https://github.com/antfu/ni.git

## Reproduction Steps

1. Install `ni` package globally.

   ```sh
   npm install -g @antfu/ni
   ```

2. Run the following commands to concurrently run scripts with different string lengths.

   ```sh
   # You can choose any script names.
   nr un & nr deux & nr trois & nr quatre
   ```

   > **Note**
   > If the issue does not occur on the first run, repeat the command multiple times.

3. Once the issue occurs, the `ni` command will stop working. For example, if you try to run a script that does not exist, it will not output an error message.
