# **My Windows Terminal setup**
This is my window Terminal setup.
I did this to save time setting up the Terminal on a new computer and hope it will be helpful to you.
You don't have to adjust all of these. Adapt to your work style.

![Terminal Screenshot](https://github.com/chinhchin/window-terminal-setup/blob/master/readme-assets/terminal%20screenshot%201.png?raw=true)
![Terminal Screenshot](https://github.com/chinhchin/window-terminal-setup/blob/master/readme-assets/terminal%20screenshot%202.png?raw=true)
![Terminal Screenshot](https://github.com/chinhchin/window-terminal-setup/blob/master/readme-assets/terminal%20screenshot%203.png?raw=true)

### **Go to**
- **[Version record](./version-record.json)**
- See how to run Linux on Windows Terminal [here](https://github.com/chinhchin/WSL-setup.git).

### **OS requirement**
- Windows 10, 11

### **Content**
#### 1. [Install and setup Terminal](./readme.md#1-install-and-setup-terminal)
1. [Install font](./readme.md#11-install-font)
2. [Install 2 softwares from Microsoft Store.](./readme.md#12-install-2-softwares-from-microsoft-store)
3. [Setting Terminal](./readme.md#13-setting-terminal)
#### 2. [Install and setup Terminal software](./readme.md#2-install-and-setup-terminal-software)
1. [Install Terminal software](./readme.md#21-install-terminal-software)
2. [Enable Terminal software](./readme.md#22-enable-terminal-software)

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
2. Open Setting in Terminal (Ctrl - ,).
3. At "**Startup**" pane select default profile to "*PowerShell*" that install from [1.2](./readme.md#12-install-2-softwares-from-microsoft-store).
4. At **Actions** pane remove all shortcut at "**New tab, profile index: (0 - 8)**" and change short cut at "**Switch to tab, index: 0 - 7** to "*ctrl+shift+(1 - 8)*"
5. At "**Default**" pane in "**Profiles**" group select "**Color scheme**" to ("*One Half Dark*" if your window is dark mode,  "*One Half Light*" if your Windows is light mode) and **"Font face"** to "*CaskaydiaCove NF*" and "**Cursor shape**" to  "*Vintage ( _ )*" and "**Background opacity**" to (*50%* if your Windows is dark mode and "*75%*" if your Windows is light mode).
6. At "**Appearance**" pane select "*Show acrylic in tab row(requires relaunch)*" to on.
7. Press "*Save*" Button.

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

Type this command in your terminal.
```
cd (your\document\path)
mkdir PowerShell
New-Item -Path $PROFILE.CurrentUserCurrentHost -ItemType File
start $PROFILE.CurrentUserCurrentHost
```

And copy data from this [file](Microsoft.PowerShell_profile.ps1) to your terminal and save.
