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
- The theme used is Catppuccin using Firefox Color: [Link](https://color.firefox.com/?theme=XQAAAAJMBAAAAAAAAABBqYhm849SCicxcUcPX38oKRicm6da8pFtMcajvXaAE3RJ0F_F447xQs-L1kFlGgDKq4IIvWciiy4upusW7OvXIRinrLrwLvjXB37kvhN5ElayHo02fx3o8RrDShIhRpNiQMOdww5V2sCMLAfedxuJLwbcnxN_YEJNRaPz1Sbba3ncrdPQRlNpXIjOuG8-o1VYRaO3ALyE6-1vBDLJKMLAZ1kzPFz1tUhLbRqjsSyEA7fKOhwdVMGn-UD5UdDWJxJeoy-TtBciJAP65dHx2ZOfkh5PEMwlyE0Z4Iu0gE79ZPRglMEBzBPwiLgWmfGdqDN1Cz-ra9DaCmBIwb-AQIz-wAqFZIwxSG8N45ZUveR9kAegDeCbJOMUMGpJ-0KpK95mKNu-2kwNMLv2qkKYy9uHbc2pXwPwj1t_74pdGTyX38hPuOKTW0RpjJAE7N6RfwSn66occ1JSRtaTTS1QZ5pO4mQeaYF2xURmUJ-M0vAlKhXSEhPYP8wPWocVzZdXQ23_ciHGxsrnJ9usa462mlDbUePUhdPUtJRYAuMbYlUTBDqLsFrXMkZIqVr_wEpBjA)

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
- `f` for fullscreen
- `q, w, a, s` for switching focus
- `z, x` for switching focus between displays
