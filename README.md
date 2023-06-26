# My .files
This repository is supposed to be a backup of my (most important) configuration files just in case my computer dies.
Feel free to take inspiration from these and modify them to your liking - I've made them easy to edit.

### Outline
- **Theming**
  - userChrome
  - simplebarrc
- **Window Management**
  - yabairc
  - skhdrc

&nbsp;

## Theming

#### userChrome.css
This Firefox configuration converts the top tab and address bar into one so theres more space for the webpage.
- Looks better if you remove your toolbar items
- Does not work on Windows

![userChrome_example](https://github.com/peterdev22/dotfiles/assets/95014170/d5f40ce4-a541-4c23-90e8-8a330ddaa21a)

&nbsp;

#### simplebarrc
[simple-bar](https://github.com/Jean-Tinland/simple-bar) is a menu bar replacement that uses [Übersicht](https://github.com/felixhageloh/uebersicht). I've included a config file which you can put into your `~/.simplebarrc`. You can then get it into simple-bar by enabling the 'External config file' setting - a import button will appear and you can use that to import the config.

**NOTE: Things will look weird before you add the custom theme.**

To import the custom theme, go to `/lib/styles/themes` and add the `simplebartheme.js` file to the folder. Make sure to reference it in the `themes.js` file! (Code below)

_Line 23 ->_ ```import * as PeterBlue from "./themes/simplebartheme.js";```

_Line 48 ->_ ```PeterBlue: PeterBlue.theme``` 

Now go to the themes tab in setting and select 'Peter Blue', and you're done!

![simplebar_example](https://github.com/peterdev22/dotfiles/assets/95014170/7024fb3a-35c4-46c7-881e-54c53e1d5720)

&nbsp;

## Window Management

#### yabairc
I use [yabai](https://github.com/koekeishiya/yabai) for tiled window management on MacOS. My config file is nice and simple and includes padding but you can easily edit this file for yourself!

&nbsp;

#### skhdrc
[skhd](https://github.com/koekeishiya/skhd) is used in conjunction with yabai to allow the keyboard to control window positioning (you're probably going to want to control via kb).
This file uses the hyper key (`ctrl + alt + cmd`) for moving windows around. Use the hyper key plus `shift` to move the window to another display and use `t` to toggle a tiled window, `e` to balence tiles, `f` for fullscreen.

**The controls are `ctrl + alt + cmd` and...**
- `arrows` for swappping windows around
- `j, k, h, l` for cutting windows around
- `shift + left` or `right` for changing displays
- `t` to toggle tile for a window
- `e` to balence tiled windows
- `f` for fullscreen
- `s, w, a, d` for switching focus
