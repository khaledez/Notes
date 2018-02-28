# Shell

I use `zsh` as the default shell, here is part of `.zshrc` config:

```
# case-insensitive completion
zmodload -i zsh/complist
zstyle ':completion:*' matcher-list 'm:{a-zA-Z-_}={A-Za-z_-}' 'r:|=*' 'l:|=* r:|=*'

# Antigen configuration lines
source /usr/local/share/antigen/antigen.zsh

antigen use oh-my-zsh

antigen bundle git
#antigen bundle pip
#antigen bundle command-not-found
antigen bundle brew

antigen bundle zsh-users/zsh-syntax-highlighting

antigen theme agnoster

antigen apply
# End of Antigen configuration
```
