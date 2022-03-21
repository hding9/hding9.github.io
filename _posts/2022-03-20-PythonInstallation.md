---
layout: post
title: Install Python and Virtualenv on MacOS
date: 2022-03-20 23:27:43
description:
tags: ['MacOS', 'Python', 'Virtualenv', 'Virtualenvwrapper']
categories: Guide
---

#### Install
---
Install python and python2 using HomeBrew.

```sh
brew install python python@2
```

Python are installed in `/usr/local/Cellar/python@3.x` via HomeBrew.

Symlinks are created in `/usr/local/bin/` in addition to `/usr/local/opt/`.

To create symlink manually, e.g. `brew link python3`, which will create symbolic link in `/usr/local/bin/python3` that points to `/usr/local/Cellar/python@3.x/3.x.x/bin/python3`.

The message after installation:

> Unversioned symlinks `python`, `python-config`, `pip` etc. pointing to
> `python3`, `python3-config`, `pip3` etc., respectively, have been installed into
> `/usr/local/opt/python@3.x/libexec/bin`

which means to let `python`, `pip` start `python3` and `pip3` (referred from [here](https://stackoverflow.com/a/51912712)):
```
echo 'export "PATH=/usr/local/opt/python@3.x/libexec/bin:$PATH"' >> ~/.zshrc
```

Install Python packages with `pip`:
```
/usr/local/opt/python@3.x/bin/pip3 <package>
```
They will install into the site-package directory
```
/usr/local/bin/python3.x/site-packages
```

To let the installed `python@3.x` first in PATH:
```
echo 'export "PATH=/usr/local/opt/python@3.x/bin:$PATH"' >> ~/.zshrc
```
For compilers to find python@3.x:
```
export LDFLAGS="-L/usr/local/opt/python@3.x/lib"
```
For pkg-config to find python3.x:
```
export PKG_CONFIG_PATH="/usr/local/opt/python@3.x/lib/pkgconfig"
```

Install `virtualenv` & `virtualenvwrapper`
```
python3 -m pip install virtualenv
python3 -m pip install virtualenvwrapper
```

#### Configuration
---
```
export WORKON_HOME=$HOME/.virtualenv
export VIRTUALENVWRAPPER_PYTHON=/usr/local/bin/python3
export VIRTUALENVWRAPPER_VIRTUALENV=/usr/local/bin/virtualenv
source /usr/local/bin/virtualenvwrapper.sh
```
During startup, `virtualenvwrapper.sh` finds the first python and `virtualenv` programs on the `$PATH` and remembers them to use later. It is import for the `PATH` to be set **before** sourcing `virtualenvwrapper.sh`.

To override the `$PATH` search, set the variable `VIRTUALENVWRAPPER_PYTHON` to the full path of the interpreter to use and `VIRTUALENVWRAPPER_VIRTUALENV` to the full path of the `virtualenv` binary to use. Both variables must be set before sourcing `virtualenvwrapper.sh`.

#### Quick-Start
---
Run `workon` to see a list of environments.

Run `mkvirtualenv temp` to create an environment called `temp`.

Run `workon temp` to enter the environment.

Run `rmvirtualenv temp` to remove.