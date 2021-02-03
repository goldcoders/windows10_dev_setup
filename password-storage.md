# How To Use Pass Unix in windows 10 Powershell and QTPass

## requirements
- wsl arch
- powershell
- yay on wsl arch (optional)
- pacman on arch

## Inside powershell

`mkdir .password-store`

## Inside arch wsl

- Install pass and pass-otp

`yay pass` or with pacman `sudo pacman -S pass`

`yay pass-otp` or with pacman `sudo pacmand -S pass-otp`

- Change to home directory

`cd ~`

- link windows folder to linux folder

`ln -s /mnt/Users/$YOURUSERNAME/.password-store .password-store`



## on your powershell script create a new function called pass

- open powershell profile

`code $PROFILE`

- add this

`function pass {arch run pass $args}`

## Pass Init

- change directory inside arch wsl

`cd ~/.password-store`

- initialize pass

`pass init <GPG-ID>`
  
- initialize git

`pass git init`

`pass git add .`

`pass git commit -m "init"`



## Install QtPass

- assuming you have chocolatey package manager in windows 10 run this command

`sudo choco install qtpass`

- open qtpass

- Find gpg command

`Get-Command gpg`

- if gpg is not found try to install it

`sudo choco install Gpg4win`

- Add the File .exe path to Qtpass

- Find git command

`Get-Command git`

- If git is not installed try to install it

`sudo choco install git`

- Add the File .exe path to Qtpass

- add this path to QtPass 

`%USERPROFILE%\.password-store`

- Since no pwgen command is available in windows

```js
// You can either create a .bat file and link that to pwgen counter part in windows like the pass command

// You can always set up `password generation` in Qtpass with the characters you want to use and max lenght

ie: max length = 18

characters: ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz1234567890~!@#$%^&*()_-+={}[]|:;<>,.?

// Try adding new Pass Either with Qtpass or powershell pass function both will work :)
```
