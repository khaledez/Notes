# Shell

I use `zsh` as the default shell, here is part of `.zshrc` config:

```zsh
# case-insensitive completion
zmodload -i zsh/complist
zstyle ':completion:*' matcher-list 'm:{a-zA-Z-_}={A-Za-z_-}' 'r:|=*' 'l:|=* r:|=*'

# Antigen configuration lines
source /usr/local/share/antigen/antigen.zsh

antigen use oh-my-zsh

antigen bundle git
if [[ `uname` == 'Darwin' ]]; then
  antigen bundle brew
fi

antigen bundle zsh-users/zsh-syntax-highlighting

antigen theme agnoster

antigen apply
# End of Antigen configuration
```
