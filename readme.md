# **My Windows Terminl setup**
This is my window Terminal setup.
I did this to save time setting up the Terminal on a new computer and hope it will be helpful to you.
You don't have to adjust all of these. Adapt to your work style.

### **Image Preview**
- Search Directory
![Terminal Screenshot](https://github.com/chinhchin/Windows-Terminal-setup/blob/master/readme-assets/Preview%20Image/terminal%20screenshot%201.png?raw=true)
- list directory with icons and colors.
![Terminal Screenshot](https://github.com/chinhchin/Windows-Terminal-setup/blob/master/readme-assets/Preview%20Image/terminal%20screenshot%202.png?raw=true)
- command suggestion
![Terminal Screenshot](https://github.com/chinhchin/Windows-Terminal-Setup/blob/master/readme-assets/Preview%20Image/terminal%20screenshot%203.png?raw=true)

### **Go to**
- [Version record](./version-record.json)
- See how to run Linux on Windows Terminal [here](https://github.com/chinhchin/WSL-setup.git).

### **Credits**
- Inspiration, list of modules and solution from [craftzdog/dotfiles-public](https://github.com/craftzdog/dotfiles-public.git).

### **OS support**
- Windows 10, 11

### **Contents**
#### 1. [Install and setup Terminal](./readme.md#1-install-and-setup-terminal)
1. [Install font](./readme.md#11-install-font)
2. [Install 2 softwares from Microsoft Store.](./readme.md#12-install-2-softwares-from-microsoft-store)
3. [Setting Terminal](./readme.md#13-setting-terminal)

#### 2. [Install and setup Terminal software](./readme.md#2-install-and-setup-terminal-software)
1. [Install Terminal software](./readme.md#21-install-terminal-software)
2. [Enable Terminal software](./readme.md#22-enable-terminal-software)

#### 3. [Usage of features](./readme.md#3-usage-of-features)
1. [Tab to get command, directory or option suggestion](./readme.md#31-tab-to-get-command-directory-or-option-suggestion)
2. [Right arrow to get command suggestion](./readme.md#32-right-arrow-to-get-command-suggestion-from-history)
3. [Directory jumper](./readme.md#33-jump-directory-by-z)
4. [Search file](./readme.md#34-search-file-directory-list-view-get-from-every-file-and-in-current-directory)
5. [Search command](./readme.md#35-search-command)
6. [Useful shortcuts command](./readme.md#36-useful-shortcuts-command-aliases)

---

## **1. Install and setup Terminal**
### **1.1 Install font.**
First, I have to install Nerd Fonts so that I can display the icons and markers used in programming nicely.

So I use [Caskaydia Cove Nerd Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/CascadiaCode.zip).

And you can see more fonts to get the one that is right for you [here](https://www.nerdfonts.com/).

### **1.2 Install 2 softwares from Microsoft Store.**
1. [Windows Terminal](https://www.microsoft.com/store/productId/9N0DX20HK701)
2. [Powershell](https://www.microsoft.com/store/productId/9MZ1SNWT0N5D)

### **1.3 Setting Terminal**
1. Open Terminal.
2. Open Settings JSON file defualt (Ctrl - Shift - ,).
3. In ["**profiles**"]["**defaults**"] setting JSON file, if your theme is dark replace it with these
```
{
    "colorScheme": "One Half Dark", "cursorShape": "vintage",
    "experimental.retroTerminalEffect": false,
    "font": 
    {
        "face": "CaskaydiaCove NF"
    },
    "opacity": 75,
    "useAcrylic": true
},
```
, but if your theme is light replace it with this
```
{
    "colorScheme": "One Half Light", "cursorShape": "vintage",
    "experimental.retroTerminalEffect": false,
    "font": 
    {
        "face": "CaskaydiaCove NF"
    },
    "opacity": 75,
    "useAcrylic": true
},
```

> **Note**
>
> Don't forget to change font face to your font.

4. In ["**actions**"] setting JSON file  replace it with this
```
[
    {
        "command": 
        {
            "action": "switchToTab",
            "index": 4
        },
        "keys": "ctrl+shift+5"
    },
    {
        "command": 
        {
            "action": "switchToTab",
            "index": 0
        },
        "keys": "ctrl+shift+1"
    },
    {
        "command": 
        {
            "action": "newTab",
            "index": 2
        },
        "keys": "ctrl+alt+3"
    },
    {
        "command": 
        {
            "action": "switchToTab",
            "index": 7
        },
        "keys": "ctrl+shift+8"
    },
    {
        "command": 
        {
            "action": "prevTab"
        },
        "keys": "alt+h"
    },
    {
        "command": 
        {
            "action": "copy",
            "singleLine": false
        }
    },
    {
        "command": "paste"
    },
    {
        "command": "find",
        "keys": "ctrl+shift+f"
    },
    {
        "command": "unbound",
        "keys": "ctrl+v"
    },
    {
        "command": "unbound",
        "keys": "ctrl+insert"
    },
    {
        "command": "unbound",
        "keys": "ctrl+c"
    },
    {
        "command": "unbound",
        "keys": "ctrl+numpad_minus"
    },
    {
        "command": "unbound",
        "keys": "alt+shift+d"
    },
    {
        "command": "unbound",
        "keys": "ctrl+numpad_plus"
    },
    {
        "command": "unbound",
        "keys": "ctrl+plus"
    },
    {
        "command": "unbound",
        "keys": "alt+down"
    },
    {
        "command": "unbound",
        "keys": "alt+left"
    },
    {
        "command": "unbound",
        "keys": "alt+right"
    },
    {
        "command": "unbound",
        "keys": "ctrl+alt+left"
    },
    {
        "command": "unbound",
        "keys": "alt+up"
    },
    {
        "command": "unbound",
        "keys": "shift+insert"
    },
    {
        "command": "unbound",
        "keys": "alt+shift+plus"
    },
    {
        "command": "unbound",
        "keys": "alt+shift+minus"
    },
    {
        "command": "unbound",
        "keys": "win+sc(41)"
    },
    {
        "command": "unbound",
        "keys": "alt+shift+up"
    },
    {
        "command": "unbound",
        "keys": "alt+shift+right"
    },
    {
        "command": "unbound",
        "keys": "alt+shift+left"
    },
    {
        "command": "unbound",
        "keys": "alt+shift+down"
    },
    {
        "command": "unbound",
        "keys": "ctrl+numpad0"
    },
    {
        "command": "unbound",
        "keys": "ctrl+0"
    },
    {
        "command": "unbound",
        "keys": "ctrl+shift+tab"
    },
    {
        "command": "unbound",
        "keys": "ctrl+tab"
    },
    {
        "command": "unbound",
        "keys": "ctrl+shift+vk(255)"
    },
    {
        "command": "unbound",
        "keys": "ctrl+1"
    },
    {
        "command": 
        {
            "action": "switchToTab",
            "index": 2
        },
        "keys": "ctrl+shift+3"
    },
    {
        "command": 
        {
            "action": "switchToTab",
            "index": 3
        },
        "keys": "ctrl+shift+4"
    },
    {
        "command": 
        {
            "action": "switchToTab",
            "index": 4294967295
        },
        "keys": "ctrl+shift+9"
    },
    {
        "command": 
        {
            "action": "splitPane",
            "split": "auto",
            "splitMode": "duplicate"
        }
    },
    {
        "command": 
        {
            "action": "switchToTab",
            "index": 1
        },
        "keys": "ctrl+shift+2"
    },
    {
        "command": 
        {
            "action": "newTab",
            "index": 1
        },
        "keys": "ctrl+alt+2"
    },
    {
        "command": 
        {
            "action": "switchToTab",
            "index": 5
        },
        "keys": "ctrl+shift+6"
    },
    {
        "command": 
        {
            "action": "nextTab"
        },
        "keys": "alt+l"
    },
    {
        "command": 
        {
            "action": "newTab",
            "index": 0
        },
        "keys": "ctrl+alt+1"
    },
    {
        "command": 
        {
            "action": "switchToTab",
            "index": 6
        },
        "keys": "ctrl+shift+7"
    },
    {
        "command": 
        {
            "action": "newTab",
            "index": 3
        },
        "keys": "ctrl+alt+4"
    },
    {
        "command": 
        {
            "action": "newTab",
            "index": 4
        },
        "keys": "ctrl+alt+5"
    },
    {
        "command": 
        {
            "action": "newTab",
            "index": 5
        },
        "keys": "ctrl+alt+6"
    },
    {
        "command": 
        {
            "action": "newTab",
            "index": 6
        },
        "keys": "ctrl+alt+7"
    },
    {
        "command": 
        {
            "action": "newTab",
            "index": 7
        },
        "keys": "ctrl+alt+8"
    },
    {
        "command": 
        {
            "action": "newTab",
            "index": 8
        },
        "keys": "ctrl+alt+9"
    }
],
```

> **Align of the shell's index**
>
> You can align the shell's index for for ease of pressing "*ctrl+alt+(index)*" by Press "**Open JSON file**" button at pane to open file. Then, go to settings.json.profiles.list to edipress "**Open JSON file**" button at pane to open file. Then, go to settings.json.profiles.list to aligh them.

> **Shortcuts**
>
> You can see what each shortcut run what command in Setting in "*Actions*" pane.

5. In (**Settings**) tab of **Windows Terminal**, in "**Appearance**" pane, set "*Use acrylic material in the tab row (requires relaunch)*" to "**On**".

6. Relaunch **Windows Terminal**.

## **2. Install and setup Terminal software**
### **2.1 Install Terminal software**

Type these command in your terminal
> **Note**
>
> If problem about administrator permission occured, type "*sudo*" in front of that command.

1. Install [Scoop](https://scoop.sh/).
```
iwr -useb get.scoop.sh | iex
```

2. Install [Curl](https://curl.se/) and [Jq](https://stedolan.github.io/jq/).
```
scoop install curl sudo jq
```

3. Install [Git](https://git-scm.com/) 
```
winget install -e --id Git.Git
```

4. Install [Neovim](https://neovim.io/)
```
scoop install neovim gcc
```

5. Install [Oh My Posh](https://ohmyposh.dev/)
```
winget install oh-my-posh
```

6. Install [Terminal-Icons](https://github.com/devblackops/Terminal-Icons)
```
Install-Module -Name Terminal-Icons -Repository PSGallery
```

7. Install [Z](https://www.powershellgallery.com/packages/z/)
```
Install-Module -Name z -Force
```

8. Install [PSReadLine](https://docs.microsoft.com/en-us/powershell/module/psreadline/)
```
Install-Module -Name PSReadLine -AllowPrerelease -Scope CurrentUser -Force -SkipPublisherCheck
```

9. Install [PSFzf](https://github.com/kelleyma49/PSFzf)
```
scoop install fzf
Install-Module -Name PSFzf -Scope CurrentUser -Force
```

### **2.2 Enable Terminal software**
1. Type this command in your terminal.
```
cd (your\document\path)
mkdir PowerShell
New-Item -Path $PROFILE.CurrentUserCurrentHost -ItemType File
start $PROFILE.CurrentUserCurrentHost
```

2. Relaunch **Windows Terminal**.

And copy data from this [file](Microsoft.PowerShell_profile.ps1) to your terminal and save.

## **3. Usage of features**
### **3.1 Tab to get command, directory or option suggestion**
1. Type some command.
2. Press "*Tab*" to get suggestion.
3. Type followed by suggestion then, press "*Tab*" again.

![Illustration](https://github.com/chinhchin/Windows-Terminal-setup/blob/master/readme-assets/Usage%20of%20features/1.png?raw=true)

### **3.2 Right arrow to get command suggestion** (from history)
1. Type some command.
2. If it show suggestion of command at right of cursor, press "*Right*" key, if you want to get that command.

![Illustration](https://github.com/chinhchin/Windows-Terminal-setup/blob/master/readme-assets/Usage%20of%20features/2.png?raw=true)

### **3.3 Directory jumper**
1. Type ```z ``` and followed by all directory path or some part of directory path

You can also jump over directory.

![Illustration](https://github.com/chinhchin/Windows-Terminal-setup/blob/master/readme-assets/Usage%20of%20features/3.png?raw=true)

### **3.4 Search file** (Directory list view get from every file and in current directory)

1. Search file by press "*Ctrl-F*".
2. Type directory or file name and choose command by press "*Up*" and "*Down*" key.
3. Press "*Enter*" to select command or press "*Esc*" to cancel.

![Illustration](https://github.com/chinhchin/Windows-Terminal-setup/blob/master/readme-assets/Usage%20of%20features/4.png?raw=true)

### **3.5 Search command**
1. Search command by press "*Ctrl-R*"
2. Type command that you want to use that you've used before and choose command by press "*Up*" and "*Down*"
3. Press "*Enter*" to select command or press "*Esc*" to cancel.

![Illustration](https://github.com/chinhchin/Windows-Terminal-setup/blob/master/readme-assets/Usage%20of%20features/5.png?raw=true)

### **3.6 Useful shortcuts command** (aliases)
- **Vim** - nvim
- **ll** - list files and folders in current directory
- **grep** - find string
- **cls** and **clr** - clear screen

> **Tips**
>
> You can add or edit alias at $PROFILE.CurrentUserCurrentHost directory from this command ```Set-Alias <shortcut command> <full command>```.
