---
layout: post
title: Install Python and Virtualenv on MacOS
date: 2022-03-21 01:01:15
description:
tags: ['MacOS', 'Python', 'Virtualenv', 'Jupyter Notebook']
categories: Tips
---
To run jupyter notebook in virtual environment, one approach is to have one global jupyter notebook installation, but to point to different kernels to run as the backend.

Assume you have installed jupyter notebook not in a virtualenv. To install on MacOS

```sh
brew install jupyter
```

Enter into virtual environment and install ipykernel
```sh
workon virtualenv-name

pip install ipykernel
```

Install a new kernel
```sh
python -m ipykernel install --user --name=virtualenv-name
```
or
```sh
ipython kernel install --user --name=virtualenv-name
```