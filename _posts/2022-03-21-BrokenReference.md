---
layout: post
title: Broken Python Reference After Brew Upgrade
date: 2022-03-21 00:57:53
description:
tags: ['macos', 'python', 'virtualenv', 'homebrew']
categories: tips
---

It seems the references are broken. It shows like this:
```
dyld: Library not loaded: @executable_path/../.Python
  Referenced from: /Users/carrot/.virtualenvs/py3env/bin/python
  Reason: image not found
```

In fact, there is a problem with the library, you need to regenerate the links of the Python interpreter. In this case, this is just to remove the existing links and re-execute the virtualenv command.

First, deactivate the virtualenv
```
(py3env) ~ $ deactivate
```
then, find and delete all the symlinks, remove ```-delete``` flag to see symlinks
```
$HOME/.virtualenvs $ find py3env -type l -delete
```
Last, recreate virtualenv
```
$HOME/.virtualeves $ virtualenv py3env
```