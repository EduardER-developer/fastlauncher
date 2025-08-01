# FastLauncher

TUI Application Launcher. Alternative to rofi/wofi

![main windows](https://github.com/probeldev/fastlauncher/blob/main/guides/screenshots/main.png?raw=true)

## Support OS

Linux - Done

Windows - Work in progress

Mac Os - Work in progress

## Examples

### Logout Manager

[Example config](https://github.com/probeldev/fastlauncher/blob/main/guides/examples/logout-manager/cfg.json) 

![Logout manager](https://github.com/probeldev/fastlauncher/blob/main/guides/screenshots/logout-manager.png?raw=true)

### Emoji Select 

[Example config](https://github.com/probeldev/fastlauncher/blob/main/guides/examples/emoji/emoji.json) 

![Emoji select](https://github.com/probeldev/fastlauncher/blob/main/guides/screenshots/emoji-select.png?raw=true)


## Installation

[Full guide for Arch Linux with KDE](https://github.com/probeldev/fastlauncher/tree/main/guides/arch_kde/readme.md)

### Go
Installation

```bash
go install github.com/probeldev/fastlauncher@latest     
```


If you get an error claiming that fastlauncher cannot be found or is not defined, you
may need to add `~/go/bin` to your $PATH (MacOS/Linux), or `%HOME%\go\bin`
(Windows)

Zsh

```bash
echo "export PATH=\$PATH:~/go/bin" >> ~/.zshrc
```

Bash

```bash
echo "export PATH=\$PATH:~/go/bin" >> ~/.bashrc
```

### Nix

```bash
nix profile install github:probeldev/fastlauncher 
```


## Usage 

### All apps from OS

```bash
fastlauncher
```

### Apps from config

```bash
fastlauncher --config ~/script/fast-launcher/cfg.json
```

Example file [cfg.json](https://github.com/probeldev/fastlauncher/blob/main/cfg.json) 

It's launched with the help of window manager. Example hyprland.conf:

```
$terminal = foot
$menu = $terminal -T fast-launcher fastlauncher --config ~/script/fast-launcher/cfg.json
bind = $mainMod, D, exec, $menu


windowrulev2 = float,title:(fast-launcher)
windowrulev2 = pin,title:(fast-launcher)
windowrulev2 = size 1000 600,title:(fast-launcher)
windowrulev2 = center(1), title:(fast-launcher)
```


