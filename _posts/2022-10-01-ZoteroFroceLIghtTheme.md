---
layout: post
title: Force Light Theme on Zotero
date: 2022-10-01 15:08:19
decription:
tags: ['zotero', 'theme', 'linux']
categories: fix
---

The GUI display of Zotero on Ubuntu system with dark theme can be very vague. 
It is nearly impossoble to read the paper title on the tab with black font on a dark background.
Only the activated paper table has a white background.
Most of the time I have to cycle through each tab to find what papers I have opened, which is very frustrating.


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/zoterodark.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Zotero on Unbuntu 22.04 with Dracula theme.
</div>

One work around is to force zotero start with a light theme.
We can add environment variable `GTK_THEME=Default` in `zotero.desktop` when starting zotero.

```bash
Exec=env GTK_THEME=Default bash -c "$(dirname $(realpath $(echo %k | sed -e 's/^file:\/\///')))/zotero -url %U"
```