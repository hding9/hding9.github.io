---
layout: post
title: Disable repeating keys on MacOS
date: 2022-03-20 23:18:51
description:
tags: ['MacOS', 'VSCode', 'Repeating Keys']
categories: Guide
---

When typing in some applications on MacOS, pressing and holding a key for example ```a``` gives you ```à á â ä æ ã å ā```. That is 
because the repeating key is enabled. To disable repeating keys in system-wide, you can type:

```
defaults write -g ApplePressAndHoldEnabled -bool false
```

In addition, it can be disabled for certain application. For example, disable repeating keys for pycharm, which is very 
helpful when using plugin ```IdeaVim```.

```
defaults write com.jetbrains.pycharm ApplePressAndHoldEnabled -bool false
```
For CLion:
```
defaults write com.jetbrains.clion ApplePressAndHoldEnable -bool false
```

For VSCodium:
```
defaults write com.visualstudio.code.oss ApplePressAndHoldEnabled -bool false
```

For VSCode:
```
defaults write com.microsoft.VSCode ApplePressAndHoldEnabled -bool false
```

---
Referred from [here](https://gist.github.com/lsd/1e1826907ab7e49c536a).