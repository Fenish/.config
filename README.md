# My Hyprland dotfiles

## Installed tools

- Walker
- Waybar
- Dolphin
- Alacritty
- Wlogout
- Waypaper
- Swww
- Hyprpicker
- Wl-clipboard
- Gdm
- Pavucontrol
- Nerd fonts
- Zsh

## Install packages

```sh
yay -S walker-bin waybar dolphin alacritty wlogout waypaper swww hyprpicker wl-clipboard gdm pavucontrol nerd-fonts
```

## Hyprland plugins

- Hy3

```sh
hyprpm update
hyprpm add https://github.com/outfoxxed/hy3
```

## Install font

```sh
sudo pacman -S nerd-fonts
sudo cp fonts/Feather.ttf /usr/share/fonts/TTF/
```

## Apply all dotfiles

```sh
sudo mv . ~/.config
reboot
```

## Zsh settings

### Install starship

```sh
curl -sS https://starship.rs/install.sh | sh
```

### Install oh-my-zsh

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### 3rd party plugins

```sh
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

git clone "https://github.com/MichaelAquilina/zsh-autoswitch-virtualenv.git" "$ZSH_CUSTOM/plugins/autoswitch_virtualenv"

git clone git@github.com:zdharma-continuum/history-search-multi-word.git
```

### Enable zsh plugins

~/.zshrc

```sh
eval "$(starship init zsh)"
export STARSHIP_CONFIG=~/.config/starship/starship.toml

plugins=(git sudo zsh-autosuggestions zsh-syntax-highlighting starship autoswitch_virtualenv history-search-multi-word)
```
