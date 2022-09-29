---
layout: post
title: VSCode Keymaps with VIM plugin
date: 2022-04-12 18:47:34
description:
tags: ['vim', 'VSCode', 'ctrl', 'keybindings', 'keymaps']
categories: Tips
---

# VIM plugin
Vim is a powerful text editor with tons of plugins which combined together are capable to fulfill any requests.
It is also my favorate text editor when writing some light documents.
What attracts me most is its powerful and rapid cursor movement without moving your hand away from keyboard.
That is, all movements can be done with just different kinds of combinations of keys.
However, vim lacks of a morden interface for some users. I know it can be made to a whole different fancy level with some plugins.
Stil, that requries some research and configurations. Also, when it get's bulkier, the start speed can be lower.

# Disable some "ctrl" keybdings of vim plugin

VSCode currently is my daily driver for coding, and vim plugin makes it more efficient which enables my hands focus 
on the keyboard and get rid of the mouse. One thing I found really bothers me is the `<ctrl-c>` binding for copy in vscode.
When you have vim plugin installed `<ctrl-c>` will bind to the "stop" functionality like it does as a shell command.
I personaly don't use `<ctrl-c>` as break out too much. Instead, I'd prefer it function as the 'copy' shortcut.

So, in order to disable `<ctrl-c>` of vim in vscode, just type `ctrl`+`shift`+`p` for command palette, go to `Preferences: Open Settings (UI)`,
and search for `Vim: Handle Keys`. Click `Edit in settings.json`, then add `<ctrl-c>: false,`, save and close.
It now should behave as the copy shortcut.

# Navigation in VSCode (vim style)
- `ctrl + j` and `ctrl + k` shift focus between editors in an editor group and terminal windows in the terminal.
- `ctrl + h` and `ctrl + l` shift focus between editor groups including the terminal.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/keybindings.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

Referred from [here](https://stackoverflow.com/a/71519133)
