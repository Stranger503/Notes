1.Change Bios Time Same as Date command.
==============================
hwclock -w

2.Change Kernal time.
===================
date -s 00:00:00

3.Change time zone
==================
sudo ln -sf /usr/share/zoneinfo/Asia/Kolkata /etc/localtime

4.Newbaot -crontab
==================
newsboat -x reload

5.Right Click Shortcut.
=======================
Shift+F10

6.Arch linux PGP signature.
===========================
sudo pacman -S archlinux-keyring

7. Hide Vim(~)
==============

set fillchars=fold:\ ,vert:\│,eob:\ ,msgsep:‾

8.Hide Vim Number and Relative number
=====================================

set nu! && set nornu

9.How to set a service.
=======================
sudo ln -s  /etc/runit/sv/cronie/ /run/runit/service/

10.How to flash windows 10.
---------------------------
sudo woeusb -d  Entertainment/HDD/WIN/Win10.iso /dev/sda --target-filesystem ntfs

11. How to install Windows
--------------------------

sudo woeusb -d  Entertainment/ISo/WIN11..iso /dev/sdb --target-filesystem ntfs
