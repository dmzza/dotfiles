# dotfiles

## Getting Started
1. Clone this repo into `~/Developer`
2. `ln -s ~/Developer/dotfiles/.zshrc ~/.zshrc`


When you need a new dotfile in the home directory, follow this process to move it into
this repository before making changes to it.

Suppose the name of the new dotfile is `.config` and this repo lives in `~/Developer/dotfiles`

1. `mv ~/.config ~/Developer/dotfiles/.config`
2. `ln -s ~/Developer/dotfiles/.config ~/.config`
3. To verify that the link has been made: `ls -a ~`
4. Commit the new file to the repo

Then you can make changes to the file and commit each change to document it. 

## Installing Homebrew
The latest instructions are available on [brew.sh](https://brew.sh)
This is just a summary of the steps:
1. From anywhere, run:
```
xcrun git clone https://github.com/homebrew/brew.git /tmp/homebrew
[[ $(arch) == i386 ]] && sudo mv /tmp/homebrew /opt/brew
[[ $(arch) == arm64 ]] && sudo mv /tmp/homebrew /opt/homebrew
```
2. 
```
[[ -d /opt/homebrew/bin ]] && echo "/opt/homebrew/bin" | sudo tee /etc/paths.d/10-brew
[[ -d /opt/brew/bin ]] && echo "/opt/brew/bin" | sudo tee /etc/paths.d/20-brew
```
3. Close and reopen your Terminal app so your shell picks up the addition to the `$PATH`.
4. `brew update --force`

## Installing CocoaPods
The .zshrc file is already setup to support sudo-less installation of gems.
1. `gem install cocoapods`
There is no step two.

## Installing Oh My Zsh
_Coming soon_
