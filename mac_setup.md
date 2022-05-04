### Install brew
```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Install git
```
$ brew install git
```

### Fetch the dotfiles repository
```
$ cd
$ mkdir -p work/github.com
$ cd work/github.com
$ git clone https://github.com/savula15/dotfiles.git
```

### Install and setup iterm2
Manual steps
- Install latest iterm2 from https://iterm2.com/downloads.html
- Point iterm2 to read/write config to ~/work/github.com/dotfiles/iterm2-config
- This can be done under iTerm2 > Preferences > General > Preferences.

### Install Oh-My-Zsh and powerlevel10k theme
```
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

```
$ git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

- Set ` ZSH_THEME="powerlevel10k/powerlevel10k" ` in ` ~/.zshrc `
- Optional: If config wizard doesn't trigger automatically, run ` p10k configure `

### Install dotfiles
```
$ cd ~/work/github.com/dotfiles
$ ./bin/install_config.sh
```

### Ssh configuration
- Generate ssh key
- Add ssh keys etc to github.com etc

### Fuzzy finder
```
$ brew install fzf
$ /usr/local/opt/fzf/install
```

### Miscellaneous 

```
$ brew install tmux
$ brew install coreutils
$ brew install clang-format
$ brew install golang
```

### Increase key repeat rate
```
defaults write -g InitialKeyRepeat -int 15 # normal minimum is 15 (225 ms)
defaults write -g KeyRepeat -int 1 # normal minimum is 2 (30 ms)
```

### Setup NeoVim

```
$ brew install neovim
$ python -m pip install --user --upgrade pynvim
```

Also, after opening a go file, one will need to execute :GoInstallBinaries
to get various binaries that are needed for vim-go plugin to properly
function.


