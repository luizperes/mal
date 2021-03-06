# mal - MyAnimeList Command Line Interface

[![Build Status](https://travis-ci.org/ryukinix/mal.svg?branch=master)](https://travis-ci.org/ryukinix/mal)
[![codecov](https://codecov.io/gh/ryukinix/mal/branch/master/graph/badge.svg)](https://codecov.io/gh/ryukinix/mal)
[![PyPi version](https://img.shields.io/pypi/v/mal.svg)](https://pypi.python.org/pypi/mal/)
[![Requirements Status](https://requires.io/github/ryukinix/mal/requirements.svg?branch=master)](https://requires.io/github/ryukinix/mal/requirements/?branch=master)
[![PyPi License](https://img.shields.io/pypi/l/mal.svg)](https://pypi.python.org/pypi/mal/)
[![PyPI pyversions](https://img.shields.io/pypi/pyversions/mal.svg)](https://pypi.python.org/pypi/mal/)
[![PyPI status](https://img.shields.io/pypi/status/mal.svg)](https://pypi.python.org/pypi/mal/)
[![HitCount](https://hitt.herokuapp.com/ryukinix/mal.svg)](https://github.com/ryukinix/mal)


## Description

`mal` is a command-line client for [MyAnimeList.net](http://myanimelist.net/) which uses the official [API](http://myanimelist.net/modules.php?go=api).
It should remain functional indefinitely (unlike web-scraping alternatives).
It is currently in alpha development so new ideas are welcome!
This project was inspired initially in [mal](https://github.com/pushrax/mal).

## Features

* Searching your anime list
* Fetch your anime list
* List animes in certain status (e.g. watching)
* Increment or decrement episodes seen of animes
* Add animes to your plan to watch list
* Edit contents of your animes on its your own preferred text editor:
  tags, status, score.
* Print your MAL stats! Just like MyAnimeList stats.

And more are currently being developed!

## TL;DR | Demos

![Main Usage](https://cloud.githubusercontent.com/assets/7642878/19803847/59295fd0-9ce1-11e6-9292-7e52266de4af.gif)


![Listing Animes By Status](https://cloud.githubusercontent.com/assets/7642878/19803846/59157a9c-9ce1-11e6-93a7-30665ae859bf.gif)

## Requirements

- Python 3.4+
- [setuptools](https://pypi.python.org/pypi/setuptools/3.5.1) (For installing and developing)
- [requests](http://docs.python-requests.org/en/latest/index.html)
- [appdirs](https://pypi.python.org/pypi/appdirs)
- [decorating](https://pypi.python.org/pypi/decorating/)
- [argparse](https://docs.python.org/3.5/library/argparse.html) (Merged into stdlib since version 3.2)

Check [requirements.txt](requirements.txt) for exact versions.

## Installation

### Using pip

From the command line run:

```
pip install --user mal
```

### Manual Installation

Clone this project and run inside it:

```
make install
```

Probably we'll need have super-user permissions, but I'd recommend you
to install inside of a virtualenv or use the `pip install --user' stuff.

### On ArchLinux

If you're using the archlinux distro this project has been packaged and uploaded to
the AUR as [python-mal-git](https://aur.archlinux.org/packages/python-mal-git).

## Usage

### Authenticating

The program needs your credentials to access your list. In the first call to any valid command the program will ask for your username and password and save it in **plain text** in the default path (on linux `~/.config/mal/myanimelist.ini`).

The file will be save in the following format:


```ini
[mal]
username = your_username
password = your_password

```

After authenticating you can start using the program.

### Using The Interface

When `mal` is executed without any arguments the help message is displayed:

```
usage: mal [-h] [-v]
           {search,filter,increase,inc,decrease,dec,login,list,config,drop,stats,add,edit}
           ...

MyAnimeList command line client.

positional arguments:
  {search,filter,increase,inc,decrease,dec,login,list,config,drop,stats,add,edit}
                        commands
    search              search an anime
    filter              find anime in users list
    increase (inc)      increase anime's watched episodes by one
    decrease (dec)      decrease anime's watched episodes by one
    login               save login credentials
    list                list animes
    config              Print current config file and its path
    drop                Put a selected anime on drop list
    stats               Show anime watch stats
    add                 add an anime to the list
    edit                edit entry

optional arguments:
  -h, --help            show this help message and exit
  -v, --version         show the version of mal


```

You can also use the `-h` or `--help` options on `mal` or any of its subcommands to see specific help message.


## Contributing

Look at [CONTRIBUTING.md](CONTRIBUTING.md)


## License

[GPLv3](LICENSE)
