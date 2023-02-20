#Bash Preferences

```
vim .bash_profile
```

Append the following code to the bottom of the  bash profile.

```bash
#CURRENT GIT BRANCH IN PROMPT
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}

#CUSTOM BASH ESTTINGS
export PS1="\u@\h:\W\[\033[32m\]\$(parse_git_branch)\[\033[00m\] \n$ "
export CLICOLOR=1
export LSCOLORS=ExFxBxDxCxegedabagacad
alias ls='ls -Gh'

```

