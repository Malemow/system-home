# Man-home Not Finished

---

## Install Package

### Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew --version
```

### Terminal & Shell

1. Install iterm2

````zsh
brew install iterm2

2. Install zsh oh-my-zsh

```zsh
brew install zsh zsh-completions
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
````

3. Install Powerlevel10k

```zsh
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

4. Install Font
   > use Hack Nerd Font

- [Nerd Theme](https://www.nerdfonts.com/font-downloads)

5. Set Zsh Theme Powerlevel10k

```zsh
vim ~/.zshrc
```

- set ZSH_THEME="powerlevel10k/powerlevel10k"
- command: soruce ~/.zshrc
- set setting for p10k command: p10k configure

### Install plugin

- Terminal Plugin
  - zsh-autosuggestion
  - zsh-syntax-highlighting
  - btop
  - eza
  - fzf
  - ripgrep
- [Item2 Theme](https://iterm2colorschemes.com/)
  - tokyonight

```zsh
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
brew install btop eza fzf ripgrep
```

2. Replace

```
# bak
git clone --branch mac https://github.com/Malemow/system-home.git ~/mac-setting

mv ~/.zshrc ~/.zshrc.bak
mv ~/.p10k.zsh ~/.p10k.zsh.bak

mv ~/mac-setting/.zshrc ~/
mv ~/mac-setting/.p10k.zsh ~/
mv ~/mac-setting/.gitconfig ~/
mv ~/mac-setting/.gitmessage.template ~/

mkdir -p ~/.config/eza/
mv ~/mac-setting/theme.yml ~/.config/eza/

source ~/.zshrc
```

### Vim

- Install Neovim

```zsh
brew install neovim vim
brew install --HEAD utf8proc

git clone https://github.com/Malemow/nvim-lazyvim.git ~/.config/nvim
```

## Package

### Rust

```zsh
brew install rust
brew install rustup-init
rustup-init
rustup component add rust-analyzer
```

### Nvm

```zsh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash
. ~/.zshrc

nvm install 18
nvm use 18
```

### [git-cz](https://github.com/streamich/git-cz)

```zsh
npm install -g git-cz # 然後新增 ~/changelog.config.js
mv ~/mac-setting/changelog.config.js ~/
```
