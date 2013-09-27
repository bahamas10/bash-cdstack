bash-cdstack
============

Store the last X directories visited using `cd` in bash

See the blog post here: http://daveeddy.com/2013/09/14/directory-management-with-cd/

Installation
------------

### basher

Use [basher](https://github.com/bahamas10/basher) to manage this plugin

After installing `basher`, install this plugin by running

    basher install git://github.com/bahamas10/bash-cdstack.git

Or install manually for `basher` with

    cd ~/.basher/plugins
    git clone git://github.com/bahamas10/bash-cdstack.git

### manually

    git clone git://github.com/bahamas10/bash-cdstack.git
    cd bash-cdstack
    cat cdstack.bash >> ~/.bashrc
    exec bash

Usage
-----

![cdstack](http://daveeddy.com/static/media/2013/09/cdstack.png)

You `cd` around like you normally would, and the directories are pushed into a
stack. Use the function `s` to view the stack of directories, and run `s "$num"` to
`cd` into the directory listed. Use `b` to jump back 1 directory.

Exports
-------

### Global Variables

- `CD_STACK_MAX` - the max number of directory names to store, defaults to 15
- `CD_STACK_REVERSE` - set this variable to reverse the stack when printed with `s`
- `_CD_STACK` - (private) the stack object itself (an array)
- `_CD_STACK_PTR` - (private) the current position in the stack

### Environmental Variables

None

### Functions

- `cd()` - `cd` as you would expect it, but it records directories into the stack
- `s()` - show the current directory stack, or pass an argument to move into a stacked dir
- `b()` - jump back 1 directory in the stack

### Aliases

None

License
-------

MIT
