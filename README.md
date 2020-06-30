# Dotfiles

## Table of contents
* [Overview](#overview)
* [Examples](#examples)
* [Requirements](#requirements)
* [Key Bindings](#key-bindings)
* [Setup](#setup)

## Overview
This is my config for i3wm, the tiling window manager I have running on Ubuntu. Some of the config files, however, may be used on GNU/Linux systems that don't have i3wm, such as the compton config and the rofi config.
**Note**
  - `$mod` key is `Mod1` *(Alt on most keyboards)*
    - change this to `Mod4` for Windows key on most keyboards
  - *capslock* is configured to act as backspace
    - delete *line 221* in the [config](config) file if you don't want this admittedly odd configeration
  - the i3wm default **j-k-l-;** movement keys are configured to the more Vim-familiar **h-j-k-l**

## Examples

> Screenshot of window manager on dual screen setup

![Screenshot](.images/Screenshot.png "Colourful!")

> launching FireFox in rofi

![Screenshot](.images/rofi.png "Launching time!")

## Requirements
The *config* file references the following programs:
  - [i3blocks](https://github.com/vivien/i3blocks)
    - *a feed generator for status bars*
      - required for the status bar
      - `i3blocks.conf` is the associated config file
  - [Compton](https://github.com/chjj/compton)
    - *a compositor for X11*
      - required for blur effect on windows
      - *bonus* works well at fixing screen tearing issues
  - [Rofi](https://github.com/davatorium/rofi)
    - *a window switcher, application launcher and dmenu replacement*
      - required for launching applications
The following programs are referenced in the *config* file as a shortcut
  - [Ranger](https://github.com/ranger/ranger)
    - file manager for the console
  - amixer
    - volume control
  - Firefox
  - Chrome

## Key Bindings

  | Key                                | Purpose                                                                             |
  | ---                                | -------                                                                             |
  | $mod + (1-9,0)                     | Switch to workspaces with number 1-10                                               |
  | $mod + Shift + (1-9,0)             | Move the container to the workspaces with number 1-10                               |
  | $mod + h (j, k, l)                 | focus left (down, up, right) window                                                 |
  | $mod + Shift + h (j, k, l)         | move focused window left (down, up, right)                                          |
  | $mod + r , (h, j, k, l)            | enter resize mode , (shrink width, grow width, shrink height, grow height)          |
  | $mod + Return                      | terminal                                                                            |
  | $mod + Shift + r                   | Restart I3 inplace                                                                  |
  | $mod + Shift + e                   | exit i3 (logs you out of your X session)                                            |
  | $mod + r                           | Activate resize mode                                                                |
  | $mod + space                       | Change focus between tiling and floating windows                                    |
  | $mod + Shift + space               | Toggle floating status of the focused container                                     |
  | $mod + a                           | focus the parent container                                                          |
  | $mod + d                           | focus the child container                                                           |
  | $mod + e                           | Toggle the layout of the focused container                                          |
  | $mod + h                           | Split the current container horizontally                                            |
  | $mod + v                           | Split the current container vertically                                              |
  | $mod + f                           | Fullscreen mode for the focused container                                           |
  | $mod + q                           | Lock the system                                                                     |
  | Middle Mouse Button                | Kill the focused window                                                             |
  | $mod + shift + q                   | Kill the focused window                                                             |
  | $mod + shift + x                   | lock computer                                                                       |
  | $mod + i                           | launch Firefox                                                                      |
  | $mod + m                           | mute                                                                                |
  | $mod + ,                           | decrease volume                                                                     |
  | $mod + .                           | increase volume                                                                     |
  | $mod + /                           | max volume                                                                          |
  | $mod + Delete                      | shutdown                                                                            |
  | $mod + End                         | reboot                                                                              |
  | $mod + Page Down                   | exit i3                                                                             |

## Setup

**Backup your existing i3 config :)**

    git clone https://github.com/Alex0Blackwell/i3wm.git
    cd dotfiles/
    mv .config/* ~/.config

Install [dependencies](#requirements)

**Credits**
  - The rofi config is based on the one done (here)[https://github.com/mustaqimM/dotfiles/tree/master/.config/rofi] by (Mustaqim Malim)[https://github.com/mustaqimM].

## License
Licensed under the [MIT](LICENSE) license.
