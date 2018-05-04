# LUCI Color Scheme

[NetApp](https://www.netapp.com) created [LUCI](http://luci.netapp.com) as a "Library for User-Centered Interfaces". This is my adoption of LUCI's color theme for the macOS Terminal.app, VIM and more.

## ANSI to LUCI color mapping

More information about the colors used for the LUCI Design System are described in more detail [here](http://luci.netapp.com/visual-language/color.html). This table shows the mapping I used.

| ANSI Color         | LUCI Color                       |
| -----------------: | :--------------------------------|
| Black (0)          | #000000 (Black)                  |
| Red (1)            | #DA1E21 (error-primary)          |
| Green (2)          | #498128 (success-primary)        |
| Yellow (3)         | #F88400 (warning-primary)        |
| Blue (5)           | #0067C5 (NetApp Blue)            |
| Magenta (6)        | #9F82F1 (color-10)               |
| Cyan (7)           | #01ADBD (color-5)                |
| White (8)          | #F6F6F6 (background-color-light) |
| Bright Black (0)   | #454545 (background-color-dark)  |
| Bright Red (1)     | #FF4548 (error-chart)            |
| Bright Green (2)   | #6FC13E (success-chart)          |
| Bright Yellow (3)  | #FFAC00 (warning-chart)          |
| Bright Blue (5)    | #1E4A93 (hover)                  |
| Bright Magenta (6) | #4FAAFF (focus)                  |
| Bright Cyan (7)    | #7BD8E1 (color-4)                |
| Bright White (8)   | #FFFFFF (White)                  |

## Installation

Clone this repository to any directory you want.

### Terminal.app

Import 'Luci.terminal' to your macOS Terminal.

### CLICOLORS, LSCOLORS and a colorful prompt

Add `export CLICOLOR=1` and `export LSCOLORS=axfxcxdxbxegedabagacad` to your bash profile.

```shell
echo 'export CLICOLOR=1' >> ~/.bash_profile
echo 'export LSCOLORS=axfxcxdxbxegedabagacad' >> ~/.bash_profile
```


```shell
export PS1="\[\033[00m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\] \$ "
```


#### Understanding LSCOLORS

| Attribute                                         | Foreground color | Background color |
|--------------------------------------------------:|:----------------:|:----------------:|
| directory                                         | a (Black)        | x (Default)      |
| symbolic link                                     | f (Magenta)      | x (Default)      |
| socket                                            | c (Green)        | x (Default)      |
| pipe                                              | d (Yellow)       | x (Default)      |
| executable                                        | b (Red)          | x (Default)      |
| block special                                     | e (Blue)         | g (Cyan)         |
| character special                                 | e (Blue)         | d (Yellow)       |
| executable with setuid bit set                    | a (Black)        | b (Green)        |
| executable with setgid bit set                    | a (Black)        | g (Cyan)         |
| directory  writable to others, with sticky bit    | a (Black)        | c (Green)        |
| directory  writable to others, without sticky bit | a (Black)        | d (Yellow)       |

|  Code  | Meaning (color)                           |
|:------:|-------------------------------------------|
|   a    | Black                                     |
|   b    | Red                                       |
|   c    | Green                                     |
|   d    | Brown                                     |
|   e    | Blue                                      |
|   f    | Magenta                                   |
|   g    | Cyan                                      |
|   h    | Light Grey                                |
|   A    | Bold black, usually shows up as dark grey |
|   B    | Bold red                                  |
|   C    | Bold green                                |
|   D    | Bold brown, usually shows up as yellow    |
|   E    | Bold blue                                 |
|   F    | Bold magenta                              |
|   G    | Bold cyan                                 |
|   H    | Bold light grey; looks like bright white  |
|   x    | Default foreground or background          |
