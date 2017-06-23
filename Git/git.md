# Simple Git Use
## The most commonly used git 
- git init
- git clone
- git add
- git del
- git commit
- git push
- git pull
- git config

## Git config
There are three level config
* .git/config
> Exist in the repository directory, setting with --local option or by default. With the highest procedence.
* ~/.gitconfig
> User-specific configuration. Setting with --glocal option
* /etc/gitconfig
> System-wide configuration. Setting with --system. 
```
$ git config --global user.name "My Name"
$ git config --glocal user.email "myname@mydomain.com"

// if omit the --global option or using --file, this would only affect the current repository

$ git config --unset --glocal user.email 
// this will unset the settings
```
* Usage of git config
```
usage: git config [<options>]

Config file location
    --global              use global config file
    --system              use system config file
    --local               use repository config file
    -f, --file <file>     use given config file
    --blob <blob-id>      read config from given blob object

Action
    --get                 get value: name [value-regex]
    --get-all             get all values: key [value-regex]
    --get-regexp          get values for regexp: name-regex [value-regex]
    --get-urlmatch        get value specific for the URL: section[.var] URL
    --replace-all         replace all matching variables: name value [value_regex]
    --add                 add a new variable: name value
    --unset               remove a variable: name [value-regex]
    --unset-all           remove all matches: name [value-regex]
    --rename-section      rename section: old-name new-name
    --remove-section      remove a section: name
    -l, --list            list all
    -e, --edit            open an editor
    --get-color           find the color configured: slot [default]
    --get-colorbool       find the color setting: slot [stdout-is-tty]

Type
    --bool                value is "true" or "false"
    --int                 value is decimal number
    --bool-or-int         value is --bool or --int
    --path                value is a path (file or directory name)

Other
    -z, --null            terminate values with NUL byte
    --name-only           show variable names only
    --includes            respect include directives on lookup
    --show-origin         show origin of config (file, standard input, blob, command line)

```
* git of the

## Git branch


## Git merge
 