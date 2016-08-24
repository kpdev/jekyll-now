---
layout: post
title: Different notes
---

Some tips for linux, vim and others

[linux] Add swap file:
sudo fallocate -l 2g /mnt/2GB.swap
sudo chmod 600 /mnt/2GB.swap 
sudo mkswap /mnt/2GB.swap
sudo swapon /mnt/2GB.swap

[vim] Close current buffer in split
:bd | bp #
This could be added to vimrc:
command Bd bp\|bd \#

