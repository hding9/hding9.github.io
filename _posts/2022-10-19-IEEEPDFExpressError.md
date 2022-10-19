---
layout: post
title: IEEE PDF Express Font XXX Not Embedded Error
date: 2022-10-19 14:25:57
decription:
tags: ['pdf', 'latex']
categories: fix
---

When submitting pappers to IEEE PDF Express for validation, there's usually an error about a font embedding.

e.g.,

> Errors: Font TimesNewRomanPS-BoldItalicMT, TimesNewRomanPS-BoldMT is not embedded (15x on page 8) 

A quick fix can be done on Windows with adobe installed.

1. Open the pdf file with Edge, Chrome, or Adobe.
2. Print the file and select Adobe printer.
3. Click on properties and then select "Adobe PDF Settings" tab.
4. Uncheck "Rely on system fonts only; do not use document fonts".
5. Click on the Edit button which is after "Default Settings: Standard".
6. Click on Fonts on the left column, and add the not embedded fonts to "Always Embedded" sections.
7. Click on OK, and save it to a new settings.
8. Use the new setting to print the pdf file.

The new pdf file should pass the IEEE PDF Express validation check.


Referred from [here](http://xiaohui-blog.blogspot.com/2012/04/fixing-font-not-embedded-issue-to-pass.html).
