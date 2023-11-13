# MacOS Ansible Playbook

This is my personal playbook for setting up a fresh install of MacOS.

## How to use

First of all, you'll need to install `XCode` and `Homebrew` manually.

```bash
xcode-select --install
bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

export PATH="/usr/local/bin:/usr/local/sbin:~/bin:$PATH"

Then, you need to install `ansible` via brew.

```
brew update
```

```
brew install ansible
```

Now, you can run the entire playbook or a certain tag via `-t <tagName>`

```
ansible-playbook playbook.yml
```

Check all the applications on <add file here>

Sadly, some changes need to be done manually. They are listed down below

### iTerm2

1. Clone the `Catppuccin` repository from https://github.com/catppuccin/iterm
2. Follow the instructions in [usage](https://github.com/catppuccin/iterm#usage) section to change theme
3. Open Settings -> Profiles -> Default
4. General -> Working Directory -> Reuse previous session's directory
5. Text -> Font -> Anonymous Pro
6. Text -> Font Size -> 14

### Finder

Finder

    Finder -> Preferences
        General -> Show these on the desktop -> Select None
            I try to keep my desktop completely clean.
        General -> New Finder windows show -> Home Folder
            I prefer to see my home folder in each new finder window instead of recent documents
        Advanced -> Show all filename extensions -> Yes
        Advanced -> Show warning before changing an extension -> No
        Advanced -> When performing a search -> Search the current folder
    View
        Show Status Bar
        Show Path Bar
        Show Tab Bar


### Dock

System Preferences

    Dock & Menu Bar
        Size -> Small as possible
        Position on screen -> Right
        Automatically hide and show the Dock -> Yes


asdf plugin add nodejs https://github.com/asdf-vm/asdf-nodejs.git
asdf install nodejs latest
asdf global nodejs latest
