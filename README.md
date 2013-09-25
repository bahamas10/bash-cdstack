bash-cdstack
============

Store the last X directories visited using cd in bash

See the blog post here: http://daveeddy.com/2013/09/14/directory-management-with-cd/

Installation
------------

Use [basher](https://github.com/bahamas10/basher) to manage this plugin

After installing `basher`, install this plugin by running

    cd ~/.basher/plugins
    git clone git://github.com/bahamas10/bash-cdstack.git

Usage
-----

![cdstack](http://daveeddy.com/static/media/2013/09/cdstack.png)

You `cd` around like you normally would, and the directories are pushed into a
stack. Use the function `s` to view the stack of directories, and run `cs $num` to
`cd` into the directory listed.

Exports
-------

### Global Variables

- `CD_STACK_MAX` - the max number of directory names to store, defaults to 15
- `_CD_STACK` - the stack object itself (an array)

### Environmental Variables

None

### Functions

- `cd()` - `cd` as you would expect it, but it records directories into the stack
- `s()` - show the current directory stack
- `cs()` - `cd` into a stacked directory by using its number

License
-------

MIT
