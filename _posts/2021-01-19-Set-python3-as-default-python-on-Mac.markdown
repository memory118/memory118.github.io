---
layout: post
title:  "Set python3 as default python on Mac"
date:   2021-01-19 22:44:52 +0800
categories: env
tags: python
---
python2 and python3 are the most popular python versions which generally exist in our computers at the same time . However, as we know, they are incompatible at some time, even with different syntax. For example, you need to use "print()" to print your strings for python3; what's more, python3 uses utf-8 as default encoding format so you can denote your codes in Chinese but don't need to specify the utf-8 encoding.

Since the python(2) and python3 projects might exist in our computer at the same time, so mostly we cannot remove one of python version. Here is a simple way to switch your python version between python(2) and python3 on Mac.

Steps:

1. new/edit **~/.bashrc**, add the following line in:

   `alias python="python3"`

2. Option

   1. You can use the following way to make it effective in time for the current terminal

      `source ~/.bashrc`

   2. You can also use the following way to make it effective for all the terminals

      1. new/edit **~/.bash_profile**, add the following line in:

         `source ~/.bashrc`