
### paste it on .bashrc or .profile
```
parse_git_branch(){
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}

PS1="\[\e[01;32m[\u@\h|\W]:\[\033[00m\]\w\[\033[31m\]\$(parse_git_branch)\[\033[00m\]\$ "

```
