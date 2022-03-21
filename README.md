# Using git-auto-complete for zsh users
Source code: https://github.com/git/git/tree/master/contrib/completion
## Objective:
To use git command + tab and it shows suggestions, just like when you cd + tab then you get list of files/directories in your current directory.

## Installation
In your terminal:
1) Download git-completion.bash to your local
```
curl https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash -o ~/.git-completion.bash
```
2) Create a directory for git-completion.zsh
```
mkdir ~/.zsh/
```

3) Download git-completion.zsh to your local (inside ~/.zsh/) and rename it to _git.zsh
```
curl https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.zsh -o ~/.zsh/_git.zsh
```
4) Copy this to ~/.zshrc
```
fpath=(~/.zsh $fpath)
autoload -U compinit && compinit
zstyle ':completion:*:*:git:*' script ~/.git-completion.bash
```
5) Restart your terminal or `source ~/.zshrc`
