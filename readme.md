# **My indows Terminl setup**
This is my window Terminal setup.
I did this to save time setting up the Terminal on a new computer and hope it will be helpful to you.
You don't have to adjust all of these. Adapt to your work style.

### **Preview Image**
- Search Directory
![Terminal Screenshot](https://github.com/chinhchin/Windows-Terminal-setup/blob/0.1.b.2/readme-assets/Preview%20Image/terminal%20screenshot%201.png)
- list directory with icons and colors.
![Terminal Screenshot](https://github.com/chinhchin/Windows-Terminal-setup/blob/0.1.b.2/readme-assets/Preview%20Image/terminal%20screenshot%202.png?raw=true)
- command suggestion
![Terminal Screenshot](https://github.com/chinhchin/Windows-Terminal-Setup/blob/0.1.b.2/readme-assets/Preview%20Image/terminal%20screenshot%203.png?raw=true)

### **Go to**
- [Version record](./version-record.json)
- See how to run Linux on Windows Terminal [here](https://github.com/chinhchin/WSL-setup.git).

### **OS support**
- Windows 10, 11

### **Credits**
- Inspiration, list of modules and solution from [craftzdog/dotfiles-public](https://github.com/craftzdog/dotfiles-public.git).

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
### **1.1. Install font.**
First, I have to install Nerd Fonts so that I can display the icons and markers used in programming nicely.

So I use [Caskaydia Cove Nerd Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/CascadiaCode.zip).

And you can see more fonts to get the one that is right for you [here](https://www.nerdfonts.com/).

### **1.2. Install 2 softwares from Microsoft Store.**
1. [Windows Terminal](https://www.microsoft.com/store/productId/9N0DX20HK701)
2. [Powershell](https://www.microsoft.com/store/productId/9MZ1SNWT0N5D)

### **1.3. Setting Terminal**
1. Open Terminal.
2. Open Setting in Terminal (Ctrl - ,).
3. At "**Startup**" pane select default profile to "*PowerShell*" that install from [1.2](./readme.md#12-install-2-softwares-from-microsoft-store).
4. At **Actions** pane remove all shortcut at "**New tab, profile index: (0 - 8)**" and change short cut at "**Switch to tab, index: 0 - 7** to "*ctrl+shift+(1 - 8)*" and remove shortcut "*ctrl+v*" to "*paste*"
5. At "**Default**" pane in "**Profiles**" group select "**Color scheme**" to ("*One Half Dark*" if your window is dark mode,  "*One Half Light*" if your Windows is light mode) and **"Font face"** to "*CaskaydiaCove NF*" and "**Cursor shape**" to  "*Vintage ( _ )*" and "**Background opacity**" to (*50%* if your Windows is dark mode and "*75%*" if your Windows is light mode).
6. At "**Appearance**" pane select "*Show acrylic in tab row(requires relaunch)*" to on.
7. Press "*Save*" Button.

## **2. Install and setup Terminal software**
### **2.1. Install Terminal software**

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

### **2.2. Enable Terminal software**
Type this command in your terminal.
```
cd (your\document\path)
mkdir PowerShell
New-Item -Path $PROFILE.CurrentUserCurrentHost -ItemType File
start $PROFILE.CurrentUserCurrentHost
```

And copy data from this [file](Microsoft.PowerShell_profile.ps1) to your terminal and save.

## **3. Usage of features**
### **3.1. Tab to get command, directory or option suggestion**
1. Type some command.
2. Press "*Tab*" to get suggestion.
3. Type followed by suggestion then, press "*Tab*" again.

![Illustration](https://github.com/chinhchin/Windows-Terminal-setup/blob/0.1.b.2/readme-assets/Usage%20of%20features/1.png)

### **3.2. Right arrow to get command suggestion** (from history)
1. Type some command.
2. If it show suggestion of command at right of cursor, press "*Right*" key, if you want to get that command.

![Illustration](https://github.com/chinhchin/Windows-Terminal-setup/blob/0.1.b.2/readme-assets/Usage%20of%20features/2.png)

### **3.3. jump directory by Z**
1. Type ```z ``` and followed by all directory path or some part of directory path

You can also jump over directory.

![Illustration](https://github.com/chinhchin/Windows-Terminal-setup/blob/0.1.b.2/readme-assets/Usage%20of%20features/3.png)

### **3.4. Search file** (Directory list view get from every file and in current directory)
1. Search file by press "*Ctrl-F*".
2. Type directory or file name and choose command by press "*Up*" and "*Down*" key.
3. Press "*Enter*" to select command or press "*Esc*" to cancel.

![Illustration](https://github.com/chinhchin/Windows-Terminal-setup/blob/0.1.b.2/readme-assets/Usage%20of%20features/4.png)

### **3.5. Search command**
1. Search command by press "*Ctrl-R*"
2. Type command that you want to use that you've used before and choose command by press "*Up*" and "*Down*"
3. Press "*Enter*" to select command or press "*Esc*" to cancel.

![Illustration](https://github.com/chinhchin/Windows-Terminal-setup/blob/0.1.b.2/readme-assets/Usage%20of%20features/5.png)

### **3.6. Useful shortcuts command** (aliases)
- **Vim** - nvim
- **ll** - list files and folders in current directory
- **grep** - find string
- **cls** and **clr** - clear screen

> **Tips**
>
> You can add or edit alias at $PROFILE.CurrentUserCurrentHost directory from this command ```Set-Alias <shortcut command> <full command>```.
