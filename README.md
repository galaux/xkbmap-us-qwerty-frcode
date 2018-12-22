This is an X keyboard configuration file based on a 100% standard US Qwerty
that also provides French punctuation along with several frequently used
programming symbols. These supplementary characters are accessed through
the Alt and Alt+Shift keys. Have a look at the file to get a representation
of the added keys.

It can be installed by simply putting the configuration file in directory
`/usr/share/X11/xkb/symbols/`. To load it, run `setxkbmap us_qwerty_frcode`
or put the following lines in a file such as
`/etc/X11/xorg.conf.d/00-keyboard.conf`:

```
Section "InputClass"
        Identifier "system-keyboard"
        MatchIsKeyboard "on"
        Option "XkbLayout" "us_qwerty_frcode"
        # Optional: Caps Lock key becomes Ctrl
        Option "XkbOptions" "ctrl:nocaps"
EndSection
```

Files:

- `us_qwerty_frcode`: X keyboard configuration file
- `PKGBUILD`: source package for Arch Linux
- `README.MD`: this file
