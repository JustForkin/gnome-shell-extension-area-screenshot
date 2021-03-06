gnome-shell-extension-area-screenshot
=====================================

gnome-shell-extension-area-screenshot is a simple extension for creating
screenshots of a specific area on your screen.

Installation
------------

To install the extension, clone this repository and symlink the directory
"area-screenshot@dasprids.de" into "~/.local/share/gnome-shell/extensions/".
Then restart gnome-shell (&lt;Alt&gt; + F2 and enter "r"), open
gnome-tweak-tool and enable the extension.

Configuration
-------------

By default, this extension is configured to work with the keybinding
&lt;Super&gt; + Print. You can change this binding via gsettings, although
a configuration tool will be added soon. When you are not installing the
extension via via https://extensions.gnome.org, you have to compile the
gschema file manually.

Usage
-----

When you hit &lt;Super&gt; + Print now, you can select an area on your screen
with your mouse. After releasing your mouse, a new screenshot will be saved in
your local "Pictures" directory with the current timestamp. You can also take
a screenshot of a single window by simply clicking on it.

When taking an area screenshot, you can set a timer to be able to open context
menus and such, which can't usually be captured. To set the timer, simply press
the numbers 1 to 9 on your keyboard to define the countdown. The timer will
appear in the bottom left of your screen. After making your selection, it will
count down to zero. Pressing 0 on your keyboard will deactivate the timer.

Advanced usage
--------------

This extension allows you to process screenshots automatically after taking
them. For this purpose, it checks for an executable in the directory
"~/bin/area-screenshot-post". If this file exists, it will be executed with
the absolute filename of the generated screenshot as argument.

An example for automatically uploading taken screenshots can be found in the
examples directory.
