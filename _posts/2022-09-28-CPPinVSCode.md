---
layout: post
title: Change cpp Building Path in VSCode
date: 2022-09-28 23:47:07
decription:
tags: ['vscode', 'cpp', 'compile', 'windows']
categories: tips
---

When build and run c++ program in VSCode on Window PC, all object files, executables, link files and debug files and generated in project root folder,
which is very disorgnized. We can edit `.vscode/task.json` to make the compiled file to be saved in disired folders.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/disorgnizedfiles.png" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/taskjson.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The output files in working directory and the default task settings.
</div>

According to [this](https://stackoverflow.com/a/64102155), just modify `/Fe`, and add `/Fd`, `/Fo` arguments would do the trick.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/disorgnizedfilesafter.png" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/taskjsonafter.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The output files are all in "bin", and the edited task settings.
</div>