usb-rofi
========

[![usb-rofi check](https://github.com/andrelcmoreira/usb-rofi/workflows/usb-rofi%20check/badge.svg)](https://github.com/andrelcmoreira/usb-rofi/actions)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

### Overview

**usb-rofi** is a simple tool to help the management of USB flash drives using
rofi app launcher and udev. It's composed by the udev rule `usb-rofi.rules`
and the script `usb-rofi`. The rule is responsible for trigger the script when
a new device is attached to the system, which in turn will prompt the user for
the action to be performed. The main usage for this tool is for tiling window
managers such as i3, dmw, bspwm, etc.

### Dependencies

- udev
- rofi
- notify-send

### Installation

```bash
$ make usb-rofi
$ sudo make install
```

### Usage

After the installation, the `usb-rofi` is ready to detect and notify the user
when a new flash drive is attached to the system. To improve the usability,
you can bind a hotkey to umount devices easily. In my case (i3), would
be something like this:

```bash
bindsym $mod+u exec "qsudo /usr/bin/usb-rofi -u"
```

### Supported distros

So far, the `usb-rofi` was tested only in void-linux and debian.

### Demo

![video](resources/.video.gif)
