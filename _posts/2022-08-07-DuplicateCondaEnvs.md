---
layout: post
title: Duplicate Conda Envs in Spaceship Prompt
date: 2022-08-07 11:49:43
decription:
tags: ['conda environment', 'spaceship', 'oh-my-zsh']
categories: fix
---

Sometimes new installed `conda` displays duplicate environment names in the [spaceship prompt](https://spaceship-prompt.sh/).

It shows like this:

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/duplicateenvbefore.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

This is becuase by default `conda` shows the activated environments in prompt.

You can disable it by this:

```bash
conda config --set changeps1 False
```

Now the displayed conda environment on the top is gone:

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/duplicateenvbefore.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
