# macos_terminal 💻
[iTerm2](https://iterm2.com/) configuration for macos

# Prerequisites 🚦
- [homebrew](https://brew.sh/) `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
- [iTerm2](https://iterm2.com/) `brew install --cask iterm2`
- [git](https://git-scm.com/download/mac) `brew install git`

# Install Steps (in [iTerm2](https://iterm2.com/)) 🗒️

### 1. Zsh
```
brew install zsh
chsh -s /opt/homebrew/bin/zsh
chsh -s /usr/local/bin/zsh
```

### 2. [ohmyzsh](https://github.com/ohmyzsh/ohmyzsh)
```
brew install curl
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
source ~/.zshrc
```

### 3. [powerlevel10k](https://github.com/romkatv/powerlevel10k)
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
- add `export ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`.

### 4. [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
```
brew install zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
- add `zsh-autosuggestions` to `plugins` in `~/.zshrc`.

### 5. [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
```
brew install zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
echo "source ${(q-)PWD}/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc
source ./zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```

### 6. Refresh
```
source ~/.zshrc && zsh
```
