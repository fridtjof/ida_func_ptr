# ida_func_ptr for IDA Pro

<p align="center">
<img alt="plugin" src="screenshots/main.png"/>
</p>

## Overview

ida_func_ptr is a small utility plugin for [IDA Pro](https://www.hex-rays.com/products/ida/).
The plugin allows you to copy C function pointer definitions of functions through the context menus.

For example the screenshot above will copy the following text onto the clipboard:

```c
int(* PCMain_cpp_PlayPreIntro)() = (int(*)())(0x00646FF0);
void(* PCMain_PlayIntroLogos)() = (void(*)())(0x00647250);
```

## Installation

### Requirements

You will need to have PyQT5 in the Python install used by IDA.
Running `pip3 install pyqt5` in an elevated command prompt should work.
If it doesn't, the Python installation that comes first in your PATH is probably not the one IDA uses.
In that case, you're on your own, sorry :/

Install Prefix into the IDA plugins folder.

- Copy the `ida_func_ptr.py` file into the IDA plugins folder
    - On Windows, the folder is at `%APPDATA%\Hex-Rays\IDA Pro\plugins`
    - On MacOS, the folder is at `$HOME/.idapro/plugins`
    - On Linux, the folder may be at `$HOME/.idapro/plugins`

The plugin has only been tested on IDA Pro 7.5 for Windows.
