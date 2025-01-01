# DOSAlias
script for adding some  common DOS commands as aliases to bash

## Installation
to install and run this script run the following commands \
`git clone https://github.com/alphanumericcharter/DOSAlias/` \
`cd DOSAlias` \
`chmod +x dosalias`  -marks the file as executable \
`./dosalias`   -begins setup

During installation you will be asked if you have a .bash_aliases file you want to add the new aliases to. \
Choose yes if you do have that file and want to write the aliases to it. \
Choose no if you don't have that file _or_ if you don't want to write to it. 
Choosing no will create a file called .dosaliases and add it to .bashrc

## Uninstallation
### To remove the new aliases if you have chosen yes during the installation: 
`nano ~/.bash_aliases` \
then remove the following lines:
```
alias cls='clear' 
alias cd..='cd ..' 
alias copy='cp' 
alias ver='uname -a'  
alias help='man'
``` 
### To remove the new aliases if you have chosen no during the installation:
`rm ~/.dosaliases` \
`nano ~/.bashrc` 
\
then remove: 

```
if [ -f ~/.dosaliases ]; then
            . ~/.dosaliases
        fi
```
