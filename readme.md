# Setting up new machine

## ZSH

```shell
sudo dnf install zsh
sudo chsh -s $(which zsh)
```

## Fonts and Theme

```shell
sudo dnf install powerline powerline-fonts
ls /usr/share/powerline/zsh/powerline.zsh
echo $SHELL
echo $ZSH_CUSTOM
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
mkdir -p ~/.local
cd ~/.local
git clone --filter=blob:none https://github.com/ryanoasis/nerd-fonts
cd nerd-fonts
./install.sh
ls ../share/fonts/NerdFonts
reboot
```

## ZSH Theme

```shell
omz theme list
omz theme set powerlevel10k/powerlevel10k
vim ~/.zshrc
p10k configure
```

## ZSH Plugins

```shell
omz update
omz plugin list
omz plugin info fzf
omz plugin load fzf
omz plugin enable fzf
omz plugin disable fzf
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
omz plugin enable zsh-autosuggestions
omz plugin enable zsh-syntax-highlighting
```

## Google Chrome

```shell
sudo dnf install fedora-workstation-repositories
sudo dnf config-manager --set-enabled google-chrome
sudo dnf install google-chrome-stable
reboot
```

## Git, GitHub, and dot-files

```shell
sudo dnf install gh
mkdir Projects
cd Projects
gh auth login
gh repo clone ebelin/dotfiles
cd dotfiles
```
