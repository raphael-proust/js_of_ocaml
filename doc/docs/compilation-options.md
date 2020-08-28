---
id: compilation-options
title: Compilation options
sidebar_label: Compilation options
---


| Option name       | Description                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------|
| --version         | Display the version of the compiler                                                                    |
| -o file           | Set the output filename to `file`                                                                      |
| --source-map      | Generate sourcemap                                                                                     |
| --opt {1,2,3}     | Set the compilation profile (default 1). See **Optimization** section below.                           |
| --pretty          | Pretty print javascript output                                                                         |
| --no-inline       | Disable code inlining                                                                                  |
| --debug-info      | Output debug information                                                                               |
| -I dir            | Add `dir` to the list of  include directories                                                          |
| --file file[:dir] | Register `file` to the pseudo filesystem  and choose the the destination directory `dir` (default `/`) |
| --enable option   | Enable option `option`                                                                                 |
| --disable option  | Disable option `option`                                                                                |

## Optimizations

 * For Debugging: `--pretty --no-inline --debug-info` + eventually `--disable staticeval --disable share`
 * For Production: `--opt 3`. It minimize the generated javascript by applying
   various optimizations until a fix-point is reached

## List of option to "--disable" or "--enable"

| Option name | Default | Description                                  |
|-------------|---------|----------------------------------------------|
| pretty      | false   | Pretty print the javascript output           |
| debuginfo   | false   | Output debug information (location)          |
| deadcode    | true    | Deadcode elimination                         |
| inline      | true    | Code inlining                                |
| shortvar    | true    | Shorten variable names                       |
| staticeval  | true    | Static evaluation of constants               |
| share       | true    | Share string and number constants            |
| strict      | true    | Enable strict mode                           |
| debugger    | true    | Keep debugger statements. Stripped otherwise |
| genprim     | true    | Generate dummy primitives when missing       |
| excwrap     | true    | Wrap js exception into ocaml ones            |
| optcall     | true    | Javascript optimizations                     |