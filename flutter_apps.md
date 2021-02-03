# Set Up Flutter in Windows 10 the Right Way

## basic requirements

- `choco`

## install dart-sdk

sudo choco install dart-sdk

## to enable pub command in the system add to env path

`C:\tools\dart-sdk\bin`

`%USERPROFILE%\AppData\Local\Pub\Cache\bin`

## Install flutter version manager

`pub global activate fvm`

## Install flutter 

`fvm install stable`

`fvm install beta`

`fvm install dev`


## Set Default Flutter Version

`fvm use stable --global`

## add sdk command in powershell

- to set flutter sdk per project add `sdk` function in powershell

```ps1
function Update-FlutterSDK { pub global run fvm:main use $args}
Set-Alias -Name sdk -Value Update-FlutterSDK -Option AllScope
```

Note: you can use pub global run fvm:main use `version` but this shortcut command is time saver

## Set up your VS code settings to use different flutter sdk version

`code $env:appdata\Code\User\settings.json`

add the following line

```json
"dart.flutterSdkPaths": [
    "$USERPROFILE\\fvm\\versions\\stable",
    "$USERPROFILE\\fvm\\versions\\beta",
    "$USERPROFILE\\fvm\\versions\\dev",
  ],
```
## Changing SDK on vscode

- type `ctrl + p` then type `Flutter: Change SDK` then enter

- choose your sdk version suited for you project

