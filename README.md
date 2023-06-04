# My .files
This repository is supposed to be a backup of my (most important) configuration files just in case my computer dies. Anyone is free to use these for themselves as this is a public repo.
I recommened you take inspiration from these but i'll be impressed if you can use these for yourself as config files are a very personal thing. (The Firefox theme is pretty cool though so you can definitely try using that!)

### Outline
- **Theming**
  - userChrome
- **Window Management**
  - yabairc
  - skhdrc

&nbsp;

## Theming

#### userChrome.css
This Firefox configuration converts the top tab and address bar into one so theres more space for the webpage.
- Removing as many buttons as possible from your toolbar makes it look a lot better
- Does not work on Windows

![userChrome_example](https://github.com/peterdev22/dotfiles/assets/95014170/d5f40ce4-a541-4c23-90e8-8a330ddaa21a)

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
