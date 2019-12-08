<div align="center">
<h3>todo-ng</h3>
<img src="https://github.com/georgeabr/py-todo-ng/blob/master/py-todo-ng.png">

</div>

## Overview
A little program to remind you of upcoming events / unfinished tasks.

Put them into `~/.zshrc` or `~/.bashrc` or whatever you want, and it will stop you from
putting off stuff.

Pickled (i.e., serialized) todo list objects are saved in ~/.local/share/py-todo/todo.dat by default.


## Dependencies
* python >=3.5 (sys, re, pickle, pathlib, datetime, readline)

## Tested Platforms
* Linux
* OSX (tested on 10.14 Mojave)

* Manual Installation (Linux)
```
$ git clone https://github.com/aesophor/py-todo.git
$ cd py-todo && sudo cp todo /usr/bin/todo
```

* Manual Installation (OSX)
```
$ git clone https://github.com/aesophor/py-todo.git
$ cd py-todo && cp todo /usr/local/bin/
```

## Usage
```
Usage: ./todo-ng <argument>
	a -a --add add                              -- Add a new item.
	a -a --add <title> <date or days>           -- Add a new item with a title and expiry date provided.
	e -e --edit <index>                         -- Edit an item.
	e -e --edit <index> <title> <date or days>  -- Edit an item with a title and expiry date provided.
	m -m --move <index> <new index>             -- Move an item from index to new index.
	r -r --remove <indices...>                  -- Remove items by their indices.
	l -l --list ls                              -- List all items.
	s -s --sort                                 -- Sort items chronologically.
	-org --orgfile <filename>                   -- Add org file todos.

	h -h --help                                 -- Display help message.
	v -v --version                              -- Display version info.

Use date in format YYYY/MM/DD - 2020/07/05, or <days>d - 3d, for due date of todo item

Configuration Options (See ~/.config/todo-ng/config):
* color = true / false
* detail_mode = true / false
Reminders data file: ~/.local/share/todo-ng/todo.dat  ```
```

```
[PY-TODO]
color = true / false
detail_mode = true / false
week_start_day = Sun
```

```
## Detail Mode

Discrete Mathematics Exam (Next Wednesday; 5 days left)  # detail_mode = true
Discrete Mathematics Exam (5 days left)                  # detail_mode = false
```

## Contributors from original repo:
https://github.com/aesophor/py-todo
Special thanks to all the contributors! (In lexicographical order)
* [Arsukeey](https://github.com/Arsukeey) - Added Detail Mode (e.g., Next Wednesday)
* [christophergeiger3](https://github.com/christophergeiger3) - Reformatted code
* [diplozoon](https://github.com/diplozoon) - Reformatted code
* [jonaylor89](https://github.com/jonaylor89) - More robust config parsing
* [luvhalvorson](https://github.com/luvhalvorson) - Updated README.md
* [MMarinov97](https://github.com/MMarinov97) - Added compatibility with emacs org file
* [patatman](https://github.com/patatman) - Improved -a --add. Tested py-todo on MacOS
* [RewoundVHS](https://github.com/RewoundVHS) - AUR Package Maintainer, Color Mode
* [Steampunkery](https://github.com/Steampunkery) - Added -e --edit, -m --move, refactoring

## License
Available under the [MIT License](https://github.com/aesophor/py-todo/blob/master/LICENSE)
