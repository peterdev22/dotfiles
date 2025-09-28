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
    - skhdrc
    - skhdrc-new

&nbsp;

## Theming

#### userChrome.css
This Firefox configuration converts the top tab and address bar into one so theres more space for the webpage.
- Looks better if you remove your toolbar items
- Does not work on Windows
- Tabs will resize to fit the space, but it can get annoying with >10 tabs
- Themes:
  - Firefox Color - Catppuccin Mocha: [Link](https://color.firefox.com/?theme=XQAAAAJJBAAAAAAAAABBqYhm849SCicxcUcPX38oKRicm6da8pFtMcajvXaAE3RJ0F_F447xQs-L1kFlGgDKq4IIvWciiy4upusW7OvXIRinrLrwLvjXB37kvhN5ElayHo02fx3o8RrDShIhRpNiQMOdww5V2sCMLAfedxuJKgKfYC0MgwphhfNqnG95yk9dbmoYTESCyaIPra1KFX29L9nLE5glNIsTm6faWK-3xbCKWAqSjZFO_VM9Wj_BYadsw2D1O60ylxFuTgUzlM3hW73I74s39LWAtaQcBMFUkmt-_Jj0QeC05EQAu-gaTkZE97kimAaYQiVW5Sqt9_GtXx3o-lg1164JYHZ9a-E2aGDmOLV6jVF4tFX-FFsc1MvLSUqqD-tWd_EUfqKap7GtNqx7wBhQDRqJqxWbRGcqxWBco0ZLIbQmlH_hli2TlnusOmkBgg9I_Bkyh6JsdNGHnTDgxnRr2lmwXKgr31f1qGwK9bRTJXmvTZFAayMxCSrkFMQmYNuz13yQbrWa610YWjML7YErRZua7-upk5E3uKlgt0bYUuQyuQrx-RpaGQQWpRM-sTZxPdipi-dzPXW2v_-3cxUg)
  - Firefox Color - Black (theme used in the image below): [Link](https://color.firefox.com/?theme=XQAAAALNAQAAAAAAAABBqYhm849SCia-yK6EGccwS-xMDPrv2Sw6Caq-qy5QgqeHG4K15H9ICig-sRkmwHSgkvNfRgb2eiAvUQOJakLbb3uF3IgUz-J1EU98VivSeSjHyhxtbiv__Eq4aMsHJWFQtL0d3qwZciJQvOorcFd30VaDzDXWOYPHZr2JnvMWcBoLCEZuU58rkkWK0revnEJm0PrBBezwaos3-X0WxCjXuSw_Z8RCaQxrnoPJSkHmESwD_4A4hQ2uWaRAywcMcFDeJyiqvdChxFUVN4epoV-O2bGHAI8Vru6CAfK8m7PrBmzyXUkhrU8d167M8e8pfgcgegfke61nABH29W75BweHn_ygo60)
  - Any theme from [Firefox add-ons](https://addons.mozilla.org/en-US/firefox/themes/) should work fine.

<img width="4320" height="2784" alt="userchrome old example" src="https://github.com/user-attachments/assets/085ec31d-4c8e-4f32-828a-0e5e2c4e5290" />

#### userChrome.css (NEW VERSION)
My new userChrome is designed for vertical tabs and it also leans into more of a rounded look. This userChrome does not transform the urlbar so it is **a lot** more responsive to window resizing compared to my last userChrome.
- Themes used:
  - [Adaptive Tab Bar Colour](https://github.com/easonwong-de/Adaptive-Tab-Bar-Colour) - works well with this. Makes Firefox recolour depending on the website (similar to Safari).
  - Firefox Color - Black (same one linked above).

<img width="4320" height="2784" alt="userchrome new example" src="https://github.com/user-attachments/assets/c90a75b1-3174-4cd7-b4d1-7072247ca2a6" />

&nbsp;

#### simplebarrc
[simple-bar](https://github.com/Jean-Tinland/simple-bar) is a menu bar replacement that uses [Übersicht](https://github.com/felixhageloh/uebersicht). I've included a config file which you can put into your `~/.simplebarrc`. You can then get it into simple-bar by enabling the 'External config file' setting - a import button will appear and you can use that to import the config.

**NOTE: Things will look weird before you add the custom theme.**

To import the custom theme, go to `/lib/styles/themes` and add the `simplebartheme.js` file to the folder. Make sure to reference it in the `themes.js` file! (Code below)

_Line 23 ->_ ```import * as PeterBlue from "./themes/simplebartheme.js";```

_Line 48 ->_ ```PeterBlue: PeterBlue.theme``` 

Now go to the themes tab in setting and select 'Peter Blue', and you're done!

![simplebar_example](https://github.com/peterdev22/dotfiles/assets/95014170/7024fb3a-35c4-46c7-881e-54c53e1d5720)

>*Note, I don't actually use simplebar anymore but may again in the future. Currently I work with the menu bar hidden to maximise desktop space.*

&nbsp;

## Window Management

#### yabairc
I use [yabai](https://github.com/koekeishiya/yabai) for tiled window management on MacOS. My config file is nice and simple and can include padding but you can easily edit this file for yourself!

&nbsp;

#### skhdrc
[skhd](https://github.com/koekeishiya/skhd) is used in conjunction with yabai to allow the keyboard to control window positioning (you're probably going to want to control via kb).
My setup file uses the hyper key (`ctrl + alt + cmd`) for moving windows around. Two files are included in this repository (I use the `skhdrc-new` version now, but the old file is still included as a backup).

**The controls are `ctrl + alt + cmd` and...**

##### skhdrc - full setup
- `arrows` for swappping windows around
- `j, k, h, l` for cutting windows around
- `shift + left` or `right` for changing displays
- `t` to toggle tile for a window
- `f` for fullscreen
- `q, w, a, s` for switching focus
- `z, x` for switching focus between displays

##### skhdrc-new - simple, no focus controls, wasd movement
- `w, a, s, d` for swappping windows around
- `shift + a` or `d` for changing displays
- `f` for fullscreen
- `q` for switching modes between bsp and stack
