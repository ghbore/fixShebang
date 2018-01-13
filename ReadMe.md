# fixShebang

## Rationale

Sometimes when using someone's scripts, the parser path in shebang would be different between developers and users.  So the platform portability would be a problem, especially when developer use hard coded shebang, rather than strict 'env' shebang.

Thus this script aims to fix this problem, by updating parser path to right one (detect by 'env' or user defined config file).

This script was only tested on Ubuntu and CentOS, and depends on bash and following commands: file, whereis, awk, sed and head.

## Usage

fixShebang [-b ''] [-c ''] [-d] [-s] file1 ...

    -b str    backup file suffix
    -c file   path config filename
    -d        turn on debug
    -s        turn on strict mode (env)

## Arguments

### -c file

Path config file follows BASH variable defination rule, for example:

```bash
# this is a comment line
env=/usr/bin/env # this is a comment
```
