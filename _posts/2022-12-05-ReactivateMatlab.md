---
layout: post
title: Reactivate Matlab One Month Trial Error Fix
date: 2022-12-05 16:27:54
decription:
tags: ['matlab', 'activation', 'trial']
categories: fix
---

Matlab has 1 month trial for educational account. When reactivating the trial after expiration on linux, it shows cannot activate for now due to some privilege issue.

To fix, go to where your acitvation file is located from terminal and run it.

```bash
$ cd /usr/local/MATLAB/R2022b/bin
$ sudo ./activate_matlab.sh
```

Login and input a username for activation, the matlab is ready to use after completion.


Referred from [here](https://www.mathworks.com/matlabcentral/answers/304652-license-manager-error-9-when-run-as-administrator-but-not-normally#answer_406443).
